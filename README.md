# Greedy Layerwise CNN

This is a peliminary research code.

Code for experiments on greedy supervised layerwise CNNs

CIFAR experiments can be reproduced using cifar.py

Imagenet experiments for 1-hidden layer use the standalone imagenet_single_layer.py

Imagenet experiments for k=2+ can be run with imagenet.py

Note k in the paper corresponds to nlin in the code

Some example results

k=3 (~91.7) 
```
python cifar.py --ncnn 4 --nlin 2 --feature_size 128 --down [1] 

```

k=2 (~90.4)

```
python cifar.py --ncnn 4 --nlin 1 --feature_size 128 --down [1] 

```

k=1 (~88.3) much more interesting model theoretically 
```
python cifar.py --ncnn 5 --nlin 0 --feature_size 256 --down [1,3] --bn 0

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
python imagenet_single_layer.py --ncnn 8

```

To be added soon CIFAR pruning experiments, linear separability experiments,  and code for reducing of final auxillary network
