* 0. Documentação Nest Prisma ORM
``` 
https://docs.nestjs.com/recipes/prisma
```

* 1. Instalando o nestJS como global no computador
```
npm install -g @nestjs/cli
```

* 2. Criando o projeto NestJS
```
npx nest new project
```

* 3. Entrando na pasta do projeto
```
cd project
```

* 4. Instalando o prisma ORM
```
npm install prisma --save-dev
```

* 5. Iniciando o prisma com ou sem provider de banco
```
npx prisma init
```
||
```
npx prisma init --datasource-provider mysql
```

* 6. Criando model Users
```
model User {
    id Int @id @default(autoincrement())
    email String @unique
    name String?

    @@map("user")
}
```

* 7. Realizando nosso primeiro migrate gerando primeira tabela
```
npx prisma migrate dev
```