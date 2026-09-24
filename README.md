# ECE_ing5_Gr02_Big_Data_labs

Labs of the ECE ING5 Big Data Processing course (fall 2026).

## Group

- Group: gr-02
- Oscar SCHWARTZ, oscarico92
- <Prénom NOM>, <username GitHub>
- <Prénom NOM>, <username GitHub>

## Labs

| Lab | Topic | Notebook |
|---|---|---|
| 02 | Introduction and RDDs: word count | [word_count.ipynb](./02.introduction-and-rdds/lab_pyspark_jupyter_docker/word_count.ipynb) |

## Running the labs

The notebooks run in the [`quay.io/jupyter/pyspark-notebook`](https://jupyter-docker-stacks.readthedocs.io/) docker image:

```bash
docker run --name pyspark_notebook --rm -d \
  -p 8888:8888 -p 4040:4040 \
  -v "$(pwd)":/home/jovyan/work \
  quay.io/jupyter/pyspark-notebook
docker logs pyspark_notebook 2>&1 | grep "token="
```

The input books (Project Gutenberg) are downloaded by the first cell of each notebook.
