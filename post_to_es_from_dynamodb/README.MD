**Post data from DDB to ES**

Add existing data from DDB stream to ES index

* requirements
    * python 3.6
    * OS linux

* install required packages

``` > pip intall -r ./requirements.txt ```

* check credentials in ~/.aws/credentials

```
[default]
aws_access_key_id = {aws_access_key_id}
aws_secret_access_key = {aws_secret_access_key}
```

* run script

```
> python ./post_to_es_from_dynamodb.py --tn Recipe --ak {aws_access_key_id} --sk {aws_secret_access_key} --esarn arn:aws:dynamodb:us-west-2:343395846365:table/Recipe/stream/2018-06-14T16:46:37.777 --lf arn:aws:lambda:us-west-2:343395846365:function:ddb-to-es
```

