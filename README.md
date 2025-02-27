# time-series-dataset

整理搜集到的times-series数据集

## ETT
7维数据，OT(油温)为预测目标， h1/h2数据集每小时一点，m1、m2数据集每15min一点
来源：https://github.com/zhouhaoyi/ETDataset/tree/main/ETT-small

## Weather
总共21为数据，OT为预测目标
数据集时间：2020-01-01 00:00:10 - 2021-01-01 00:00:00 每10min一点
引用:  https://gis.cdc.gov/grasp/fluview/fluportaldashboard.html
这个数据集在informer https://arxiv.org/pdf/2012.07436、
 Autoformer https://openreview.net/pdf?id=J4gRj6d5Qm中都有使用

## Traffic
总共862维度 （还需要确认一些论文中引入了哪些维特征，感觉全部使用太多了)
数据集时间：2016/7/1 2:00- 2018/7/2 1:00 每1h一点
引用：http://pems.dot.ca.gov/

## Wind
总共7维数据，target为预测目标
数据集时间：2020-01-01 00:00:00 - 2021-05-22 00:00:00 每10min一点
引用：https://github.com/PaddlePaddle/PaddleSpatial/tree/main/paddlespatial/datasets

## Exchange rate
总共7维数据
数据集时间： 1990/1/1 0:00 - 2010/10/10 0:00 每天一点
引用： Guokun Lai, Wei-Cheng Chang, Yiming Yang, and Hanxiao Liu. Modeling long-and short-term temporal patterns with deep neural networks. In SIGIR, 2018  

## ILI (illness)
总共7维数据
数据集时间：2002-01-01 00:00:00-2020-06-30 00:00:00 每7天1点
引用: https://gis.cdc.gov/grasp/fluview/fluportaldashboard.html

## AirQualityUCI
括号中有GT的是真实值，PT08.S1之类的是传感器的测量值,其括号值为其对什么气体进行采样测量，最后三列是温度、相对湿度和绝对湿度
这里面的数据可以进行拆分，例如选取CO(GT)、PT08.S1(CO)、T、RH、AH五列输入到模型中,即气体真实值、传感器测量值、温度、相对湿度、绝对湿度
引用：https://archive.ics.uci.edu/dataset/360/air+quality
