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
- 