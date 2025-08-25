(Primeiro passo) (configurando vlan)

Switch> enable
Switch# configure terminal
Switch(config)# vlan numero
Switch(config-vlan)# name um nome qualquer
Switch(config)# interface tipodeethernet 0/0 OU interface range tipodeethernet 0/0-0
Switch(config-if)# switchport acess vlan numero
Switch(config) end OU write