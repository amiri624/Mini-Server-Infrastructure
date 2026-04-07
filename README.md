# Mini-Server-Infrastructure

## Step one

```bash
sudo apt update
sudo apt install docker.io docker-compose -y
```

## Then

```bash
sudo systemctl start docker
sudo systemctl enable docker
```

## Test

```bash
docker run hello-world
```

## Step two

```bash
docker run -d -p 8080:80 nginx
```
