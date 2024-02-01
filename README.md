# Phishing para captura de senhas do Facebook

### Ferramentas

- Kali Linux
- setoolkit

### Configurando o Phishing no Kali Linux

- Acesso root: ``` sudo su ```
- Iniciando o setoolkit: ``` setoolkit ```
- Tipo de ataque: ``` Social-Engineering Attacks ```
- Vetor de ataque: ``` Web Site Attack Vectors ```
- Método de ataque: ```Credential Harvester Attack Method ```
- Método de ataque: ``` Site Cloner ```
- Obtendo o endereço da máquina: ``` ifconfig ```
- URL para clone: http://www.facebook.com

### Resutados para Versão do Facebook sem Defesa 

![Alt text](./passwd.png "Optional title")

### Resultado Atual do Facebook com Defesa
-Observem que o site do facebook está usando um script que deve estar fazendo hashs e codifgicado em base64 os dados 
da página web , espcecialmente login e senha. Essa defesa é justamente contra script maliciosos pouco elaborados.
![Alt text](./Capturar21.JPG "Optional title")
