# **ESCO 3C 通路深度節能精算器 v3.2.1 (標準版)**

### **(ESCO 3C Retail Deep Energy Saving Calculator \- Standard Edition)**

**專為 3C 連鎖通路打造的離線版決策支援系統**

整合 IPMVP 國際量測驗證標準、台電 113 年最新費率結構 (高壓/低壓累進) 與 ESCO 財務分潤模型。  
本版本為純前端執行版，無須 API Key，無數據上傳風險，適合內部快速評估與客戶端演示。

## **🌟 v3.2.1 版本特色 (Release Highlights)**

### **1\. ⚡ 支援雙軌電價模式 (精準校正)**

針對 3C 通路不同規模的門市，內建 **113 年 4 月 1 日** 公告之最新費率：

* **高壓需量契約 (High Voltage)**:  
  * 適用大型旗艦店。  
  * 精準計算「基本電費（夏月 $223.6/kW）」與「流動電費（尖峰 $5.78/度）」。  
  * 包含時間電價 (TOU) 尖離峰效益模擬。  
* **低壓營業用-累進費率 (Low Voltage Commercial)**:  
  * 適用一般中小型門市。  
  * 模擬 **「累進費率」** 特性，強調節能省下的是最昂貴的級距（夏季最高 **$7.43/度**），計算邊際效益。

### **2\. 🛡️ 高隱私與安全性 (Privacy First)**

* **無 AI 依賴**: 移除外部 AI 連線功能，無需申請或輸入 Google Gemini API Key。  
* **純本機執行**: 所有計算邏輯皆在瀏覽器端完成，輸入的營收與電費數據**絕不上傳**至任何伺服器。  
* **離線可用**: 下載後即便無網路環境（如機房或客戶會議室）也能正常演示。

### **3\. 📊 IPMVP 績效驗證模擬**

* 採用 **IPMVP Option B** 標準公式：$E\_{savings} \= (E\_{baseline} \- E\_{post}) \\pm E\_{adj}$。  
* 提供互動式介面調整基準線與變因（如天氣、營運時數調整）。

### **4\. 💰 ESCO 財務與 ESG 儀表板**

* **財務模型**: 模擬 5 年期現金流，展示 CAPEX 轉 OPEX 後的淨利變化。  
* **ESG 永續**: 依據經濟部係數 (0.495 kg CO2e/kWh) 自動計算減碳量。  
* **SDGs 指標**: 對接 SDG 7 (潔淨能源)、SDG 9 (工業創新)、SDG 12 (責任消費) 與 SDG 13 (氣候行動)。

## **🛠️ 技術架構 (Tech Stack)**

本專案採用現代化前端技術，封裝為**單一 HTML 檔案**：

* **Core**: React 18 (via ESM)  
* **Styling**: Tailwind CSS (CDN)  
* **Charts**: Recharts  
* **Icons**: Lucide React  
* **Compiler**: Babel Standalone (瀏覽器即時編譯 JSX)

## **🚀 快速開始 (Quick Start)**

### **方法一：直接執行 (最簡單)**

1. 下載本專案的 index.html 檔案。  
2. 直接雙擊檔案，使用 Chrome、Edge 或 Safari 瀏覽器開啟。  
3. 開始使用！

### **方法二：部署至 GitHub Pages (推薦)**

若您希望有一個公開網址方便分享給客戶：

1. 將 index.html 上傳至您的 GitHub Repository。  
2. 進入 Repository 的 **Settings** \> **Pages**。  
3. 在 **Build and deployment** \> **Branch** 選擇 main (或 master)。  
4. 儲存後，GitHub 會生成專屬網址 (例如 https://yourname.github.io/esco-calculator/)。

## **📖 操作指南**

1. **設定參數**:  
   * 輸入「單店平均月電費」。  
   * 切換 **\[高壓需量\]** 或 **\[營業用-累進\]** 模式，系統會自動切換對應的費率參數。  
2. **調整節能率**:  
   * 拖拉滑桿設定照明與空調的預期節能比例。  
3. **檢視報表**:  
   * 切換下方分頁查看 **績效驗證**、**財務模型**、**ESG 政策** 與 **SDGs 目標**。  
4. **查閱費率**:  
   * 點擊右上角 **「費率表」**，查看內建的台電 113 年詳細電價表與時間電價定義。

## **📄 免責聲明 (Disclaimer)**

本系統之電費計算基於台電 113 年 4 月公告之費率表進行模擬，實際電費計算可能涉及功率因數調整、超約罰款及流動電費折扣等複雜變因，精確數據請以台電正式帳單為準。本工具僅供節能效益評估參考。

Created with ❤️ for Energy Sustainability.