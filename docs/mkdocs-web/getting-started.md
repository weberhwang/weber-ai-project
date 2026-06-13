# MkDocs + Material 入門筆記

## 目標

用 Markdown 建立一個可以本機預覽、未來可部署成靜態網站的知識庫。

## 基本工作流

```text
1. 編輯 .md
2. 執行本機預覽指令
3. 確認網站內容
4. 建置靜態網站
5. 部署或分享
```

## Python 安裝

MkDocs 是 Python 生態系的工具，所以在安裝 MkDocs 之前，需要先確認電腦已經有 Python 和 pip。

### 1. 下載 Python

到 Python 官方網站下載 Windows 安裝程式：

```text
https://www.python.org/downloads/windows/
```

建議下載最新版的 Python 3。

### 2. 執行安裝程式

打開下載好的 Python 安裝程式後，第一個畫面請先勾選：

```text
Add python.exe to PATH
```

這個選項很重要。勾選後，之後才能在 VS Code Terminal、PowerShell 或命令提示字元中直接使用：

```text
python
pip
```

勾選完成後，再點選：

```text
Install Now
```

### 3. 確認 Python 是否安裝成功

安裝完成後，請重新開啟 VS Code Terminal，執行：

```powershell
python --version
pip --version
```

如果成功，會看到 Python 和 pip 的版本資訊。

### 4. 如果 python 指令不能用

有些 Windows 環境會使用 `py` 指令管理 Python。可以改試：

```powershell
py --version
py -m pip --version
```

只要能看到 Python 和 pip 的版本號，就代表 Python 環境可用。

### 5. 安裝 MkDocs 與 Material

確認 Python 和 pip 都可以使用後，安裝 MkDocs：

```powershell
pip install mkdocs mkdocs-material
```

如果你的環境是使用 `py` 指令，則改用：

```powershell
py -m pip install mkdocs mkdocs-material
```

## 常用指令

本機預覽網站：

```powershell
mkdocs serve
```

建置正式靜態網站：

```powershell
mkdocs build
```
## 部署網站到 GitHub
```
git add .
git commit -m "Update docs"
git push
mkdocs gh-deploy
```
https://weberhwang.github.io/weber-ai-project/