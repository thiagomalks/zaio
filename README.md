# ZAIO - Zabbix All In One

<p>Implementado para um servidor com as seguintes configura&ccedil;&otilde;es:</p>
<p>SO: Ubuntu 20.04 (ou superior)<br />CPU: 4<br />RAM: 8GB<br />Disco: 100GB</p>
<p>Ambiente Zabbix com estimativa de 50 hosts, rentenção de dados de 30d com trends de até 365d</p>
<p>Clone o reposit&oacute;rio em seu servidor e execute o arquivo install.sh como root</p>

````
git clone https://github.com/thiagomalks/zaio
````
````
./install.sh
````
<p>Itens da Instala&ccedil;&atilde;o:<br />1 - Docker Engine CE<br />2 - Zabbix Server PSQL 6.0.12<br />3 - Zabbix Web Nginx 6.0.12<br />4 - Zabbix Agent2 6.0.12<br />5 - PostgreSQL 14-6</p>
<p>Para atualização, basta verificar a versão de desejada no Docker Hub e alterar a tag no docker-compose, recriando posteriormente os serviços</p>
<p>Ap&oacute;s instala&ccedil;&atilde;o, acesse o Zabbix pelo navegador utilizando o IP do servidor de instala&ccedil;&atilde;o.</p>
<p>Se aparecer uma mensagem de erro de conexão com o banco, é por que este ainda está sendo populado. Aguarde até 5 minutos</p>
<p>User: Admin<br />Pass: zabbix</p>
<p>Após logar, vá em Configuration - Hosts , selecione o host Zabbix server<br> no Agent, mude para DNS e coloque zabbix-agent no campo DNS name, para que o agent do zabbix fique ativado </p>
<p>Acesse o Portainer pelo navegador utilizando o IP do servidor de instala&ccedil;&atilde;o:9000.</p>
<p><strong>Diret&oacute;rios Principais da Instala&ccedil;&atilde;o</strong></p>
<p>Docker Compose: /home/zabbix</p>
<p>PostgreSQL e Zabbix persistent files: /opt/</p>
