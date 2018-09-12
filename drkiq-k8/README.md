# iBug-DevOps-challenge

K8 setup
-------------------

1. start minishift from [here](https://docs.okd.io/latest/minishift/getting-started/quickstart.html)
2. `oc new-project myproject`
3. `oc process -f rubyontailsapp-template.yaml | oc create -f -`
4. `cp Dockerfile.drkiq Dockerfile && oc start-build drkiq --from-dir=. --follow`
5. `cp Dockerfile.sidekiq Dockerfile && oc start-build sidekiq --from-dir=. --follow`
6. try to access the [route](http://drkiq-myproject.192.168.99.100.nip.io)

