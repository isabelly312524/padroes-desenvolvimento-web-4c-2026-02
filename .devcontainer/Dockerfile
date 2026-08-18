#definição da imagem
FROM maven:3.9-eclipse-temurin-21-noble
#desabilita a instalação interativa
ENV DEBIAN_FRONTEND=noninteractive

#instala as ferramentas que não existem na imagem base
#remove os arquivos temporarios provenientes do processor de instalação
# apt-get  update - atualiza o repositorio do software
# apt-get install - instala as ferramentas
# git-lfs - ferramenta para armazenar de arquivos binários
# curl - ferramentas para testar APIs
# apt-get clean e rm - limpam arquivos temporarios 
RUN apt-get update && apt-get install -y \
    mysql-server-8.0 \
    git \
    git-lfs \
    curl \
    unzip \
    zip \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*
