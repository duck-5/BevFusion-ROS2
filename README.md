To execute the docker:

docker run -it -v ${PWD}/mmdet3d:/mmdetection3d/mmdet3d -v ${PWD}/models:/mmdetection3d/models --net host --gpus all -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix valohai/mmdetection3d:0.3 bash


To run the demo:
python3 projects/BEVFusion/setup.py develop
`export CHECKPOINT_FILE=models/bevfusion_converted.pth`

python projects/BEVFusion/demo/multi_modality_demo.py demo/data/nuscenes/n015-2018-07-24-11-22-45+0800__LIDAR_TOP__1532402927647951.pcd.bin demo/data/nuscenes/ demo/data/nuscenes/n015-2018-07-24-11-22-45+0800.pkl projects/BEVFusion/configs/bevfusion_lidar-cam_voxel0075_second_secfpn_8xb4-cyclic-20e_nus-3d.py ${CHECKPOINT_FILE} --cam-type all --score-thr 0.2 --show


Required:
mmcvfind . -type f -size +100M
demo (for data)

configs  dataset-index.yml  demo  mmcv  mmdet3d  mmdet3d.egg-info  model-index.yml  models  projects  requirements.txt  setup.cfg  setup.py


dataset-index.yml  demo  mmcv  mmdet3d mmdet3d.egg-info  model-index.yml  models  projects  requirements.txt  setup.cfg  setup.py


mmcv
