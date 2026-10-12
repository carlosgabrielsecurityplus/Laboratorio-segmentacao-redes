# Laboratório 01 — Planejamento e Topologia de Rede

## 1. Objetivo

Construir uma infraestrutura de rede no Cisco Packet Tracer para estudar os conceitos de domínios de colisão, domínios de broadcast, endereçamento IPv4, roteamento e análise de tráfego.

## 2. Equipamentos utilizados

- 1 roteador Cisco 2911
    
- 2 switches Cisco 2960
    
- 4 computadores PC-PT
    
- Cabos Copper Straight-Through
    

## 3. Topologia da rede

A topologia foi organizada em dois segmentos de rede, interligados por um roteador central.

Cada switch conecta dois computadores, formando a estrutura física que será utilizada nos testes de comunicação.

  

## 4. Planejamento de endereçamento IPv4

|Dispositivo|Endereço IPv4|Máscara|Gateway|
|---|---|---|---|
|PC0|192.168.10.10|255.255.255.0|192.168.10.1|
|PC1|192.168.10.20|255.255.255.0|192.168.10.1|
|PC2|192.168.20.10|255.255.255.0|192.168.20.1|
|PC3|192.168.20.20|255.255.255.0|192.168.20.1|

## 5. Conceitos envolvidos

**Domínio de colisão:** cada conexão Ethernet entre um computador e uma porta de switch representa um domínio de colisão separado.

**Domínio de broadcast:** cada segmento de rede conectado a uma interface distinta do roteador representa um domínio de broadcast, considerando a configuração planejada.

**Roteamento:** o roteador permitirá a comunicação entre as redes 192.168.10.0/24 e 192.168.20.0/24.

## 6. Estado inicial

A topologia física foi montada no Cisco Packet Tracer.

As conexões entre computadores e switches apresentaram indicadores verdes. As conexões entre switches e roteador apresentaram indicadores vermelhos, indicando a necessidade de verificar e ativar as interfaces do roteador.

## 7. Próximas etapas

- Configurar as interfaces do roteador.
    
- Atribuir endereços IPv4 aos computadores.
    
- Realizar testes de conectividade com ping.
    
- Analisar pacotes ARP e ICMP.
    
- Registrar evidências dos testes.