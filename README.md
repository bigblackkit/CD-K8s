![CI_CD_k8s_7](https://github.com/user-attachments/assets/9b84c3d2-956a-4658-ad57-d7e9b777b1ab)

CI: https://github.com/bigblackkit/CI-K8s.git

Tree:

CD-K8s
│   ├── HelmChart
│   │   └── KitChart
│   │       ├── Chart.yaml
│   │       ├── templates
│   │       │   ├── deployment.yaml
│   │       │   ├── hpa.yaml
│   │       │   └── service.yaml
│   │       └── values.yaml
│   ├── KitApp
│   │   ├── applications
│   │   │   └── kitapp.yaml
│   │   └── Main.yaml
│   └── README.md

![изображение](https://github.com/user-attachments/assets/f2317f71-8351-488b-ac51-cac1452347f6)

![изображение](https://github.com/user-attachments/assets/e5ced8a7-cdbc-4aed-a569-6a3d19dfbd93)

![изображение](https://github.com/user-attachments/assets/3b6bbbae-6ece-4024-9ec1-ea2933abfc91)


1. После того как Jenkins Сделает нам новый Docker image,
его тег он любезно поместит в файл values.yaml даннгого репозитория и в связи с внесёнными изменениями ,
Gitlab отправляет Webhook в ArgoCD
2. ArgoCD сразуже реагирует на внесённые изменения и обновляет Docker image в нашем кламтере K8s

