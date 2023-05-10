## pod

- Pod는 Kubernetes에서 실행 가능한 가장 작은 단위이며, 하나의 컨테이너를 포함할 수 있습니다.
- `pod.yaml` 파일은 "argocd-helloworld"라는 이름을 가진 Pod를 생성하고, 해당 Pod에는 "nginx" 이미지를 실행하는 하나의 컨테이너가 있습니다. 또한, 이 Pod에는 80번 포트로 노출된 포트가 설정되어 있으며, 리소스 제한으로 64Mi 메모리와 0.2 CPU를 설정하고 있습니다. 이 파일은 kubectl apply 명령어를 사용하여 Kubernetes 클러스터에 적용되어 실행될 수 있습니다.

## Service

- Service는 클러스터 내에서 실행 중인 Pod들을 추상화하여 접근 가능한 단일 IP 주소와 포트로 제공하는 역할을 합니다.
- `service.yaml` 파일에서 생성되는 Service의 이름은 "argocd-helloworld"이며, Pod의 selector가 "app: argocd-helloworld"인 Pod들을 대상으로 합니다. 이 Service는 포트 80으로 노출되며, 대상 포트도 80으로 설정되어 있습니다. 따라서 이 Service를 통해 클러스터 내에서 실행 중인 "argocd-helloworld"라는 이름의 Pod에 접근할 수 있게 됩니다.
