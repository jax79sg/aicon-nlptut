# O'Reilly Artificial Intelligence Conference

## Natural Language Processing with Deep Learning training

## Delip Rao, Brian McMahan

This is the Dockerfile creation repository.

For dev, start from the root directory which contains the Dockerfile,
please run the following commands (replacing LOCALPORT with whatever you'd like)

(data should come with repo, so no need to download fresh)
```
docker build -t dl4nlp .
docker run -p LOCALPORT:8888 -d --name dev dl4nlp
```

If running outside of docker, can do the following from root dir (where you can see day_1, day_2, etc):

```
export DL4NLPRoot=$(pwd)
jupyter notebook --notebook-dir=$(pwd)
```

Assuming all necessary things are installed.
