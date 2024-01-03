# PROXY

O proxy é um servidor intermediário que atua como um intermediário entre um cliente e um servidor. Os proxies são usados para uma variedade de propósitos, incluindo:

Redirecionamento de tráfego: Os proxies podem ser usados para redirecionar o tráfego da Internet de um cliente para outro servidor. Isso pode ser usado para melhorar o desempenho ou a segurança da rede.
Filtragem de conteúdo: Os proxies podem ser usados para filtrar o conteúdo da Internet que é acessado por clientes. Isso pode ser usado para bloquear sites indesejados ou conteúdo prejudicial.
Cache: Os proxies podem ser usados para armazenar em cache o conteúdo da Internet que é acessado por clientes. Isso pode melhorar o desempenho da rede, pois os clientes não precisam acessar o servidor original sempre que precisarem do conteúdo.

## Instalação

Para instalar o proxy squid use o comando:

`sudo apt-get install squid3`

Reinicie o Squid:

`sudo systemctl restart squid`

O Squid será instalado e iniciado automaticamente.


## Configuração

Para configurar o Squid, edite o arquivo de configuração `/etc/squid/squid.conf.`

Para criar uma regra de proxy, adicione uma nova linha ao arquivo squid.conf. A linha deve conter as seguintes informações:

Nome da regra: O nome da regra de proxy.
Endereço IP ou nome de host: O endereço IP ou nome de host do servidor proxy.
Porta do proxy: A porta do proxy.
Permissões: As permissões de acesso à regra de proxy.

[![novoacl](https://i.im.ge/2023/12/29/xx1B0z.novoacl.png)](https://im.ge/i/xx1B0z)

[![Screenshot_2023-11-16_17-26-11](https://i.im.ge/2023/12/29/xx1kCG.Screenshot-2023-11-16-17-26-11.png)](https://im.ge/i/xx1kCG)


Para reiniciar o Squid após a configuração, execute o seguinte comando:

`sudo systemctl restart squid`





## Teste

Paginas bloqueadas

[![Screenshot_2023-11-16_17-27-51](https://i.im.ge/2023/12/29/xx1fDL.Screenshot-2023-11-16-17-27-51.png)](https://im.ge/i/xx1fDL)
[![Screenshot_2023-11-16_17-28-16](https://i.im.ge/2023/12/29/xx1ZgT.Screenshot-2023-11-16-17-28-16.png)](https://im.ge/i/xx1ZgT)
[![Screenshot_2023-11-16_17-28-36](https://i.im.ge/2023/12/29/xx1Kec.Screenshot-2023-11-16-17-28-36.png)](https://im.ge/i/xx1Kec)
[![Screenshot_2023-11-16_17-28-47](https://i.im.ge/2023/12/29/xx1W00.Screenshot-2023-11-16-17-28-47.png)](https://im.ge/i/xx1W00)
[![dominio](https://i.im.ge/2023/12/29/xx1JVy.dominio.png)](https://im.ge/i/xx1JVy)

Logs de Acesso no arquivo `/var/log/squid.` O nome do arquivo de log padrão é access.log. Este arquivo contém um registro de todas as solicitações HTTP feitas pelo proxy Squid.

Você pode alterar o nome e a localização do arquivo de log padrão editando o arquivo de configuração `/etc/squid/squid.conf.` A diretiva access_log especifica o nome e a localização do arquivo de log

[![Screenshot_2023-11-16_17-32-03](https://i.im.ge/2023/12/29/xx1zvx.Screenshot-2023-11-16-17-32-03.png)](https://im.ge/i/xx1zvx)
[![Screenshot_2023-11-16_17-32-25](https://i.im.ge/2023/12/29/xx1pSa.Screenshot-2023-11-16-17-32-25.png)](https://im.ge/i/xx1pSa)
[![Screenshot_2023-11-16_17-32-41](https://i.im.ge/2023/12/29/xx1v6J.Screenshot-2023-11-16-17-32-41.png)](https://im.ge/i/xx1v6J)
[![tempo](https://i.im.ge/2023/12/29/xx14rS.tempo.png)](https://im.ge/i/xx14rS)

[![log](https://i.im.ge/2023/12/29/xx1Gg6.log.png)](https://im.ge/i/xx1Gg6)


O proxy de tempo desbloqueado

[![tempo2](https://i.im.ge/2023/12/29/xx2QDK.tempo2.png)](https://im.ge/i/xx2QDK)
[![tempofunci](https://i.im.ge/2023/12/29/xx2TE9.tempofunci.png)](https://im.ge/i/xx2TE9)

## Extra

Aqui estão alguns comandos adicionais que você pode usar para gerenciar o Squid:

Para exibir a lista de todas as regras de proxy:

`squid -k parse`

Para verificar se o Squid está funcionando:

`squid -k check`

Para parar o Squid:

`sudo systemctl stop squid`

Para iniciar o Squid:

`sudo systemctl start squid`

Para reiniciar o Squid:

`sudo systemctl restart squid`