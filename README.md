# Tutorial MongoDB

_Inspired from [mongodbtutorial](https://www.mongodbtutorial.org/getting-started/mongodb-shell/)._

## Tips

Docker container: [here](https://hub.docker.com/_/mongo)
Mongo shell: `mongosh`

## Commands

```js
db          # Show used database
show dbs    # Show all databases
use bookdb  # Use or create database named bookdb
```

### CRUD

```js
db.books.insertOne({
  title: 'MongoDB insertOne',
  isbn: '0-7617-6154-3',
});

db.books.insertMany([
  {
    _id: 1,
    title: 'Unlocking Android',
    isbn: '1933988673',
    categories: ['Open Source', 'Mobile'],
  },
  {
    _id: 2,
    title: 'Android in Action, Second Edition',
    isbn: '1935182722',
    categories: ['Java'],
  },
  {
    _id: 3,
    title: 'Specification by Example',
    isbn: '1617290084',
    categories: ['Software Engineering'],
  },
  {
    _id: 4,
    title: 'Flex 3 in Action',
    isbn: '1933988746',
    categories: ['Internet'],
  },
  {
    _id: 5,
    title: 'Flex 4 in Action',
    isbn: '1935182420',
    categories: ['Internet'],
  },
  {
    _id: 6,
    title: 'Collective Intelligence in Action',
    isbn: '1933988312',
    categories: ['Internet'],
  },
  {
    _id: 7,
    title: 'Zend Framework in Action',
    isbn: '1933988320',
    categories: ['Web Development'],
  },
  {
    _id: 8,
    title: 'Flex on Java',
    isbn: '1933988797',
    categories: ['Internet'],
  },
  {
    _id: 9,
    title: 'Griffon in Action',
    isbn: '1935182234',
    categories: ['Java'],
  },
  { _id: 10, title: 'OSGi in Depth', isbn: '193518217X', categories: ['Java'] },
  {
    _id: 11,
    title: 'Flexible Rails',
    isbn: '1933988509',
    categories: ['Web Development'],
  },
  {
    _id: 13,
    title: 'Hello! Flex 4',
    isbn: '1933988762',
    categories: ['Internet'],
  },
  {
    _id: 14,
    title: 'Coffeehouse',
    isbn: '1884777384',
    categories: ['Miscellaneous'],
  },
  {
    _id: 15,
    title: 'Team Foundation Server 2008 in Action',
    isbn: '1933988592',
    categories: ['Microsoft .NET'],
  },
  {
    _id: 16,
    title: 'Brownfield Application Development in .NET',
    isbn: '1933988711',
    categories: ['Microsoft'],
  },
  {
    _id: 17,
    title: 'MongoDB in Action',
    isbn: '1935182870',
    categories: ['Next Generation Databases'],
  },
  {
    _id: 18,
    title: 'Distributed Application Development with PowerBuilder 6.0',
    isbn: '1884777686',
    categories: ['PowerBuilder'],
  },
  {
    _id: 19,
    title: 'Jaguar Development with PowerBuilder 7',
    isbn: '1884777864',
    categories: ['PowerBuilder', 'Client-Server'],
  },
  {
    _id: 20,
    title: 'Taming Jaguar',
    isbn: '1884777686',
    categories: ['PowerBuilder'],
  },
  {
    _id: 21,
    title: '3D User Interfaces with Java 3D',
    isbn: '1884777902',
    categories: ['Java', 'Computer Graphics'],
  },
  {
    _id: 22,
    title: 'Hibernate in Action',
    isbn: '193239415X',
    categories: ['Java'],
  },
  {
    _id: 23,
    title: 'Hibernate in Action (Chinese Edition)',
    categories: ['Java'],
  },
  {
    _id: 24,
    title: 'Java Persistence with Hibernate',
    isbn: '1932394885',
    categories: ['Java'],
  },
  {
    _id: 25,
    title: 'JSTL in Action',
    isbn: '1930110529',
    categories: ['Internet'],
  },
  {
    _id: 26,
    title: 'iBATIS in Action',
    isbn: '1932394826',
    categories: ['Web Development'],
  },
  {
    _id: 27,
    title: 'Designing Hard Software',
    isbn: '133046192',
    categories: ['Object-Oriented Programming', 'S'],
  },
  {
    _id: 28,
    title: 'Hibernate Search in Action',
    isbn: '1933988649',
    categories: ['Java'],
  },
  {
    _id: 29,
    title: 'jQuery in Action',
    isbn: '1933988355',
    categories: ['Web Development'],
  },
  {
    _id: 30,
    title: 'jQuery in Action, Second Edition',
    isbn: '1935182323',
    categories: ['Java'],
  },
]);

db.products.insertMany([
  {
    _id: 1,
    name: 'xPhone',
    price: 799,
    releaseDate: ISODate('2011-05-14'),
    spec: { ram: 4, screen: 6.5, cpu: 2.66 },
    color: ['white', 'black'],
    storage: [64, 128, 256],
  },
  {
    _id: 2,
    name: 'xTablet',
    price: 899,
    releaseDate: ISODate('2011-09-01'),
    spec: { ram: 16, screen: 9.5, cpu: 3.66 },
    color: ['white', 'black', 'purple'],
    storage: [128, 256, 512],
  },
  {
    _id: 3,
    name: 'SmartTablet',
    price: 899,
    releaseDate: ISODate('2015-01-14'),
    spec: { ram: 12, screen: 9.7, cpu: 3.66 },
    color: ['blue'],
    storage: [16, 64, 128],
  },
  {
    _id: 4,
    name: 'SmartPad',
    price: 699,
    releaseDate: ISODate('2020-05-14'),
    spec: { ram: 8, screen: 9.7, cpu: 1.66 },
    color: ['white', 'orange', 'gold', 'gray'],
    storage: [128, 256, 1024],
  },
  {
    _id: 5,
    name: 'SmartPhone',
    price: 599,
    releaseDate: ISODate('2022-09-14'),
    spec: { ram: 4, screen: 9.7, cpu: 1.66 },
    color: ['white', 'orange', 'gold', 'gray'],
    storage: [128, 256],
  },
  {
    _id: 6,
    name: 'xWidget',
    spec: { ram: 64, screen: 9.7, cpu: 3.66 },
    color: ['black'],
    storage: [1024],
  },
]);
```

#### Operators

**Comparison**

$eq: Equal To Operator
$lt: Less Than Operator
$lte: Less Than or Equal To Operator
$gt: Greater Than Operator
$gte: Greater Than or Equal To Operator
$ne: Not Equal To Operator
$in: In Operator
$nin: Not In Operator

**Logical**

```js
db.products.find({price: 899});

# Projection (equals to SELECT fields)
db.products.find({}, {
    _id: 0,
    name: 1,
    price: 1,
    spec : { screen: 1 }
});

db.products.find({
    storage: {
        $gt: 128
    }
}, {
    name: 1,
    storage: 1
});
```

### Agregation

Example

```js
use coffeeshop

db.sales.insertMany([
	{ "_id" : 1, "item" : "Americanos", "price" : 5, "size": "Short", "quantity" : 22, "date" : ISODate("2022-01-15T08:00:00Z") },
	{ "_id" : 2, "item" : "Cappuccino", "price" : 6, "size": "Short","quantity" : 12, "date" : ISODate("2022-01-16T09:00:00Z") },
	{ "_id" : 3, "item" : "Lattes", "price" : 15, "size": "Grande","quantity" : 25, "date" : ISODate("2022-01-16T09:05:00Z") },
	{ "_id" : 4, "item" : "Mochas", "price" : 25,"size": "Tall", "quantity" : 11, "date" : ISODate("2022-02-17T08:00:00Z") },
	{ "_id" : 5, "item" : "Americanos", "price" : 10, "size": "Grande","quantity" : 12, "date" : ISODate("2022-02-18T21:06:00Z") },
	{ "_id" : 6, "item" : "Cappuccino", "price" : 7, "size": "Tall","quantity" : 20, "date" : ISODate("2022-02-20T10:07:00Z") },
	{ "_id" : 7, "item" : "Lattes", "price" : 25,"size": "Tall", "quantity" : 30, "date" : ISODate("2022-02-21T10:08:00Z") },
	{ "_id" : 8, "item" : "Americanos", "price" : 10, "size": "Grande","quantity" : 21, "date" : ISODate("2022-02-22T14:09:00Z") },
	{ "_id" : 9, "item" : "Cappuccino", "price" : 10, "size": "Grande","quantity" : 17, "date" : ISODate("2022-02-23T14:09:00Z") },
	{ "_id" : 10, "item" : "Americanos", "price" : 8, "size": "Tall","quantity" : 15, "date" : ISODate("2022-02-25T14:09:00Z")}
]);

db.sales.aggregate([
	{
		$match: { item: "Americanos" }
	},
	{
		$group: {
			_id: "$size",
			totalQty: {$sum: "$quantity"}
		}
	},
	{
		$sort: { totalQty : -1}
	}
]);

```
