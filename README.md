BAPI-Loader-Creator
===================

Automate the creation of reports which load data based on BAPIs.


So you are an ABAP developer and you were requested to create a very simple and straightforward Z program which calls a BAPI to adjust or mass update some data on the server.

Then, you create a new Z program which receives the input data from a text file, populate some variables based on BAPI's formal parameters and then calls the BAPI itself.
The report works just well and you have done your role as an ABAP developer sucessfully.

It might happen to have the same problem happenning again but for a different business object. Then, another ABAP developer, maybe you maybe not is requested to create a new Z program similar to the first one. As the first program was intended to be used just once, the chances of using the first program as a template of some kind is minimal.

Later on, the same business object from the first scenario have to be maintained using the same method. It's very likely that you (or other developer) won't search for programs using that BAPI and even if you do, it's unlikely that the same program will suit you as will might need different paramenters in your program.

This project aims to solve this problem. The creation of new programs for this task can be automated given solely the BAPI name.

In other words, give a BAPI name for us and we will generate a Z program for you. This program will:
- Read an input file based on your BAPI parameters
- Calls the BAPI and BAPI_TRANSACTION_COMMIT.
- Output BAPI's result (RETURN table)
- Do some error handling
- Give you the possibility to include AUTHORIZATION-CHECKS
- Manage all Z programs generated for each BAPI
