# openapi-with-go


Dockerコンテナ内でOpenAPI Generator CLIを実行して、指定されたOpenAPI定義からGo言語のクライアントコードを生成
指定されたOpenAPI定義から生成されたGo言語のクライアントコードが、ホストマシン上の /local/out/go ディレクトリに出力される
```
docker run --rm -v "${PWD}:/local" openapitools/openapi-generator-cli generate \
    -i https://raw.githubusercontent.com/openapitools/openapi-generator/master/modules/openapi-generator/src/test/resources/3_0/petstore.yaml \
    -g go \
    -o /local/out/go
```