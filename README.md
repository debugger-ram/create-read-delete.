# create-read-delete.
Environment Setup
Operating system: Ubuntu 18.04
Python: Python3.6 or higher
Install Python dependency packages: python3 -m pip install -r requirements.txt
Run app.py to run the backend server.
To start datastore from default file location, run python3 app.py
To start datastore from user defined file location, run python3 app.py --datastore=<absolute_path_of_your_datastore>
Test Environment Setup
To test the Create operation of data in datastore, run python3 test_create_data.py for default datastore or run python3 test_create_data.py --datastore=<absolute_path_of_your_datastore> for custom datastore location.
To test the Read operation of data in datastore, run python3 test_read_data.py for default datastore or run python3 test_read_data.py --datastore=<absolute_path_of_your_datastore> for custom datastore location.
To test the Delete operation of data in datastore, run python3 test_delete_data.py for default datastore or run python3 test_delete_data.py --datastore=<absolute_path_of_your_datastore> for custom datastore location.
Accessing DataStore CRD operations as a library
A class named DataStoreCRD in the file datastore/CRD/functions.py contains all the CRD operations.
A class function DataStoreCRD().check_create_data(<key-value-data>, <datastore directory>) can be used to create a data in DataStore.
A class function DataStoreCRD().check_read_data(<key>, <datastore directory>) can be used to read a data from the DataStore.
A class function DataStoreCRD().check_delete_data(<key>, <datastore directory>) can be used to delete a data from the DataStore.
REST API Examples
Create data in DataStore - API: http://localhost:5000/datastore/create & Data: {"abc": {"data1": "value1", "data2": "value2", "data3": "value3", "Time-To-Live": 5000, "CreatedAt": "2020-02-27T05:07:53.133320"}, "def": {"data1": "value1", "data2": "value2", "data3": "value3", "Time-To-Live": 50, "CreatedAt": "2020-02-27T05:07:53.133343"}} & API Type: POST.
Read data from datastore - API: http://localhost:5000/datastore/read?key=abc & API Type: GET.
Delete data from datastore - API: http://localhost:5000/datastore/delete?key=abc & API Type: DELETE.
