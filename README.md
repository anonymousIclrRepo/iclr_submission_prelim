# layerwiseCNN

Code for experiments on greedy supervised layerwise CNNs

CIFAR pruning experiments  and code for updating the final auxillary final update

CIFAR experiments can be reproduced using cifar.py

Imagenet experiments for 1-hidden layer use the standalone imagenet_single_layer.py

Imagenet experiments for k=2+ can be run with imagenet.py


Some example results

k=3 (~91.7) 
```
python cifar.py --ncnn 4 --nlin 2 --feature_size 128 --epochdecay 15 --nepochs 50 --down [1] --prog 1

```

k=2 (~90.4)

```
python cifar.py --ncnn 4 --nlin 1 --feature_size 128 --epochdecay 15 --nepochs 50 --down [1] --prog 1

```

k=1 much more interesting model theoretically but performance  88.3 and bigger
```
python cifar.py --ncnn 5 --nlin 0 --feature_size 256 --epochdecay 15 --nepochs 50 --down [1,3] --bn 0

```

Imagenet

k=3 
```
python imagenet.py --ncnn 8 --nlin 2 

```

k=2 

```
python imagenet.py --ncnn 8 --nlin 1 

```

k=1 model
```
python imagenet_single_layer.py 

```
