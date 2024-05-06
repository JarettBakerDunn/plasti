This container hosts a built version of plasti.

docker run -it --rm -v $HOME/plasti:/home/plasti_user/work geodynamics/plasti

This command will start the plasti docker image and give you terminal access. Any changes made in the /home/plasti/work directory will be reflected on the host machine at home/plasti.
