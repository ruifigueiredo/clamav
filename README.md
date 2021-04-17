# Table of Contents

1.  [clamav working synology](#orgc9abce8)
    1.  [Failed updates synology](#orgf088007)


<a id="orgc9abce8"></a>

# clamav working synology


<a id="orgf088007"></a>

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
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/sigwhitelist.ign
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/jurlbl.ndb
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/spamimg.hdb
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/spamattach.hdb
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/blurl.ndb
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/malwarehash.hsb
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/malware.expert.hdb
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/hackingteam.hsb
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/winnow_malware.hdb
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/winnow_malware_links.ndb
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/winnow_extended_malware.hdb
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/winnow.attachments.hdb
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/winnow_bad_cw.hdb
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/bofhland_cracked_URL.ndb
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/bofhland_malware_URL.ndb
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/bofhland_phishing_URL.ndb
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/bofhland_malware_attach.hdb
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/crdfam.clamav.hdb
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/porcupine.ndb
    DatabaseCustomURL http://ftp.swin.edu.au/sanesecurity/porcupine.hsb

Add DatabaseMirror

    Add DatabaseMirror clamavdb.c3sl.ufpr.br

Run freshclam with config's update.

    $ cd /volume1/@appstore/AntiVirus/engine/clamav/bin
    
    $ ./freshclam -v
