# DHCP

<b>O que é DHCP e quando utilizar:</b>

O DHCP simplifica a configuração de dispositivos em redes e ajuda a garantir que todos os dispositivos tenham as informações de configuração necessárias para se comunicar com outros dispositivos na rede.


## Instalação

Para instalação do DNSMASQ em uma máquina linux basta digitar o comando:

``apk add dnsmasq``

para ver o <b>estado</b> do serviço:

``service dnsmasq status ``

## Configuração

Para configurar, criamos um arquivo <b> (asa.conf) </b> no diretório <b>(dnsmasq.d)</b>.

Para editar o arquivo, digite:

``nano /etc/dnsmasq.d/asa.conf``


<b> Definição da faixa de ip </b>
(ip inicial, ip final, máscara de rede, tempo que o dispositivo fica com o ip)

dhcp-range=10.0.19.10,10.0.19.100,255.255.255.0,12h

<b> Definiçao do DNS </b>

dhcp-option=3, 10.0.0.19.254

<b> DNS Google </b>(opcional)

dhcp-option=6,8.8.8.8 

<b> Definição do domínio</b> (opcional)

dhcp-option=15,pernambuco.lab

<b>Local do LOG</b> 

log-facility=/var/log/dnsmasq.log

<b> OBSERVAÇÃO: </b> 

``rc-service dnsmasq start`` para <b> iniciar </b>  o serviço

``rc-service dnsmasq stop`` para <b> parar </b>  o serviço 

## Teste

Em seguida segue a imagem da configuração do <b>servidor</b>:

![Alt text](<conf xarope.png>)

Configuração dos clientes:

![Alt text](58f4d50d-2036-4db4-bcc8-d29bdc31c3c1.png)


![Alt text](<maq windxp.png>) ![Alt text](<maq wid7.png>)