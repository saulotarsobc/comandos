# 😁 Comando básicos -> Huawei NE40E

## 🚧 OPS!! Em construção... 🚧

<!-- <h1 align="center">
<img alt="ne40e" title="ne40e" src="./img/ne40e.png" />
</h1> -->

![ne40e](./img/ne40e.png)

### ADICIONAR USUARIO OU MUDAR SENHA - ADD USER OR CHANGE PASSWORD

```md
aaa
local-user nome@domain.com password cipher [senha]
```

### ADICIONAR TIPOS DE SERVICO AO USER

```md
local-user nome@domain.com service-type <service>
```

> pode adicionar esses servicos: ssh, ftp, http, snmp, mml, qx, telnet ou terminal

### ALTERAR NIVEL DE ACESSO DO USUARIO

```md
local-user nome@domain.com level 3
```

### ALETERAR REGRAS DE BLOQUEIO NO CASO DE ERRO DE SENHA

```md
local-user nome@domain.com state block fail-times 3 interval 5
```

### MUDAR PORTA SSH - CHANGE SSH PORT

```md
ssh server port [porta]
```

### ROTAS ESTÁTICAS - STATIC ROUTES

```md
ip route-static [ip_do_cliente] [mascara ex: 24] [ip_do_concentrador] description [descricao]
```

> ip route-static 192.168.2.1 24 192.168.0.1 description para_narnia

### MONITORAR TRAFEGO - TRAFFIC MONITOR

```md
monitor interface-statistics interface [interface] interval [segundos] times [numero vezes ou 'infinity']
```

> monitor interface-statistics interface GigabitEthernet 0/3/4 interval 2 times infinity

### VERIFICAR ROTAS - DISPLAY ROUTING

#### NORMAL

```md
display ip routing-table protocol static
```

#### COM FILTRO

```md
display ip routing-table protocol static | include [expressao]
```

### UPTIME

```md
display version
```

### IP ADDRESS

#### ADD

```md
ip address [ip] [mascara]
ip address [ip] [mascara] sub
ip address [ip] [mascara] sub
```

#### REMOVER

```md
undo ip address [ip] [mascara] sub
undo ip address [ip] [mascara] sub
undo ip address [ip] [mascara]
```

### GATEWAY

```md
ip route-static 0.0.0.0 0.0.0.0 [ip_gateway]
```

> ip route-static 0.0.0.0 0.0.0.0 172.31.255.1

### EXIBIR IPS ANUNCIADOS DO PEER

```md
display bgp peer
display bgp routing-table peer [ip_do_peer] advertised-routes
```

### SOBRE BGP

#### Exibir blocos redes 'saindo' por prefixo

```md
display ip ip-prefix [nome_do_prefixo]
```

## DISPLAY INTERFACE

```md
display interface brief
```

## VERIFICAR CPU

```md
display cpu-usage
display cpu-monitor information all
display cpu monitor history
display cpu-defend all statistics
```
