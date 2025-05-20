(primeiro passo)

switch> enable
Switch# configure terminal
Switch(config)# hostname sw-01
Switch(config)# service password-encryption
Switch(config)# service timestamps log datetime msec
Switch(config)# logging buffered 4096
Switch(config)# no ip domain-lookup
Switch(config)# banner motd #banner de aviso#
Switch(config)# enable secret senha_segura
Switch(config)# username nome_de_usuario secret senha_segura
Switch(config)# username nome_de_usuario password senha_nao_segura
Switch(config)# username nome_de_usuario privilege 15 secret senha_segura
Switch(config)# no cdp run
Switch(config)# no lldp run
Switch(config)# line console 0
Switch(config)# login local
Switch(config)# password senha_nao_segura
Switch(config)# logging synchronous
Switch(config)# exec-timeout minuto segundo
Switch(config)# end
Switch# write

(segundo passo) (VTY)

Switch> enable
Switch# configure terminal
Switch(config)# line vty 0 4
Switch(config-line)# login local
Switch(config-line)# password senha_nao_segura
Switch(config-line)# logging synchronous
Switch(config-line)# exec_timeout minuto segundo
Switch(config-line)# transport input ssh
Switch(config-line)# end
Switch# write

(terceiro passo) (SVI)

Switch> enable
Switch# configure terminal
Switch(config)# ip default-gateway gateway.padrao
Switch(config)# interface vlan 1
Switch(config-if)# description Interface de SVI
Switch(config-if)# ip address IPv4 MáscaraDeSubrede
Switch(config-if)# no shutdown
Switch(config-if)# end OU do write
Switch# write

(quarto passo) (SSH)

Switch> enable
Switch# configure terminal
Switch(config)# ip domain-name dominio.infra
Switch(config)# crypto key generate rsa general-keys modulus 1024
Switch(config)# ip ssh version 2
Switch(config)# ip ssh time-out 60
Switch(config)# ip ssh authentication-retries 2
Switch(config)# end OU write
Switch# write

(quinto passo) (Interface de LAN)

Router> enable
Router# configure terminal
Router(config)# interface tipodeconexao ?/?
Router(config-int) description Interface de Gateway da LAN
Router(config-int) ip address 192.168.1.254 255.255.255.0
Router(config-int)# no shutdown
Router(config)#end OU write 

(sexto passo) (Backups)   (confirmar: ENTER) (cancelar: CTRL C)

copy origem destino  (running-config, startup-config, flash: , tftp: )

(sétimo passo) (config roteador)

Switch> enable
Switch# configure terminal
Switch(config)# hostname nome_do_roteador
Switch(config)# interface tipodeconexao ?/?
Switch(config-if)# ip address IPv4 MascaraDeSubrede
Switch(config-if)# no shutdown
Switch(config-if)# description qualquer frase ou palavra
Switch(config-if)# exit
Switch(config)# interface serial ?/?
Switch(config-if)# clock rate numero
Switch(config-if)# bandwidth numero
Switch(config-if)# exit
Switch(config)# router rip
Switch(config-router)# network ?.?.?.0 (adicionar todas as conexões com 0 no final)
Switch(config-router)# end
Switch# write