<h1 align="center">😁 Comando básicos -> Huaweu NE40E</h1>

<h4 align="center">
  🚧 OPS!! Em construção... 🚧
</h4>

<h1 align="center">
  <img alt="ne40e" title="ne40e" src="../img/ne40e.png" />
</h1>

## ◾ MUDAR SENHA - CHANGE PASSWORD
```
aaa
local-user root password cipher [seua_senha]
comm
```

## ◾ MUDAR PORTA SSH - CHANGE SSH PORT
    ssh server port [porta]

## ◾ ROTAS ESTÁTICAS - STATIC ROUTES
    ip route-static [ip_do_cliente] 32 [ip_do_concentrador] description [descricao]

## ◾ MONITORAR TRAFEGO - TRAFFIC MONITOR
	monitor interface-statistics interface GigabitEthernet 0/3/4 interval 2 times infinity

### ◾  VERIFICAR ROTAS - DISPLAY ROUTING
  ### ◾ NORMAL
    display ip routing-table protocol static

  ### ◾ COM FILTRO
    display ip routing-table protocol static | include <EXPRESSÃO>

## ◾ UPTIME
    display version

## ◾ IP ADDRESS ADD
    ip address <IP> <MÁSCARA>
    ip address <IP> <MÁSCARA> sub
    ip address <IP> <MÁSCARA> sub

## ◾ IP ADDRESS REMOVE
    undo ip address <IP> <MÁSCARA> sub
    undo ip address <IP> <MÁSCARA> sub
    undo ip address <IP> <MÁSCARA>
    commit

GATEWAY
	ip route-static 0.0.0.0 0.0.0.0 <ip gateway>
	commit
