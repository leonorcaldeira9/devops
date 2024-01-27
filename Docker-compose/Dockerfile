# Usa a imagem base do Ubuntu 20.04
FROM ubuntu:20.04 

# Define a variável de ambiente para a versão do Ansible
ENV ANSIBLE_VERSION 2.9.17

# Atualiza a lista de pacotes e instala o gcc e o Python 3.
# O gcc é necessário para a compilação de algumas dependências do Python.
# O Python 3 é necessário para executar o Ansible.
RUN apt-get update; \
    apt-get install -y gcc python3; \
    apt-get install -y python3-pip; \
    apt-get clean all

# Atualiza o pip para a versão mais recente e instala o Ansible.
# O Ansible é uma ferramenta para automação de IT, como o provisionamento de infraestruturas e configurações.
RUN pip3 install --upgrade pip; \
    pip3 install "ansible==${ANSIBLE_VERSION}"; \
    pip3 install ansible