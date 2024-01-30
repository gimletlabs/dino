# Eval notes

<!-- TOC -->

- [Eval notes](#eval-notes)
  - [ViT-S/8](#vit-s8)
  - [ViT-S/16](#vit-s16)
  - [ViT-S/16 fp16](#vit-s16-fp16)
  - [ViT-S/14 DinoV2](#vit-s14-dinov2)
  - [ViT-Ti/16](#vit-ti16)

<!-- /TOC -->

Base command
`python ./eval_linear.py --data_path=/datasets/imagenet/ILSVRC/Data/CLS-LOC/ --evaluate`

## ViT-S/8

```sh
python ./eval_linear.py --data_path=/datasets/imagenet/ILSVRC/Data/CLS-LOC/ --evaluate --patch_size=8
```

```text
Model vit_small built.
We load the reference pretrained linear weights.
Downloading: "https://dl.fbaipublicfiles.com/dino/dino_deitsmall16_pretrain/dino_deitsmall16_linearweights.pth" to /home/vihang/.cache/torch/hub/checkpoints/dino_deitsmall16_linearweights.pth
100.0%
Test:  [  0/391]  eta: 0:17:39  loss: 0.380281 (0.380281)  acc1: 93.750000 (93.750000)  acc5: 98.437500 (98.437500)  time: 2.708638  data: 1.828419  max mem: 846
Test:  [ 20/391]  eta: 0:01:20  loss: 0.559775 (0.560542)  acc1: 84.375000 (85.156250)  acc5: 96.875000 (96.837798)  time: 0.091588  data: 0.000287  max mem: 993
Test:  [ 40/391]  eta: 0:00:53  loss: 0.504800 (0.601536)  acc1: 84.375000 (84.032012)  acc5: 97.656250 (96.455793)  time: 0.083965  data: 0.000281  max mem: 993
Test:  [ 60/391]  eta: 0:00:42  loss: 0.502291 (0.564686)  acc1: 87.500000 (85.245902)  acc5: 97.656250 (96.695697)  time: 0.081432  data: 0.000253  max mem: 993
Test:  [ 80/391]  eta: 0:00:36  loss: 0.716538 (0.618657)  acc1: 79.687500 (83.516590)  acc5: 96.093750 (96.508488)  time: 0.083536  data: 0.000242  max mem: 993
Test:  [100/391]  eta: 0:00:32  loss: 0.623209 (0.628215)  acc1: 85.156250 (83.408106)  acc5: 96.093750 (96.441832)  time: 0.083887  data: 0.000238  max mem: 993
Test:  [120/391]  eta: 0:00:28  loss: 0.531973 (0.632460)  acc1: 83.593750 (83.316116)  acc5: 96.875000 (96.526343)  time: 0.083836  data: 0.000224  max mem: 993
Test:  [140/391]  eta: 0:00:25  loss: 0.435032 (0.619030)  acc1: 89.843750 (83.626995)  acc5: 97.656250 (96.636746)  time: 0.083697  data: 0.000240  max mem: 993
Test:  [160/391]  eta: 0:00:23  loss: 0.679810 (0.630977)  acc1: 81.250000 (83.448175)  acc5: 95.312500 (96.462539)  time: 0.084011  data: 0.000206  max mem: 993
Test:  [180/391]  eta: 0:00:20  loss: 1.136989 (0.689275)  acc1: 69.531250 (81.979454)  acc5: 90.625000 (95.795925)  time: 0.083333  data: 0.000245  max mem: 993
Test:  [200/391]  eta: 0:00:18  loss: 1.277641 (0.747734)  acc1: 64.843750 (80.612562)  acc5: 90.625000 (95.114272)  time: 0.082513  data: 0.000226  max mem: 993
Test:  [220/391]  eta: 0:00:16  loss: 1.096730 (0.774484)  acc1: 73.437500 (80.062217)  acc5: 91.406250 (94.768100)  time: 0.081201  data: 0.000229  max mem: 993
Test:  [240/391]  eta: 0:00:14  loss: 0.753314 (0.788769)  acc1: 78.906250 (79.839860)  acc5: 92.968750 (94.508558)  time: 0.083774  data: 0.000209  max mem: 993
Test:  [260/391]  eta: 0:00:12  loss: 1.213251 (0.828748)  acc1: 64.843750 (78.747605)  acc5: 90.625000 (94.064296)  time: 0.083779  data: 0.000236  max mem: 993
Test:  [280/391]  eta: 0:00:10  loss: 1.027571 (0.848783)  acc1: 74.218750 (78.386343)  acc5: 92.187500 (93.808385)  time: 0.083863  data: 0.000228  max mem: 993
Test:  [300/391]  eta: 0:00:08  loss: 1.108118 (0.867847)  acc1: 72.656250 (77.974460)  acc5: 89.843750 (93.513808)  time: 0.083811  data: 0.000254  max mem: 993
Test:  [320/391]  eta: 0:00:06  loss: 1.179348 (0.883526)  acc1: 71.875000 (77.587130)  acc5: 88.281250 (93.251071)  time: 0.083823  data: 0.000246  max mem: 993
Test:  [340/391]  eta: 0:00:04  loss: 1.224718 (0.904226)  acc1: 67.187500 (77.057368)  acc5: 89.062500 (93.032900)  time: 0.084049  data: 0.000241  max mem: 993
Test:  [360/391]  eta: 0:00:02  loss: 0.979421 (0.914856)  acc1: 75.000000 (76.820031)  acc5: 91.406250 (92.949273)  time: 0.083515  data: 0.000244  max mem: 993
Test:  [380/391]  eta: 0:00:00  loss: 0.814474 (0.913746)  acc1: 76.562500 (76.851624)  acc5: 93.750000 (92.950295)  time: 0.083795  data: 0.000182  max mem: 993
Test:  [390/391]  eta: 0:00:00  loss: 0.723986 (0.911126)  acc1: 76.562500 (76.908000)  acc5: 93.750000 (92.980000)  time: 0.082328  data: 0.000111  max mem: 993
Test: Total time: 0:00:35 (0.090729 s / it)
* Acc@1 76.908 Acc@5 92.980 loss 0.911
Accuracy of the network on the 50000 test images: 76.9%
```

```sh
python eval_knn.py --arch=vit_small --patch_size=8 --data_path=/datasets/imagenet/ILSVRC/Data/CLS-LOC --dump_features eval_knn_vits_8_features
```

```text
Will run the code on one GPU.
| distributed init (rank 0): env://
git:
  sha: 66febe141b5fc6ba5cdcf33407b1049ec3c6c462, status: has uncommited changes, branch: gimlet

arch: vit_small
batch_size_per_gpu: 128
checkpoint_key: teacher
data_path: /datasets/imagenet/ILSVRC/Data/CLS-LOC
dist_url: env://
dump_features: eval_knn_vits_8_features
gpu: 0
half: False
load_features: None
local_rank: 0
nb_knn: [10, 20, 100, 200]
num_workers: 10
patch_size: 8
pretrained_weights:
rank: 0
temperature: 0.07
use_cuda: True
world_size: 1
Data loaded with 1281167 train and 50000 val imgs.
Model vit_small 8x8 built.
Please use the `--pretrained_weights` argument to indicate the path of the checkpoint to evaluate.
Since no pretrained weights have been provided, we load the reference pretrained DINO weights.
Extracting features for train set...
Storing features into tensor of shape torch.Size([1281167, 384])
  [    0/10010]  eta: 8:41:41    time: 3.126985  data: 1.496408  max mem: 4515
  <REMOVED>
  [10009/10010]  eta: 0:00:00    time: 0.636899  data: 0.000107  max mem: 6392
 Total time: 1:28:46 (0.532138 s / it)
Extracting features for val set...
Storing features into tensor of shape torch.Size([50000, 384])
  [  0/391]  eta: 0:10:42    time: 1.642119  data: 1.128212  max mem: 6392
  <REMOVED>
  [390/391]  eta: 0:00:00    time: 0.636005  data: 0.000107  max mem: 6465
 Total time: 0:03:28 (0.534096 s / it)
Features are ready!
Start the k-NN classification.
10-NN classifier result: Top1: 78.33, Top5: 90.896
20-NN classifier result: Top1: 78.33, Top5: 92.4
100-NN classifier result: Top1: 76.916, Top5: 93.662
200-NN classifier result: Top1: 76.096, Top5: 93.792
```

## ViT-S/16

```sh
python ./eval_linear.py --data_path=/datasets/imagenet/ILSVRC/Data/CLS-LOC/ --evaluate --patch_size=16
```

```text
Model vit_small built.
We load the reference pretrained linear weights.
Test:  [  0/391]  eta: 0:22:05  loss: 0.312423 (0.312423)  acc1: 95.312500 (95.312500)  acc5: 98.437500 (98.437500)  time: 3.391267  data: 1.672790  max mem: 4970
Test:  [ 20/391]  eta: 0:03:44  loss: 0.452702 (0.475851)  acc1: 86.718750 (86.904762)  acc5: 97.656250 (97.693452)  time: 0.464485  data: 0.000323  max mem: 5559
Test:  [ 40/391]  eta: 0:03:07  loss: 0.463861 (0.515941)  acc1: 85.156250 (85.575457)  acc5: 98.437500 (97.351372)  time: 0.463942  data: 0.000553  max mem: 5559
Test:  [ 60/391]  eta: 0:02:49  loss: 0.441266 (0.489972)  acc1: 87.500000 (86.680328)  acc5: 96.875000 (97.297643)  time: 0.467964  data: 0.000543  max mem: 5559
Test:  [ 80/391]  eta: 0:02:33  loss: 0.650984 (0.539812)  acc1: 82.812500 (85.310571)  acc5: 96.875000 (97.077546)  time: 0.434674  data: 0.000379  max mem: 5559
Test:  [100/391]  eta: 0:02:22  loss: 0.532990 (0.551392)  acc1: 86.718750 (85.202661)  acc5: 96.875000 (96.975557)  time: 0.471931  data: 0.000890  max mem: 5559
Test:  [120/391]  eta: 0:02:10  loss: 0.470687 (0.562025)  acc1: 84.375000 (85.156250)  acc5: 97.656250 (97.068698)  time: 0.433611  data: 0.000233  max mem: 5559
Test:  [140/391]  eta: 0:01:58  loss: 0.380097 (0.549805)  acc1: 88.281250 (85.328014)  acc5: 98.437500 (97.212988)  time: 0.431170  data: 0.000219  max mem: 5559
Test:  [160/391]  eta: 0:01:48  loss: 0.662740 (0.561041)  acc1: 83.593750 (85.161102)  acc5: 96.875000 (97.069099)  time: 0.430035  data: 0.000231  max mem: 5559
Test:  [180/391]  eta: 0:01:37  loss: 0.863500 (0.605005)  acc1: 75.781250 (84.016747)  acc5: 93.750000 (96.620338)  time: 0.430917  data: 0.000213  max mem: 5559
Test:  [200/391]  eta: 0:01:28  loss: 1.101570 (0.655729)  acc1: 67.968750 (82.812500)  acc5: 92.187500 (96.120958)  time: 0.433986  data: 0.000225  max mem: 5559
Test:  [220/391]  eta: 0:01:18  loss: 0.844362 (0.674672)  acc1: 78.906250 (82.356476)  acc5: 94.531250 (95.927602)  time: 0.430764  data: 0.000229  max mem: 5559
Test:  [240/391]  eta: 0:01:08  loss: 0.683789 (0.683675)  acc1: 82.031250 (82.277619)  acc5: 94.531250 (95.753371)  time: 0.431250  data: 0.000218  max mem: 5559
Test:  [260/391]  eta: 0:00:59  loss: 0.949632 (0.718124)  acc1: 73.437500 (81.324832)  acc5: 92.187500 (95.402299)  time: 0.433487  data: 0.000230  max mem: 5559
Test:  [280/391]  eta: 0:00:50  loss: 0.819773 (0.732555)  acc1: 77.343750 (81.010899)  acc5: 93.750000 (95.231873)  time: 0.430006  data: 0.000199  max mem: 5559
Test:  [300/391]  eta: 0:00:41  loss: 0.940584 (0.748425)  acc1: 75.000000 (80.658223)  acc5: 92.968750 (95.021802)  time: 0.430271  data: 0.000224  max mem: 5559
Test:  [320/391]  eta: 0:00:31  loss: 0.984055 (0.761864)  acc1: 76.562500 (80.332457)  acc5: 90.625000 (94.818438)  time: 0.429488  data: 0.000225  max mem: 5559
Test:  [340/391]  eta: 0:00:22  loss: 1.017162 (0.777974)  acc1: 72.656250 (79.928061)  acc5: 92.968750 (94.680169)  time: 0.430123  data: 0.000207  max mem: 5559
Test:  [360/391]  eta: 0:00:13  loss: 0.895487 (0.788876)  acc1: 76.562500 (79.655038)  acc5: 93.750000 (94.587517)  time: 0.434021  data: 0.000202  max mem: 5559
Test:  [380/391]  eta: 0:00:04  loss: 0.642365 (0.789293)  acc1: 77.343750 (79.615732)  acc5: 95.312500 (94.582513)  time: 0.429795  data: 0.000159  max mem: 5559
Test:  [390/391]  eta: 0:00:00  loss: 0.642365 (0.787828)  acc1: 78.906250 (79.612000)  acc5: 95.312500 (94.622000)  time: 0.426404  data: 0.000113  max mem: 5559
Test: Total time: 0:02:54 (0.446400 s / it)
* Acc@1 79.612 Acc@5 94.622 loss 0.788
Accuracy of the network on the 50000 test images: 79.6%
```

```sh
python eval_knn.py --arch=vit_small --patch_size=16 --data_path=/datasets/imagenet/ILSVRC/Data/CLS-LOC --dump_features eval_knn_vits_16_features
```

```text
Will run the code on one GPU.
| distributed init (rank 0): env://
git:
  sha: 314dd801c98fc4098afc70abbeafcb506b2c907e, status: has uncommited changes, branch: gimlet

arch: vit_small
batch_size_per_gpu: 128
checkpoint_key: teacher
data_path: /datasets/imagenet/ILSVRC/Data/CLS-LOC
dist_url: env://
dump_features: eval_knn_vits_16_features
gpu: 0
load_features: None
local_rank: 0
nb_knn: [10, 20, 100, 200]
num_workers: 10
patch_size: 16
pretrained_weights:
rank: 0
temperature: 0.07
use_cuda: True
world_size: 1
Data loaded with 1281167 train and 50000 val imgs.
Model vit_small 16x16 built.
Please use the `--pretrained_weights` argument to indicate the path of the checkpoint to evaluate.
Since no pretrained weights have been provided, we load the reference pretrained DINO weights.
Extracting features for train set...
Storing features into tensor of shape torch.Size([1281167, 384])
  <REMOVED>
  [10009/10010]  eta: 0:00:00    time: 0.106392  data: 0.000068  max mem: 2600
 Total time: 0:14:44 (0.088400 s / it)
Extracting features for val set...
Storing features into tensor of shape torch.Size([50000, 384])
  <REMOVED>
  [390/391]  eta: 0:00:00    time: 0.106757  data: 0.000093  max mem: 2673
 Total time: 0:00:35 (0.091346 s / it)
Features are ready!
Start the k-NN classification.
10-NN classifier result: Top1: 74.402, Top5: 88.422
20-NN classifier result: Top1: 74.444, Top5: 90.02
100-NN classifier result: Top1: 72.902, Top5: 91.482
200-NN classifier result: Top1: 72.062, Top5: 91.546
```

## ViT-S/16 fp16

```sh
git checkout vihang/eval_half
python ./eval_linear.py --data_path=/datasets/imagenet/ILSVRC/Data/CLS-LOC/ --evaluate --patch_size=16
```

```text
Model vit_small built.
We load the reference pretrained linear weights.
Test:  [  0/391]  eta: 0:12:20  loss: 0.380615 (0.380615)  acc1: 92.968750 (92.968750)  acc5: 98.437500 (98.437500)  time: 1.892996  data: 1.365466  max mem: 428
Test:  [ 20/391]  eta: 0:00:56  loss: 0.560059 (0.560416)  acc1: 84.375000 (85.193452)  acc5: 96.875000 (96.837798)  time: 0.065381  data: 0.033924  max mem: 502
Test:  [ 40/391]  eta: 0:00:43  loss: 0.504395 (0.601469)  acc1: 84.375000 (84.032012)  acc5: 97.656250 (96.455793)  time: 0.092914  data: 0.063916  max mem: 502
Test:  [ 60/391]  eta: 0:00:37  loss: 0.502441 (0.564628)  acc1: 87.500000 (85.245902)  acc5: 97.656250 (96.695697)  time: 0.088490  data: 0.056156  max mem: 502
Test:  [ 80/391]  eta: 0:00:32  loss: 0.716309 (0.618588)  acc1: 79.687500 (83.497299)  acc5: 96.093750 (96.508488)  time: 0.087520  data: 0.056728  max mem: 502
Test:  [100/391]  eta: 0:00:32  loss: 0.624023 (0.628162)  acc1: 85.156250 (83.369431)  acc5: 96.093750 (96.449567)  time: 0.142970  data: 0.106644  max mem: 502
Test:  [120/391]  eta: 0:00:38  loss: 0.532715 (0.632407)  acc1: 83.593750 (83.283833)  acc5: 96.875000 (96.532800)  time: 0.290818  data: 0.251886  max mem: 502
Test:  [140/391]  eta: 0:00:33  loss: 0.434326 (0.618959)  acc1: 89.843750 (83.610372)  acc5: 97.656250 (96.642287)  time: 0.084812  data: 0.056365  max mem: 502
Test:  [160/391]  eta: 0:00:29  loss: 0.679688 (0.630884)  acc1: 81.250000 (83.438470)  acc5: 95.312500 (96.472244)  time: 0.090619  data: 0.059577  max mem: 502
Test:  [180/391]  eta: 0:00:26  loss: 1.135742 (0.689190)  acc1: 69.531250 (81.970822)  acc5: 90.625000 (95.804558)  time: 0.091500  data: 0.063739  max mem: 502
Test:  [200/391]  eta: 0:00:23  loss: 1.276367 (0.747667)  acc1: 64.062500 (80.600902)  acc5: 90.625000 (95.122046)  time: 0.100896  data: 0.070123  max mem: 502
Test:  [220/391]  eta: 0:00:20  loss: 1.095703 (0.774410)  acc1: 73.437500 (80.048077)  acc5: 91.406250 (94.771635)  time: 0.092003  data: 0.062661  max mem: 502
Test:  [240/391]  eta: 0:00:17  loss: 0.752930 (0.788651)  acc1: 79.687500 (79.830135)  acc5: 92.968750 (94.511800)  time: 0.094443  data: 0.063852  max mem: 502
Test:  [260/391]  eta: 0:00:15  loss: 1.212891 (0.828628)  acc1: 64.843750 (78.744612)  acc5: 90.625000 (94.064296)  time: 0.093591  data: 0.065633  max mem: 502
Test:  [280/391]  eta: 0:00:12  loss: 1.028320 (0.848688)  acc1: 74.218750 (78.380783)  acc5: 92.187500 (93.808385)  time: 0.107170  data: 0.071783  max mem: 502
Test:  [300/391]  eta: 0:00:10  loss: 1.108398 (0.867766)  acc1: 72.656250 (77.966674)  acc5: 89.843750 (93.513808)  time: 0.096569  data: 0.064147  max mem: 502
Test:  [320/391]  eta: 0:00:08  loss: 1.179688 (0.883463)  acc1: 71.875000 (77.579829)  acc5: 88.281250 (93.251071)  time: 0.105090  data: 0.072960  max mem: 502
Test:  [340/391]  eta: 0:00:05  loss: 1.224609 (0.904156)  acc1: 67.187500 (77.050495)  acc5: 89.062500 (93.032900)  time: 0.094860  data: 0.061611  max mem: 502
Test:  [360/391]  eta: 0:00:03  loss: 0.979492 (0.914785)  acc1: 75.000000 (76.813539)  acc5: 91.406250 (92.949273)  time: 0.096149  data: 0.064149  max mem: 502
Test:  [380/391]  eta: 0:00:01  loss: 0.813477 (0.913679)  acc1: 76.562500 (76.849573)  acc5: 93.750000 (92.950295)  time: 0.099188  data: 0.069708  max mem: 502
Test:  [390/391]  eta: 0:00:00  loss: 0.726074 (0.911055)  acc1: 76.562500 (76.906000)  acc5: 93.750000 (92.980000)  time: 0.096989  data: 0.064411  max mem: 502
Test: Total time: 0:00:43 (0.110753 s / it)
* Acc@1 76.906 Acc@5 92.980 loss 0.911
Accuracy of the network on the 50000 test images: 76.9%
```

## ViT-S/14 DinoV2

```sh
git checkout vihang/eval_v2
python ./eval_linear.py --data_path=/datasets/imagenet/ILSVRC/Data/CLS-LOC/ --evaluate
```

```text
Model vit_small built.
Test:  [  0/391]  eta: 0:18:37  loss: 0.287185 (0.287185)  acc1: 93.750000 (93.750000)  acc5: 98.437500 (98.437500)  time: 2.858557  data: 1.847843  max mem: 965
Test:  [ 20/391]  eta: 0:01:33  loss: 0.449175 (0.454168)  acc1: 87.500000 (87.723214)  acc5: 97.656250 (97.953869)  time: 0.121201  data: 0.000267  max mem: 966
Test:  [ 40/391]  eta: 0:01:03  loss: 0.399514 (0.491631)  acc1: 87.500000 (86.432927)  acc5: 97.656250 (97.618140)  time: 0.107072  data: 0.000223  max mem: 966
Test:  [ 60/391]  eta: 0:00:51  loss: 0.369379 (0.460332)  acc1: 89.843750 (87.435963)  acc5: 98.437500 (97.745902)  time: 0.107282  data: 0.000181  max mem: 966
Test:  [ 80/391]  eta: 0:00:44  loss: 0.691794 (0.530860)  acc1: 81.250000 (85.648148)  acc5: 96.093750 (97.289738)  time: 0.106931  data: 0.000173  max mem: 966
Test:  [100/391]  eta: 0:00:39  loss: 0.607871 (0.549595)  acc1: 85.937500 (85.295483)  acc5: 96.875000 (97.145730)  time: 0.107492  data: 0.000128  max mem: 966
Test:  [120/391]  eta: 0:00:35  loss: 0.616540 (0.561549)  acc1: 83.593750 (85.040031)  acc5: 97.656250 (97.113895)  time: 0.107259  data: 0.000171  max mem: 966
Test:  [140/391]  eta: 0:00:32  loss: 0.387987 (0.549117)  acc1: 87.500000 (85.250443)  acc5: 98.437500 (97.279477)  time: 0.107170  data: 0.000180  max mem: 966
Test:  [160/391]  eta: 0:00:29  loss: 0.590641 (0.559286)  acc1: 84.375000 (85.170807)  acc5: 96.875000 (97.190411)  time: 0.107158  data: 0.000197  max mem: 966
Test:  [180/391]  eta: 0:00:26  loss: 0.819142 (0.592688)  acc1: 77.343750 (84.189399)  acc5: 94.531250 (96.900898)  time: 0.111123  data: 0.000660  max mem: 966
Test:  [200/391]  eta: 0:00:24  loss: 0.910006 (0.629575)  acc1: 71.093750 (83.290578)  acc5: 92.968750 (96.536847)  time: 0.167249  data: 0.050212  max mem: 966
Test:  [220/391]  eta: 0:00:23  loss: 0.771277 (0.641363)  acc1: 78.906250 (83.070560)  acc5: 95.312500 (96.440187)  time: 0.251233  data: 0.136657  max mem: 966
Test:  [240/391]  eta: 0:00:22  loss: 0.604386 (0.646282)  acc1: 82.031250 (82.977827)  acc5: 96.875000 (96.297977)  time: 0.215593  data: 0.095335  max mem: 966
Test:  [260/391]  eta: 0:00:18  loss: 0.910095 (0.676159)  acc1: 74.218750 (82.100096)  acc5: 93.750000 (96.012931)  time: 0.113562  data: 0.000376  max mem: 966
Test:  [280/391]  eta: 0:00:15  loss: 0.777899 (0.686569)  acc1: 78.906250 (81.897798)  acc5: 94.531250 (95.915814)  time: 0.122285  data: 0.000526  max mem: 966
Test:  [300/391]  eta: 0:00:12  loss: 0.817981 (0.694610)  acc1: 77.343750 (81.701620)  acc5: 94.531250 (95.790075)  time: 0.117873  data: 0.000669  max mem: 966
Test:  [320/391]  eta: 0:00:10  loss: 0.937429 (0.705814)  acc1: 76.562500 (81.466608)  acc5: 92.968750 (95.614291)  time: 0.191644  data: 0.070490  max mem: 966
Test:  [340/391]  eta: 0:00:07  loss: 0.908184 (0.720872)  acc1: 76.562500 (81.052969)  acc5: 92.968750 (95.456837)  time: 0.126619  data: 0.001506  max mem: 966
Test:  [360/391]  eta: 0:00:04  loss: 0.798275 (0.728798)  acc1: 78.906250 (80.825831)  acc5: 94.531250 (95.409886)  time: 0.213799  data: 0.093423  max mem: 966
Test:  [380/391]  eta: 0:00:01  loss: 0.649764 (0.727318)  acc1: 82.812500 (80.868602)  acc5: 96.093750 (95.421178)  time: 0.134691  data: 0.009982  max mem: 966
Test:  [390/391]  eta: 0:00:00  loss: 0.589799 (0.725904)  acc1: 80.468750 (80.892000)  acc5: 96.875000 (95.444000)  time: 0.129553  data: 0.002552  max mem: 966
Test: Total time: 0:00:57 (0.146009 s / it)
* Acc@1 80.892 Acc@5 95.444 loss 0.726
Accuracy of the network on the 50000 test images: 80.9%
```

## ViT-Ti/16

Trained manually on TinyImageNet and separately on ImageNet.

To train the Linear Classifier head:

```sh
python ./eval_linear.py --pretrained_weights=weights/dino_vitti_tinyimageimagenet.pth --data_path=/datasets/imagenet/ILSVRC/Data/CLS-LOC/ --arch=vit_tiny
```

