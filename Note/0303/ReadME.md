# 題目:Mini/Micro LED Design and Challenges for Advanced Displays
# 講者:葉志庭
# 日期:2026/03/03
# 筆記內容:
## 一、 技術定義與市場趨勢
### 1. Mini LED 與 Micro LED 的區別
- 定義方式： 通常以晶片尺寸區分，Micro LED 晶片尺寸小於 $100\mu m$，且通常不含藍寶石襯底。
- 應用決策： 選擇 Mini 或 Micro LED 取決於螢幕的「觀看距離」。
### 2. 人眼視覺極限與 PPI 需求
- 解析度邏輯： 螢幕愈小，觀看距離愈近，所需的 PPI (Pixels Per Inch) 愈高。
  * AR 應用： 觀看距離約 $0.5\text{ cm}$，需高達 $17,463 \text{ PPI}$。
  * 手機應用： 觀看距離約 $20\text{ cm}$，需約 $436 \text{ PPI}$。
  * 電視應用： 觀看距離若為 $300\text{ cm}$，僅需約 $29 \text{ PPI}$。
### 3. 顯示技術對比 (LCD vs. OLED vs. Micro LED)
- Micro LED 優勢： 在亮度 (Brightness)、對比度 (Contrast)、厚度 (Thickness) 與耐用性 (Ruggedness) 上表現卓越。
- 主要挑戰： 目前在「成熟度/接受度」以及「成本」方面仍有待優化。


## 二、 製造製程與結構
### 1. Micro LED 生產流程
- 關鍵技術： 包含巨量轉移 (Mass Transfer)、Pick and Place 以及 P to P 鍵合 (bonding)。
- 流程階段：
  1. COW (Chip on Wafer)： 使用 ICP RIE 蝕刻出所需的 Micro LED 晶片尺寸。
  2. COC 1 & 2 (Chip on Carrier)： 透過第一次轉移並使用雷射修阻機 (Laser Trimming) 去除壞點，再進行第二次轉移排列間距。
  3. 巨量轉移： 將晶片移至目標基板（如 LTPS 基板）。
### 2. 全彩化方案對比
- RGB Micro LED： 分別轉移紅、綠、藍三種晶片，修補週期長，良率較低。
- 色彩轉換 (Color Conversion)： 使用藍光 LED 搭配量子點 (QD) 轉換層，僅需轉移藍光晶片，良率較高且波長一致性較佳。


## 三、 進階背光設計 (Mini LED)
### 1. 核心特色
- 高性能指標： 亮度高於 $1000 \text{ nits}$，支持區域控光 (Local Dimming) 功能。
- ZOD (Zero Optical Distance)： 實現超薄化設計，減少光學距離。
### 2. 研究成果：3D 反射杯設計 (車用)
- 使用 Bezier 曲線 優化擴散反射腔列陣 (DRCA)。
- 數學模型： $B(t) = (1-t)^3 P_a + 3(1-t)^2 tP_b + 3(1-t) t^2 P_c + t^3 P_d, t \in [0, 1]$。
- 實測數據： 在 $12.3$ 吋模組中，亮度達到 $23,044 \text{ nits}$，NTSC 色域達 $119.2\%$。
### 3. ZOD 手機與筆電應用
- 手機： 厚度僅 $0.98 \text{ mm}$，功耗 $1.44 \text{ W}$，具備高亮度均勻性 ($92\%$)。
- 筆電： 使用 LGMS 鏡片與 LS 膜，消除暈輪現象 (Halo phenomenon)，厚度僅 $1.7 \text{ mm}$。


## 四、 Micro LED 晶片優化與矽光子應用
### 1. 晶片結構與測量
- 外延結構： 包含 5 對 MQW (多量子阱) 主動層。
- 光電特性： 在 $400 \text{ mA}$ 驅動下，電壓為 $2.9 \text{ V}$，輻射通量為 $112 \text{ mW}$，EQE 約 $10.5\%$。
### 2. HRTF (高反射薄膜) 優化
- 結合介電薄膜與金屬薄膜 (Al, Ag)，優化光分布以達到全角度發光。
- 效果： 提升顏色純度與轉換效率，紅、綠量子點轉換效率分別提升 $1.46$ 與 $1.97$ 倍。
### 3. 矽光子 (Silicon Photonics) 應用
- Micro LED 可應用於「共封裝光學 (CPO)」技術。
- 矽光收發元件六大部件： 光源 (Light Source)、光導 (Light Guide)、調製器 (Modulator)、光電偵測 (Photo-detection)、低成本組裝、智慧化設計。
## 五、 總結
1. 觀看距離決定技術： 根據應用場景的距離決定使用 Mini 或 Micro LED。
2. 超薄與高亮度： 透過 ZOD 技術與 3D 反射杯，實現了超薄 ($< 2 \text{ mm}$) 且超高亮度 ($> 18,000 \text{ nits}$) 的背光模組。
3. 性能提升： 提出 HRTF 與 RCPEF 技術，顯著改善了 Micro LED 的色純度與光轉換效率。
