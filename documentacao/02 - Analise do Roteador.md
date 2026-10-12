# Configurações do Roteador 

## 1. Diagnóstico inicial

Antes de iniciar a configuração das interfaces, foi realizada uma verificação do estado operacional do roteador Cisco 2911.

### Comandos utilizados

`enable`

Permite acessar o modo EXEC privilegiado do Cisco IOS, necessário para executar comandos administrativos e de diagnóstico.

`show ip interface brief`

Exibe um resumo das interfaces de rede, incluindo seus endereços IPv4, estado administrativo e estado do protocolo de linha.

### Resultados observados

|Interface|Endereço IPv4|Status|Protocol|
|---|---|---|---|
|GigabitEthernet0/0|unassigned|administratively down|down|
|GigabitEthernet0/1|unassigned|administratively down|down|
|GigabitEthernet0/2|unassigned|administratively down|down|
|Vlan1|unassigned|administratively down|down|

Todas as interfaces apresentaram o estado `administratively down`, indicando que estavam desativadas administrativamente.

Também foi identificado que nenhuma interface possuía endereço IPv4 configurado.

## 2. Verificação de vizinhos — CDP

### Comando utilizado

`show cdp neighbors`

O Cisco Discovery Protocol (CDP) permite identificar dispositivos Cisco diretamente conectados, apresentando informações como identificação do dispositivo, interface local e porta remota.

### Resultado observado

Nenhum dispositivo vizinho foi identificado.

### Análise técnica

A ausência de vizinhos é compatível com o estado administrativamente desativado das interfaces do roteador.

Após a ativação dos enlaces, será realizada uma nova verificação para confirmar a descoberta dos switches.

## 3. Próxima configuração

Habilitar as interfaces conectadas aos switches e atribuir os endereços IPv4 definidos no planejamento da rede.