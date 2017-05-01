# Apache Hadoop 2.8.0 Docker image

[![DockerPulls](https://img.shields.io/docker/pulls/sysk/hadoop.svg)](https://hub.docker.com/r/sysk/hadoop/)
[![DockerStars](https://img.shields.io/docker/stars/sysk/hadoop.svg)](https://hub.docker.com/r/sysk/hadoop/)

# Build the image

If you'd like to try directly from the Dockerfile you can build the image as:

```
docker build  -t sysk/hadoop:2.8.0 .
```
# Pull the image

The image is also released as an official Docker image from Docker's automated build repository - you can always pull or refer the image when launching containers.

```
docker pull sysk/hadoop:2.8.0
```

# Start a container

In order to use the Docker image you have just build or pulled use:

**Make sure that SELinux is disabled on the host. If you are using boot2docker you don't need to do anything.**

```
docker run -it sysk/hadoop:2.8.0 /etc/bootstrap.sh -bash
```

## Testing

You can run one of the stock examples:

```
cd $HADOOP_PREFIX
# run the mapreduce
bin/hadoop jar share/hadoop/mapreduce/hadoop-mapreduce-examples-2.8.0.jar grep input output 'dfs[a-z.]+'

# check the output
bin/hdfs dfs -cat output/*
```
