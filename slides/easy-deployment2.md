##  Easy Application Deployment - Ebay

Containerize service dependencies and address thema s environment variables.

	FROM teddziuba/python2.7

	ADD requirements.txt /tmp/requirements.txt
	RUN pip install -r /tmp/requirements.txt
<!-- .element: class="bash" -->

	docker run -d teddziuba/postgresql-development-9.2

	docker run -t -i -p 8000:8000 -e DATABASE_URL='...' -v /path/to/src:/app-dev 
		ebaynow python /app-dev/manage.py runserver 0.0.0.0:8000
