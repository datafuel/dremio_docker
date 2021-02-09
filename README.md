# Dremio docker-compose

## About
Local setup for Dremio on docker-compose

## Quickstart
1. Clone repo `git clone https://github.com/datafuel/dremio_docker.git`
2. Run `cd dremio_docker`
3. Rename **.env.example** to **.env** and replace dummy values with yours
4. Run `docker-compose up` then access the services

## Tutorials

### Configuring S3 for Minio (source : [Dremio Docs](https://docs.dremio.com/data-sources/s3.html#configuring-s3-for-minio))

To configure your **S3 source** for **Minio** in the Dremio UI:

1. Under *Advanced Options*, check **Enable compatibility mode (experimental)**.
2. Under *Advanced Options > Connection Properties*, add **fs.s3a.path.style.access** and set the value to **true**.
3. Under *Advanced Options > Connection Properties*, add the **fs.s3a.endpoint** property and its corresponding server endpoint value (*minio:9000* in the Datafuel ecosystem).