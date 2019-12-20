# docker_for_ruby_exec_env_gem3_host_dir
The third way to manage gems with Docker(host directory mounted)

名前付きボリュームを使わない方法として
ホスト環境のディレクトリをBundleのディレクトリにマウントする方法がある。

確認方法としては
何かgemをGemfileに追加しコンテナを起動する。
```
docker-compose run --rm app bash
```
このときにbundle installが実行され、
ホストのディレクトリにファイルが格納される。

再度コンテナを起動してもgemファイルは共有されているのため
bundle installは実行されない
```
docker-compose run --rm app bash
```
