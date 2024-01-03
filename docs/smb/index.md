# SMB

O Server Message Block (SMB) é um protocolo de rede que permite que computadores compartilhem arquivos, pastas e impressoras. O SMB é um protocolo muito comum e é usado em uma variedade de sistemas operacionais, incluindo Windows, macOS e Linux.

O SMB funciona enviando e recebendo mensagens entre computadores. As mensagens SMB são codificadas em um formato binário eficiente.


## Instalação

Instalar o servidor Samba no Alpine Linux é bem similar ao processo em outras distribuições, mas os comandos específicos serão diferentes. Veja como fazer:

1.Instalação:

Abra um terminal e execute o seguinte comando para instalar o pacote Samba:

`apk add samba`

Isso instalará o pacote Samba e seus dependências.

2.Verificação de status:

Verifique se o Samba está rodando com o comando:

`rc-service samba status`

3.Configuração:

O principal arquivo de configuração do Samba no Alpine Linux é `/etc/samba/smb.conf.` Você pode editá-lo com um editor de texto como o nano:

`nano /etc/samba/smb.conf`

Recomenda-se não modificar diretamente o arquivo de configuração padrão `(smb.conf.default).` Em vez disso, crie uma nova seção específica para o seu compartilhamento.

4.Criando um compartilhamento:

Adicione uma nova seção ao arquivo smb.conf com as seguintes informações:

Nome: O nome do compartilhamento de arquivos que os usuários verão.
Permissões: As permissões de acesso para leitura e/ou escrita (ex.: read list).
Localização: O caminho para o diretório que deseja compartilhar.
Exemplo:

[![sambaxarope2](https://i.im.ge/2023/12/29/xx1Fbc.sambaxarope2.png)](https://im.ge/i/xx1Fbc)


5.Reinicialização e confirmação:

Depois de editar o `smb.conf`, reinicie o Samba para aplicar as alterações:

`rc-service samba restart`

Verifique se o compartilhamento está acessível usando o comando:

`rc-service samba status`

6.Em seguida usaremos o comando samba-tool para provisionar um dominio. O comando samba-tool domain provision é usado para provisionar um novo domínio Samba. Ele cria o domínio, os usuários e grupos administrativos, e as zonas de domínio DNS.

[![sambacomando](https://i.im.ge/2023/12/30/xgOwJC.sambacomando.png)](https://im.ge/i/xgOwJC)

Para usar o comando, você precisa fornecer as seguintes informações:

Nome do domínio: O nome do domínio que você deseja criar.
Endereço IP do controlador de domínio: O endereço IP do controlador de domínio que será usado para hospedar o domínio.
Senha do administrador do domínio: A senha do administrador do domínio.


## Configuração

[![sambaxarope](https://i.im.ge/2023/12/29/xx1uiT.sambaxarope.png)](https://im.ge/i/xx1uiT)

## Teste
No teste temos duas familias com sobrenomes distintos, no qual a familia "Carvalho" não pode acessar a pasta da familia "Feitosa" e vice-versa.

1. Criar 2 grupos para dois de seus sobrenomes;
2. Criar 4 usuários, dois para cada um dos sobrenomes;
3. Compartilhar duas pastas com dois de seus sobrenome, compartilhado para o grupo com o sobrenome correspondente. 

[![samba2f](https://i.im.ge/2023/12/29/xx1SAx.samba2f.png)](https://im.ge/i/xx1SAx)
[![samba2c](https://i.im.ge/2023/12/29/xx12aG.samba2c.png)](https://im.ge/i/xx12aG)
[![samba2](https://i.im.ge/2023/12/29/xx1OGL.samba2.png)](https://im.ge/i/xx1OGL)
[![samba](https://i.im.ge/2023/12/29/xx1dpa.samba.png)](https://im.ge/i/xx1dpa)
[![josesambafeitosa](https://i.im.ge/2023/12/29/xx1s1J.josesambafeitosa.png)](https://im.ge/i/xx1s1J)
[![clarasamba](https://i.im.ge/2023/12/29/xx1awy.clarasamba.png)](https://im.ge/i/xx1awy)
[![calsasambacarvalho](https://i.im.ge/2023/12/29/xx17KS.calsasambacarvalho.png)](https://im.ge/i/xx17KS)
[![adsamba2](https://i.im.ge/2023/12/29/xx1IXz.adsamba2.png)](https://im.ge/i/xx1IXz)
[![adsamba](https://i.im.ge/2023/12/29/xx1Li6.adsamba.png)](https://im.ge/i/xx1Li6)



