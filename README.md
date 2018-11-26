# Credit Scoring

This is a work in progress to define a model able to predict the probabily of credits payment failure.


## Try it locally

To try the solution locally, you need to download the `solution.ipynb` file and open it with a `jupyter notebook`.

If you don't have a `jupyter notebook` installed locally, here are alternatives:



### Docker

I personnaly use this docker image:

```
# REPLACE /local/file/name with your local project's folder
docker run -v /local/file/name:/home/jovyan/work -p 8888:8888 jupyter/scipy-notebook
```

This will create a `jupyter notebook` service listening on port 8888.
At the end of the command, the terminal will print an URL you can use to play with `.ipynb` files, like:

```
Copy/paste this URL into your browser when you connect for the first time,
    to login with a token:
        http://(f07f637e6952 or 127.0.0.1):8888/?token=9b8cf03d4f8e6ba2f5456c2706e61ef7e7d2dc20b1d47db0
```


NOTE: this docker comes pre-installed with a lot of `python` libraries. However, if you need to install more packages, you need to connect to the running docker instance.

Print docker instance number from another console:

```
docker ps

# 
# CONTAINER ID        IMAGE                            COMMAND                  CREATED             STATUS              PORTS                      NAMES
# f07f637e6952        jupyter/scipy-notebook           "tini -g -- start-..."   2 hours ago         Up 2 hours          0.0.0.0:8888->8888/tcp     competent_wilson

```

Copy docker's id like `f07f637e6952`

Now enter into the container in bash mode:

```
docker exec -it f07f637e6952 bash
```

Then to install any python package, use `conda`, for example:

```
conda install plotly
```

### Use an online service

There are some online services deploying `jupyter notebooks` on the fly from github repos like this one.
One of the most famous is: [mybinder.org](https://mybinder.org/).

Just follow instructions there with this repo :)

