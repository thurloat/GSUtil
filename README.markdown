# GSUtil
#### http://code.google.com/p/gsutil/ - A command line tool for interacting with cloud storage services
****
I have added some additional functionality that has allowed us to more easily adopt the Google Storage solution. It was created to migrate our application's static resources from S3 to GS

#### Sample Usage
        $./gsutil cp -ztcp libs/* gs://mybucket/

#### Options
        -t  Tries to automagically detect your file's Content Type header and assigns it
        
        -c  Sets the caching headers up to have far-future expiry
        
        -p  Creates the resource with a public-read canned ACL
        
        -z  Compress eligable files with GZIP prior to uploading

### Known Issues
    - using the public flag on small files occasionally fails with a 404, key not found... Invesitgation Insues.