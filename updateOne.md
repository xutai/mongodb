


updateOne can only update existing fields, or using "upsert" to insert a new document!

in compass, i can use "aggregations" tab, then add staga "$addFields"
- [https://docs.mongodb.com/manual/reference/operator/aggregation/addFields/](https://docs.mongodb.com/manual/reference/operator/aggregation/addFields/)

compass example
```
/**
 * newField: The new field name.
 * expression: The new field expression.
 */
{
  "price": 0
}
```