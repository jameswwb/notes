## Window 安装环境

1. office
2. 7z
3. mpv
4. everything
5. beyond compare
6. git
7. github desktop
8. tortoisegit
9. ultraedit
10. leevpn



## vnpy 安装环境

1. 安装anaconda

```
安装 Anaconda2-5.2.0-Windows-x86.exe  （所有option 全部disable）
pip install -r requirements.txt
pip install distributed
pip install grin
python -m pip install --upgrade pip
pip install TA_Lib-0.4.17-cp27-cp27m-win32.whl
```

2. vscode 设置

```
vnpy27.code-workspace - office
{
	"folders": [
		{
			"path": "vnpy"
		}
	],
	"settings": {
		"python.pythonPath": "D:\\Anaconda2\\python.exe",		
		"python.linting.pylintEnabled": true,
		"terminal.integrated.env.windows": {
			"PYTHONPATH":"F:\\Gitee\\VNMod\\vnpy;F:\\Gitee\\VNMod\\vnpy\\vnpy\\trader\\app\\algoTrading\\algo;F:\\Gitee\\VNMod\\vnpy\\vnpy\\trader\\app\\ctaStrategy\\strategy"
		}
	},
}
```

3. 乱码问题
cmd terminal : chcp 65001