ansible-Proxy
=============

ansibleを使って、CentOSにプロキシの設定をしま

ansible...サーバ構成管理ソフトウェア  

対象環境
-----
CentOS 6.4 64bit   (virtualbox + vagrantで構築)

実行環境
-----
```
	$ ansible --version  
	ansible 1.2.2  
	$ ruby -v  
	ruby 1.9.3p194 (2012-04-20 revision 35410) [x86_64-darwin11.4.2]
```

proxyの設定場所
------
roles/proxy/vars/main.yml  
```
https_proxy: "https://proxy.example.com:8080/"  
http_proxy: "http://proxy.example.com:8080/"  

```


proxyを設定するもの
------
+ bash
+ git
+ Ruby - gem
+ wget
+ curl
+ yum

実行手順
----
簡易版  
hosts内に対象サーバのIPアドレスを入力しておくこと。  

```
ansible-playbook setup.yml -i hosts
```

