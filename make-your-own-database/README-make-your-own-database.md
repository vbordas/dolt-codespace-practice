# Make Your Own Database with the Agent

**Your job:** create a database with **2 tables and 1 foreign key** that
connects them, on a topic you choose. The agent dreams up the tables and
made-up data with you, helps you build the database, and helps you share it
on DoltHub.

A **foreign key** is a column in one table that must match the key of a row
in the other table. It's what connects the two tables: for example, if one
table lists a coffee shop's drinks and the other its orders, each order's
`drink_id` must be a drink that's really on the menu.

## Before you start

Do the setup in the [main README](../README.md#before-you-start) first:
Dolt must be installed in your codespace, and you must be logged in to
DoltHub. Stay signed in to DoltHub in a browser tab.

Copy each prompt into the agent and press **Enter**. Read what the agent says
before you go on. Replace the parts in capitals with your own details. If the
agent asks to install something or run a command, allow it.

## Step 1: Dream Up the Database

Pick your topic. Then:

```default
Dream up a small practice database about YOUR TOPIC. Give it two tables connected by one foreign key, with 5 to 10 rows of made-up data in each. Don't create anything yet: explain in plain words what each table holds, its columns, its primary key, and how the foreign key connects the tables. Show me a few example rows.
```

Check the design before you go on. It must have **exactly 2 tables and 1
foreign key**. If it has more tables or keys, or no foreign key, ask the agent
to fix it. If you want other changes (another column, different data, more
rows), tell the agent. Make sure you can answer:

- What is the primary key of each table?
- Which column is the foreign key, and which table does it point to?

## Step 2: Build It

Choose a short name for your database, with dashes instead of spaces, such
as `coffee-shop` or `sneaker-collection`.

```default
Save the design as a SQL file called make-your-own-database/DATABASE-NAME.sql. Then create a new Dolt database in the folder make-your-own-database/DATABASE-NAME, load the SQL file into it, show me both tables, and commit it with a message that says what the database is.
```

## Step 3: Ask Questions

```default
Suggest three interesting questions about my data that need both tables. Answer each one with SQL that joins the tables, and show me the SQL.
```

## Step 4: Share It on DoltHub

On DoltHub, go to <https://www.dolthub.com/profile> and click
**Create Database**. Give it the same name as your database
(`DATABASE-NAME`), make it **Public**, and click **Create**. Leave it empty.

```default
Add my DoltHub database YOUR-DOLTHUB-USERNAME/DATABASE-NAME as the remote called origin and push main to it. Then give me the DoltHub links to my database and to each of its two tables.
```

Open the links. On DoltHub, open **Commit Log** to see your commit.

## What to Hand In

1. The link to your database on DoltHub. It must have 2 tables and 1
   foreign key.
2. Short answers, in your own words:
   - What are your two tables, and what is the primary key of each?
   - What is the foreign key, and which table does it point to?
   - Which of the three questions in Step 3 was most interesting, and what
     was the answer?
