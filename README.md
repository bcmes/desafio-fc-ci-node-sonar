- configurei o docker-compose
- instalei o sonar-scanner localmente
- docker compose up -d
- docker exec -it node bash
- npm init
- npm install jest @types/jest sonar-scanner --only-dev
- configurei a propriedade script no package,json
```bash
"scripts": {
    "test": "jest --coverage"
  },
```
- escrevi o codido da pasta src
- npm run test
- no sonar http://localhost:9000 foi cadastrado o projeto 'js-project' e gerado o token para o projeto.
    - desafio-js: sqp_ae9427533ded0d746cb93ac0ac039f88bf016ed6
- Configurei o file 'sonar-project.properties' no projeto.
- exit (para sair do container)
- Executei o comando: sonar-scanner
- > commitei e subi essa versao inicial <
- adicionei os diretorios '.github/workflows' e o file 'ci.yaml' para um test inicial, e subi para analisar..
- criei a conta e vinculei o projeto manualmente no https://sonarcloud.io
    - na opcão "Choose your Analysis Method" escolhi "With GitHub Actions"
    - foi gerado um 'SONAR_TOKEN' que inseri no GitHub/<PROJETO>/Settings/Secrets and variables/Actions/Repository secrets.
- atualizei meu 'ci.yaml' com dados de conexao para o sonar-cloud
- se tiver usando, tem de atualizar o cadastro da action no github..
- Obs.: Quando passa no step do sonnar-cloud, isso só quer dizer que foi enviado com sucesso para a cloud o código para analise, se aprovado lá, ele responde para o github, habilitando assim o botao de merge.
- congigurei no github a branch master para aceitar o codigo, somente se os test e o sonar 'passar'.