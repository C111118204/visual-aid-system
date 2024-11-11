# 小組作業4:

## 繪出系統環境圖 (DFD)
```mermaid
flowchart TD
    使用者 -->|語音輸入/需求導航| 輔助APP
    輔助APP -->|語音回饋| 使用者
    輔助APP -->|獲取位置| GPS系統
    GPS系統 -->|回傳當前位置| 輔助APP
    輔助APP -->|偵測周圍環境| 影像處理系統
    影像處理系統 -->|回傳物體及障礙物資訊| 輔助APP
    輔助APP -->|提供語音提示| 語音系統
    語音系統 -->|播放語音提示| 使用者
    輔助APP -->|啟動導航並提供路徑| 地圖系統
    地圖系統 -->|回傳導航資訊| 輔助APP
```
## 繪製DFD 圖0 (須至少有三項以上的 程序)
```mermaid
flowchart TD
    %% 定義外部實體和資料流
    使用者 -->|請求導航| 輔助APP
    使用者 -->|上傳圖像| 輔助APP
    使用者 -->|回饋| 輔助APP
    
    %% 定義處理程序和資料流
    subgraph DFD 0 圖
        輔助APP -->|位置資訊| 獲取位置處理
        獲取位置處理 --> GPS系統
        GPS系統 -->|回傳當前位置| 獲取位置處理
        獲取位置處理 -->|位置資訊| 導航處理
        
        輔助APP -->|影像資料| 影像處理
        影像處理 -->|物件和障礙物資訊| 整合數據
        導航處理 -->|導航路徑| 整合數據
        整合數據 -->|語音指示| 輔助APP
        
        整合數據 -->|調整導航參數| 使用者回饋處理
        使用者回饋處理 -->|更新導航資料| 輔助APP
    end
    
    %% 定義外部實體
    GPS系統 --> 獲取位置處理
    使用者 -->|語音指示| 輔助APP
```






# test
[example](https://lucid.app/lucidchart/894bf7f1-2374-4871-8ea4-2faefd8ee8a7/edit?shared=true&page=0_0#)  
[example](https://lucid.app/lucidchart/8dedf4c3-5f60-4c8a-b19c-889225e00b1c/edit?shared=true&page=0_0#)  
[test](https://online.visual-paradigm.com/share.jsp?id=333636303635342d31)  
