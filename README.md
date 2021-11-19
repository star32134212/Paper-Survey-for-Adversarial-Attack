# 對抗攻擊論文懶人包

## 攻擊類

| 年份 | 出處 | 標題                                              | 類型      | 懶人包                           | link                                     |
| ---- | ---- | ------------------------------------------------- | --------- | -------------------------------- | ---------------------------------------- |
| 2015 |   ICLR   | Explaining and Harnessing Adversarial Examples | Attack | FGSM : 一拳超人攻擊法 | [link](https://arxiv.org/abs/1412.6572) |
| 2017 |   ICLR   | Adversarial examples in the physical world | Attack | IFGSM : FGSM的推廣，用迭代的方式分多步進行擾動，在白箱效果比 FGSM 好 | [link](https://arxiv.org/abs/1607.02533) |
| 2016 | CVPR | DeepFool: a simple and accurate method to fool deep neural networks  | Attack | Deepfool : 會算可以擾動成功的最小擾動 | [link](https://arxiv.org/pdf/1511.04599.pdf) |
| 2017 |  | Towards Evaluating the Robustness of Neural Networks | Attack | C&W : 與IFGSD一樣的迭代攻擊 | [link](https://arxiv.org/abs/1608.04644) |
| 2014 |  | Intriguing properties of neural networks | Attack | 以能達到攻擊目的的前提下最小化擾動預算 | [link](https://arxiv.org/abs/1312.6199)|
| 2017 | CVPR | Universal adversarial perturbations  | Attack | 找到一個通用的對抗點，讓他可以對每張圖都達到攻擊效果 | [link](https://arxiv.org/abs/1610.08401)|
| 2018 |  | Adversarial Patch | Attack | 捨棄以往思路，不在意擾動預算，設計一個可見的擾動，對所有圖片進行無差別攻擊 | [link](https://arxiv.org/abs/1712.09665)|
| 2019 |  | ShapeShifter: Robust Physical Adversarial Attack on Faster R-CNN Object Detector | Attack | 對目標檢測器進行攻擊 | [link](https://arxiv.org/abs/1804.05810)|
| 2019 | ICLR | Adversarial Reprogramming of Neural Networks | Attack | 擾動原本任務，讓目標模型做指定的簡單任務 | [link](https://arxiv.org/abs/1806.11146)|
|  |  |  |  |  | [link]()|
|  |  |  |  |  | [link]()|

## 防禦類


| 年份 | 出處 | 標題                                              | 類型      | 懶人包                           | link                                     |
| ---- | ---- | ------------------------------------------------- | --------- | -------------------------------- | ---------------------------------------- |
| 2017 |  SSP  |  Distillation as a Defense to Adversarial Perturbations against Deep Neural Networks | Defense/蒸餾 | 防禦性蒸餾 : 利用一個大參數模型訓練一個小參數模型 | [link](https://arxiv.org/abs/1511.04508) |
| 2018 |  CVPR    | Defense against Adversarial Attacks Using High-Level Representation Guided Denoiser | Defense/去噪 | PGD&HGD : 去掉擾動再丟進分類器 | [link](https://arxiv.org/abs/1712.02976) |
| 2018 |  ICLR    | Mitigating Adversarial Effects Through Randomization | Defense/增加隨機層 | 迭代攻擊的遷移性差，若在進入 CNN model 前對圖片做一些隨機處理，就可以防禦迭代攻擊 | [link](https://arxiv.org/abs/1711.01991) |
| 2016 |  CVPR    | Improving the Robustness of Deep Neural Networks via Stability Training | Defense/對抗訓練 | 在Loss function加入了一個穩定度Loss，對大量擾動樣本進行訓練 | [link](https://arxiv.org/abs/1604.04326) |
| 2017 |      | APE-GAN: Adversarial Perturbation Elimination with GAN | Defense/GAN | 用GAN將對抗例重構成乾淨的圖片 | [link](https://arxiv.org/abs/1707.05474) |
| 2017 |      | Training Ensembles to Detect Adversarial Examples | Defense/檢測 | 檢測每一張輸入的圖像是不是對抗例 | [link](https://arxiv.org/abs/1712.04006) |
| 2018 |      | Adversarial Defense based on Structure-to-Signal Autoencoders | Defense/AE/空間轉換 | 使用一個轉換器做梯度轉換，使原本攻擊者使用的梯度失去參考價值 | [link](https://arxiv.org/abs/1803.07994) |
| 2018 |      | Adversarial Logit Pairing | Defense/logit pairing | 使用 logit pairing 做對抗訓練，在大型資料集可以取得比傳統對抗訓練更好的效果 | [link](https://arxiv.org/abs/1803.06373) |
|2018 |   ICLR   | DEFENSE-GAN: PROTECTING CLASSIFIERS AGAINST ADVERSARIAL ATTACKS USING GENERATIVE MODELS | Defense/GAN | 不用對抗樣本，而是自型添加隨機噪聲來訓練生成器 | [link](https://arxiv.org/abs/1805.06605) |
|  |      |  | Defense/ |  | [link]() |

## 其他
| 年份 | 出處 | 標題                                              | 類型      | 懶人包                           | link                                     |
| ---- | ---- | ------------------------------------------------- | --------- | -------------------------------- | ---------------------------------------- |
| 2017 |      | Towards Evaluating the Robustness of Neural Networks | 公式推導 | 將求對抗例的過程推導成一個最優化問題 | [link](https://arxiv.org/abs/1608.04644) |
|  |      |  |  |  | [link]() |
