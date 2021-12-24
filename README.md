# django-mptt Tutorial

## install
### virtual environment
```
sudo apt-get install python3-venv 
python3 -m venv .env
source .env/bin/activate
```

### install requirement
```
sudo apt -y install python3-pip
python3 -m pip install --upgrade pip
python -m pip install -r ./requirement.txt
```

### Database
```
python manage.py migrate apps.mpttexample
```


### create some data to test
```
python manage.py shell
```

```
from apps.mpttexample.model import Genre
rock = Genre.objects.create(name="Rock")
blues = Genre.objects.create(name="Blues")
Genre.objects.create(name="Hard Rock", parent=rock)
Genre.objects.create(name="Pop Rock", parent=rock)
```

## Run example
```
python manage.py runserver
```


URL : http://127.0.0.1:8000/genres/

![Alt text](mpttexample.jpg?raw=true "mptt-example")

## django-mptt

https://django-mptt.readthedocs.io/en/latest/tutorial.html

