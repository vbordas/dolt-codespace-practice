# Dolt Codespace

A GitHub Codespace where an AI agent sets up [Dolt](https://www.dolthub.com),
a SQL database with Git-style versioning, and helps you clone, change, commit
and push a database you own on DoltHub.

## Before you start

Do this setup once in each codespace. If you delete the codespace and make a
new one, do it again.

1. **Make a DoltHub account.** Go to <https://www.dolthub.com>, click
   **Sign Up**, and follow the steps (you'll get an email to confirm your
   account). Write down your DoltHub **username** and the **email** you used.
   Stay signed in to DoltHub in a browser tab.
2. **Start a codespace.** Click **Code → Codespaces → Create codespace on
   main** on this repo, and start your agent in the terminal.
3. **Install Dolt and tell it who you are.** Copy this into the agent,
   with your own name and DoltHub email, and press **Enter**:

   ```default
   Install Dolt in this codespace and set it up with my name YOUR NAME and my DoltHub email YOUR EMAIL.
   ```

   Dolt puts your name and email on every change you save (every
   **commit**), so people can see who made it.
4. **Log in to DoltHub yourself, in a second terminal.** Dolt needs
   permission to use your DoltHub account. It gets it with a **key**: a long
   code that Dolt makes and you add to your account.
   - Open a new terminal: in the menu at the top, click **Terminal**, then
     **New Terminal** (or click the **+** in the terminal panel).
   - Type `dolt login` and press **Enter**.
   - Dolt shows a link that starts with
     `https://www.dolthub.com/settings/credentials`. Click it (or copy it
     into your browser).
   - DoltHub opens the **Credentials** page with the key already filled in.
     In **Description**, type `codespace`. Click **Create**.
   - Go back to that terminal. After a few seconds Dolt says you are logged
     in and shows your DoltHub username.
5. **Check it.** Go back to the agent and type:

   ```default
   Check that I'm logged in to DoltHub, and tell me which username Dolt is using.
   ```

   It should say **your** DoltHub username. If not, run `dolt login` again
   and click the new link.

## Exercises

Each folder is one exercise, with its own directions in a `README-` file:

| Folder | What you do |
|---|---|
| [make-your-own-database](make-your-own-database/README-make-your-own-database.md) | Pick a topic and the agent dreams up a small database about it: two tables joined by one foreign key. You build it, query it, and push it to DoltHub. |
| [retail-orders](retail-orders/README-retail-orders.md) | The agent installs Dolt, logs you in to DoltHub, builds a retail orders database from `retail-orders.sql`, and pushes it to a new database on your DoltHub account. |
| [sales-csv-data](sales-csv-data/README-sales-csv-data.md) | Starting from one big `sales.csv` file, you and the agent design a database with three tables (stores, products and sales), build it in Dolt, and push it to DoltHub. |
| [excel-to-database](excel-to-database/README-excel-to-database.md) | Open an Excel workbook with two worksheets, find its problems, and with the agent turn it into a database whose keys keep those problems out. |
| [dolt-branches](dolt-branches/README-dolt-branches.md) | Build a small boutique database with three views, raise prices on a branch, compare what the views show on each branch, push the branch to DoltHub, and open a pull request for your manager to approve. |
| [company-analysis](company-analysis/README-company-analysis.md) | The agent analyzes an existing database, [calvinw/BusMgmtBenchmarks](https://www.dolthub.com/repositories/calvinw/BusMgmtBenchmarks), compares two retail companies in one year with charts, and builds a PowerPoint deck. |

Each exercise builds its database inside its own folder (for example
`retail-orders/retail-orders`). The `.gitignore` file keeps these databases
out of GitHub: you share them on DoltHub instead.

After the setup above, **start with
[make-your-own-database](make-your-own-database/README-make-your-own-database.md).**
You can do the others in any order.
