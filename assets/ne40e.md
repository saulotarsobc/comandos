<h1 align="center">😁 Comando básicos -> Huaweu NE40E</h1>

<h4 align="center">
  🚧 OPS!! Em construção... 🚧
</h4>

<h1 align="center">
  <img alt="ne40e" title="ne40e" src="./img/ne40e.png" />
</h1>

### ◾ MUDAR SENHA - CHANGE PASSWORD
```
aaa
local-user root password cipher [sua_senha]
comm
```

### ◾ MUDAR PORTA SSH - CHANGE SSH PORT
    ssh server port [porta]

### ◾ ROTAS ESTÁTICAS - STATIC ROUTES
    ip route-static [ip_do_cliente] [mascara ex: 24] [ip_do_concentrador] description [descricao]
  Ex:
  >ip route-static 192.168.2.1 24 192.168.0.1 description para_narnia

### ◾ MONITORAR TRAFEGO - TRAFFIC MONITOR
    $ monitor interface-statistics interface [interface] interval [segundos] times [vezes(ou 'infinity')]
  Ex:
  >monitor interface-statistics interface GigabitEthernet 0/3/4 interval 2 times infinity

### ◾  VERIFICAR ROTAS - DISPLAY ROUTING
  ##### ▪️ NORMAL
    $ display ip routing-table protocol static

  ##### ▪️ COM FILTRO
    $ display ip routing-table protocol static | include [expressao]

### ◾ UPTIME
    display version

### ◾ IP ADDRESS ADD
    $ ip address [ip] [mascara]
    $ ip address [ip] [mascara] sub
    $ ip address [ip] [mascara] sub

### ◾ IP ADDRESS REMOVE
    undo ip address [ip] [mascara] sub
    undo ip address [ip] [mascara] sub
    undo ip address [ip] [mascara]
    commit

### ◾ GATEWAY
    ip route-static 0.0.0.0 0.0.0.0 [ip_gateway]
    commit
Ex:
  >ip route-static 0.0.0.0 0.0.0.0 172.31.255.1

### ◾ EXIBIR IPS ANUNCIADOS DO PEER
    $ display bgp peer
    $ display bgp routing-table peer [ip_do_peer] advertised-routes