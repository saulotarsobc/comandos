<!-- <h1 align="center">😁 Comando básicos -> Huawei NE40E</h1> -->

<!-- <h4 align="center">
🚧 OPS!! Em construção... 🚧
</h4> -->

# 😁 Comando básicos -> Huawei NE40E

## 🚧 OPS!! Em construção... 🚧

<!-- <h1 align="center">
<img alt="ne40e" title="ne40e" src="./img/ne40e.png" />
</h1> -->

![ne40e](./img/ne40e.png)

### ◾ MUDAR SENHA - CHANGE PASSWORD

```md
aaa
local-user root password cipher [senha]
```

### ◾ MUDAR PORTA SSH - CHANGE SSH PORT

```md
ssh server port [porta]
```

### ◾ ROTAS ESTÁTICAS - STATIC ROUTES

```md
ip route-static [ip_do_cliente] [mascara ex: 24] [ip_do_concentrador] description [descricao]
```

> ip route-static 192.168.2.1 24 192.168.0.1 description para_narnia

### ◾ MONITORAR TRAFEGO - TRAFFIC MONITOR

```md
monitor interface-statistics interface [interface] interval [segundos] times [numero vezes ou 'infinity']
```

> monitor interface-statistics interface GigabitEthernet 0/3/4 interval 2 times infinity

### ◾VERIFICAR ROTAS - DISPLAY ROUTING

#### ▪️ NORMAL

```md
display ip routing-table protocol static
```

#### ▪️ COM FILTRO

```md
display ip routing-table protocol static | include [expressao]
```

### ◾ UPTIME

display version

### ◾ IP ADDRESS

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

### ◾ GATEWAY

```md
ip route-static 0.0.0.0 0.0.0.0 [ip_gateway]
```

> ip route-static 0.0.0.0 0.0.0.0 172.31.255.1

### ◾ EXIBIR IPS ANUNCIADOS DO PEER

```md
display bgp peer
display bgp routing-table peer [ip_do_peer] advertised-routes
```

### ◾ SOBRE BGP

#### ▪️ Exibir blocos redes 'saindo' por prefixo

```py
display ip ip-prefix [nome_do_prefixo]
```
