# Introduction #

CouchDB-FUSE is a FUSE module written in Python, allowing CouchDB databases to be mounted as as virtual file systems.  The file system outline is planned as follows:


# File System Outline #

  * mnt/
    * dbname/
      * all\_docs/
        * id1/
          * value (this contains the JSON-encoded dump of this document)
          * _attachments
            * att1.jpg
            * ...
        * id2/
          * value
        * ...
      *_view/
        * designdoc1/
          * viewname/
            * key1/
              * doc (this is a symlink to something like `_all\_docs/id1'
              * value_

# Problems #

So far the only problem I have come across is choosing an appropriate way to encode keys, in particular complex ones.  It would be nice to be able to split keys into hierarchies of directories, using group and group\_level for reduce views.