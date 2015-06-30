Ingredients

* scp siren:/deposit/inputs/dumps/gmodevohackathon.xml.gz ...
* git clone git@github.com:peterjc/mediawiki_to_git_md.git
* git clone git@github.com:NESCent/Tools-for-Evo-Hack.git
* install docker
* define a 'pandoc' command 
    #!/bin/bash
    exec docker run -v `pwd`:`pwd` jagregory/pandoc $*
* kludge the invocation of 'pandoc' in convert.py
         '/Users/jar/a/NESCent/repo/Tools-for-Evo-Hack/' + mw_filename],
