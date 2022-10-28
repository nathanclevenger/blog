# Programming with URLs

What if you could code in your browser?  I don't mean in the browser window, but actually in the address bar.

What if you could type `eval.do/1+1` into your browser and you saw:

```json
{
  "eval": "1+1",
  "result": 2
}
```

And you wouldn't even have to type it yourself, because the web is built on links like: <https://eval.do/1+1>.  Anyone could simply click on that link, and see results.

But wouldn't this be limiting?  How could you compose complex programs?

Let's assuming you have a large JSON file, like the Northwind database: <https://json.fyi/northwind.json>

It consists of several root collections:
```json
{
  "Category": [],
  "Customer": [],
  "Employee": [],
  "EmployeeTerritory": [],
  "OrderDetail": [],
  "Product": [],
  "Region": [],
  "SalesOrder: []",
  "Shipper: []",
  "Supplier: []",
  "Territory: []"
}
```

Where each root collection holds an array of items like:
```json
{
  "Category": [
    {
      "picture": null,
      "entityId": 1,
      "description": "Soft drinks, coffees, teas, beers, and ales",
      "categoryName": "Beverages"
    },
    {
      "picture": null,
      "entityId": 2,
      "description": "Sweet and savory sauces, relishes, spreads, and seasonings",
      "categoryName": "Condiments"
    },
    {
      "picture": null,
      "entityId": 3,
      "description": "Desserts, candies, and sweet breads",
      "categoryName": "Confections"
    }
  ]
}
```

But what if you wanted to just get the category collection out of the large file, how would you do it?  You could download the file and manually edit it.  You could copy and paste it into an online editor.  

But what if you could just pluck the Category collection right out of the entire file? <https://pluck.do/Category/json.fyi/northwind.json>
