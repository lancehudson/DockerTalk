##  Easy Application Deployment - Ebay

Fails on a clean Ubuntu (precise) install

	pip install lxml
<!-- .element: class="bash" -->

Duh... Install OS Dependencies
<!-- .element: class="fragment" data-fragment-index="1" -->

	sudo apt-get install python-dev libxml2-dev libxslt1-dev 
<!-- .element: class="fragment bash" data-fragment-index="1" -->

Vagrant
<!-- .element: class="fragment" data-fragment-index="2" -->

	install_cmd = "apt-get update; apt-get install -y python-dev "\
		"libxml2-dev libxslt1-dev; pip install -r requirements.txt;"
	config.cm.provision :shell, :inline => install_cmd
<!-- .element: class="fragment" data-fragment-index="2" -->