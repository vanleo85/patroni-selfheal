Порядок доработки
docker build -t harbor.svc.vkusvill.ru/zalando/patroni-selfheal:latest .

postgresql.acid.zalan.do/test-sonarqube
  добавить раздел: 


  sidecars:
    - name: "patroni-selfheal"
      image: "harbor.svc.vkusvill.ru/zalando/patroni-selfheal:latest"
      resources:
        limits:
          cpu: 500m
          memory: 500Mi
        requests:
          cpu: 100m
          memory: 100Mi

docker pull harbor.svc.vkusvill.ru/zalando/patroni-selfheal