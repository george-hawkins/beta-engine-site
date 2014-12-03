Setup
-----

Clone repo and create gh-pages content as per "[Creating Project Pages manually](https://help.github.com/articles/creating-project-pages-manually/)".

    $ git clone git@github.com:george-hawkins/beta-engine-site.git
    $ cd beta-engine-site/
    $ git checkout --orphan gh-pages
    $ git rm -rf .
    $ mv .../crash.svg .
    $ mv .../index.html .
    $ git add index.html crash.svg
    $ git commit -a -m "Initial gh-pages import."
    $ git push origin gh-pages

Create CNAME file as per "[Adding a CNAME file to your repository](https://help.github.com/articles/adding-a-cname-file-to-your-repository/)".

    $ vi CNAME
    $ git add CNAME 
    $ git commit -m 'Added CNAME file as per https://help.github.com/articles/adding-a-cname-file-to-your-repository/'

Make local permanently track remote as per [SO](http://stackoverflow.com/a/2286030/245602) and push changes.

    $ git branch -u origin/gh-pages gh-pages
    $ git push

Create CNAME DNS record (at godaddy in this case) and check changes have taken affect, as per "[Tips for configuring a CNAME record with your DNS provider](https://help.github.com/articles/tips-for-configuring-a-cname-record-with-your-dns-provider/)".

    $ dig www.beta-engine.net +nostats +nocomments +nocmd

Changes may take some time to propagate.

Favicon
-------

Created using favicon generator as per [SO](http://stackoverflow.com/a/19590415/245602).
