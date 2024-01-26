<head>
  <link rel="stylesheet" type="text/css" href="style.css">
</head>


#  Estudos do meio do caminho

### Túneis de desenvolvimento

Como estava desenvolvendo no VScode, então utilizei os [túneis de desenvolvimento da própria Microsoft](https://learn.microsoft.com/pt-br/azure/developer/dev-tunnels/overview) para gluns testes!


### Deploy no Vercel 

O deploy fiz pelo vercel [URL](https://clone-tabnews-3pf2.vercel.app/).
A versel é a criadora do Next.js, por isso essa escolha. A Versel está super integrada ao framework desse projeto. 

"Os túneis de desenvolvimento permitem que os desenvolvedores compartilhem com segurança serviços Web locais na Internet".

### Next

Renderizar a página do lado do cliente pode levar uma série de consequências ruim para experiência do usuário (lentidão no carregamento do conteúdo) e danos ao SEO. 

Solução? renderizar do lado do servidor aplicando uma pré-renderização estática. 

O Next.js é um framework para o React para executar a pré-renderização de forma simples. 

Para instalar o Next.js, você precisa ter o Node.js instalado para usar do comando npm

https://www.freecodecamp.org/portuguese/news/o-manual-do-next-js-para-iniciantes/

1- package.json é um manifesto que guarda metadados do projeto, como autor e descrição. Alguns scripts, como npm run! mas principalmente guarda as dependências instaladas com 'npm install', como o react ou next!

2 - package-lock.json toma conta exclusivamente com as dependências e suas versões, e as dependências das suas dependências. 

### git-introducao

**VSCode**

O VSCode tem uma timeline que valida cada alteração do seu código e você pode visitar como um versionamento.

<div class="imagem-container">
  <img src="./imgs/image.png">
</div>

**Lista de comandos abordados**

* git log - listar os commits do repositório.
* git add - sobe alterações para a staging area.
* git commit - realiza novos commits.
* git commit --amend - subsitui o commit anterior por um novo, mas aproveita as alterações dele.
* git diff - calcula a diferença entre as versões/alterações dos arquivos.

**Git log e fotos**

Commit significa compromisso, você se responsabiliza com essas alterações. O commit tem um hash que é um identificador único.


**3 estágios**

1º Modified - todos arquivos modificados.

2º Staged - Qual desses arquivos vai ser commitado.

3º Commit - É registrado a modificação.

**git commit --amend**

Como remendar um erro localmente?

Se o commit estiver errado, você pode usar o --amend.

```git commit --amend```

ammend se aplica exatamente e unicamente ao último commit, o que está mais na ponta final do histórico de commits.

Com git commit --amend --no-edit, essa flag --no-edit vai fazer com que você faça o "amend", mas sem precisar mudar mensagem de commit nem nada.

```
# Edit hello.py and main.py
git add hello.py
git commit 
# Realize you forgot to add the changes from main.py 
git add main.py 
git commit --amend --no-edit
```

Os comando push e push com force serão utilizado para jogar nossos commits em origin.

```
git push --force
# Empurrar de forma forçada alterações locais para o origin.
git push -f
# Forma comprimida do comando anterior.
```

Mas por quê preciso fazer um commit forçado? Porque você pertubou a linha do tempo.

<div class="imagem-container">
  <img src="./imgs/lokitimeline.png" class="lokitimeline">
</div>


Ao utilizar o ammend, é criado outro commit que subtituirá o ammendado! Não há sobrescrição de commits, pois eles são imutáveis, portanto, possuem hashs únicos.
Então commit (A) que existe tanto local quanto no remoto, que foi ammendado, foi, na verdade, descartado, e substituiu pelo ammend, commit (B). 
Apesar de você ter descartado o último commit (A) do seu repositório local e existe outro (B), o commit (A) ainda existe no reposositório remoto.

Essa foi a pertubação da linha do tempo entre o que está o local e que está no origin. Quebrando a ordem e a dependência sequencial. 


<div class="imagem-container">
  <img src="./imgs/commitpertubado.png" class="commitpertubado">
</div>

