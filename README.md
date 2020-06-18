# Caliban DLVM tutorial

## Pre-requisites

### Install Caliban from source (forked)

```bash
$ git clone https://github.com/sagravat/caliban.git
$ cd caliban
$ make build
$ source env/bin/activate
```

## Caliban DLVM Examples

### pytorch example

#### Run Caliban locally
```bash
$ cd <caliban-dlvm-tutorial cloned dir>
$ cd pytorch
$ caliban run --nogpu --dlvm pytorch trainer.mnist -- --epochs 2 
```

#### Run Caliban in cloud from GCE instance
```bash
$ cd <caliban-dlvm-tutorial cloned dir>
$ cd pytorch
$ caliban cloud --nogpu --dlvm pytorch trainer.mnist -- --epochs 2 
```

#### Run Caliban in cloud from non-GCE instance
To set up a service account to enable access to cloud resources, follow these [instructions](https://caliban.readthedocs.io/en/latest/getting_started/cloud.html#create-a-service-account-key).
```bash
$ export GOOGLE_APPLICATION_CREDENTIALS=<key.json>
$ export PROJECT_ID_=<GCP PROJECT_ID_>
$ cd <caliban-dlvm-tutorial cloned dir>
$ cd pytorch
$ caliban cloud --nogpu --dlvm pytorch trainer.mnist -- --epochs 2 
```

### Create notebook instance using DLVM
```bash
$ export GOOGLE_APPLICATION_CREDENTIALS=<key.json>
$ export PROJECT_ID_=<GCP PROJECT_ID_>
$ cd <caliban-tutorial-dlvm cloned dir>
$ cd pytorch
$ caliban notebook --nogpu --dlvm pytorch 
```
This will launch a Jupyterlab notebook pre-installed with an extension that allows you to submit your notebook to run on AI Platform. You can specify your configuration requirements and your hardware (GPUs and TPUs).


### TensorFlow example
Same thing as pytorch except use tf-<version> 
```bash
$ cd <caliban-dlvm-tutorial cloned dir>
$ cd tesnorflow
$ caliban run --nogpu --dlvm tf-21 trainer.mnist -- --epochs 2 
```


