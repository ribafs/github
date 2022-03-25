# Criação e uso de token para o Github

## Observação
Como tive alguma dificuldade para acessar com senha, cheguei a pensar em abandonar o Github por conta de não mais conseguir atualizar repositórios via git. Refleti e lembrei que não conheço nada similar ao Github. Então fui estudar e trago aqui o resultado de como resolvi. 

## Criação

Quando acontecer do Github não mais aceitar senha para sincronizar seus repositórios e indicar que em seu lugar deve usar um token, então siga estes passos.

- Acessar p Github
- Clique no avatar acima e à direita
- Settings
- Role a tela e clique em Developer Settings
- Personal access tokens
- Generate new token
- Selecione tudo que deseja controlar
- E salve

Receberá algo assim:

ghp_YQYFFqcoDiNcexVpTZbBeCJJsz2tuN2mllfr

## Como usar o token criado

Ao invés de usar a senha usaremos o token, então guarde-o bem. Se esquecer remova e gere outro

-    Se estiver atualizando para usar HTTPS, a URL poderá ser parecida com esta:
-    https://github.com/USERNAME/REPOSITORY.git

-    Se estiver atualizando para usar SSH, a URL poderá ser parecida com esta:
-    git@github.com:USERNAME/REPOSITORY.git

Acesse pelo terminal a pasta do repositório
```
git remote -v
> origin  git@github.com:USERNAME/REPOSITORY.git (fetch)
> origin  git@github.com:USERNAME/REPOSITORY.git (push)
```
Altere a URL do remote de SSH para HTTPS com o comando git remote set-url.
```
git remote set-url origin https://github.com/USERNAME/REPOSITORY.git
```

Verifique se o URL remote foi alterado.
```
$ git remote -v
# Verify new remote URL
> origin  https://github.com/USERNAME/REPOSITORY.git (fetch)
> origin  https://github.com/USERNAME/REPOSITORY.git (push)
```
Verifique se o URL remote foi alterado.
```
    $ git remote -v
    # Verify new remote URL
    > origin  https://github.com/USERNAME/REPOSITORY.git (fetch)
    > origin  https://github.com/USERNAME/REPOSITORY.git (push)
```
Na próxima vez que você aplicar git fetch, git pull ou git push no repositório remote, precisará fornecer seu nome de usuário no lugar da senha, insira seu token de acesso pessoal (PAT).

Exemplo:

Acessar o diretório
```
git add .
git commit -m 'Atualização X'
git pull
git push
```
```
No ramo main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
Already up to date.
Username for 'https://github.com': ribafs
Password for 'https://ribafs@github.com': AquiOTokendoGithub
Everything up-to-date
```
Crédito:

https://docs.github.com/pt/get-started/getting-started-with-git/managing-remote-repositories#switching-remote-urls-from-ssh-to-https

## Sugestões

Sugestões e informações extras serão muito bem vindas.

