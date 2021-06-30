# Comparison-HTTP

HTTP 1.0, 1.1, 2.0を比較。

## http

```txt
curl http://example.com/ http://example.com -v --http1.0
curl http://example.com/ http://example.com -v --http1.1
curl http://example.com/ http://example.com -v --http2
```

## https

```txt
SSLKEYLOGFILE=/tmp/secret.log curl https://example.com/ https://example.com -v --http1.0
SSLKEYLOGFILE=/tmp/secret.log curl https://example.com/ https://example.com -v --http1.1
SSLKEYLOGFILE=/tmp/secret.log curl https://example.com/ https://example.com -v --http2
```

## files

`http.pcapng`: http3つ全体のキャプチャ  
`http1.0.pcapng`: 全体のキャプチャからhttp1.0の部分だけを切り取り  
`http1.0.txt`: curl時のログをコピペ

それぞれ対応したプロトコルとバージョンがファイル名。

`https/secret.log`: HTTPSのシークレットファイル。  
WireShark`設定>Protocols>TLS>Master-Secret log filename`からインポートすればHTTPSの中身が見れる。

```txt
.
├── http
│   ├── http.pcapng
│   ├── http1.0.pcapng
│   ├── http1.0.txt
│   ├── http1.1.pcapng
│   ├── http1.1.txt
│   ├── http2.0.pcapng
│   └── http2.0.txt
└── https
    ├── https.pcapng
    ├── https1.0.pcapng
    ├── https1.0.txt
    ├── https1.1.pcapng
    ├── https1.1.txt
    ├── https2.0.pcapng
    ├── https2.0.txt
    └── secret.log
```
