# MedSupplyNet-A Web Solution for Medical Wholesalers
The project's objective is to make the distribution of medicines to different medical stores more efficient. With this project, we aimed to provide a simpler, more effective option for both store owners and clients in need of life-saving pharmaceuticals. 
This project is a web application that allows a Medical Wholesaler to manage the pharmaceutical-related data. The application uses a local database to store information about medicines, pharmaceutical products, and user details.
### Functionalities of the project:
1.	After successful login, supplier can view, edit and delete the details of the available clients (medical stores) from the database.
2.	Details of a new client medical store can be added with a unique MID. 
3.	It allows several medical store owners to place orders for the medicines and other healthcare products. Supplier has the option to review those orders and, once those orders have been fulfilled, he can delete the respective entries.
4.	Medical Store Owners (Clients) can view a list of available pharmaceutical items, including their names, quantities, and related information.
5.	Supplier can add the medicines and products as per availability to the database, providing details such as name, quantity.
6.	We can also view the date and time, when a new entry was made and deleted.
The project uses a Flask web server to handle user requests and render HTML templates. It also utilizes SQLAlchemy to interact with the database, making it easy to manage and retrieve pharmaceutical data. Additionally, the application incorporates sessions to handle user logins and logouts securely.
### SQL Table Info:
1.	Table: ‘posts’ stores the details of the client medical stores with MID as the primary key. Auto increment is applied over the MID and all entries must be NOT NULL.
2.	Table: ‘medicines’ stores the order details received by the medical stores. The MID column of this table is a foreign key which refers to the same column of ‘posts’ table. Also [MEDICINES] & [PRODUCTS] column of this table refers to the [medicine] column of ‘addmd’ table and [products] column of ‘addpd’ table.
3.	‘logs’ table stores the history of the order received and order fulfilled. [MID] column of this table refers to the same column of ‘medicines’ table.
4.	‘addmd’ and ‘addpd’ tables stores the list of available medicines and products respectively.
