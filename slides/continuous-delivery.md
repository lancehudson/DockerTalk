## Continuous Delivery - Cambridge Healthcare

* Converted their entire staging environment from a handful of AMI's to a single docker host

* Whenever a new github branch get started, Jenkins (Continuous Integration Server) automatically builds a new Docker image from it. 

* If all tests pass the container becomes avaliable internally and they recieve a campfire notification. Otherwise the Docker image is left behind for examination.