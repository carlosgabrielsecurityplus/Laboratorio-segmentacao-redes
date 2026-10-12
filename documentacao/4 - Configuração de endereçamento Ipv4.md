### Objetivo

Configurar os endereços IPv4 das interfaces do roteador Cisco 2911, permitindo que ele atue como gateway padrão para as duas redes locais.

### Comandos utilizados

```text
Router# configure terminal
Router(config)# interface gigabitEthernet 0/0
Router(config-if)# ip address 192.168.10.1 255.255.255.0
Router(config-if)# exit
Router(config)# interface gigabitEthernet 0/1
Router(config-if)# ip address 192.168.20.1 255.255.255.0
Router(config-if)# no shutdown
Router(config-if)# end
Router# show ip interface brief
Router# copy running-config startup-config
Destination filename [startup-config]?
Building configuration...
[OK]
```

### Persistência da configuração na NVRAM

Após a configuração e verificação das interfaces, foi executado o comando `copy running-config startup-config`.

Esse comando copia a configuração atualmente em execução (_running-config_), armazenada na RAM, para a configuração de inicialização (_startup-config_), armazenada na NVRAM.

O objetivo é preservar as configurações do equipamento após uma reinicialização.

O retorno `[OK]` confirmou que a operação foi concluída com sucesso.

**Observação:** na primeira tentativa, foi digitado `y` na solicitação do nome do arquivo, resultando no erro `%Error copying nvram:y: (Invalid argument)`. Na segunda tentativa, foi pressionado Enter para aceitar o nome padrão `startup-config`, e o salvamento foi concluído corretamente.
### Resultados obtidos

|Interface|Endereço IPv4|Máscara|Estado|
|---|---|---|---|
|GigabitEthernet0/0|192.168.10.1|255.255.255.0|up/up|
|GigabitEthernet0/1|192.168.20.1|255.255.255.0|up/up|

### Análise técnica

As interfaces GigabitEthernet0/0 e GigabitEthernet0/1 foram configuradas com endereços IPv4 pertencentes a redes distintas.

O roteador possui duas redes diretamente conectadas:

- 192.168.10.0/24
    
- 192.168.20.0/24
    

O estado `up/up` confirma que os enlaces estão operacionais. A comunicação entre computadores de redes diferentes será validada posteriormente por meio de testes de conectividade.
