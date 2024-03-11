## ROS2 Humble + OMPL - Docker

Repo provides a quick start with a ROS2 Humble + OMPL development in Docker.

### Setup

```shell
git clone https://github.com/JeelChatrola/ROS-2-OMPL-DockerImage.git && cd ROS-2-OMPL-DockerImage
./run.sh -h
```

### Building

```shell
./run.sh -w dev_ws -i [YOUR_IMAGE_NAME:TAG] -b
```

### Running

- Update `.tmux.conf` if you need to enable additional `tmux` features
- Update `.session.yml` to customize Tmuxinator UI

Note that the above configs are mapped as volumes to docker image.

```shell
./run.sh -w dev_ws -i [YOUR_IMAGE_NAME:TAG] -r
```

### Development

- Follow [this guide](https://code.visualstudio.com/docs/remote/containers) to prepare VSCode for remote development in a container.
- Start the docker container via the command from the [Running](#running) section.
- Open VSCode and [attach](https://code.visualstudio.com/docs/remote/attach-container) to the running container.
- Open your ROS2 workspace and enjoy.

### Notes

- Mouse is enabled by default
- Use pageup/pagedown keys to switch between `tmux` windows (mouse click also works)
- Press shift key to select the text via mouse
- `tmux` ctrl+b prefix is remapped to ctrl+a
- ctrl+a -> x -> y series closes the `tmux` and docker session
