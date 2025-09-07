#jail.local是faile2ban的配置文件
开启了8个模块。
dovecot, nginx-botsearch, nginx-http-auth, nginx-limit-req, postfix, postfix-sasl, recidive, sshd



# dnf -y --enablerepo=elrepo-kernel install kernel-lt
一直卡滞在
ELRepo.org Community Enterprise Linux Repository - el8

@解决方法

原始文件内容：
```
baseurl=http://elrepo.org/linux/elrepo/el8/$basearch/
	http://mirrors.coreix.net/elrepo/elrepo/el8/$basearch/
	http://mirror.rackspace.com/elrepo/elrepo/el8/$basearch/
	http://linux-mirrors.fnal.gov/linux/elrepo/elrepo/el8/$basearch/
mirrorlist=http://mirrors.elrepo.org/mirrors-elrepo.el8
```
注释掉mirrorlist，baseur每个模块都仅留一个URL
```
baseurl=http://mirror.rackspace.com/elrepo/elrepo/el8/$basearch/
# mirrorlist=http://mirrors.elrepo.org/mirrors-elrepo.el8
```
四个模块的链接不同，每个模块都指定一个url即可解决。
