# Jupyter-download-problem-solution

**需要以系統管理員執行**

因路徑限制直接在cmd打指令會錯誤，改用虛擬環境減少路徑長度  

**用虛擬環境安裝**  
cd C:\  # 切換到根目錄

python -m venv jupyterenv

C:\jupyterenv\Scripts\activate

pip install jupyter

**更新 Jupyter 相關套件（推薦，排除潛在 Bug）：**  
pip install --upgrade jupyter notebook jupyterlab

**生成 Jupyter 配置文件（如果尚未生成）：**  
jupyter notebook --generate-config (可以直接找找看)

**文件頂部導入OS：**  
import os
在C:\\Users\\使用者名稱加入文件夾temp_jupyter_runtime_data

在文件底部添加 c.ServerApp.runtime_dir = "C:\\Users\\使用者名稱\\temp_jupyter_runtime_data"
找到
c.ServerApp.use_redirect_file = True 並改成 c.ServerApp.use_redirect_file = False

**(.bat檔可放桌面)用.bat檔開啟時需要右鍵->以系統管理員執行**  
**手動啟動**  
cd C:\  
C:\jupyterenv\Scripts\activate   
jupyter notebook

**requirements為常用套件**  
可以在虛擬環境內安裝，之後的project都可使用，須先把檔案放到路徑中   
在cmd cd 到對應的路徑輸入：  
pip install -r requirements.txt


