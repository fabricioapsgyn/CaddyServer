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
1. Faça o download do binário do Caddyserver no site: https://caddyserver.com/download.
2. Crie uma pasta qualquer para jogar esse binário. Ex.: C:\Program Files\Caddy.
3. Renomeie o binário para qualquer nome e jogue na pasta do passo anterior. Ex.: C:\Program Files\Caddy\caddy.exe
4. Se preferir pode colocar o caminho da pasta C:\Program Files\Caddy nas variaveis de ambiente no path das variaveis de sistema.
5. Abra o cmd ou promt de sua preferência como administrador e execute o seguinte comando: caddy --version
6. Se retornar a versao do caddyserver entao podemos passar para o proximo passo. 

### **2. Configuração Básica** 🛠️
1. Crie um arquivo de nome Caddyfile na mesma pasta do passo 2. Ex.: C:\Program Files\Caddy\Caddyfile
2. O nome do arquivo anterior precisa ser Caddyfile com a letra C em maiúscula e sem extensão.
3. Dentro desse arquivo Caddyfile coloque apenas isso, mudando apenas o nome do site:
```
seusite.com.br {
	     encode gzip
	     reverse_proxy 127.0.0.1:8885
        }
```
4. Abra o cmd ou promt de sua preferência como administrador e execute o seguinte comando:
```
caddy run --config "C:\Program Files\Caddy\Caddyfile"
```
5. Com seu DNS configure o alias apontando para o ip da sua vps. Ex.: seusite.com.br A 40.50.60.70

