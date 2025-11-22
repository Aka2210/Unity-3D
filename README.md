# Unity 3D 槍戰遊戲專案（GDG On Campus NCKU）
Unity 3D 槍戰類遊戲專案整理筆記，方便未來投履歷 / 面試。

---

# 1. 專案背景與動機

**社團背景：**  
GDG On Campus NCKU（成大軟體開發社 Unity 組）

**專案來源：**  
此專案原本在社團的官方 GitHub 組織開發，之後 fork 到個人帳號作為作品集展示用途。

**專案目的：**
- 練習完整的 Unity 3D 遊戲製作流程  
- 熟悉多人協作（GitHub flow、Issue、分工）  
- 製作一款可展示的 3D 槍戰遊戲 Prototype  
- 練習 C# 遊戲邏輯、角色控制、射擊系統、UI、場景設計  

**為何值得當作品集？**
- 是能「真的遊玩」的成品（Repo readme 提供可執行檔）  
- 涉及多個核心 Unity 技能（角色控制、動畫、碰撞、Raycast、Prefab 管理等）  
- 展示你具備遊戲開發的端到端能力  

---

# 2. 專案概覽

**Repository：**  
Unity-3D（fork from gdg-on-campus-ncku/Unity-3D）

**主要技術：**
- C#：控制角色、武器、彈藥、UI 行為  
- Unity 標準 API：Transform、CharacterController、Input System  
- Prefab 與 Scene 管理  
- ShaderLab / HLSL（依專案需求加入的視覺效果）  

**專案結構：**
Assets/
├── Scripts/ # Player、Weapon、Enemy… 各種遊戲邏輯
├── Prefabs/ # 子彈、角色、敵人、武器等
├── Scenes/ # 場景（主場景、測試場景）
├── Materials/ # 材質
├── UI/ # 遊戲 UI
Packages/
ProjectSettings/


**可執行檔：**  
提供 Google Drive 下載連結，可直接開啟 `Unity_3D.exe` 遊玩。
Google Drive: https://drive.google.com/drive/folders/1y6vEzuYe16lNo7HiYAzUrcorPXpwHn9z?usp=sharing

---

# 3. 遊戲玩法概念（高層設計）

## 視角與操作
- 第一人稱 / 第三人稱視角（依實作）
- WASD 控制移動  
- 滑鼠控制視角  
- 滑鼠左鍵射擊  

## 武器系統
- 基本槍械（步槍 / 手槍）
- 開槍行為由射線（Raycast）或子彈 Prefab 判斷命中
- 子彈數量扣除（UI 顯示）

## 場景設計
- 3D 地圖（建築、庭院、障礙物）
- 掩體、平台、階梯  
- 可放置敵人生成點  

## UI 功能
- 血量條  
- 子彈數量  
- 暫停選單  

---

# 4. 主要腳本說明（依你的 Repo 可再擴寫）

- `PlayerController.cs`  
  - 控制走路、跳躍、轉向、移動速度  
  - 鏡頭控制（Camera look）  

- `GunController.cs`  
  - 開槍、射擊間隔、Reload  
  - 射線偵測判定命中  

- `Bullet.cs`  
  - 子彈飛行軌跡  
  - 命中後銷毀  

- `EnemyAI.cs` 
  - 巡邏 / 追擊玩家  
  - 血量、受傷動畫  

- `GameManager.cs`  
  - 遊戲流程、計分、初始化  

---

# 5. 我在此專案的貢獻（作品集重點）

- 角色控制系統  
- 射擊系統（Raycast 判定、Hit 效果）  
- 建立場景
- UI 設計與功能實作  
- Prefab 模組化（武器、敵人）  
- 協作流程（GitHub 分支、Commit、Issue）

---

# 6. 可執行檔（Demo）

下載連結參照 Repo README。  
Windows 使用者可直接點擊 `Unity_3D.exe` 遊玩。



