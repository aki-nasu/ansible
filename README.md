# ansible
## ansible-server 初期処理
### ansible-serverにansibleをインストール
https://docs.ansible.com/ansible/2.9_ja/installation_guide/intro_installation.html#ubuntu-ansible

```bash
sudo apt update;sudo apt install -y software-properties-common;sudo apt-add-repository --yes --update ppa:ansible/ansible;sudo apt install ansible -y;
```
### sshに必要な鍵をアップロード
```bash
mkdir ~/.ssh
# 鍵ファイルをアップロードする
chmod 600 ~/.ssh/id_rsa
```

### git clone
```bash
git clone https://github.com/aki-nasu/ansible.git
```

## guacamole-server セットアップ
事前に、[VMを作成する](https://qiita.com/aki-nasu/items/aacecb5be224d28f7131)

### setup_guacamole_server.ymlを実行する
hostsのIPアドレスと`ansible/guacamole/docker-compose.yml` のパスワードを修正してから実行する
```bash
ansible-playbook setup_guacamole_server.yml -i hosts
```
