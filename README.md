### Criando projeto Nest Backend Prisma ORM e Mysql
* <b>0.</b> Documentação Nest Prisma ORM
``` 
https://docs.nestjs.com/recipes/prisma
```

* <b>1.</b> Instalando o nestJS como global no computador
```
npm install -g @nestjs/cli
```

* <b>2.</b> Criando o projeto NestJS
```
npx nest new project
```

* <b>3.</b> Entrando na pasta do projeto
```
cd project
```

* <b>4.</b> Instalando o prisma ORM
```
npm install prisma --save-dev
```

* <b>5.</b> Iniciando o prisma com ou sem provider de banco
```
npx prisma init
```
||
```
npx prisma init --datasource-provider mysql
```

* <b>6.</b> Criando model Users
```
model User {
    id Int @id @default(autoincrement())
    email String @unique
    name String?

    @@map("user")
}
```

* <b>7.</b> Realizando nosso primeiro migrate gerando primeira tabela
```
npx prisma migrate dev
```