### Objetivo

Habilitar as interfaces GigabitEthernet0/0 e GigabitEthernet0/1 do roteador Cisco 2911, estabelecendo os enlaces físicos com os dois switches da topologia.

### Comandos utilizados

```
Router# configure terminal
Router(config)# interface gigabitEthernet 0/0
Router(config-if)# no shutdown
Router(config-if)# exit
Router(config)# interface gigabitEthernet 0/1
Router(config-if)# no shutdown
Router(config-if)# end
Router# show ip interface brief
```

### Explicação técnica

O comando `no shutdown` remove a desativação administrativa de uma interface, permitindo seu funcionamento.

O comando `show ip interface brief` foi utilizado para verificar o estado operacional das interfaces após a ativação.

### Resultados

|Interface|Endereço IPv4|Status|Protocol|
|---|---|---|---|
|GigabitEthernet0/0|unassigned|up|up|
|GigabitEthernet0/1|unassigned|up|up|

### Análise técnica

O estado `up/up` indica que as interfaces estão operacionais nas camadas física e de enlace.

Entretanto, as interfaces ainda não possuem endereços IPv4 configurados, sendo necessária uma etapa posterior de endereçamento para permitir a comunicação entre as redes.