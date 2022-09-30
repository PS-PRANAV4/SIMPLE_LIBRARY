# SIMPLE_LIBRARY

#setingup project
first: install virtualenviorment
secodn: activate virtual enviorment
clone this repository by typing “git clone https://github.com/PS-PRANAV4/SIMPLE_LIBRARY.git”

third: install requirments

	command – pip install -r requirment.txt

runsever – python manage.py runserver
now you are good to go no more changes needed everything is setup


#API DOCS
To get access token
	/api/ token
	method- post
	params – nil
	body -  username, password
	sample - 
		{
			“username” – pranav,
			“password” – 123
		}
after this a access token will be given use this and add it in header as given below to get authenticated into other view or else will get 401 error

sample - {
		“Authorization”: “bearer <token>”
	}


To get all ebooks
	/get-all-ebooks 
	method – get
	params -nil
	body -nil



To create ebook
	/create-ebook
	method – post
	params – nil
	body -  Title,  Author, Genre, Review, Favorite(optional true or false)
	sample -
			{

"Title": "welcome",
"Author": "pranav",
"Genre": "Fantasy",
"Review": 2
}



To update ebook
	/update-ebook
	method – put
	params – nil 
	body - 	Title(new Title or old Title),  Author(old Author or new Author), Genre(new Genre or old Genre), Review(new Review or old Review), Favorite(new or old)




To delete ebook
	/delete-ebook/<int:id>
	method – delete
	params: id(id of ebook)
	body – nil


To search e-book
	can enter a key and will match with every field and returns the value
	method – post
	params – nil
	body – details(key to search)
	sample - 
		{
			details:”p”
		}

	
	
 



