# NOTE
#### The bulk of my codes and features were pulled into or re-created in the official tool from Google. I won't be maintaining this any longer :) 


# GSUtil
#### http://code.google.com/p/gsutil/ - A command line tool for interacting with cloud storage services
****
I have added some additional functionality that has allowed us to more easily adopt the Google Storage solution. It was created to migrate our application's static resources from S3 to GS

#### Sample Usage
        $./gsutil cp -ztp -c 2984000 libs/* gs://mybucket/

#### New Copy Options
        -t  Tries to automagically detect your file's Content Type header and assigns it
        
        -c  [int:seconds] Sets the caching headers up to have far-future expiry. Defaults to 1 month.
        
        -p  Creates the resource with a public-read canned ACL
        
        -z  Compress eligable files with GZIP prior to uploading
****
### Known Issues
    - using the public flag on small files occasionally fails with a 404, key not found... Invesitgation Insues.
    
### Roadmap

    - Adding wildcard useage to the gsutil rb command
    - Switching the set public canned acl cp option to accept an arg, incase you want to apply a special acl rather than pub or priv
    - extend the gzip functionality to work cloud-to-cloud through a local tempfile
    