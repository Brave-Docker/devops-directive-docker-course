.PHONY: build
build:
	docker build --tag my-scratch-image .

# Have to authenticate to dockerhub and create repo first:
# https://docs.docker.com/engine/reference/commandline/login/
.PHONY: push-dockerhub
push-dockerhub:
	docker tag my-scratch-image bravejongen/my-scratch-image		# defaults to latest
	docker push bravejongen/my-scratch-image
	
	docker tag my-scratch-image bravejongen/my-scratch-image:v2
	docker push bravejongen/my-scratch-image:v2



# Have to authenticate to ghcr.io first
# https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry#authenticating-to-the-container-registry
.PHONY: push-github-packages
push-github-packages:
	docker tag my-scratch-image ghcr.io/sidpalas/my-scratch-image 			# defaults to latest
	docker push ghcr.io/sidpalas/my-scratch-image

	docker tag my-scratch-image ghcr.io/sidpalas/my-scratch-image:abc-123 	# defaults to latest
	docker push ghcr.io/sidpalas/my-scratch-image:abc-123
