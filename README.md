.
├── vehicleservice                            # root service folder
|   ├── handler
|   |   ├── endpoint                          # contain all api endpoint
|   |   |   ├── endpoint1.py
|   |   |   ├── endpoint2.py
|   |   ├── inputbd                           # contain all request model that interactive by client
|   |   |   ├── input1.py
|   |   |   ├── input2.py 
|   |   ├── app.py                            # contain factory function
|   |   ├── event_handler.py                  # contain function that run before service start like dependency injection
|   |   ├── main.py                           # contain service instance
|   ├── hexagonalmodel                        # contain domain of service and dependency
|   |   ├── adpater                           # contain dependency
|   |   |   ├── production                    # contain production dependency
|   |   |   |   ├── adapter1.py
|   |   |   |   ├── adapter2.py
|   |   |   ├── test                          # contain test dependency (for run test case)
|   |   |   |   ├── testadapter1.py
|   |   |   |   ├── testadapter2.py
|   |   ├── domain                            # contain all domain of service
|   |   |   ├── base                          # contain base file
|   |   |   |   ├── aggregate.py              # contain aggregate base model for inplement by service model
|   |   |   |   ├── exception.py              # contain all custom exception
|   |   |   |   ├── publish.py                # contain decorator function that publish data to local publish service
|   |   |   |   ├── singleton.py              # contain metaclass of registry model
|   |   |   |   ├── utils.py                  # contain logic that hard to understand and replace it with function name that people can understand
|   |   |   ├── model                         # contain model that use in this service
|   |   |   |   ├── servicemodel.py           # contain aggregate model of this service 
|   |   |   |   ├── othermodel.py
|   |   |   ├── usecase                       # contain all usecase in this service (logic)
|   |   |   |   ├── logic1.py
|   |   |   |   ├── logice2.py
|   |   |   ├── registry.py                   # contain repository model for create repository pattern 
|   |   ├── port                              # contain abstractclass of dependency that use in this service
|   |   |   ├── abstractclass1.py
|   |   |   ├── abstractclass2.py
|   ├── infrastructure                        # contain all infrastructure file 
|   |   ├── config                            # contain config file of this service
|   |   |   ├── file like .env file
|   |   ├── database                          # contain database connection file
|   |   |   ├── databaseconnection.py
└── ...
