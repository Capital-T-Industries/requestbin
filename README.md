# We have discontinued the publicly hosted version of RequestBin due to ongoing abuse that made it very difficult to keep the site up reliably. Please see instructions below for setting up your own self-hosted instance.

Originally Created by [Jeff Lindsay](http://progrium.com)

License
-------
MIT


Looking to self-host?
=====================

## Deploy your own instance using Docker

Run an instance of the RequestBin docker image hosted on [Docker Hub](https://hub.docker.com/r/clarketm/requestbin/); specify the desired port (default: 8000) to expose on your server/machine: 

```
$ PORT=8000
$ docker run -p $PORT:8000 clarketm/requestbin
```

Your own private RequestBin instance will be running on the specified port.


Contributors
------------
 * Barry Carlyon <barry@barrycarlyon.co.uk>
 * Jeff Lindsay <progrium@gmail.com>
