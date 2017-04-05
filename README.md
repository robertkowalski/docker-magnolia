# docker-magnolia

## Usage

```
# build image
docker build -t mysupervisord .

# mount light-modules folder into current dir outside container
docker run -d --name magnolia -p 8080:8080 -v $(pwd):/opt/magnolia/light-modules -t -i mysupervisord

# delete old image, rebuild and run
docker rm mysupervisord && docker build -t mysupervisord . && docker run -d --name magnolia -p 8080:8080 -v $(pwd):/opt/magnolia/light-modules -t -i mysupervisord

```

## Helpful commands

```
# get logs
docker logs magnolia

# attach to container

docker attach magnolia
```
