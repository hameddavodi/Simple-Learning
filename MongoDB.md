# MongoDB

Reviewed: No
Type: Reading

# 1- General commands:

```jsx
use databasename
show collections
db.collection.'command'
```

# 2- Insertion and update:

```jsx
# Insert different values to field 1 and field 2
db.collection.insertMany([
	
	{field1:value1,field2:value2},

	{field1:value3,field2:value4}

])

# Update existing value based on a condition
db.collection.updateMany(

	{filter},

	{$set:{field1:value1,field2:value2}}

)
```

# 3- Aggregations:

## 1- $MATCH:

```jsx
# for CONDITIONS

db.collection.aggregation([

	{$match: {field1:value1}}

])

# multi CONDITIONS

db.collection.aggregate([
  {$match: {$and:[

        { field1: value1 },  # each condition is in separet curly bracket
        { field2: { $gt: value2 } },
        { field3: { $ne: value3 } }

      ]}}
]);
```

## 2- $UNWIND

```jsx
# Decompose nested tags

db.collection.aggregate([

  { $unwind: '$arrayField' }

]);
```

## 3-$PROJECT

```jsx
# Rename and Show
db.collection.aggregate([

  { $project: { newField1: expression1, newField2: expression2 } }

]);

expressions can be 0,1 > show, not show
										"$tagname" to rename

# other expressions that can be used are:
		$size: number of elements within a tag

e.g. {$project: { _id:0,'City':'$name', "number_of_heads": {$size: '$heads'}}}

		$sum: Calculates the sum of numerical values in an array or within documents.
		$avg: Calculates the average of numerical values in an array or within documents.
    $max: Returns the maximum value from an array or among documents.
    $min: Returns the minimum value from an array or among documents.
    $concat: Concatenates multiple strings or expressions.
    $cond: Performs conditional evaluations and returns different values based on specified conditions.

e.g: 

$project: {
      _id: 0,
      'City': '$name',
      "number_of_heads": {
        $cond: {
          if: { $gte: [ { $size: "$heads" }, 3 ] },
          then: { $size: "$heads" },
          else: null
        }

```

## 4-$COUNT

```jsx
# Count the number of outputs

db.collection.aggregate([

  { $count: 'countField' }

]);
```

## 5- $GROUP

```jsx
# Group specific tags with specific operations

db.collection.aggregate([

  { $group: { _id: '$field', newField: { $sum: '$field' } } }

]);

db.collection.aggregate([
  { $group: { _id: null, total: { $sum: '$field' } } }
]);

db.collection.aggregate([
  { $group: { _id: null, average: { $avg: '$field' } } }
]);

```

## 6-$SORT

```jsx
# Sorting
db.collection.aggregate([

  { $sort: { field1: 1, field2: -1 } }

]);
```

# 3-Order of Aggregations

1. $Match
2. $Group
3. $Project
4. $Sort
5. $Count

# 4- TIPS:

```jsx
# To refer a tag in expression mode we use '$tag'

e.g. 

{$project:{'City':'$name',_id:0}}
{$project: { _id:0,'City':'$name', "number_of_heads": {$size: '$heads'}}},

# the order of double matching is like:

db.mnexam.aggregate([
  {$match: {"heads.election_year": { $gte: 2000 }}},
  {$project: { _id:0,'City':'$name', "number_of_heads": {$size: '$heads'}}},
  {$limit:3},
  {$match: {"number_of_heads": { $gt: 2}}},
  {$project: {"_id": 0,"city_name": "$name"}}
])

# think about each one like a pipline
```
