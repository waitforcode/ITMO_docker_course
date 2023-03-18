# Kubernetes (minicube) example
### 1. Установка и запуск
![start_kuber.png](screens%2Fstart_kuber.png)
### 2. Создание и запуск сервисов
`Вопрос: важен ли порядок выполнения этих манифестов? Почему?`
Порядок выполнения манифестов важен, потому что как минимум deployment зависит от  container и configmap.
![postgre.png](screens%2Fpostgre.png)
![pods.png](screens%2Fpods.png)
#### Nextcloud
![nextcloud.png](screens%2Fnextcloud.png)
![nextcloud_dash.png](screens%2Fnextcloud_dash.png)
### Minicube dashboard
![minicube_dash.png](screens%2Fminicube_dash.png)
![minicube_dash_view.png](screens%2Fminicube_dash_view.png)
`Вопрос: что (и почему) произойдет, если отскейлить количество реплик postgres-deployment в 0, затем обратно в 1, после чего попробовать снова зайти на Nextcloud?`
Будет ошибка, потому что при даунскейле все данные внутри БД удаляются и когда мы заново ее поднимаем - там уже нет таблиц с учетками и данными для nextcloud.