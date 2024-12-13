# MT_systemなどの異常検知手法について
正常データを用いた判別器生成モデル

* 以下の各モデルは、正常データにより判別器を生成し、異常値の判定を行う

| モデル                        | データ分布             | 特徴                                                                       | 
| ----------------------------- | ---------------------- | -------------------------------------------------------------------------- | 
| MT法                          | 正規分布               | マハラノビス距離に変換することで、異常値の閾値を設定                       | 
| LOF(局所外れ値度)               | 非正規分布             | k-最近傍法をベースにして、正常データ群での凝集度を考慮した距離を算出することで異常値を識別する | 
| PCA(主成分分析)による異常検知 | 変数間の関係が線形関係 | 正常データからPCAにより正常部分空間を作り、そこからの復元データとの誤差値に基づいて判別する。                  | 

## MT法
* pythonコード1:
  * [mahalanobis-taguchi-method.ipynb](https://github.com/yoshi-cow/MT_system/blob/main/mahalanobis-taguchi-method.ipynb)
* pythonコード2(SN比の説明含む):
  * [SN_ratio_in_MT_method.ipynb](https://github.com/yoshi-cow/MT_system/blob/main/SN_ratio_in_MT_method.ipynb) 

## LOF(局所外れ値度) 
* 概要:
  * [LOF_explaining_theory.ipynb](https://github.com/yoshi-cow/MT_system/blob/main/LOF_explaining_theory.ipynb)
* pythonコード:
  * [LOF_code_example.ipynb](https://github.com/yoshi-cow/MT_system/blob/main/LOF_code_example.ipynb)

## PCAによる異常検知
* 概要:
  * [PCA_Anomaly_Detection_Explanation.ipynb](https://github.com/yoshi-cow/MT_system/blob/main/PCA_Anomaly_Detection_Explanation.ipynb)
* pythonコード:
  * [PCA_Anomaly_Detection_sample_code.ipynb](https://github.com/yoshi-cow/MT_system/blob/main/PCA_Anomaly_Detection_sample_code.ipynb)
