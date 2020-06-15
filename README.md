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
$ cd <caliban-tutorial cloned dir>
$ cd pytorch
$ caliban run --nogpu --dlvm pytorch trainer.mnist -- --epochs 2 
```

#### Run Caliban in cloud from GCE instance
```bash
$ cd <caliban-tutorial cloned dir>
$ cd pytorch
$ caliban cloud --nogpu --dlvm pytorch trainer.mnist -- --epochs 2 
```

#### Run Caliban in cloud from non-GCE instance
```bash
$ export GOOGLE_APPLICATION_CREDENTIALS=<key.json>
$ cd <caliban-tutorial cloned dir>
$ cd pytorch
$ caliban cloud --nogpu --dlvm pytorch trainer.mnist -- --epochs 2 
```

### Create notebook instance using DLVM
```bash
$ cd <caliban-tutorial cloned dir>
$ cd pytorch
$ caliban notebok --nogpu --dlvm pytorch 
```

### TensorFlow example
Same thing as pytorch except use tf 
```bash
$ caliban cloud --nogpu --dlvm tf trainer.mnist -- --epochs 2 
```


