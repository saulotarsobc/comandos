<!-- <h1 align="center">😁 Comando básicos -> Huawei NE40E</h1> -->

<!-- <h4 align="center">
🚧 OPS!! Em construção... 🚧
</h4> -->

# 1. 😁 Comando básicos -> Huawei NE40E

## 1.1. 🚧 OPS!! Em construção... 🚧

<!-- <h1 align="center">
<img alt="ne40e" title="ne40e" src="./img/ne40e.png" />
</h1> -->

![ne40e](./img/ne40e.png)

### 1.1.1. ◾ MUDAR SENHA - CHANGE PASSWORD

```md
aaa
local-user root password cipher [senha]
commit

```

### 1.1.2. ◾ MUDAR PORTA SSH - CHANGE SSH PORT

```md
ssh server port [porta]

```

### 1.1.3. ◾ ROTAS ESTÁTICAS - STATIC ROUTES

```md
ip route-static [ip_do_cliente] [mascara ex: 24] [ip_do_concentrador] description [descricao]

```

> ip route-static 192.168.2.1 24 192.168.0.1 description para_narnia

### 1.1.4. ◾ MONITORAR TRAFEGO - TRAFFIC MONITOR

```md
monitor interface-statistics interface [interface] interval [segundos] times [numero vezes ou 'infinity']

```

> monitor interface-statistics interface GigabitEthernet 0/3/4 interval 2 times infinity

### 1.1.5. ◾VERIFICAR ROTAS - DISPLAY ROUTING

#### 1.1.5.1. ▪️ NORMAL

```md
display ip routing-table protocol static

```

#### 1.1.5.2. ▪️ COM FILTRO

```md
display ip routing-table protocol static | include [expressao]

```

### 1.1.6. ◾ UPTIME

display version

### 1.1.7. ◾ IP ADDRESS

#### 1.1.7.1. ADD

```md
ip address [ip] [mascara]
ip address [ip] [mascara] sub
ip address [ip] [mascara] sub
commit

```

#### 1.1.7.2. REMOVER

```md
undo ip address [ip] [mascara] sub
undo ip address [ip] [mascara] sub
undo ip address [ip] [mascara]
commit

```

### 1.1.8. ◾ GATEWAY

```md
ip route-static 0.0.0.0 0.0.0.0 [ip_gateway]
commit

```

> Ex: ip route-static 0.0.0.0 0.0.0.0 172.31.255.1

### 1.1.9. ◾ EXIBIR IPS ANUNCIADOS DO PEER

display bgp peer
display bgp routing-table peer [ip_do_peer] advertised-routes

### 1.1.10. ◾ SOBRE BGP

#### 1.1.10.1. ▪️ Exibir blocos redes 'saindo' por prefixo

```py
display ip ip-prefix [nome_do_prefixo]

```
