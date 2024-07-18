# Passo a passo para instalação de:
## -node
## -express
## -nodemon
## -sucrase e...
## -criar arquivo .gitignore

```
node -v 
```
mostra versão

- cria arquivo index.js na pasta do projeto
- cria pasta src e coloca o arquivo index.js dentro dela

```
node src/index.js
```
vai rodar o backend no terminal

```
npm init -y 
```
responde yes para tudo automaticamente e cria o package.json

dentro do pckage.json adiciona nos scripts:
```
"dev": "node src/index.js 
```
para rodar com o comando npm run dev

```
npm install -g nodemon 
```
instala o nodemon

```
npm install nodemon -D 
```
instala o nodemon no projeto para atualização da pagina

dentro do pckage.json ALTERA nos scripts em 
```
"dev": "nodemon src/index.js 
```

```
npm install sucrase -D 
```
instala sucrase para transpilar javascript

na mesma raiz onde esta o package.json cria arquivo nodemon.json e cola a configuração no arquivo criado:
```
{
	"execMap": {
	    "js": "node -r sucrase/register"
	}
}
```

na mesma raiz do package.json cria um arquivo chamado:
```
.gitignore
```
e dentro dele coloca escreve o nome da pasta:
```
node modules
```
não permite que a pasta node modules suba para o GitHub
