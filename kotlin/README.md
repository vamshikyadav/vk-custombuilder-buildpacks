# Kotlin Sample Application

## Building

```bash
pack build kotlin --builder vk-builder:bionic --path /path/to/kotlin/app
```

## Running

```bash
docker run --rm --tty --publish 8080:8080 applications/kotlin
```

## Viewing

```bash
curl -s http://localhost:8080/actuator/health | jq .
```
