# DHCP

O Dynamic Host Configuration Protocol (DHCP) é um protocolo de rede que automatiza a atribuição de endereços IP e outras configurações de rede a dispositivos clientes em uma rede. O DHCP funciona enviando e recebendo mensagens entre dispositivos clientes e servidores DHCP.

## Instalação

Utilize o comando `sudo apt install dnsmasq` para instalação do dnsmasq que iremos utilizar para configurar o dhcp



## Configuração

Arquivo de configuração: A configuração principal do dnsmasq é realizada no arquivo `/etc/dnsmasq.conf.`
Endereços DNS e encaminhamento: Após configurar o dnsmasq, adicione o endereço local como servidor DNS no arquivo `/etc/resolv.conf.` Isso garante que todas as consultas sejam enviadas ao dnsmasq.


[![dhcp](https://i.im.ge/2023/12/30/xgLw6Y.dhcp.png)](https://im.ge/i/xgLw6Y)

## Teste

Conecte um dispositivo à rede gerenciada pelo dnsmasq.
Tente fazer uma solicitação de DNS, como acessar um site.

[![dhcpxp1](https://i.im.ge/2023/12/30/xgDsxa.dhcpxp1.png)](https://im.ge/i/xgDsxa)

Verifique os logs do dnsmasq em `/var/log/dnsmasq.log` para garantir que as consultas estejam sendo processadas corretamente.

[![logdhcp](https://i.im.ge/2023/12/30/xgDldr.logdhcp.png)](https://im.ge/i/xgDldr)



