# Kubernetes 101 for Python Developers

PyConDE & PyData Berlin 2019 // @christianbarra

---

## Get ready

- Clone `git@gitlab.com:PyBootCamp/k8s-101-python-developers.git`
- Follow the README

--

## Today's goals

- Learn how to structure a modern Python application
- Use terraform to create/destroy infrastructure
- Learn some basic concepts about Kubernetes and GKE
- Move your application from your machine to the cloud using GKE

---

# Docker quick recap

--

### Dockerfile

Let's open the `Dockerfile`

--

### docker build

Time to build our first container

```bash
docker build -t pybootcamp/basil:0.1 --target production .
```

```out
Do you know what `target` means?
```

It should take a couple of minutes to build the image.

--

### docker-compose

Now we can run docker-compose locally

```bash
env TAG=0.1 docker-compose up -d
```

Check your browser http://localhost:8080/events

--

### docker ps

If you type

```bash
docker ps
```

You should see 2 containers running, `basil` and `redis`.

--

### docker logs

If you type

```bash
docker logs k8s-101-python-developers_basil_1
```

Try calling http://localhost:8080/healthcheck

You should see the logs coming from the basil-web app.

--

# Q&A Session
