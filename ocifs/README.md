# ocifs

## how to build

`docker-images/ocifs/.oci` に OCIFS で使用する Config ファイルと対応する秘密鍵を格納し、コンテナ・イメージをビルドする。

```sh
docker image build -t ocifs .
```

### how to use

```sh
$ docker container run -it --rm ocifs help
Usage:
       ocifs [<options>] <bucket>[/<subfolder>] <mountpoint>
       ocifs [<options>] --check-bucket <bucket>

Options:

  --auth=<auth-method> : Set the authentication method, either api_key
      (the default), instance_principal or resource_principal
  --config=<config-file> : OCI configuration file (default: ~/.oci/config)
  --region=<region-name> : OCI region or domain
  --cache=<cache-directory> : OCIFS cache directory (default: ~/.ocifs)
  --cache-fsfree=<limit>: Cache filesystem free space limit
  --cache-keep: Do not remove the OCIFS cache directory on exit
  --cache-purge=never|<value>: Delay before purging cache file
  --cache-reuse: Reuse data from the OCIFS cache directory
  --debug=<level>[,<level>...] : Debug levels (all cache fops oci other)
```
