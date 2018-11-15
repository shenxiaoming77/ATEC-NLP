# ATEC-NLP
蚂蚁金服比赛 15th/2632


ATEC比赛是一次让人难忘的比赛，经常看到其他的小伙伴频频上分给自己带来的压力。这对我来说也是一次难得的学习机会，同时也有幸跟很多知名大佬同台竞技，其中的乐趣到现在还怀念。希望有机会能再遇到那些人，再比一次。

比赛的总结写在了博客中 https://blog.csdn.net/cuihuijun1hao/article/details/82318792

目录中的代码很多都是我的尝试代码，以下是各个代码的数据表现

初赛模型 | 线下F1 分数|线上提交
------------ | -------------| -------------
CharAndPinyin.py | 0.52|未尝试
CharAndWord.py | 0.55| 0.638（融合）
RnnCnn.py |0.53|0.61
DSSM.py | 0.33|0.41
xgboost_main.py | 0.27|未尝试


复赛模型  | 测试集分数|线上提交
------------ | -------------| -------------
Siamese+传统特征|0.698|0.7008

复赛模型（DecomposeAtteintion） | 测试集分数|线上提交
------------ | -------------| -------------
cnn-da.py | 0.683|未尝试
decomChar.py |0.685| 未尝试
decomWordChar.py | 0.688|0.7006(单模型)
unique.py | 0.682|未尝试
unique-cnn.py | 0.685|未尝试


注意：DRCN模型测试集分数是从初赛数据中随机挑出3万个数据进行的实验，因为那个时候比赛时
间不多了，线上排队时间太长，所以拿小数据进行了实验。

复赛模型（DRCN） | 测试集分数|线上提交(A榜)|线上提交（B榜）
------------ | -------------| -------------|-------------
2layer.py | 0.591|0.7129（单模型）|0.7218(模型融合)
AE.py |不收敛| 未尝试|未尝试
cos-atten.py | 0.564|未尝试|未尝试
GRU.py | 无记录，但是记得效果不好|未尝试|未尝试
WordChar.py | 0.582|0.7086|未尝试
WordEmbFixed.py|0.546|未尝试|未尝试

注意：DIIN 模型比赛最后一天写的，对应分数都线上训练数据测试集数据。

复赛模型（DIIN） |线上测试集分数
------------ | -------------
char.py | 0.71
fusegate.py |0.64
SelfAtten.py | 0.68
，

模型融合|测试集分数|提交分数
------------ | -------------| -------------
Siamese 传统特征 + Descompose Atten Word Char + DRCN Word + DRCN Char|0.7152|未尝试
Decompose Attention Word Char + DRCN Word + DRCN Char|0.7173|未尝试
DRCN Word+DRCN Char + DIIN Char|0.7242|0.733（最终分数）
DRCN Word+DRCN Char + DIIN Char + Decompose Attention + Siamese 传统特征|未尝试（没来得及）|未尝试

