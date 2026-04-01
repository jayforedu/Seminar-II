# 題目:如何打造台版 Edge Impulse TinyML 開發平台
# 講者:許哲豪
# 日期:2026/03/31
# 筆記內容:
這次參加院上（電機資訊學院）舉辦的專題演講，由 Edge AI Taiwan 的許哲豪（Jack Hsu）講師帶來關於打造台版 Edge Impulse TinyML 開發平台的分享，讓我對邊緣運算與微型機器學習（TinyML）有了更深一層的體悟。平時在處理深度學習或電腦視覺模型時，往往習慣依賴如 RTX 4060 等高效能 GPU 來進行高強度的平行運算與模型訓練。然而，這場演講徹底翻轉了我的視角，將焦點帶到了資源極度受限的微控制器（MCU）領域。

演講一開始清楚點出了「邊緣智慧」與「雲端生成智慧」的根本差異。比起雲端龐大的算力與無限資源，TinyML 強調在極小模型與超低功耗下，完成聲音、影像或感測器的 AI 推論。這讓我聯想到，未來若要將影像辨識或是機器人導航（如 ROS 系統結合感測器）真正落地到輕量級的邊緣裝置上，硬體的算力牆與記憶體牆是首要跨越的障礙。講師詳細梳理了各大廠的 MCU 與 NPU 架構，如 Arm Cortex-M 系列與 Ethos-U 加速器，甚至介紹了奇景、新唐、瑞昱等台灣本土大廠的開發板，讓我對國產硬體在 Edge AI 生態系中的發展潛力感到相當振奮。

此外，演講深入探討了 Edge Impulse 這個強大的平台，它提供了從資料收集、模型訓練、EON 模型優化到最終部署的端到端（End-to-End）解決方案。在模型優化方面，要在 SRAM 與 Flash 容量極小的 MCU 上運行 AI，模型壓縮技術至關重要。正如 Ray（2022）在其回顧研究中指出，TinyML 的核心挑戰在於如何在資源受限的物聯網設備上執行機器學習模型，這需要演算法與硬體的深度協同設計。為了達到此目標，量化（Quantization）與剪枝（Pruning）是不可或缺的技術。Jacob 等人（2018）提出的純整數運算量化技術，便是讓複雜的神經網路得以在不支援浮點運算的邊緣設備上高效運行的關鍵，這與演講中提到使用 TensorFlow Lite (LiteRT) 進行模型轉換的概念不謀而合。

最後，講師提到了自建平台會遇到的技術痛點，包含硬體算子相容性與利用自動化機器學習（AutoML）尋找最佳網路結構（NAS）。這呼應了 Lin 等人（2020）提出的 MCUNet 架構，其透過 TinyNAS 與 TinyEngine 的結合，能夠針對特定 MCU 的嚴苛記憶體限制，自動搜索並編譯出最佳的神經網路架構。這次的演講不僅補足了我在邊緣部署上的知識缺口，更讓我深刻意識到，未來在進行演算法設計時，除了追求模型的準確率，更應將模型的輕量化與終端硬體的落地可行性納入綜合考量。
# 參考文獻
Jacob, B., Kligys, S., Chen, B., Zhu, M., Tang, M., Howard, A., Adam, H., & Kalenichenko, D. (2018). Quantization and training of neural networks for efficient integer-arithmetic-only inference. Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition, 2704–2713. https://doi.org/10.1109/CVPR.2018.00286

Lin, J., Chen, W.-M., Lin, Y., Cohn, J., Gan, C., & Han, S. (2020). MCUNet: Tiny deep learning on IoT devices. Advances in Neural Information Processing Systems, 33, 11711–11722.

Ray, P. P. (2022). A review on TinyML: State-of-the-art and prospects. Journal of King Saud University - Computer and Information Sciences, 34(4), 1595–1623. https://doi.org/10.1016/j.jksuci.2021.11.019
