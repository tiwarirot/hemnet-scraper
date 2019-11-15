# hemnet-scraper
Python webscraper for hemnet house prices

This script fetches house price information ("slutpriser") from hemnet.se and output it to a CSV file. The columns of the CSV table are:

* region (county)
* location
* street_address
* num_of_rooms
* size
* fee
* final_price
* initial_price
* year_built

It browses specifically the counties of: *Stockholm*, *Nacka*, *Sollentuna*, and *Sundbyberg*. 

To change the default run settings (starting page, number of pages), modify the last line:

```
SlutPriserScraper(start_page=1,num_of_pages=50,use_google_maps_api=False).to_csv()
```

Note that the number of pages cannot be higher than 50.

If you wish to use Google API to calculate the distance to central station and add that to your CSV data, you will need an API key (follow instructions here: https://developers.google.com/maps/documentation/distance-matrix/get-api-key). Set your API key value in *config.py* and change the paramter _use_google_maps_api_ to True.


The resulting CSV file is written to CSV directory.

