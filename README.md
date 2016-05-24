# DHuS Product Synchroniser Scripts
Synchronise products between instances of the DHuS.

## HowTo use

### Set the environment variables that configure the DHuS:

+ **DHOST** DHuS Host address eg: localhost:8080, scihub.copernicus.eu/dhus/
+ **DLOGIN** DHuS login username to connect to the $DHOST DHuS
+ **DPASS** DHuS login password to connect to the $DHOST DHuS

### Use a command:

Parameters between angle brackets (chevrons) are mandatory.

Parameters between brackets ([]) are optional.

Create a Synchroniser:  
```
./createSynchronizer <-D_SCHEDULE=cron_expression> <-D_SERVICEURL=URL_to_remote_DHuS_to_sync> <-D_SERVICELOGIN=account> <-D_SERVICEPASSWORD=password> [-D_LABEL=my_sync] [-D_PAGESIZE=X] [-D_REQUEST=start|stop] [-D_REMOTEINCOMING=path/to/mountpoint/] [-D_COPYPRODUCT=true|false] [-D_FILTERPARAM=filter_expression] [-D_SOURCECOLLECTION=resource/path] [-D_LASTINGESTIONDATE=date]
```

List synchronisers / print a synchroniser:  
```./getSynchronizer [synchroniser id]```

Delete a synchroniser:  
```./deleteSynchronizer <synchroniser id>```

Update a synchroniser:  
```./updateSynchronizer <synchroniser id> [any options accepted by createSynchronizer]```

Start a synchroniser:  
```./startSync <synchroniser id>```

Stop a synchroniser:  
```./stopSync <synchroniser id>```

