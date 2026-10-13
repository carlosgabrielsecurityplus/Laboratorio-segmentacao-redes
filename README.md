
# Laboratório de Segmentação de Redes — Cisco Packet Tracer

## Sobre o projeto

Laboratório prático desenvolvido no Cisco Packet Tracer com o objetivo de implementar e validar a comunicação entre duas redes IPv4 distintas, utilizando um Roteador Cisco 2911.

O projeto contempla planejamento de endereçamento, configuração de interfaces, implementação de DHCP, testes de conectividade e documentação técnica das etapas.

## Topologia de rede

A infraestrutura é composta por:

- 1 roteador Cisco 2911
    
- 2 switches Cisco 2960
    
- 4 computadores
    
- 2 redes IPv4 distintas

![Topologia final do laboratório](evidencias/8-%20topologia%20final.png)  

## Planejamento de endereçamento

|Rede|Sub-rede|Interface|Gateway|
|---|---|---|---|
|REDE10|192.168.10.0/24|GigabitEthernet0/0|192.168.10.1|
|REDE20|192.168.20.0/24|GigabitEthernet0/1|192.168.20.1|

## Implementação

### Configuração do roteador

Foram configuradas e habilitadas duas interfaces GigabitEthernet para permitir o roteamento entre as redes diretamente conectadas.

### Serviço DHCP

O roteador Cisco 2911 foi configurado como servidor DHCP, utilizando dois pools independentes:

- REDE10: distribuição automática de endereços na rede 192.168.10.0/24.
    
- REDE20: distribuição automática de endereços na rede 192.168.20.0/24.
    

Os endereços de .1 até .9 foram excluídos da distribuição automática em cada rede.

### Testes de conectividade

Foram realizados testes ICMP entre computadores da mesma rede e de redes diferentes.

Os resultados confirmaram a comunicação local e o funcionamento do roteamento IPv4 entre as duas redes.
![Teste de conectividade entre redes](evidencias/7-%20Teste%20de%20conectividade%20entre%20redes.png)
## Tecnologias e conceitos utilizados

- Cisco Packet Tracer
    
- Cisco IOS
    
- Endereçamento IPv4 e máscara de sub-rede
    
- Roteamento entre redes diretamente conectadas
    
- DHCP
    
- ARP e ICMP
    
- Comandos de diagnóstico e verificação
    
- Git e GitHub
    
- Documentação técnica em Markdown
    

## Arquivo do laboratório

O arquivo `laboratorio-segmentacao-redes.pkt` contém a topologia e as configurações implementadas no Cisco Packet Tracer.

## Objetivo educacional

Este projeto foi desenvolvido para consolidar conhecimentos de infraestrutura de redes, configuração de dispositivos Cisco, serviços de rede e diagnóstico de conectividade, como parte de um portfólio prático de tecnologia da informação e segurança cibernética.
## Documentação técnica

Todas as etapas do laboratório foram registradas na pasta `documentacao`, incluindo planejamento, configurações, comandos Cisco IOS e evidências.

A documentação está organizada em cinco etapas:

1. **Planejamento da rede** — definição da topologia e do endereçamento IPv4.
    
2. **Análise inicial do roteador** — diagnóstico das interfaces e identificação do estado operacional.
    
3. **Ativação das interfaces** — habilitação das conexões físicas do Cisco 2911.
    
4. **Configuração do endereçamento IPv4** — atribuição dos gateways às interfaces do roteador.
    
5. **Implementação do DHCP** — criação dos pools, distribuição automática de endereços e testes de conectividade.
    

Os documentos estão disponíveis na pasta [ver documentação](documentacao/)
