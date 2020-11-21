# Generative-Jamdani

Based on [pix2pix-tensorflow](https://affinelayer.com/pix2pix/) which is tensorflow port of [pix2pix](https://phillipi.github.io/pix2pix/) by Isola et al.

## Interactive Demo
![Demo](https://i.imgur.com/4r83NO3.gif)


Sample output generated by our Generative-Jamdani from input sketches, like these examples from the original paper:

<img src="docs/dataset-disp.png" width="auto"/>

This is an implementation of [pix2pix-tensorflow](https://github.com/affinelayer/pix2pix-tensorflow) on **Jamdani Noksha** dataset.  It is meant to be a faithful implementation of the original work and so does not add anything.  

## Setup

### Prerequisites
- Tensorflow 1.4.1

### Recommended
- Linux with Tensorflow GPU edition + cuDNN

### Getting Started

```sh
# clone this repo
git clone https://github.com/raihan-tanvir/generative-jamdani.git
cd generative-jamdani

python pix2pix.py \
  --mode train \
  --output_dir model/ \
  --max_epochs 150 \
  --input_dir dataset/train \
  --which_direction BtoA
# test the model
python pix2pix.py \
  --mode test \
  --output_dir output/ \
  --input_dir dataset/test \
  --checkpoint model/
```

The test run will output an HTML file at `output/index.html` that shows input/output/target image sets.



## Datasets

The data format used by this program is the same as the original pix2pix format, which consists of images of input and desired output side by side like:

<img src="docs/ab.png" width="256px"/>

For example:

<img src="docs/163_AB.png" width="256px"/>

### Datasets Link

| dataset | example |
| --- | --- |
| [JamdaniNoksha-B Dataset](https://drive.google.com/drive/folders/1IwyV8yg4fVTvPFcD9fHg1Dpyw5xwInS1?usp=sharing)  <br> 1116 images   | <img src="dataset-example/B.jpg" width="256px"/> |
| [JamdaniNoksha-BRes Dataset](https://drive.google.com/drive/folders/1SWFlNSUujRiI7KC7sTODL1vcLqCfVN3V?usp=sharing)  <br> 1983 images   | <img src="dataset-example/BRes.png" width="256px"/> |
| [JamdaniNoksha-Skel Dataset](https://drive.google.com/drive/folders/1SWFlNSUujRiI7KC7sTODL1vcLqCfVN3V?usp=sharing)  <br> 7932 images   | <img src="dataset-example/Skel.png" width="256px"/> |
| [JamdaniNoksha-RedB Dataset](https://drive.google.com/drive/folders/1SWFlNSUujRiI7KC7sTODL1vcLqCfVN3V?usp=sharing)  <br> 913 images   | <img src="dataset-example/RedB.png" width="256px"/> |
| [JamdaniNoksha-Sketch Dataset](https://drive.google.com/drive/folders/1eJCgAg2jGYjmqqe3e26QYSJIKmbhu51D?usp=sharing)  <br> 910 images   | <img src="dataset-example/Sketch.png" width="256px"/> |

## Citation

```
@inproceedings{generative-jamdani,
  title={Jamdani Motif Generation using Conditional GAN},
  author={Tanvir Rouf Shawon, Raihan Tanvir, Humaira Ferdous Shifa, Susmoy Kar, Mohammad Imrul Jubair},
  publisher={International Conference on Computer and Information Technology},
  venue={Ahsanullah University of Science & Technology, Dhaka, Bangadesh},
  year={2020}
}
```

## Acknowledgments
This is a implementation of [pix2pix-tensorflow](https://github.com/affinelayer/pix2pix-tensorflow) on **Jamdani Noksha** dataset.  Thanks to the Tensorflow [Affinelayer](https://github.com/affinelayer) for making such a wonderful port!  And special thanks to Phillip Isola for the original [pix2pix](https://phillipi.github.io/pix2pix/).
