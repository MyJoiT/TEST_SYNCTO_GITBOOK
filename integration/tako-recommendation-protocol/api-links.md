# API Links

## API Base Link

### Based on Polygon Mainnet

[https://api.tako.so](https://testapi.takoyaki.so/)

### Based on Mumbai Testnet

[https://testapi.tako.so](https://testapi.takoyaki.so/)

## How To Use

### For GET Method API

Assume you will use the API DistributeOffers its route is "/v1/curator/accepted".

The first step you should compose the base link with the API route:

`https://api.tako.so/v1/curator/accepted?profileId=35466&cursor=0`

Please refer to the API documentation for specific parameters and requirements.

Now you can request the full link using JavaScript, Python, cURL, etc. Then you will receive a response from the Tako server.

### For POST method API

Similar to GET method, but you need to pass the parameters in the request body as application/json.
