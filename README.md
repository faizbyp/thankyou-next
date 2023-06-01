# Thank You, Next

A repo for learning Next JS. [Tutorial from Web Dev Simplified](https://youtu.be/NgayZAuTgwM)

## Setup

Creating Next app
```bash
npx create-next-app@latest
```

Installing Prisma
```bash
npm i prisma -D
```

Init Prisma with SQLite
```bash
npx prisma init --datasource-provider sqlite
```

Create schema (model)

Migrating schema to DB
```bash
npx prisma migrate dev --name init
```

## Few notes

Next JS can communicate to DB:(SQLite) via an ORM:(Prisma).

Next JS consist of 2 component, **client** and **server**.

- By default it is using server component. But if a function runs on the server, it must be declared explicitly by using `"use server"`.
- If you're writing a component with event listener or any other property which runs on the client, it must be declared with `"use client"` on the top level of the file.