# Thank You, Next

A repo for learning Next JS using Tailwind, SQLite 3, and Prisma ORM. [Tutorial from Web Dev Simplified](https://youtu.be/NgayZAuTgwM)

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

## Notes

Next JS can communicate to `DB:(SQLite)` via an `ORM:(Prisma)`.

Next JS consists of 2 components, **client** and **server**.

- By default it is always using server component. But if a function runs on the server, it must be declared explicitly by using `"use server"`.
- If you're writing a component with event listener or any other property which runs on the client, it must be declared with `"use client"` on the top level of the file.

## SQLite

[SQLite Cheat Sheet](https://www.sqlitetutorial.net/sqlite-cheat-sheet/)

Opening SQLite CLI:
```bash
sqlite3 prisma/dev.db
```

Show all tables:
```sql
.tables
```

Change show settings:
```sql
-- Showing attributes
.show 

-- Turning on header and change mode to column
.header on
.mode column
```

Selecting table:
```sql
select * from Todo;
```
