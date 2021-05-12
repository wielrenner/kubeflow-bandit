# Kubeflow Bandit
https://github.com/wielrenner/kubeflow-bandit

## Updating requirements
- pip install pip-tools
- pip compile

## Building the container
- docker login
- docker build . -t wroosmalen/kubeflow-ad-bidding:tagname
- docker push wroosmalen/kubeflow-ad-bidding:tagname

## Deploying the app
- kubectl apply -f ad-bidding.yaml -n log-replayer

## Getting IP of the app
- kubectl get pods -n log-replayer -o wide

## Interacting with the app
- pip install httpie
- http http://192.168.3.167:8080