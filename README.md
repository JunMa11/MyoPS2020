# MyoPS2020
Code of the solution to MyoPS 2020

![Pipeline](https://github.com/JunMa11/MyoPS2020/blob/main/Pipeline.PNG)

## Train

Prepare [nnUNet format](https://github.com/MIC-DKFZ/nnunet/blob/master/documentation/dataset_conversion.md) data

for FOLD in `[0,1,2,3,4,5]`

- Whole LV segmentation
`nnUNet_train 2d nnUNetTrainerV2 400 FOLD`

- Scars segmentation
`nnUNet_train 2d nnUNetTrainerV2 401 FOLD`

- Edema + scars segmentation
`nnUNet_train 2d nnUNetTrainerV2 402 FOLD`


## Inference

Download trained models here (PW: 2021)

- Whole LV segmentation
`nnUNet_predict -i input_path -o output_path -m 2d -t 400`

- Scars segmentation
`nnUNet_predict -i input_path -o output_path -m 2d -t 401`

- Edema + scars segmentation
`nnUNet_predict -i input_path -o output_path -m 2d -t 402`

