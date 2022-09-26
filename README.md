# Human-comfort
# Human Comfort

 A human comfort prediction framework for indoor personnel based on time-series analysis

## Steps

-   Please note that, the source code is not provided for the time being, we provide the test executable file of the pre-trained model to verify the achievability of the proposed framework.The source code can be downloaded from the following link：
    链接: https://pan.baidu.com/s/1kpdktb9BGOvzo2uxF_wOoQ?pwd=8cxm 提取码: 8cxm 复制这段内容后打开百度网盘手机App，操作更方便哦
-   After running demotest.exe, the confusion matrix, precision, Macro_F1 and Micro_F1 will be displayed in the console, and the corresponding result graph will be saved in the model and result folder


## Experimental environment

| Environment | Description          |      |
| ----------- | -------------------- | ---- |
| Language    | Python3.6            |      |
| Frame       | tensorflow-gpu1.15.0 |      |
| IDE         | Pycharm              |      |
| Equipment   | CPU and GPU          |      |

## Dataset

We selected the Controlled dataset to verify the performance of the proposed framework. 
[Controlled dataset](https://github.com/jonfranc/occutherm)

Dataset Description
The format of Controlled dataset is CSV. Its data were collected from a nearly year-long indoor environmental control experiment in Pittsburgh, Pennsylvania, USA, in which environmental information, physiological measurements of participants, and subjective feedback on human comfort were collected through a mobile application, and data were collected from the same participant at adjacent moments. The total number of participants in the dataset is 65, the total amount of data is 7313, and the collection time is from 2017-07-18 to 2018-2-13, with variable specific collection time per day, a minimum sampling unit of minutes, and a small sampling interval.



## File Description

| File name        | Description                                                  |      |
| ---------------- | ------------------------------------------------------------ | ---- |
| pycache          | Cached bytecode files                                        |      |
| dataset          | Dataset storage location and newly generated sample datasets when solving class imbalance problem |      |
| model and result | Pretrained model and result storage location                 |      |
| demotest.exe     | test file                                                    |      |

## Comparison experiment

The comparison models chosen for this study are Random Forest (RF),Support Vector Machine (SVM), Long Short-Term Memory network (LSTM) and Bi-directional Long Short-Term Memory (BiLSTM)


| Comparison Algorithm | Epoch | Macro_F1   | Micro_F1（accuracy） |
| -------------------- | ----- | ---------- | -------------------- |
| RF                   | -     | 0.8627     | 0.8761               |
| SVM                  | -     | 0.8222     | 0.8530               |
| LSTM                 | 100   | 0.8901     | 0.9156               |
| BiLSTM               | 100   | 0.9414     | 0.9605               |
| HC-BiLSTM(ours)      | 100   | **0.9482** | **0.9659**           |



