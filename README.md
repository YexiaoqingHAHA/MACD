# MACD
ifbd

MACD_python 项目程序文件说明
## 文件说明
* initial_data
  + strategies.csv：存储了30个初始化参数
  + config.ini：初始化程序中的所有参数
  + log.conf：日志记录的配置信息
* real_data

  记录实时训练（真实交易）的信息
  + result_data:
    - initial_stocks.csv
    - in_sample_srategies.csv
    - out_sample_srategies.csv
  + mid_data
    - signal.csv
    - pnl.csv
    - return.csv
  + real_signal.csv
  
  记录实时交易的信号
* backtest_data

记录回测情况的信息
  + result_data:
    - initial_stocks.csv
    - in_sample_srategies.csv
    - out_sample_srategies.csv
  + mid_data
    - signal.csv
    - pnl.csv
    - return.csv
* relearning_data

  记录再学习过程中参数的参数
  + stockTrainInfo.csv :记录股票的训练进度
  + parameter_info: 单支股票的训练结果
  
* logs

  日志文件

## 功能说明
* 实时训练（每周股票推荐）： 
  + 参数配置：config.ini---->TrainInfo
    - trainInfoFile=real_data\train_period_index.xlsx : train_period_index.xlsx文件中记录了股票推荐的日期信息，根据这个进行自动训练（需要手动对文件进行管理）
  + 程序执行：py generatedStockRecommendation.py
* 实时信号: 
  + 参数配置：config.ini---->TrainInfo
    - stockStrategyNum
    - step
  + 程序执行：py realSignal.py
* 历史回测：py backtest.py
* 参数再学习：py relearning.py


