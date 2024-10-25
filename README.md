# Exploration of Natural Language
The aim of this repository is to explore natural language. The end goal is to convert audio files into sheet music.

## Building the image
```
docker build -t <your_image_name> .
```

## Running the container
1) With exposed port and mounted volume (no gpus)

    for linux
    ```
    docker run -p 8888:8888 -v ./exploration:/home/user/app <your_image_name>
    ```
    for windows
    ```
    docker run --gpus all -p 8888:8888 -v ${PWD}\exploration:/home/user/app <your_image_name>
    ```

2) With exposed port and mounted volume (with gpus)

    for linux
    ```
    docker run --gpus all -p 8888:8888 -v ./exploration:/home/user/app <your_image_name>
    ```

    for windows
    ```
    docker run --gpus all -p 8888:8888 -v ${PWD}\exploration:/home/user/app <your_image_name>
    ```