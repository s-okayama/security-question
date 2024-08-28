# security-question
## 概要
bastionにはsearchsploitというエクスプロイトデータベースのコマンドライン検索ツールがインストールされています。このツールを使って、postgresサーバの脆弱性を突いてください。

## searchsploitの使い方
```bash
$ searchsploit nginx // searchsploit service でそのserviceに関する脆弱性が検索できます。
└─# searchsploit nginx
------------------------------------------------------------------------------------------------------------------------------------------------------------- ---------------------------------
 Exploit Title                                                                                                                                               |  Path
------------------------------------------------------------------------------------------------------------------------------------------------------------- ---------------------------------
Nginx (Debian Based Distros + Gentoo) - 'logrotate' Local Privilege Escalation                                                                               | linux/local/40768.sh
Nginx 0.6.36 - Directory Traversal                                                                                                                           | multiple/remote/12804.txt
Nginx 0.6.38 - Heap Corruption                                                                                                                               | linux/local/14830.py
Nginx 0.6.x - Arbitrary Code Execution NullByte Injection                                                                                                    | multiple/webapps/24967.txt
Nginx 0.7.0 < 0.7.61 / 0.6.0 < 0.6.38 / 0.5.0 < 0.5.37 / 0.4.0 < 0.4.14 - Denial of Service (PoC)                                                            | linux/dos/9901.txt
Nginx 0.7.61 - WebDAV Directory Traversal                                                                                                                    | multiple/remote/9829.txt
Nginx 0.7.64 - Terminal Escape Sequence in Logs Command Injection                                                                                            | multiple/remote/33490.txt
Nginx 0.7.65/0.8.39 (dev) - Source Disclosure / Download                                                                                                     | windows/remote/13822.txt
Nginx 0.8.36 - Source Disclosure / Denial of Service                                                                                                         | windows/remote/13818.txt
Nginx 1.1.17 - URI Processing SecURIty Bypass                                                                                                                | multiple/remote/38846.txt
Nginx 1.20.0 - Denial of Service (DOS)                                                                                                                       | multiple/remote/50973.py
Nginx 1.3.9 < 1.4.0 - Chuncked Encoding Stack Buffer Overflow (Metasploit)                                                                                   | linux/remote/25775.rb
Nginx 1.3.9 < 1.4.0 - Denial of Service (PoC)                                                                                                                | linux/dos/25499.py
Nginx 1.3.9/1.4.0 (x86) - Brute Force                                                                                                                        | linux_x86/remote/26737.pl
Nginx 1.4.0 (Generic Linux x64) - Remote Overflow                                                                                                            | linux_x86-64/remote/32277.txt
PHP-FPM + Nginx - Remote Code Execution                                                                                                                      | php/webapps/47553.md
------------------------------------------------------------------------------------------------------------------------------------------------------------- ---------------------------------
Shellcodes: No Results

$ searchsploit -m 25499 // これが使えるなと思ったらsearchsploit -m CVE IDでその脆弱性に関するエクスプロイトをダウンロードできます。
$ ls -al 
25499.py

$ pyhton3 25499.py // 後はUsageに従って実行するだけです。
 ````
<details>
<summary>Hint1: ヒントを見たい方はこちら。</summary>

- 確かpostgresqlのバージョンは11.7を使用していた気がしますが・・・。  
- searchsploitで検索すると・・・。
</details>

<details>
<summary>Hint2: ヒントを見たい方はこちら。</summary>

1. sample-apiの中になにかあるかもしれないです。
</details>