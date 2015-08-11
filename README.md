sudo apt-get install ansible
-
cd ansible_example/
ansible-playbook bootstrap.yml || ansible-playbook -i hosts bootstrap.yml
-
cd app/
ansible-playbook site.yml -i production -K --ask-vault-pass
-

ansible-vault decrypt secrets.yml
-
Vault password: foobar
ansible-vault encrypt secrets.yml
-
or
ansible-vault create secrets.yml
-
-
Errors:
-
psql: could not connect to server: No such file or directory
    Is the server running locally and accepting
    connections on Unix domain socket "/var/run/postgresql/.s.PGSQL.5432"?


sudo locale-gen uk_UA.UTF-8
-
sudo dpkg-reconfigure locales
-
