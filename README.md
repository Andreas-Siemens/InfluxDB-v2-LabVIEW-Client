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
At the tab `Write` you can write data into your InfluxDB database. For doing this replace the content in the fields `Bucket` and `Measurement` with your own data. Also leave both field for timestamp precision at `Sesonds`. After this initialize the write client by clicking on the button `Init Write Data`.<p>


# Licence
The client is available as open source under the terms of the [MIT Licence](/LICENSE)
