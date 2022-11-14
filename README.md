Commands:

	show dbs
	use db_name
	
	Adding New Documents
	db.collection_name.insertOne()
	db.cn.insertMany()
	
	Finding Documents
	db.cn.find({condition}, {filter 0,1})
	db.cn.findOne({})
	
	Sorting and limiting
	db.cn.find().count()
	db.cn.find().limit(5)
	db.cn.find.sort({1, -1})
	
