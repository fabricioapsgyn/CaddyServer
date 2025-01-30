# CaddyServer
Configuração básica do caddyserver


# 🌐 **CaddyServer**

`CaddyServer` 
A maioria das pessoas usa o Caddy como um servidor web ou proxy, mas, em sua essência, o Caddy é um servidor de servidores. 
Com os módulos necessários, ele pode assumir o papel de qualquer processo de longa duração!
Possui caracteristicas avançadas, como:
- 🔗 HTTPS/TLS para domínios personalizados.
- 📊 Provisionar certificados dinamicamente.
- ⚙️ Tudo o que você precisa para TLS e PKI.
- 🛠️ API de configuração on-line.
- 🔒 Compatível com PCI, HIPAA e NIST.
- 📋 HTTPS para localhost.
- 🚀 Coordenação de cluster.

---
### **1. Instalação ** 🛠️
a. Faça o download do binário do Caddyserver no site: https://caddyserver.com/download.
b. Crie uma pasta qualquer para jogar esse binário. Ex.: C:\Program Files\Caddy.
c. Renomeie o binário para qualquer nome e jogue na pasta do passo anterior. Ex.: C:\Program Files\Caddy\caddy.exe
d. Se preferir pode colocar o caminho da pasta C:\Program Files\Caddy nas variaveis de ambiente no path das variaveis de sistema.
e. Abra o cmd ou promt de sua preferência como administrador e execute o seguinte comando: caddy --version
f. Se retornar a versao do caddyserver entao podemos passar para o proximo passo. 

### **2. Configuração Básica** 🛠️
a. Crie um arquivo de nome Caddyfile na mesma pasta do passo 2. Ex.: C:\Program Files\Caddy\Caddyfile
b. O nome do arquivo anterior precisa ser Caddyfile com a letra C em maiúscula e sem extensão.
c. Dentro desse arquivo Caddyfile coloque apenas isso, mudando apenas o nome do site:
```
seusite.com.br {
	     encode gzip
	     reverse_proxy 127.0.0.1:8885
        }
```
d. Abra o cmd ou promt de sua preferência como administrador e execute o seguinte comando:
```
caddy run --config "C:\Program Files\Caddy\Caddyfile"
```
e. Com seu DNS configure o alias apontando para o ip da sua vps. Ex.: seusite.com.br A 40.50.60.70

