API仕様書リポジトリサンプル
===========================

API仕様を Json-HyperSchema (YAML表記)で書いて、APIドキュメントなどを生成しようというものです。

[Sample Document](./document.md)

インストール
------------

* Ruby が必要です

```sh
$ gem install prmd
```

ドキュメント生成
----------------

```sh
$ prmd combine schemata/ | prmd doc > document.md
```

