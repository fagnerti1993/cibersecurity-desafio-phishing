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
-Na situação atual do código salvo, se abrirmos no navegador veremos a página do facebook muito feia, toda desconfigurada, pois os scripts e carregamentos de css não executam corretamente se carregados localmente. Aqui caberia horas e horas mudando o código fonte se realmente desejameos um trabalho bem elaboado. Um belo exercício de front-end.

![Alt text](./Capturar2.JPG "Optional title")

-Obviamente vamos cortar caminho. Simplesmente vamos copiar o código fonte online do wwww.facebook.com no nosso arquivo index.html

![Alt text](./Capturar6.JPG "Optional title")

-Podemos ver na imagem que a página já carrega como se fosse a página online. No print a seguir, ainda não se tinha renomeado a página local para index.html

![Alt text](./Capturar8.JPG "Optional title")

-Ao procurarmos id do botão veremos onde ele está sendo manipulado no código fonte. Isso deu uma dica rápida de qual chamada de script deveria ser deletada.

![Alt text](./Capturar24.JPG "Optional title")

### Passo 3 
-Vamos remover a linha do script

![Alt text](./Capturar23.JPG "Optional title")

### Passo 4 
-Selecionamos agora no setoolkit Custom Import e em seguida devemos apontar a pasta do código fonte da página. 
- Copie o path  da pasta
 
![Alt text](./Capturar14.JPG "Optional title")

-Cole o path no setoolkit

![Alt text](./Capturar15.JPG "Optional title")

-Selecione copiar a pasta inteira (Copy entire folder)

![Alt text](./Capturar18.JPG "Optional title")

-Defina como www.facebook.com

![Alt text](./Capturar19.JPG "Optional title")

### Resultado após contorna a fefesa da página do facebook

![Alt text](./usersenhascapturados.JPG "Optional title")



