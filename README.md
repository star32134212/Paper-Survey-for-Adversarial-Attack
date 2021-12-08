# 對抗攻擊論文懶人包

## 攻擊類

| 年份 | 出處 | 標題                                                                             | 類型                | 懶人包                                                                     | link                                         |
| ---- | ---- | -------------------------------------------------------------------------------- | ------------------- | -------------------------------------------------------------------------- | -------------------------------------------- |
| 2015 | ICLR | Explaining and Harnessing Adversarial Examples                                   | Attack              | FGSM : 一拳超人攻擊法                                                      | [link](https://arxiv.org/abs/1412.6572)      |
| 2017 | ICLR | Adversarial examples in the physical world                                       | Attack              | IFGSM : FGSM的推廣，用迭代的方式分多步進行擾動，在白箱效果比 FGSM 好       | [link](https://arxiv.org/abs/1607.02533)     |
| 2016 | CVPR | DeepFool: a simple and accurate method to fool deep neural networks              | Attack              | Deepfool : 會算可以擾動成功的最小擾動                                      | [link](https://arxiv.org/pdf/1511.04599.pdf) |
| 2017 |      | Towards Evaluating the Robustness of Neural Networks                             | Attack              | C&W : 與IFGSD一樣的迭代攻擊                                                | [link](https://arxiv.org/abs/1608.04644)     |
| 2014 |      | Intriguing properties of neural networks                                         | Attack              | 以能達到攻擊目的的前提下最小化擾動預算                                     | [link](https://arxiv.org/abs/1312.6199)      |
| 2017 | CVPR | Universal adversarial perturbations                                              | Attack              | 找到一個通用的對抗點，讓他可以對每張圖都達到攻擊效果                       | [link](https://arxiv.org/abs/1610.08401)     |
| 2018 |      | Adversarial Patch                                                                | Attack              | 捨棄以往思路，不在意擾動預算，設計一個可見的擾動，對所有圖片進行無差別攻擊 | [link](https://arxiv.org/abs/1712.09665)     |
| 2019 |      | ShapeShifter: Robust Physical Adversarial Attack on Faster R-CNN Object Detector | Attack              | 對目標檢測器進行攻擊                                                       | [link](https://arxiv.org/abs/1804.05810)     |
| 2019 | ICLR | Adversarial Reprogramming of Neural Networks                                     | Attack              | 擾動原本任務，讓目標模型做指定的簡單任務                                   | [link](https://arxiv.org/abs/1806.11146)     |
| 2018 | CVPR | On the Robustness of Semantic Segmentation Models to Adversarial Attacks         | Attack/圖像語意分割 | 第一個對圖語意分割網路對抗攻擊的效果討論論文                               | [link](https://arxiv.org/abs/1711.09856)     |
| 2018 |      | Spatially Transformed Adversarial Examples                                       | Attack/空間扭曲     | 提出空間扭曲型的擾動例                                                     | [link](https://arxiv.org/abs/1801.02612)     |
| 2019 |      | One pixel attack for fooling deep neural networks                                | Attack/單點攻擊     | 不管預算而專注於一點的攻擊                                                 | [link](https://arxiv.org/abs/1710.08864)     |
|      |      |                                                                                  |                     |                                                                            | [link]()                                     |
## 防禦類


| 年份 | 出處 | 標題                                                                                    | 類型                     | 懶人包                                                                            | link                                     |
| ---- | ---- | --------------------------------------------------------------------------------------- | ------------------------ | --------------------------------------------------------------------------------- | ---------------------------------------- |
| 2017 | SSP  | Distillation as a Defense to Adversarial Perturbations against Deep Neural Networks     | Defense/蒸餾             | 防禦性蒸餾 : 利用一個大參數模型訓練一個小參數模型                                 | [link](https://arxiv.org/abs/1511.04508) |
| 2018 | CVPR | Defense against Adversarial Attacks Using High-Level Representation Guided Denoiser     | Defense/去噪             | PGD&HGD : 去掉擾動再丟進分類器                                                    | [link](https://arxiv.org/abs/1712.02976) |
| 2018 | ICLR | Mitigating Adversarial Effects Through Randomization                                    | Defense/增加隨機層       | 迭代攻擊的遷移性差，若在進入 CNN model 前對圖片做一些隨機處理，就可以防禦迭代攻擊 | [link](https://arxiv.org/abs/1711.01991) |
| 2016 | CVPR | Improving the Robustness of Deep Neural Networks via Stability Training                 | Defense/對抗訓練         | 在Loss function加入了一個穩定度Loss，對大量擾動樣本進行訓練                       | [link](https://arxiv.org/abs/1604.04326) |
| 2017 |      | APE-GAN: Adversarial Perturbation Elimination with GAN                                  | Defense/GAN              | 用GAN將對抗例重構成乾淨的圖片                                                     | [link](https://arxiv.org/abs/1707.05474) |
| 2017 |      | Training Ensembles to Detect Adversarial Examples                                       | Defense/檢測             | 檢測每一張輸入的圖像是不是對抗例                                                  | [link](https://arxiv.org/abs/1712.04006) |
| 2018 |      | Adversarial Defense based on Structure-to-Signal Autoencoders                           | Defense/AE/空間轉換      | 使用一個轉換器做梯度轉換，使原本攻擊者使用的梯度失去參考價值                      | [link](https://arxiv.org/abs/1803.07994) |
| 2018 |      | Adversarial Logit Pairing                                                               | Defense/logit pairing    | 使用 logit pairing 做對抗訓練，在大型資料集可以取得比傳統對抗訓練更好的效果       | [link](https://arxiv.org/abs/1803.06373) |
| 2018 | ICLR | DEFENSE-GAN: PROTECTING CLASSIFIERS AGAINST ADVERSARIAL ATTACKS USING GENERATIVE MODELS | Defense/GAN              | 不用對抗樣本，而是自型添加隨機噪聲來訓練生成器                                    | [link](https://arxiv.org/abs/1805.06605) |
| 2018 | ICLR | Countering Adversarial Images using Input Transformations                               | Defense/探討輸入轉換防禦 | 討論各種輸入轉換防禦法的效果與特性      | [link](https://arxiv.org/abs/1711.00117) |
| 2016 |      | Foveation-based Mechanisms Alleviate Adversarial Examples                               | Defense/凹型機制         | 使用凹型機制來緩解對抗攻擊的效果    | [link](https://arxiv.org/abs/1511.06292) |
|  2017   |   CCS   |     MagNet: a Two-Pronged Defense against Adversarial Examples    | Defense/檢測與重構                 |  提出了MagNet架構過濾掉擾動大的對抗樣本，重構擾動小的樣本讓他變回乾淨樣   | [link](https://arxiv.org/abs/1705.09064)   |
|  2020   |  NIPS    |  On the Trade-off between Adversarial
and Backdoor Robustness  | Defense/防禦平衡                 |  對抗訓練容易被後門攻擊，因此要找一個同時衡量後門攻擊與對抗攻擊的防禦方法  | [link](http://www.cs.nthu.edu.tw/~shwu/pubs/shwu-neurips-20.pdf)    |
|      |      |    | Defense/                 |    | [link]()    |
|      |      |    | Defense/                 |    | [link]()    |
|      |      |    | Defense/                 |    | [link]()    |

## 其他
| 年份 | 出處 | 標題                                              | 類型      | 懶人包                           | link                                     |
| ---- | ---- | ------------------------------------------------- | --------- | -------------------------------- | ---------------------------------------- |
| 2017 |      | Towards Evaluating the Robustness of Neural Networks | 公式推導 | 將求對抗例的過程推導成一個最優化問題 | [link](https://arxiv.org/abs/1608.04644) |
| 2017 |      | Adversarial Example Defenses: Ensembles of Weak Defenses are not Strong | 集成防禦 | 探討集合多個弱的防禦法是否能得到一個強大的防禦法，結論是No | [link](https://arxiv.org/abs/1706.04701) |
| 2018 |  ICLR    | Towards Deep Learning Models Resistant to Adversarial Attacks | 整合 | 將攻擊與防禦的模型合進同一個公式中 | [link](https://arxiv.org/abs/1706.06083) |
| 2017 |      | Intriguing Properties of Adversarial Examples | 對抗樣本產生 | 作者認為對抗樣本是因為logit機率分不具有power law，本身模型就容易被誤分類到第二高概率的label  | [link](https://arxiv.org/abs/1711.02846) |
| 2018 |      | Adversarial Examples: Attacks and Defenses for Deep Learning | 統整型論文 | 整理了近年對抗攻擊與防禦的發展 | [link](https://arxiv.org/abs/1712.07107) |
|  |      |  |  |  | [link]() |
|  |      |  |  |  | [link]() |
