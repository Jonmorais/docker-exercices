FROM alpine:3.14

# Instalando o programa thttpd
RUN apk add thttpd

# Criando um usuário simples, sem poder de administrador
RUN adduser -D static
USER static

# Criando os diretórios
WORKDIR /home/static

# Copia o arquivo html para dentro da imagem
COPY index.html index.html

# Executa o programa thttpd para entregar arquivos HTML na pasta "/home/static"
# thttpd é para executar o programa thttpd, o -D é para manter o programa executando se não, por padrão ele vai exercutar em segundo plano
# Os comandos "-h", "0.0.0.0" são para permitir qualquer IP
# Os comandos "-p", "3000" são para escutar a porta 3000, Os comandos "-d", "/home/static" significam que os diretórios utilizados serão /home/static
# "-u", "static" significa que o usuário para o qual irei servir esses arquivos é o usuário static, 
# "-l", "-" é para que os logs vão para o console.
CMD ["thttpd", "-D", "-h", "0.0.0.0", "-p", "3000", "-d", "/home/static", "-u", "static", "-l", "-"]
