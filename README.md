# He's dead, Jim
Basically, the dumbest possible thing you could to for monitoring.

## Using it
Edit `./deadjim` to monitor the stuff you care about, then add it to your
crontab like this:

```crontab
* * * * * /path/to/deadjim /tmp/deadjim.out
```

Then run the webserver:

```sh
$ ./deadjim-webserver 8080 /tmp/deadjim.out
```

You should now be able to see your page at `localhost:8080`, or from other
machines at `http://your-server:8080`.
