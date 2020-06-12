# dockerテンプレート

Nginx＋php＋PostgreSQLのdocekrテンプレート


# docker環境

| 言語　| バージョン |
| ---  | --- |
| PHP  | 7.4.* |
| PostgreSQL  | 8.0.11 |
| WEBサーバ | Nginx |
| WEB URL  | http://{docker IP}:10001/ |


# ディレクトリ構成

```bash
.      
├── docker      
│   ├── postgres                            PostgreSQL用設定ファイル
│   │   └──docker-entrypoint-initdb.d       データの初期化を自動的に走るSQL
│   ├── nginx                               nginx用Dockerfile等
│   └── php                                 php用Dockerfile等 
└── src                                     phpソースコードファイル

```    
    
    
    