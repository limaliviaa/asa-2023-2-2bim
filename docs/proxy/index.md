# PROXY SQUID

O que é o proxy squid?

É um servidor de proxy open source amplamente utilizado no Linux. 

Por que utilizá-lo?

É usado principalmente para a função de armazenamento em cache do conteúdo da web acessado pelos usuários.
O que são suas ACL e para que servem?
ACL (LISTA DE CONTROLE DE ACESSO). São regras de acesso utilizadas pelo sistema para controlar quem pode acessar o que e quando.
Como acompanhar o log de acesso?
Uma das formas de acompanhar o log de acesso é utilizando o comando:

- `tail -n 200 /var/squid/logs/access.log`
 
pois através do tail ele permite visualizar as últimas linhas de um arquivo. 
Como gerenciar o serviço (habilitar, desabilitar, iniciar, parar, testar e recarregar arquivo de configuração)?
habilitar: sudo service squid enable
desabilitar:

- `sudo service squid disable`

iniciar:   sudo service squid start
parar:  sudo service squid stop
testar: curl http://localhost:3128
recarregar arquivo de configuração:  sudo service squid reload 

Como instalá-lo?
sudo apt-get install squid 
Como configurá-lo?
/etc/squid/squid.conf
Como utilizá-lo a partir de um navegador web?

## Instalação


## Configuração

Incluir o(s) nome(s) e o conteúdo do(s) arquivo(s) de configuração.

Fazer a configuração de 4 ACLs distintas, conforme a atividade passada em sala de aula.

## Teste


