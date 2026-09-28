```
podman run --network=ps --add-host=host.containers.internal:host-gateway -d --name flowableui -p 8088:8080 --add-host=host.containers.internal:host-gateway -e SPRING_DATASOURCE_URL="jdbc:postgresql://postgres:5432/flowable" -e SPRING_DATASOURCE_USERNAME="postgres" -e SPRING_DATASOURCE_PASSWORD="postgres" -e SPRING_DATASOURCE_DRIVER_CLASS_NAME="org.postgresql.Driver" flowable/flowable-ui:latest
  ```

  ```
  podman run --add-host=host.containers.internal:172.18.64.1 -d --name flowableui -p 8088:8080 flowable/flowable-ui:latest
  ```