This repository cosists the code which::
  whenever a json document is uploaded into a designated s3 bucket,
  it triggers a lambda func. and it grabs the json part of the file and populates 
  the dynamodb table according to the key and value of the json document.

How To Use:::
  1.Create a s3 bucket
  2.Create a Dynamodb table
  3.create a lambda function with python 3.7 runtime.
  4.assume roles:
    -s3 readonly access
    -lambda basic execution role
    -dynamodb fullaccess
  5.paste the code under lambda handler
  6.create a trigger(S3) ,on whenever a object is uploaded,and add prefix .json
  7.update with your table name in the lambda code 