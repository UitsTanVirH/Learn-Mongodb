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
```
