# Sincronizando repositório do Github com repositório local

- Crio repositório no Github ou uso existente
- Então clono o repositório para meu desktop:
  - Abro o repositório (exemplo: https://github.com/ribafs/github)
  - Clico no botão verde Code
  - Clico em "git@github.com:ribafs/github.git"
  - Abro o terminal/prompt numa pasta desejada e executo:
    ```git clone git@github.com:ribafs/github.git github```
    
Com isso tenho um clone do repositório na minha pasta local github

## Agora como sincronizar o repositório local com o remoto:

Esta dica serve para repositórios simples, com apenas um branch master ou mais:

Somente na primeira vez precisa digitar os comandos das duas primeiras linhas
```
git config --global user.name "Ribamar FS"
git config --global user.email "ribafs@gmail.com"

git add .
git commit -m "Mensagem do commit"
git pull
git push
```
### Enviar a chave do teu SSH para o Github

Caso ainda não tenha enviado, antes de tentar sincronizar precisa:

- Comece instalando o SSH em seu desktop linux. No Windows quem instalou o git geralmente já vem com o SSH
- Execute o comando:
```cat ~/.ssh/id_rsa.pub```

Então ele mostra uma chave bem grande na tela, começando com ssh-rsa e terminando com seu e-mail (aqui foi isso). Selecione toda e copie para a memória.

- Abra o Github e faça login
- Clique em seu avatar acima e à direita
- Settings
- SSH and GPG Keys
- Clique no botão New SSH Key
- Digite um título e abaixo na textarea Key cole a chave que está na memória.
- Clique em Add SSH Key

Somente agora a sincronização irá funcionar corretamente.

## Dica extra:

Eu criei um pequeno script apenas com "g" e o copiei para o /usr/local/bin
Contendo os 4 comandos da sincronização. Na mensagem do commit deixo apenas "Update". Lembre: apenas para uso pessoal, não é bom para equipe.

