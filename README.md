запрос(ы) для *вставки* данных минимум о двух книгах в коллекцию **books**

books.insertMany(
   {
     title: "First book",
	 description: "story",
	 authors: "Ivanov",
	 id: 1
   },
   {
     title: "Second book",
	 description: "novel",
	 authors: "Smith",
	 id: 2
   }
)  

 - запрос для *поиска* полей документов коллекции **books** по полю *title*  
     books.find(
	     {title: {$eq: "Second book"}}
	 )
 
 
 - запрос для *редактирования* полей: *description* и *authors* коллекции **books** по *_id* записи
      books.updateOne(
	           {id: {$eq: 1}},
			   {$set: {description: "new description"},
			          {authors: "Pierro"}
			   }
	  )  
	  