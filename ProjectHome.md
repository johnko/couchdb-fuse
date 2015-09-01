A FUSE interface to CouchDB.

From the [blog post](http://www.jasondavies.com/blog/2008/11/25/edit-couchdb-attachments-directly-with-couchdb-fuse/):

## Use Cases ##

  * If you've read [My Couch or Yours? Shareable Apps Are The Future](http://jchris.mfdz.com/code/2008/11/my_couch_or_yours__shareable_ap) by jchris, this is a great time-saver if you want to edit HTML, JavaScript, CSS or even image files directly using your favourite editor.
  * Uploading large numbers of files repetitively through Futon or even via a Python prompt becomes tedious very quickly: drag'n'drop or cp `*` is the way forward!

## Installation ##

You need the following:

  1. [Python FUSE bindings](http://fuse.sourceforge.net/wiki/index.php/FusePython)
  1. [CouchDB-Python](http://code.google.com/p/couchdb-python/) 0.5 or greater
  1. [CouchDB-FUSE](http://code.google.com/p/couchdb-fuse/)

Running python setup.py install should install a couchmount script on your path.

## Usage ##

```
$ mkdir mnt
$ couchmount http://localhost:5984/jasondavies/_design%2Flinks mnt/
$ ls mnt/
$ touch mnt/foo
$ ls mnt/
foo
$ 
```

...you get the idea...

Happy Couching!

[Downloads](http://pypi.python.org/pypi/CouchDB-FUSE) available at PyPI.