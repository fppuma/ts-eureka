# ts-eureka
Playground with TypeScript

Example based on these tuturials:
- [Youtube](https://www.youtube.com/watch?v=SigVVJmUGv8)
- [Medium](https://medium.com/dottech/mejorando-los-mensajes-de-git-commit-con-husky-y-commitlint-7bddf6ab22c2)

## CommitLint Install & Config
```
npm install --save-dev @commitlint/cli @commitlint/config-conventional
```
```
echo "module.exports = {extends: ['@commitlint/config-conventional']}" > commitlint.config.js
```

## Husky Install & Config
```
npm i -D husky
```

```
npm pkg set scripts.prepare="husky install"
```

This command will create a .husky folder
```
npm run prepare
```

### Commit Message
```
npx husky add .husky/commit-msg 'npx commitlint --edit ${1}'
```