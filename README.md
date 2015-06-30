Ingredients

* git clone git@github.com:peterjc/mediawiki_to_git_md.git
* git clone git@github.com:NESCent/Tools-for-Evo-Hack.git
* cd Tools-for-Evo-Hack.git
* scp -p siren:/deposit/inputs/dumps/gmodevohackathon.xml.gz ./
* install docker
* define a 'pandoc' command, put it on path

    #!/bin/bash
    exec docker run -v `pwd`:`pwd` jagregory/pandoc $*

* kludge the invocation of 'pandoc' in convert.py

         '/path...to.../Tools-for-Evo-Hack/' + mw_filename],

* invoke with

    python /path...to.../gmodevohackathon/mediawiki_to_git_md/convert.py \`pwd\`/gmodevohackathon.xml

I could have used 'brew install pandoc' and avoided the `pwd` nonsense.

At the end of conversion I got 

    fatal: No existing author found with 'hlapp'
    Return code 128 from git commit

so I don't know whether it finished or not.

When viewed in github, the hyperlinks between pages don't work,
because they just say wiki/Foo instead of wiki/Foo.md.  However, if
the content were served by apache, wiki/Foo.md (which is stored in the
file) would be a variant of the resource wiki/Foo (virtual resource
subject to content negotiation), so maybe it's all OK.  If this turns
out to be a problem, a simple sed script will fix it.
