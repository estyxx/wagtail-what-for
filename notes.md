### Installation

mkdir wagtail-ester
cd wagtail-ester/

pdm init
git init
pdm add wagtail
pdm run wagtail start notes

pdm run python manage.py migrate
pdm run python manage.py createsuperuser

docker build -t wagtail-ester
docker run -p 8000:8000 --name wagtail-ester wagtail-ester
