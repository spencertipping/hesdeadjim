# He's dead, Jim
![image](https://i.imgflip.com/ihebz.jpg) ![image](https://memegenerator.net/img/instances/65756847/im-sorry-i-cant-hear-you-over-the-sound-of-how-awesome-i-am.jpg)

Basically, the dumbest possible thing you could to for monitoring.

## What it looks like
![image](http://storage9.static.itmages.com/i/18/0310/h_1520724312_6043538_6d65108798.png)

You'll get desktop notifications if the server drops offline, any problems
arise, or if the crontab process doesn't update within three minutes.

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

## A quick note about notifications
Chrome blocks notifications across any non-`localhost` plaintext connection,
with no workaround that I've been able to find. This means you may have to use
Firefox if you want popup notifications to work.
