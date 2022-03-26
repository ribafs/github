## Criando e usando branches

### Usando o terminal:

## Listar as branches existentes

git branch

A branch atual aparece em verde e com um asterisco à esquerda. A outra aparece em branco

## Criar nova branch

git branch nome

## Trocando da branch atual para a nova

git checkout nome

Agora realizamos o que desejamos: adicionar, alterar, etc

Então:
```
git add .
git commit -m "Alerações na branch ..."
git push -u origin nome
```
Feito isso, ao acessar o repositório no Github encontramos a mensagem acima:
 - nova2 had recent pushes less than a minute ago 

nova2 é o nome da branch que criei

E um novo botão verde "Compare & pull request"

Clique nele

- Digite um comentário sobre a nova branch e clique em Create pull request
- Role a tela e veha
- This branch has no conflicts with the base branch

Então clique no botão Merge pull request e em Confirm merge

Clique no link do repositório e veja que agora tem 2 branches. Clique no link branches

Clique no link da nova branch e verá os arquivos dela.


## Referências

https://pt.stackoverflow.com/questions/411048/como-criar-uma-nova-branch-no-github
