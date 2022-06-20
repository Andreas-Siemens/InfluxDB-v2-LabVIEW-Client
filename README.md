# InfluxDB-LabVIEW-Client
This is a simple LabVIEW client for InfluxDB which can be used with both InfluxDB OSS and InfluxDB Cloud. 
The client is written in LabVIEW 2020 and supports communication via the REST API with InfluxDB v2.x databases.
Older versions than v2.0 are not supported.

# Dependencies
-  i3 JSON Toolkit 

You can download this toolkit from the [VIPM Homepage](https://www.vipm.io/package/i3_json/?utm_source=vipm_desktop)

# Client features
- Setup database connection and authorization to the APi via tokens 
- Querying data into csv format using the Flux language 
- Writing data using the Line Protocol
- Supports gzip to reduce transfer data's size

# Getting started
For testing and understanding the way of working of this client use the `Test v2 Client.vi` in folder `\Examples`.<p>
## Setup
After starting the programm choose the tab `Setup` and click on the button `Read Setup` to read an example set of data from the directory `\Examples\Setup\`. This will show you how to fill in all required data for this programm. By clicking on the button `Write Setup` you can save your own setup data.
## Init
The tab `Init` shows you the data which is needed for connecting to the InfluDB database. Replace the example data in the cluster `DataBase Data` with the data for your own InfluxDB access. Choose whether you want to use the `Organization` name or `Organization ID`. Leave the other field always blank.
After this click on the `Init` button to initialize the client.<p>
With a click on `Check Auth` you can check the communication with your InfluxDB database. If all is OK the code in `HTTP Status` should show the value 200, otherwise you will see a corresponding error message.
## Write
At the tab `Write` you can write data into your InfluxDB database. For doing this replace the content in the fields `Bucket` and `Measurement` with your own data, or  alternatively create a bucket with the name `Test1` in your database for storing testdata. Also leave both field for timestamp precision at `Seconds`. After this initialize the write client by clicking on the button `Init Write Data`.<p>
In the tag set `Tags` there are already 2 tags defined, but you can change them and add some more tags.<p>
The field set consists of the array `Field Names` and the structure `Field Values`. Each entry in this structure represents a different data type:
  
  - cpu_temp: float type
  - error_code: signed integer
  - cpu_load: unsigned integer
  - cpu_type: string
  - cpu_busy: boolean
  
This programm will demonstrate the handling of writing different data types into InfluxDB. With a click on the button `Write Data` a data point with these 5 fields will be written to the database using the line protocol. With each clíck the field values will also be changed randomly, this prevents the writing of several identical values. 
## Query
At the tab `Query` you can read data from your FluxDB database using the Flux query language. In the field `Query` you can see already a complete query for the data you wrote before at the tab `Write`. Please make sure that the names for the bucket and the measurement are the same as you used before. With a click on the button `Query Data` the data will be read and displayed in the field `Body` in a csv format. To save this data into a file click on the button `Write csv - file`. Enable the field `with compression` for reducing transfer data's size.<p>
With a click on the button `Write Query` you can save the content of the query field into a text file. The `Read Query` button allows you to read query from an another file.



# Licence
The client is available as open source under the terms of the [MIT Licence](/LICENSE)
