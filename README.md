# AI Guardian: 結合 Google Edge AI 與 AMB82-mini 的智能實體助理

**團隊成員：** [請填入組員姓名]
**瑞昱科技計畫評審：** ✅ 願意參與[cite: 2]
**使用核心晶片：** AMB82-mini

## 1. 成品概念圖
> （請使用 ChatGPT / Midjourney 生成一張「帶有輪子且外觀有絨毛布料的可愛機器人」圖片，上傳至 github 的 assets 資料夾，並將路徑替換於下方）[cite: 2]

![AI Guardian 成品想像圖](./assets/product_image.png) 

## 2. 核心功能特色
* **視覺推理與尋物**：利用 AMB82-mini 攝影機擷取環境影像，交由 Gemma 模型進行視覺辨識，可執行如「幫我找背包」等語義指令[cite: 1]。
* **自然語音對話**：透過 AMB82-mini 麥克風收音，Gemma 進行語義理解後，由機器人擴音器播放對應回覆與 SD 卡預載情緒音效[cite: 1]。
* **機動巡視與安全防護**：支援前進、後退、轉向等移動控制，並內置紅外線避障與 IMU 防傾倒機制，確保硬體運作安全[cite: 1]。

## 3. 系統架構圖
> （建議可將以下概念使用 draw.io 繪製成圖檔上傳，以符合視覺化需求）[cite: 2]

* **AI 運算層 (Phone/Tablet)**：執行 Google Edge AI App 與 Gemma Agent，處理語音/文字/影像分析，並下達 Robot Tools 動作指令[cite: 1]。
* **通訊層 (Wi-Fi/MCP)**：負責 AI 運算層與實體機器人之間的低延遲資料與指令傳輸[cite: 1]。
* **硬體控制層 (AMB82-mini)**：負責執行 Robot Skill Layer，即時處理相機影像、紅外線測距、麥克風收音、馬達驅動與音訊播放[cite: 1]。
