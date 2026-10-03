# 🤖 Robo-Advisor: Modern Portfolio Theory (MPT) Analysis

本專案為金融科技 (Fintech) 課程分析實作，模擬理財機器人 (Robo-Advisor) 的底層運算邏輯。透過 Python 自動抓取真實金融市場歷史數據，建構投資組合機會集合 (Portfolio Opportunity Set)，並利用蒙地卡羅模擬法 (Monte Carlo Simulation) 找出最小變異投資組合 (Minimum Variance Portfolio, MVP)，提供量化的資產配置建議。

## 📊 專案亮點與核心功能

*   **自動化數據獲取**：整合 `yfinance` API，自動抓取 5 檔涵蓋不同風險特性之資產（科技股、大盤、公債、黃金、不動產）過去 5 年的每日調整後收盤價。
*   **風險與報酬量化分析**：計算各資產之年化報酬率、年化波動率，並建構共變異數矩陣 (Covariance Matrix) 與相關係數矩陣 (Correlation Matrix) 熱力圖。
*   **投資組合最適化**：隨機生成 10,000 組投資組合權重，繪製風險-報酬散佈圖 (Opportunity Set)。
*   **數據自動渲染**：程式執行完畢後，自動擷取運算結果並渲染出一份排版整齊的 Markdown 分析報告。

## 🛠️ 技術棧 (Tech Stack)

*   **開發環境**：Python 3, Jupyter Notebook (`.ipynb`)
*   **數據分析**：`pandas`, `numpy`
*   **金融數據**：`yfinance`
*   **視覺化**：`matplotlib`, `seaborn`

## 📂 資產配置標的

為驗證分散投資 (Diversification) 之效益，本專案選定以下 5 檔具備低/負相關性潛力的資產：
1.  **AAPL** (Apple Inc.)：代表個別科技股
2.  **SPY** (SPDR S&P 500 ETF)：代表美國大型股大盤
3.  **TLT** (iShares 20+ Year Treasury Bond ETF)：代表避險固定收益
4.  **GLD** (SPDR Gold Shares)：代表實體商品與抗通膨資產
5.  **VNQ** (Vanguard Real Estate Index Fund)：代表不動產市場

## 🚀 快速啟動 (How to Run)

1.  **複製專案**
    ```bash
    git clone [https://github.com/Dese-Mind/Fintech-HW-Week4.git](https://github.com/Dese-Mind/Fintech-HW-Week4.git)
    cd Fintech-HW-Week4
    ```
2.  **安裝依賴套件**
    ```bash
    pip install yfinance pandas numpy matplotlib seaborn jupyter
    ```
3.  **執行分析**
    使用 VS Code 或 Jupyter 環境開啟 `assignment2.ipynb`，依序執行所有程式碼區塊 (Run All)，即可在本地端重現完整的分析結果與視覺化圖表。
