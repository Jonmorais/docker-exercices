FROM python:alpine3.15

COPY hello.py hello.py

# CMD É UMA SUGESTÃO, TEM COMO MUDAR NA HORA DE FAZER O DOCKER RUN!, JÁ O ENTRYPOINT É FIXO!!!, NÃO TEM COMO MUDAR NA HORA DE FAZER O DOCKER RUN!
# ou seja, o CMD é uma dica do que o programa deve executar, CASO nenhum comando seja provido, como é o caso de quando executamos: docker run ex03
CMD ["python", "hello.py"] 

# USANDO OS DOIS AO MESMO TEMPO:
# ENTRYPOINT ["python"] --> Quero garantir que o primeiro comando sempre será esse
# CMD ["hello.py"] --> Se não for passado nada, esse será executado, porém eu posso pedir pro programa executar outro, como por exemplo um hello2.py!!