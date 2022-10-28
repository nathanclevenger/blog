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
  "SalesOrder": [],
  "Shipper": [],
  "Supplier": [],
  "Territory": []
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

But what if you could just pluck the Category collection right out of the entire file? 

If you visit <https://pluck.do/Category/json.fyi/northwind.json> you would see:

```json
[
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
  },
  {
    "picture": null,
    "entityId": 4,
    "description": "Cheeses",
    "categoryName": "Dairy Products"
  },
  {
    "picture": null,
    "entityId": 5,
    "description": "Breads, crackers, pasta, and cereal",
    "categoryName": "Grains/Cereals"
  },
  {
    "picture": null,
    "entityId": 6,
    "description": "Prepared meats",
    "categoryName": "Meat/Poultry"
  },
  {
    "picture": null,
    "entityId": 7,
    "description": "Dried fruit and bean curd",
    "categoryName": "Produce"
  },
  {
    "picture": null,
    "entityId": 8,
    "description": "Seaweed and fish",
    "categoryName": "Seafood"
  }
]
```

And what if you wanted to transform the camelCase to snake_case?

You could prepend `snake.case.do/` to the URL and then you would see:
```json
[
  {
    "picture": null,
    "entity_id": 1,
    "description": "Soft drinks, coffees, teas, beers, and ales",
    "category_name": "Beverages"
  },
  {
    "picture": null,
    "entity_id": 2,
    "description": "Sweet and savory sauces, relishes, spreads, and seasonings",
    "category_name": "Condiments"
  },
  {
    "picture": null,
    "entity_id": 3,
    "description": "Desserts, candies, and sweet breads",
    "category_name": "Confections"
  },
  {
    "picture": null,
    "entity_id": 4,
    "description": "Cheeses",
    "category_name": "Dairy Products"
  },
  {
    "picture": null,
    "entity_id": 5,
    "description": "Breads, crackers, pasta, and cereal",
    "category_name": "Grains/Cereals"
  },
  {
    "picture": null,
    "entity_id": 6,
    "description": "Prepared meats",
    "category_name": "Meat/Poultry"
  },
  {
    "picture": null,
    "entity_id": 7,
    "description": "Dried fruit and bean curd",
    "category_name": "Produce"
  },
  {
    "picture": null,
    "entity_id": 8,
    "description": "Seaweed and fish",
    "category_name": "Seafood"
  }
]
```

And then what if you wanted to sort those categories alphabetically by Category Name?

Just go to: <https://sort.do/category_name/snake.case.do/pluck.do/Category/json.fyi/northwind.json>
```json
```
