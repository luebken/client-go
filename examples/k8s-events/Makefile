go-build:
	GOOS=linux go build -o ./app .
docker-build: go-build
	docker build -t luebken/k8s-events .
docker-push: docker-build
	docker push luebken/k8s-events
k8s-run:
	kubectl run --rm -i k8s-events --image=luebken/k8s-events
k8s-delete:
	kubectl delete pods k8s-events