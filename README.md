# README

## TODO Lists

- [x] FCN
- [x] PSPNet
- [x] Deeplab v1
- [x] Deeplab v2
- [x] Deeplab v3
- [x] Deeplab v3+
- [ ] HRNet
- [ ] U-net (Pix2Pix)
- [x] Pix2PixHD
- [ ] Deformable Convolution v1
- [ ] Deformable Convolution v2

## Summary

### FCN-Fully Connected Network

VGG Backbones

32x down sampling

Using 1/8, 1/16, 1/32 sizes of feature maps from 3th, 4th, 5th downsampling of VGG feature map 

Upsampling method: Transposed Convolution k=3, s=2, p=1, d=1 out_padding=1

BCEWithLogitsLoss

### PSPNet - Pyramid Sence Parsing Net

Resnet34 Backbone

8x downsampling

using pooling window size of [1,2,3,6]

do AdaptiveAvgPool on last feature map

3 times (2**3=8) upsampling

Auxiliary loss & BCEWithLogitsLoss

### Deeplab v1

Resnet34 Backbone

Stem 4x down sample

Res Layers 2x downsample

Total 8x downsample

Using Atrous Convolution/Dilated Convolution

CRF Conditional Random Field (Wasted in v3)

### Deeplab v2

add ASPP Atrous Spatial Pyramid Pooling: using multiple Atrous Convolution replace pooling and concatresults

### Deeplab v3

using multi-grids in res layer5 for de-griding

modifications on ASPP

### Deeplab v3+

add a decoder to upsample results to the original size of input image

Upsample method: bilinear

### Pix2PixHD

Too much

See https://github.com/NVIDIA/pix2pixHD

