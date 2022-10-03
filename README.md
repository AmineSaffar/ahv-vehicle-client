## description
This git repository contains the launch file necessary to run the lmad mission client with an ahv robot. Currently it contains the following files.

map_param_files/params.yaml: the ros parameters necessary to configure the client.
docker-compose.yml: the docker compose file used to run the client image.
model_configs.env: the file containing environment variables used to configure the robot and locker types.
rosmaster_configs.env: the file containing environment variables used to connect the client to a running rosmaster on the robot.

## Requirements
- Docker (https://www.docker.com/get-started)

## Installing the client
Pull the git repository:

```bash
git clone https://github.com/AmineSaffar/ahv-vehicle-client.git
```

Pull the client image from the aws public registry(1.5GB):

```bash
docker pull public.ecr.aws/f7d4x8o5/mission-client-ahv:latest
```

tag the client image:

```bash
docker tag public.ecr.aws/f7d4x8o5/mission-client-ahv:latest mission-client-ahv:latest 
```

## Running the client

```bash
cd ahv-vehicle-client
docker compose up
```

## Updating
to update the client re-reun the installation instructions.

