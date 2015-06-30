Graphite Dockerfile

A supervisord controlled Graphite (0.9.12-3) in Ubuntu 14.04.2.

Usage:
```bash
docker run --restart=always --name=graphite -v /data/logs:/var/log/graphite -v /data/whisper:/var/lib/graphite/storage/whisper -p 8080:80 -p 2003:2003 -p 2004:2004 -d v00rh33s/graphite
```

Ports:
```bash
  80 - Graphite Django Interface
2003 - Carbon Line Receiver
2004 - Carbon Pickle Receiver
7002 - Carbon Cache
```

Default user created is admin / admin. 

It is also possible to use -v to present your own /etc/carbon/storage-aggregation.conf.


