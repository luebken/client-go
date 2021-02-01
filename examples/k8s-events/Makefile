go-build:
	GOOS=linux go build -o ./app .
docker-build:
	docker build -t luebken/k8s-events .
docker-push:
	docker push luebken/k8s-events
k8s-run:
	kubectl run --rm -i demo2 --image=luebken/k8s-events