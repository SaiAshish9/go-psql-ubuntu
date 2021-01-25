```
configuration step's:

sudo -u postgres psql
\l
\du 
<!-- all users -->
\c golang
SELECT current_user;
SELECT current_database();
<!-- switch to database -->
\d
<!-- select all relations -->
\q

sudo -u postgres createuser <username>
sudo -u postgres createdb golang

alter user <username> with encrypted password '<password>'

grant all privileges on database golang to saiashish



CREATE TABLE employees (
   ID INT PRIMARY KEY     NOT NULL,
   NAME           TEXT    NOT NULL,
   RANK           INT     NOT NULL,
   ADDRESS        CHAR(50),
   SALARY         REAL DEFAULT 25500.00,
   BDAY			  DATE DEFAULT '1900-01-01'
);

<!-- ID  SERIAL PRIMARY KEY NOT NULL, -->

\d employees

alter user saiashish with superuser;

CREATE TABLE books (
  isbn    char(14)     PRIMARY KEY NOT NULL,
  title   varchar(255) NOT NULL,
  author  varchar(255) NOT NULL,
  price   decimal(5,2) NOT NULL
);

\d books

INSERT INTO books (isbn, title, author, price) VALUES
('978-1503261969', 'Emma', 'Jayne Austen', 9.44),
('978-1505255607', 'The Time Machine', 'H. G. Wells', 5.99),
('978-1503379640', 'The Prince', 'Niccolò Machiavelli', 6.99);

SELECT * FROM books;


```