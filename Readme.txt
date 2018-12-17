
Libraries required: PyTorch & OpenCV

Training the GAN architecture:

The following command needs to be run in the terminal:

VGG-19 weight file is also required for the content loss. As this file is above 500 MB, we are providing the download link:

Download VGG-19 weights: https://download.pytorch.org/models/vgg19-dcbb9e9d.pth

python CartoonGAN.py --name your_project_name --src_data src_data_path --tgt_data tgt_data_path --vgg_model pre_trained_VGG19_model_path


The Input Data needs to be saved in this hierarchy.

├── data
│   ├── src_data # src data (not included in this repo)
│   │   ├── train 
│   │   └── test
│   └── tgt_data # tgt data (not included in this repo)
│       ├── train 
│       └── pair # edge-promoting results to be saved here
│
├── CartoonGAN.py # training code
├── edge_promoting.py
├── utils.py
├── networks.py
└── name_results # results to be saved here

Testing the GAN architecture:

The testing of the GAN network can be run from the trained model after 100 epochs.

python test.py --input_dir images --style Danbooru --gpu 0







