# InfluxDB-LabVIEW-Client
This is a simple LabVIEW client for InfluxDB which can be used with both InfluxDB OSS and InfluxDB Cloud. 
The client is written in LabVIEW 2020 and supports communication via the REST API with InfluxDB v2.x databases.
Older versions than v2.0 are not supported.


# Client features
- Setup database connection and authorization to the APi via tokens 
- Querying data using the Flux language into csv format
- Writing data using the Line Protocol
- Supports gzip to reduce transfer data's size

# Getting started
For testing and understanding the way of working of the client you can use the `Test Client.vi` in folder `\Examples`.


# Licence
The client is available as open source under the terms of the [MIT Licence](/LICENSE)
