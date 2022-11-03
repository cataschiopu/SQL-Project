# SQL-Project
A simple exercise to showcase basic knowledge of SQL commands (CRUD)

You get the next tables:

Locations

LocationID

LocationName

Address

City

Country

ContactPerson

Capacity

Cost



Events

EventID

LocationID

EventName

EventDate

EventCost



Create Table Locations( 

LocationID number not null, 

LocationName varchar2(100) not null, 

Address varchar2(100) not null, 

City varchar2(100) not null, 

Country varchar2(100), 

ContactPerson varchar2(100) not null,

Capacity number not null, 

Cost number not null, 

PRIMARY KEY(LocationID)

);



Create Table Events( 

EventID number not null, 

LocationID number not null, 

EventName varchar2(100) not null, 

EventDate date, 

EventCost number not null, 

PRIMARY KEY(EventID) 

);



Insert Into Locations Values (1, 'Parcul central', 'str. baritiu nr 84', 'Cluj-Napoca', 'Romania','Ana Popescu',10000,0);

Insert Into Locations Values (2, 'Casa de Cultura', 'piata unirii', 'Cluj-Napoca', 'Romania','Dan Cristian',300,1000);

Insert Into Locations Values (3, 'Piata Revolutiei', 'str. baritiu nr 84', 'Bucuresti', 'Romania','Cristina Manole',10000,1000);

Insert Into Locations Values (4, 'Hugo Restaurant', 'str. 21 decembrie 1989', 'Cluj-Napoca', 'Romania','Crina Suciu',200,500);

Insert Into Locations Values (5, 'Piata Sfatului', 'str. statului nr 100', 'Brasov', 'Romania','Liana Marinescu',600,600);



Insert Into Events Values (1, 1, 'Zilele Orasului Cluj', DATE '2017-05-05', 10000);

Insert Into Events Values (2, 1, 'Zilele Tineretului', DATE '2017-06-06', 1000);

Insert Into Events Values (3, 1, 'Marea Hamaceala', DATE '2017-07-07', 400);

Insert Into Events Values (4, 1, 'Zilele Folk', DATE '2017-05-09', 2000);

Insert Into Events Values (5, 2, 'Concert Andra', DATE '2017-07-05', 5000);

Insert Into Events Values (6, 2, 'Concert colinde', DATE '2017-12-06', 1500);

Insert Into Events Values (7, 3, 'Concert Revelion', DATE '2017-12-31', 20000);

Insert Into Events Values (8, 4, 'Eveniment testare', DATE '2017-05-07', 2000);

Insert Into Events Values (9, 4, 'Eveniment lansare revista', DATE '2017-09-07', 1000);

Insert Into Events Values (10, 5, 'Cerbul de aur', DATE '2017-09-07', 5000);



Compute the following:

1. Perform the following queries on "Locations" table: 

a. select all locations that have the capacity between 200 and 1000 persons

b. select all locations that have "a" in their name

c. Select all locations that are not in Cluj-Napoca

d. Select all locations that have the cost 0,500,600, are in Brasov and Cluj-Napoca, and han sustain a capacity greater that 1000 persons



2. Perform the following queries on "Events" table: 

a. return the results for min, max, average based on "EventCost" column

b. count how many events are associated to location 1 and 2

c. compute the average cost obtained from location 1

d. order the events based on their defined date

e. compute the total cost associated with each location (hint grouped by)



3. Perform the following queries using both tables

a. Order location name, descending, after their associated event cost

b. Select location name, location cost and event cost for a specific event

c. Return the first 3 events (with eventName, locationname), that have the greatest event cost, in alphabetical order (after their names)
