# MilkCo-Database
It is an example database for MYSQL, similar to Sakila

![](banner.jpg)

> Photo from unsplash.com/@jaypix_01

It is a database model of a Milk Company that we could use to test and evaluate Business Intelligence and Data Science.



![](milkco.jpg)

## Features

* Products (Skus) divided in types, subtypes, container (cup, bottle, etc.) and brands.
* 3 Brands: Value Pack, Auntie Annie and Red Label (cheap, normal and expensive)
* More than 10 years of sales.
* A worldwide company with offices, employees and customers across the globe.
* The products has a trends (some products are more sold than others)
* The sales has seasonal trends in the number of invoice and in the size of the invoices.
* 50 Branches (offices) across the globe.
* 1000 Employees
* 17000 Invoices starting the 2005. The invoices have stationary trends.
* 64000 Invoice details. The invoices have stationary trends.
* 3563 Customers. Some of them are companies
* The database model is vanilla and clean. It does not have views, store procedure, functions or even index (with the exception of primary key and foreign keys)
* The columns are normalized to use the minimum type of definitions.

| types              | Mysql Definition |
| ------------------ | ---------------- |
| Integer numbers    | int              |
| Strings and texts  | varchar          |
| Money and decimals | decimal(10,2)    |
| Booleans           | tinyint          |
| Date               | DateTime         |
| Timestamps         | Timestamp        |

## Specifications

* Every Indexes have a prefix called "id" with the exception of "Sku", where "sku" is the index without a prefix.
* Foreign keys don't have a special name. Usually they have the same name than the primary key.
* All tables are in plural. Composed names are written in camel case.
* Columns are written in lowercase and it starts in lowercase.

## Considerations

* It misses some features. For example, a table of purchases, the salaries and the costs of each branches are fixed
* Values are not inflationary. 
* It lacks shipping
* It does not consider taxes. If the taxes are flat, then it is not a problem.