# Gstreamer video player
This repository provides a video player based on Gstreamer, enabling video playback with start, stop and resume mechanisms. The current version is supported in Ubuntu. When running in MacOS, unstable results can be yielded due to session connection problems. 

Begin by cloning the repository and inserting desired files under the `videos` folder.

### Building the Docker image for Gstream with Python bindings
	cd docker/
	docker pull ubuntu:18.04
	docker build . -t gstreamer-python

### Setting up the Docker container to run the player.
	xhost +
	docker-compose up -d
	
### Running the container and starting the player
	docker exec -it tekever_task1 bash
	python src/gst_player.py

### Using the player

In the player window that pops up, insert the video in the text box using the absolute path. E.g `/task1/videos/video.mp4`
When the user inserts a video filepath in the text box, the player can start, stop and resume video playing. If a new filepath is supplied to the text box, the player starts playing the new video. 


