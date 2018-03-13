## Solve " Local Domains " issue on Linux (Ubuntu)

### .local conflict on Linux

#### Conflict Reason

*Microsoft uses .local as the recommended root of internal domains and serves them via unicast DNS .*

*Linux uses .local as the root of multicast DNS .*

*So you will need to reconfigure your Linux multicast DNS to use a different domain like .alocal ( for example )*

**To do that** , you need to add " domain-name=.alocal" line to the **[server]** section

#### open avahi-daemon.conf file

` sudo nano /etc/avahi/avahi-daemon.conf`

 #### add `domain-name=.alocal` to [server] section

```
[server]
domain-name=.alocal
```

 #### Then restart avahi-daemon service

 `sudo service avahi-daemon restart`

**In some cases you will need to flush your DNS**

`systemctl restart systemd-resolved.service`

**to make sure that your cache has been flushed**

`sudo systemd-resolve --statistics`

You will see something like that

```
Cache
  Current Cache Size: 0
          Cache Hits: 0
        Cache Misses: 0

```
