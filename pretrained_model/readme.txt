首先运行data_prepare.ipynb，对原数据进行加工处理，生成后续的可用于模型加工的格式

其次进行模型训练，以命令行形式运行train.py文件，读取之前加工好的数据，输出训练好的模型
因clip模型的基学习器有两种选择，有如下两种形式
Train with fine-tuning of GPT2:
python train.py --data ./data/coco/oscar_split_ViT-B_32_train.pkl --out_dir ./coco_train/
Train only transformer mapping network:
python train.py --only_prefix --data ./data/coco/oscar_split_ViT-B_32_train.pkl --out_dir ./coco_train/ --mapping_type transformer  --num_layres 8 --prefix_length 40 --prefix_length_clip 40

predict.ipynb文件用于加载训练好的模型，并对模型结果使用评价指标进行评价。
