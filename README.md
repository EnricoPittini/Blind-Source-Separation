# Blind-Source-Separation
The purpose of this project is to separate an image obtained as a sum of two images into its components, using Convolutional Neural Networks.

Several different CNN have been tried. The following table sums up the results.

| Model                                  | Parameters | MSE    |
| :------------------------------------- | ---------: | -----: |
| Convolutional autoencoder                            | 47,617     | 0.0240 |
| Two-branches convolutional autoencoder | 337,570    | 0.0062 |
| Two-branches U-Net                                  | 157,410    | 0.00049 |
| Single-branch U-Net                                  | 11,261,121    | 0.00038 |

However, the best results have been achieved with the **Attention U-Net**. In particular, the implementation is based on [this one](https://github.com/bnsreenu/python_for_microscopists/blob/master/224_225_226_models.py).

| #parameters | #epochs | Min MSE     | Mean MSE | Std MSE |
| ----- | ---- | ----------- | ------- | ------- |
| $9M$      | $32$       | $3.111e-4$ | $3.146e-4$| $2.29e-6$|

## Dependencies
- [NumPy](https://pypi.org/project/numpy/)
- [Matplotlib](https://pypi.org/project/matplotlib/)
- [Tensorflow](https://www.tensorflow.org/)

## Repository structure

    .
    ├── images    # It contains the images in the notebook   
    ├── task_description.ipynb    # Task description
    ├── Blind Source Separation.ipynb    # Notebook file
    ├── .gitignore
    ├── LICENSE
    └── README.md
    

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
