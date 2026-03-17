# 題目:The Development and Applications of BioImpedance Technology
# 講者:鄭國順
# 日期:2026/03/17
# 筆記內容:
這場演講最令我震撼之處，在於見證了基礎物理法則如何透過現代演算法，轉化為守護生命的精確影像。鄭教授從十九世紀的歐姆定律 $V=IR$ 談起，將看似簡單的導電性測量，延伸至複雜的生物阻抗技術（Bioimpedance Technology）。這種從底層原理推導至高端應用的邏輯，展現了生醫工程「化簡為繁，再化繁為簡」的深度美學。

在臨床應用的反思上，電氣阻抗斷層掃描（EIT）的發展令人印象深刻。傳統影像醫學如 CT 或 MRI 雖然精確，但在加護病房（ICU）中卻面臨無法移動與輻射風險的限制。EIT 具備無輻射、即時且可床邊監測的特性，真正解決了臨床上對於肺部功能動態監控的渴望。尤其在調整呼吸器 PEEP 設定或觀察肺部灌流時，這種「即時性」提供的資訊是無價的，能讓醫師在不傷害病患的前提下，做出最科學的醫療決策。

更令我感興趣的是演講後半段關於人工智慧的導入。在處理 EIT 的逆問題（Inverse Problem）時，傳統演算法往往難以精準分離重疊的生理信號。鄭教授團隊提出的 Semi-Siamese U-Net 架構，不僅展現了深度學習在醫學影像分離上的巨大潛力，更透過實驗證明了其在心臟與肺部影像重構上的卓越表現，其 DICE 係數分別達到了 93.56% 與 98.84%。這不.僅是技術上的突破，更象徵著 AI 已經從單純的輔助工具，進化為能夠克服物理量測限制、提升診斷品質的核心引擎。

整體而言，這場演講讓我體悟到，生醫工程師的角色不只是開發工具，更是要透過創新的思維（如權重損失函數的優化），在物理極限與臨床需求之間搭建橋樑。這種跨學科的整合——結合電子工程的量測、生理學的判讀與電腦科學的運算——正是未來精準醫療的核心價值所在。看到教授的研究成果不僅發表於國際期刊，更能實際應用於真實人體數據分析，這份將理論轉化為臨床價值的嚴謹與熱忱，確實令人深感佩服。

# 關鍵字:
BioImpedance Technology, Electrical Impedance Tomography, Ohm’s Law, Inverse Problem, Deep Learning, Semi-Siamese U-net

# 參考文獻:
Azad, R., Aghdam, E. K., Rauland, A., et al. (2022). Medical image segmentation review. arXiv. https://arxiv.org/abs/2211.14830v1

Ko, Y.-F., & Cheng, K.-S. (2021). A semi-Siamese U-Net for separating heart and lung impedance images. PLOS ONE, 16(2), e0246071. https://doi.org/10.1371/journal.pone.0246071

R. P. Henderson and J. G. Webster, "An Impedance Camera for Spatially Specific Measurements of the Thorax," in IEEE Transactions on Biomedical Engineering, vol. BME-25, no. 3, pp. 250-254, May 1978, doi: 10.1109/TBME.1978.326329.