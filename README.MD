```
sudo apt update
sudo apt install python3.8-venv
python3 -m venv venv_name
source venv_name/bin/activate
deactivate
pip install -r requirements.txt
python manage.py runserver
python manage.py shell_plus --ipython
python manage.py createsuperuser

python manage.py makemigrations
python manage.py migrate

sqlite3 db.sqlite3 "select name fROM sqlite_master WHERE type='table'"
sqlite3 db.sqlite3 'select * from auth_user'
sqlite3 db.sqlite3 '.dump auth_user'

python
>>> import sqlite3
>>> conn = sqlite3.connect("db.sqlite3")
>>> for row in conn.execute("select name fROM sqlite_master WHERE type='table'"):print(row)
>>> for row in conn.execute("select * from auth_user"):print(row)
>>>conn.close()

Ctrl-D
``` 

run django-extensions console: 
`python manage.py shell_plus --ipython`