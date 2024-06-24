# Multimodal face generation (facial-biometrics)
- **Similarity between faces:** One person resembles another person to a large degree. This can lead to many problems facing security surveillance systems.
- Facial recognition systems have difficulty distinguishing between the main person and other people who are highly similar in terms of features. Therefore, in this study, a generative convolutional neural architecture was proposed that is capable of extracting many people who have a high degree of similarity to the main person.
- This study helps generate a large number of samples of useful facial images that help biometric neural structures focus on more interesting features to distinguish between people.
- The generative neural architecture focuses on controlling the latent space by focusing on part of the dimensions of the latent space, and thus working to generate a new image that bears the features of the basic image, but with some change.
- 10 dimensions were used to control the regeneration of the image while changing the features of the generated image to make it similar to the basic image but different from it in some things through manipulation of the 10 dimensions.
- 70 dimensions were used for the basic features that define the main person, and therefore 70 represent the basic features of the image, while 10 dimensions were used to slightly change the features of the main person.
- Every time we get a different input for 10 inputs, the generative neural structure will redraw the facial image in a way that is similar to the basic image of the face but differs from it in some features.
- Adaptive instance normalization was used to reformulate the basic image of the person while changing some features and at the same time maintaining a person close to the basic person.
- The idea here is to use the normalization process within the structure of the decoder and not within the structure of the encoder.
- The encoder structure was used to form and study the basic features of the facial image and project the image features to their place within the basic 70-dimensional latent space.
- While in the case of decoding, after receiving the input from the location of the basic image within the 70-dimensional latent space, input from 10 dimensions will be passed to influence the regeneration process so that the regeneration process is conditionally normalized.
> - Note: In this study, the InfoGan methodology was used for semi-supervised conditional generation, but modifications to the InfoGan architecture were made by modifying the decoder architecture.

# Proposing a convolutional neural architecture:
![__results___20_0](https://github.com/kaledhoshme123/Multimodal-face-generation-facial-biometrics-/assets/108609519/c627c8d7-3c2a-49ec-8028-48406f8efd5c)

# Results:
## Samples of the results reached:

| Examples | #Outputs    |
| :---:   | :---: |
| ![image](https://github.com/kaledhoshme123/Multimodal-face-generation-facial-biometrics-/assets/108609519/305a1ce0-fc91-4f3a-98f1-14687becd7ba)| ![__results___38_2](https://github.com/kaledhoshme123/Multimodal-face-generation-facial-biometrics-/assets/108609519/e20aa64f-9eff-4423-8550-babc5a494775)|
| ![image](https://github.com/kaledhoshme123/Multimodal-face-generation-facial-biometrics-/assets/108609519/1df353ad-d7a7-4d9e-9cee-3809520779ae) | ![__results___39_2](https://github.com/kaledhoshme123/Multimodal-face-generation-facial-biometrics-/assets/108609519/30a2768f-4f3e-4f0d-858d-8601d8216586)|
| ![image](https://github.com/kaledhoshme123/Multimodal-face-generation-facial-biometrics-/assets/108609519/ff70ec6a-b68a-4079-9d3e-51cb395fad5a) | ![__results___40_2](https://github.com/kaledhoshme123/Multimodal-face-generation-facial-biometrics-/assets/108609519/7858e4a6-a37f-4879-bd44-953a15e57626)|
| ![image](https://github.com/kaledhoshme123/Multimodal-face-generation-facial-biometrics-/assets/108609519/0b6342e4-25e9-4ff2-a8a2-b0d7e90eb258) | ![__results___41_2](https://github.com/kaledhoshme123/Multimodal-face-generation-facial-biometrics-/assets/108609519/2056a597-c9c8-4982-8c42-953c069d3f29) |
| ![image](https://github.com/kaledhoshme123/Multimodal-face-generation-facial-biometrics-/assets/108609519/561d4d91-0c5e-4c35-b452-551b2d4dc6a4) | ![__results___42_2](https://github.com/kaledhoshme123/Multimodal-face-generation-facial-biometrics-/assets/108609519/4352ed25-edc5-42ba-9a18-c9a395d1c908)|
| ![image](https://github.com/kaledhoshme123/Multimodal-face-generation-facial-biometrics-/assets/108609519/b8d2b03a-17c3-4788-9a16-1094223a3d28) | ![__results___43_2](https://github.com/kaledhoshme123/Multimodal-face-generation-facial-biometrics-/assets/108609519/a4f90295-0832-4cb0-996d-ef3b557320c1)|
| ![image](https://github.com/kaledhoshme123/Multimodal-face-generation-facial-biometrics-/assets/108609519/85e09bd7-cf54-4657-969b-568ee0252bd3)| ![__results___44_2](https://github.com/kaledhoshme123/Multimodal-face-generation-facial-biometrics-/assets/108609519/3a09d0a9-6f77-4ad4-8270-9b99e582a148)|
| ![image](https://github.com/kaledhoshme123/Multimodal-face-generation-facial-biometrics-/assets/108609519/6dd40360-3607-48bf-9e6e-16bae57e6ea7)| ![__results___46_2](https://github.com/kaledhoshme123/Multimodal-face-generation-facial-biometrics-/assets/108609519/c1eab432-fd3a-48e2-a2f3-964a20eb043f)|
| ![image](https://github.com/kaledhoshme123/Multimodal-face-generation-facial-biometrics-/assets/108609519/2891ae4a-7113-44fd-819e-bc04a4997005)| ![__results___48_2](https://github.com/kaledhoshme123/Multimodal-face-generation-facial-biometrics-/assets/108609519/fec74d71-bb44-41af-8b5e-4efd6afb491b)|

- Note: The vast majority of the data sets that were used include pictures of people with white skin, and therefore there are a small number of black people in the data set, and even within the data set there is not a large number of pictures of Asian people. Therefore, you can retrain with a larger data set than the one I used
