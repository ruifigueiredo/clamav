
# Table of Contents

1.  [clamav working synology](#org818ad78)
    1.  [Failed updates synology](#org26e703f)


<a id="org818ad78"></a>

# clamav working synology


<a id="org26e703f"></a>

## Failed updates synology

Update freshclam.conf with repo info

    $ vi /volume1/@appstore/AntiVirus/engine/clamav/etc/freshclam.conf

Add DatabaseCustomURL

    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/junk.ndb
    
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/phish.ndb
    
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/rogue.hdb
    
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/foxhole_filename.cdb
    
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/foxhole_generic.cdb
    
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/foxhole_js.cdb
    
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/badmacro.ndb
    
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/scam.ndb
    
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/sanesecurity.ftm
    
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/sigwhitelist.ign2

Add DatabaseMirror

    Add DatabaseMirror clamavdb.c3sl.ufpr.br

Run freshclam with config's update.

    $ cd /volume1/@appstore/AntiVirus/engine/clamav/bin
    
    $ ./freshclam -v
