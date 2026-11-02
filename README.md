# Bookstore Management — College Project

> College coursework project, preserved as a record of learning and academic development.

A Windows desktop application for managing a bookstore's books, customers, and sales. Built with C#, Windows Forms, and MySQL for the **Hands On Work III** academic project (2021). The application interface is in Portuguese.

## Features

- Create, search, update, and deactivate books and customers.
- Maintain book information, including author, price, release date, page count, and stock.
- Register sales with customer selection, multiple books, quantities, and payment method.
- Deduct sold quantities from book stock.
- Browse sales and generate a sales report by month.
- Sign in through a database-backed login form.

## Technology

| Component | Technology |
| --- | --- |
| Language and interface | C# / Windows Forms |
| Runtime | .NET Framework 4.7.2 |
| Database | MySQL-compatible server |
| Database connector | MySql.Data 8.0.26 |
| IDE | Visual Studio |

## Getting started

**Database setup is incomplete in this repository:** there is no SQL schema or seed script. Running the application requires obtaining or recreating the original `bookstore_db` database, including the `login`, `livros`, `clientes`, `vendas`, and `vendas_info` tables used by the source code. Login also requires an existing account in that database.

1. Clone the repository:

   ```bash
   git clone https://github.com/EmanuelCChagas/college-bookstore-management-winforms.git
   ```

2. On Windows, install Visual Studio with .NET desktop development support and the .NET Framework 4.7.2 targeting pack.
3. Open [BookStore1.sln](BookStore1.sln).
4. Resolve the project's `MySql.Data` reference using version 8.0.26. The project declares an assembly reference rather than a NuGet package restore configuration.
5. Prepare the database described above. Connection settings are embedded in the C# forms under `Library/`; search for `datasource=` and adjust all occurrences for your local database.
6. Build the solution and run it from Visual Studio.

The original project used XAMPP for its local database environment. Database connections are made directly from the desktop application.

## Source guide

- [Library/Livros](Library/Livros): book catalog and stock forms.
- [Library/Clientes](Library/Clientes): customer management forms.
- [Library/Vendas](Library/Vendas): checkout, sales history, and monthly reporting.
- [Library/Login_Form.cs](Library/Login_Form.cs): login flow.
- [Library/Program.cs](Library/Program.cs): application entry point.

## Project status

This repository preserves an academic implementation. Payment forms perform local input checks; they do not integrate with a payment processor. The missing database setup prevents a complete first-run experience from a fresh clone.
