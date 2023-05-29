# Boa tarde professor.

# Perguntei no grupo relacionado a atividade de docker que você passou, e vi que era possível fazer por linha de comando,
# portanto loguei no docker playground que você passou anteriormente e fiz as atividades por lá, listarei abaixo os comandos
# utilizados e a breve explicação (dessa forma fixo melhor o conteúdo, já que não tenho tanta experiência com o docker)

# 1 - baixar as imagens necessárias para a criação dos containers, sendo elas o mysql e o nginx

docker pull nginx
docker pull mysql

# agora vamos executar o primeiro container do mysql

docker run -d --name mysql-docker-container -e MYSQL_ROOT_PASSWORD=docker1234 mysql

# para testar o container acima, podemos usar o comando abaixo, caso tudo esteja correto,
# uma mensagem relacionada ao mysql será exibida

docker exec -it mysql-docker-container mysql -p 

# agora, executar o container do nginx, para isso utilizaremos o comando abaixo

docker run -d --name nginx-container -p 80:80 nginx

# para testar o container no docker playground, cliquei na opção 'open port' e coloquei a porta 80, e 
# a mensagem padrão do nginx foi exibida.

