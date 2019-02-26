# IOT
Trabalho IOT

INSTALACAO PORTARIA VIRTUAL

1-) docker-compose build

2-) docker-compose up
3-) acessar o node-red da portaria virtual, na porta 1880
4-) configurar os nós:
4.1) de (3) enviar email com o usuário e senha de email
4.2) "preparacao email para visitante", colocar o ip do "porteiro"

INSTALACAO DO PORTEIRO

1-) instalar o arduino
2-) plugar o servo motor no PIN 7
3-) carregar o firmware StandardFirmdata no arduino
4-) instalar o node-red
5-) iniciar node-red na porta 80 (node-red run -p 80)
6-) importar o flow disponivel na pasta "porteiro" do repositorio
7-) configurar os nós:
7.1) registroVisitane e portariaVirtual para conectar no ip do mqtt iniciado anteriormente
7.2) arduino para conectar na porta COM correta

UTILIZACAO

1-) acesse a portaria virtual na porta 1880 /visita e cadastre seu visitante
2-) visitante receberá um email
3-) quando visitante chegar ao local onde está instalado o módulo de porteiro, este deve-se conectar à rede para acessar o link
disponibilizado no e-mail para registrar a presença
4-) o visitante, ao clicar no link disponivel no email, fará com que o sistema decida se libera o acesso ou não.
5-) em caso de acesso indevido, a porta não é destravada e um email para equipe de segurança é disparado. Usuário não será advertido
6-) em caso de acesso autorizado, a porta é destravada através do servo e o led se acende. Passados 5 segundos o servo retorna à posição original e o led se apaga.
