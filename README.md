# Vagrant + Ansibleのlemp環境

## 構成
- Centos 7.1
- Nginx 1.12
- MySQL 5.6
- PHP 7.1

## 必要ツール
- VirtualBox 5.0以上
- Vagrant 1.7以上

## 開発ディレクトリ
デフォルトのドキュメントルートは`repository/your-app/public/`になっています。  
もし変更が必要であれば`ansible/group_vars/local`ファイルの`default_docroot`を修正してください。

## 利用方法
cloneした`Vagrantfile`があるディレクトリで`vagrant up`コマンドを実行してください。  

## URL
- アプリ：[http://192.168.111.222](http://192.168.111.222)
- phpMyAdmin：[http://192.168.111.222:8080](http://192.168.111.222:8080) (id/pw root/vagrant)