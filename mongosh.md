### question 1 : Find all the information about each products
```js
>db.products.find().pretty()
```
### question 2: Find the product price which are between 400 to 800
```js
>db.products.find({ product_price: { $gte: 400, $lte: 800 } }, { _id: 0, product_price: 1 }).pretty()
```
### question 3: Find the product price which are not between 400 to 600
>db.products.find({ "price": { $lt: 400, $gt: 600 } }).pretty()
### question 4: List the four product which are grater than 500 in price
```js
>db.products.find({product_price:{"$gt":500}}).pretty()
```
### question 5: Find the product name and product material of each products
```js
>db.products.find({}, { _id: 0, product_name: 1, product_material: 1 }).pretty()
```
### question 6:  Find the product with a row id of 10
```js
>db.products.findOne({ id: "10" })
```
### question 7: Find only the product name and product material
```js
>db.products.findOne({}, { _id: 0, product_name: 1, product_material: 1 }).pretty()
```
### question 8: Find all products which contain the value of soft in product material
```js
>db.products.find({ product_material: /soft/i }).pretty()
```
### question 9: Find products which contain product color indigo and product price 492.00
```js
>db.products.find({ product_color: "indigo", product_price: 492.00 })
```
### question 10: Delete the products which product price value are same
```js
>db.products.remove({ product_price: { $eq: 492.00 } }, { justOne: false })
```