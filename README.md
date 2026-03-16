# Curso-dio-Santander-Ciberseguranca


Comando para modelo SMB
Para iniciar o ataque precisa conhcer seu usuário o comanodo e:

enum4linux -a ip_da_máquina_aqui | tee enum4_output.txt

Vai aparecer varias informações e mais embaixo vai aparecer o campo dos usuários

Ex: user[arthur] rid:[#####]

Depois disso coloque esse comando para o txt dos usuário:

echo -e "user\nmsfadmin\nservice" > smb_user.txt


Outro comando para as senhas:

echo -e "password\n123456\nWelcome123\nmsfadmin" > senhas_spray.txt


