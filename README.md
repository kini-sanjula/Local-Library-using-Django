# LOCAL LIBRARY

The purpose of the website is to provide an online catalog for a small local library, where users can browse available books and manage their accounts.
The main features that have currently been implemented are:

- There are models for books, book copies, genre, language and authors.
- Users can view list and detail information for books and authors.
- Admin users can create and manage models.
- Librarians can renew reserved books

![dj](https://user-images.githubusercontent.com/60674228/132941686-afc8fa99-b925-4f94-b518-3b5e0d12ff55.PNG)


- We've created models for the book (the details of the book), book instance (status of specific physical copies of the book available in the system), and author. 
- We have also decided to have a model for the genre so that values can be created/selected through the admin interface.
- The genre is a ManyToManyField, so that a book can have multiple genres and a genre can have many books. 
- The author is declared as ForeignKey, so each book will only have one author, but an author may have many books

# Quick Start
- To get this project up and running locally on your computer:

- Set up the Python development environment. 
- After you have Python setup, run the following commands (if you're on Windows you may use py or py -3 instead of python to start Python):
```bash
pip3 install -r requirements.txt
python3 manage.py makemigrations
python3 manage.py migrate
python3 manage.py collectstatic
python3 manage.py test # Run the standard tests. These should all pass.
python3 manage.py createsuperuser # Create a superuser
python3 manage.py runserver 
```

- Open a browser to http://127.0.0.1:8000/admin/ to open the admin site
- Create a few test objects of each type.
- Open tab to http://127.0.0.1:8000 to see the main site, with your new objects.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
