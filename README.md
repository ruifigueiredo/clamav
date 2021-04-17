# clamav working synology

Failed updates synology

  

** - Update freshclam.conf with repo info**

$ vi /volume1/@appstore/AntiVirus/engine/clamav/etc/freshclam.conf

** - Add DatabaseCustomURL**

DatabaseCustomURL [http://ftp.swin.edu.au/sanesecurity/junk.ndb](http://ftp.swin.edu.au/sanesecurity/junk.ndb) 

DatabaseCustomURL [http://ftp.swin.edu.au/sanesecurity/phish.ndb](http://ftp.swin.edu.au/sanesecurity/phish.ndb) 

DatabaseCustomURL [http://ftp.swin.edu.au/sanesecurity/rogue.hdb](http://ftp.swin.edu.au/sanesecurity/rogue.hdb)

DatabaseCustomURL [http://ftp.swin.edu.au/sanesecurity/foxhole_filename.cdb](http://ftp.swin.edu.au/sanesecurity/foxhole_filename.cdb)

DatabaseCustomURL [http://ftp.swin.edu.au/sanesecurity/foxhole_generic.cdb](http://ftp.swin.edu.au/sanesecurity/foxhole_generic.cdb) 

DatabaseCustomURL [http://ftp.swin.edu.au/sanesecurity/foxhole_js.cdb](http://ftp.swin.edu.au/sanesecurity/foxhole_js.cdb) 

DatabaseCustomURL [http://ftp.swin.edu.au/sanesecurity/badmacro.ndb](http://ftp.swin.edu.au/sanesecurity/badmacro.ndb) 

DatabaseCustomURL [http://ftp.swin.edu.au/sanesecurity/scam.ndb](http://ftp.swin.edu.au/sanesecurity/scam.ndb) 

DatabaseCustomURL [http://ftp.swin.edu.au/sanesecurity/sanesecurity.ftm](http://ftp.swin.edu.au/sanesecurity/sanesecurity.ftm) 

DatabaseCustomURL [http://ftp.swin.edu.au/sanesecurity/sigwhitelist.ign2](http://ftp.swin.edu.au/sanesecurity/sigwhitelist.ign2)

** - Add DatabaseMirror**

Add DatabaseMirror clamavdb.c3sl.ufpr.br

** - Run freshclam with config's update.**

$ cd /volume1/@appstore/AntiVirus/engine/clamav/bin

$ ./freshclam -v
