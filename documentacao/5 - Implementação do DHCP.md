
### Objetivo

Implementar o serviço DHCP (_Dynamic Host Configuration Protocol_) no roteador Cisco 2911, permitindo a distribuição automática de endereços IPv4 aos dispositivos das duas redes locais.

O próprio roteador será responsável pelo fornecimento dos parâmetros de endereçamento, eliminando a necessidade de configurar manualmente cada computador.

###  Configuração dos pools DHCP

|Parâmetro|REDE10|REDE20|
|---|---|---|
|Rede|192.168.10.0/24|192.168.20.0/24|
|Máscara|255.255.255.0|255.255.255.0|
|Gateway|192.168.10.1|192.168.20.1|
|Endereços excluídos|.1 até .9|.1 até .9|
|Primeiro IP elegível|192.168.10.10|192.168.20.10|

O comando `ip dhcp excluded-address` foi utilizado para impedir a distribuição dos primeiros endereços de cada rede, reservando-os para possíveis configurações estáticas.

O comando `ip dhcp pool` permitiu criar os pools REDE10 e REDE20. Em cada pool, foram definidos a rede correspondente e o gateway padrão por meio dos comandos `network` e `default-router`.
### 6.4. Verificação da configuração
![[Configuração DHCP no Roteador.png]]
Após a configuração, foi utilizado o comando:

`show running-config | section ip dhcp pool`

Esse comando serve para visualizar especificamente as configurações dos pools DHCP, facilitando a verificação das redes e dos gateways definidos.

A saída do roteador confirmou a presença dos pools REDE10 e REDE20, cada um associado à sua respectiva rede e gateway.
