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

### Contornando a Defesa do Facebook
-Uma solução pode ser atualizando o script python do setoolkit. Contudo não é muito interessante ficar a cada site com suas defesas
peculiares ficar colocando a mão dentro do código do set.
-Outra solução é a oferecida pelo próprio setoolkit que é realizar uma importação customizada (Custon Import) no lugar da clonagem direta( Site Cloner). Na importação customizada iremos clonar um código fonte manipulado da página original. 

![Alt text](./Capturar13.JPG "Optional title")

### Passo 1 
-Salve a página do facebook e também inspecione o botão log in e anote seu id.

![Alt text](./Capturar.JPG "Optional title")

-id do botão

![Alt text](./Capturar5.JPG "Optional title")

-Aproveite para renomear logo a págna salva para index.html, pois o setookit usa esse nome por padrão.

![Alt text](./Capturar17.JPG "Optional title")

### Passo 2 
