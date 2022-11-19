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
### Updating Documents
```
db.books.updateOne({_id: ObjectId("63711fd6051aa7bc672d14ca"), {$set: {rating: 8, pages: 355}})
db.books.updateMany({author: "Terry Pratchett"}, {$set: {author: "Terry Pratchet"}})
db.books.updateOne({_id: ObjectId("63711fd6051aa7bc672d14cb")}, {$inc: {pages: 2}})
db.books.updateOne({_id: ObjectId("63711fd6051aa7bc672d14cb")}, {$push: {genres: "fantasy"}})
db.books.updateOne({_id: ObjectId("63711fd6051aa7bc672d14cb")}, {$pull: {genres: "fantasy"}})
```

