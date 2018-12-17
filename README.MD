## Requirements
- Keras >= 2.0 (upgrade Keras to lastest version with: `sudo pip install git+git://github.com/fchollet/keras.git --upgrade`) (used 2.0.3)
- Tensorflow >= 1.0 (used 1.1.0)

## Download dataset
- Download datafrom from: http://rpg.ifi.uzh.ch/davis_data.html 
- Unzip and copy to **/event_data/raw_data** foler (see dataset_location_1.png, dataset_location2.png)

## Create train/test data
- `cd dataset_script`
- `python CREATE_DATA.py`
- change **list_scene** inside **CREATE_DATA.py** for other scene

## Run train script:
- `cd main_keras`
- `python train.py --gpu GPU_ID --scene SCENCE_ID` 
- For example: `python train.py --gpu 0 --scene shapes_rotation`     --> will train on GPU 0 and shapes_rotation sequence

## Predict & evaluate
- `cd main_keras`
- `python predict.py`
- Change **in_scene_id**, **in_net_id**, **in_model_file_name** in this file for different scene