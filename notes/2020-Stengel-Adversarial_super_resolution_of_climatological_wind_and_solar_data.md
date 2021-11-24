# Information

**Adversarial super-resolution of climatological wind and solar data**

- Stengel, Glaws, Hettinger & N. King.

- 2020

- PNAS, vol. 117, no. 29

- 16805 - 16815

- Link: ???, [Notes](notes/2020-Stengel-Adversarial_super_resolution_of_climatological_wind_and_solar_data.md)

- Description: Use of deep learning (convolutional neural network) to increase
  the spatial resolution of wind and solar radiation outputs from climate
  projections.

# Notes

## Introduction

- Deep learning technique for classical image processing problem known as
  Super-Resolution (SR).

    - Uses adversarial training.

    - Low resolution (LR) -> Mid Resolution (MR) -> High Resolution (HR).

- Interpolation don't require training data, but tends to smooth out the
  output.

- SR tries to learn edge properties or inject textures.

- Perform SR through convolutional neural network (CNN).

## Data

- Deep fully-CNN for SR.

- Idea is to perform SR on LR CCSM (a GCM).

- Training and validation data is coarsened (there is a way to do this) HR wind
  and solar spatial data.

- CCSM wind (lowest level) ~= HR wind (100 m).

- CCSM radiation -> _a lot of things_.

- HR coarse data is done in order to obtain the training and validation data.

- The SR networks are based on SRGAN with several modifications (lots of
  details in a paragraph).

- 2 step process gives better results than 1 step (better performance).

    - Can learn complex relationships.

    - Much faster because is not a deep network that requires tons of
      iterations.

    - Allows to check intermediate results.

- Networks trained with GAN.

    - Solves an ill-posed problem by inserting physically realistic small scale
      details.

    - Based on a Generator (G) and a Discriminator (D).

    - Why the name "adversarial" is kinda explained.

- SRGAN success comes from its deep CNN generator (perceptual losses works
  better).

- G is trained in 2 rounds:

    - First without D (alpha = 0) so it can have a first guess (pre-training).
      The result is very smooth to reduce RMSE (part of the CNN, not good).

    - Second round D is used (alpha = 0.001).

- D loss should remain around 0.5.

    - They employ an adaptive training scheme.

    - If loss > 0.6 -> more iterations to D.

    - If loss < 0.45 -> more iterations to G.

- The training is long, but the evaluation is quite fast.

- D is the one who learns to identify physically relevant characteristics.

    - The adversarial training pushes G to reflect this characteristics.

    - _This could be an issue? -> depends on HR distribution._

- Use our knowledge of winds statistics to validate the data.

- Validate solar data was more difficult.

    - No good theoretical framework.

    - Use MSE and spatial autocorrelations (with semivariograms).

## Results

- Comparison between GAN, CNN (pre-training) and bicubic interpolation.
  Qualitatively speaking, GAN works better.

- In terms of MSE, both deep learning methods were better than interpolation.

- CNN has better MSE performance than GAN because it is made to optimize
  content-based loss (by smoothing).

- GAN is more physically consistent by making more aggressive predictions which
  deviates more from a good MSE.

- For the statistical validation, GAN performs well enough -> turbulent flow.

- The method used (GAN) is stable to random noise.

    - Sharp edges is where the error is bigger since LR doesn't have this
      information.

- Close to the south pole a repeated pattern is seen because of the longitudinal
  stretching.

- Solar radiation results are similar to wind results.

- There is an underestimation in the semivariogram, but still GAN has a food
  performance.

## Discussion

- Adversarial training approach learns the physical relevant features and makes
  sure to preserve it in the SR. It produces a more realistic product rather than
  the others (CNN) that minimize content loss (MSE).

- They don't want to replicate HR with SR, rather create a plausible HR.

- GAN provide a way to physically consistent deep learning. 
