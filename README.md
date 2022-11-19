### Basic:
```
show dbs
use db_name
```

### Adding New Documents
```
db.books.insertOne()
db.books.insertMany()
```

### Finding Documents
```
db.books.find({condition}, {filter 0,1})
db.books.findOne({})
```

### Sorting and limiting
```
db.books.find().count()
db.books.find().limit(5)
db.books.find.sort({1, -1})
```

### Operators and Complex queries
```
db.books.find({ rating: {$gt: 7} })
db.books.find({ rating: {$gte: 7}, author: "Name" })
db.books.find({ rating: {$lt: 7} })
db.books.find({ rating: {$lte: 7}, author: "Name" })
db.books.find({$or: [{rating: 7}, {rating: 9}] })
db.books.find({$or: [{ pages: {$lt: 300}}, {pages: {$gte: 400} }]})
```

### Using $in and $nin
```
db.books.find({ rating: {$in: [7, 8, 9]}})
db.books.find({ rating: {$nin: [7, 8, 9]}})
```
### Quering Arrays 
```
db.books.find({ genres: "fantasy" })
db.books.find({"reviews.name": 'Luigi'})
```
