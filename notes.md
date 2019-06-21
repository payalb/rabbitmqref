:set noendofline binary

Removes the final new line when the file is saved.

systemctl enable firewalld
systemctl start firewalld
systemctl status firewalld
sudo firewall-cmd --add-port=15672/tcp --permanent
sudo firewall-cmd --add-port=5672/tcp --permanent
sudo firewall-cmd --add-port={4369/tcp,25672/tcp} --permanent
sudo firewall-cmd --reload
sudo firewall-cmd --list-all

sudo systemctl restart rabbitmq-server
sudo rabbitmqctl stop_app
sudo rabbitmqctl join_cluster rabbit@node01
sudo rabbitmqctl start_app
sudo rabbitmqctl cluster_status



sudo yum -y install epel-release

