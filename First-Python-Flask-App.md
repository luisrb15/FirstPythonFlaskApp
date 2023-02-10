## Requirementes for the app

First you need to install python3 and pip. Then run the following commands:
- `pip install flask`
- `pip install Flask-WTF`
- `pip install Flask-SQLAlchemy`

On the directory run the following commands:
- `python3`
- `from app import db`
- `db.create_all()`

***

##### If there is a problem with app context:
```
RuntimeError: Working outside of application context.

This typically means that you attempted to use functionality that needed
the current application. To solve this, set up an application context
with app.app_context(). See the documentation for more information.
```
It can be solved with next commands:
 - `python3`
 - `from app import app,db`
 - ```with app.app_context():
	   db.create_all()