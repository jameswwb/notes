## vnpy 运行

1. 账号配置

```
申请simnow 账号， 配置交易服务器和行情服务器地址。
.\vnpy\trader\gateway\ctpGateway\CTP_connect.json
{
    "brokerID": "9999", 
    "mdAddress": "tcp://180.168.146.187:10010", 
    "tdAddress": "tcp://180.168.146.187:10000", 
    "userID": "132654",
    "password": "Gemalto,123"    
}
```
2. 策略配置

```
.\vnpy\trader\app\ctaStrategy\CTA_setting.json
[
    {
        "name": "king keltner",
        "className": "KkStrategy",
        "vtSymbol": "rb1905"
    }
]
```



## vnpy 安装环境

1. 安装anaconda

```
安装 Anaconda2-5.2.0-Windows-x86.exe  （所有option 全部disable）
pip install -r requirements.txt
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




































1. 创建虚拟环境

> set CONDA_FORCE_32BIT=1

```
# 创建 conda 虚拟环境（ :code:`env_name` 是您希望创建的虚拟环境名）
$ conda create --name env_name python=3.5

# 如您想创建一个名为vnpy27的虚拟环境
$ conda create --name vnpy27 python=2.7

# 使用 conda 虚拟环境
$ source activate env_name
# 如果是 Windows 环境下 直接执行 activcate
$ activate env_name

# 退出 conda 虚拟环境
$ source deactivate env_name
# 如果是 Windows 环境下 直接执行 deactivate
$ deactivate env_name

# 删除 conda 虚拟环境
$ conda-env remove --name env_name
```

2. 更新pip和setup tool

```
python -m pip install --upgrade pip
pip install -U pip setuptools cython -i https://pypi.douban.com/simple
```

3. install bcolz & line_profiler & TA_Lib

```
pip install C:\Users\LL\Downloads\bcolz-1.2.1-cp35-cp35m-win_amd64.whl
pip install C:\Users\LL\Downloads\line_profiler-2.1.2-cp35-cp35m-win_amd64.whl
pip install C:\Users\LL\Downloads\TA_Lib-0.4.17-cp35-cp35m-win_amd64.whl
```

4. install RQalpha

```
pip install -i https://pypi.douban.com/simple rqalpha
rqalpha version
```

5. 获取回测数据

```
rqalpha update-bundle
```

6. 策略回测

```
rqalpha run -f C:\ProgramData\Anaconda3\envs\rqalpha\Lib\site-packages\rqalpha\examples\buy_and_hold.py -d C:\Users\LL\.rqalpha\bundle -s 2016-06-01 -e 2016-12-01 --account stock 100000 --benchmark 000300.XSHG

rqalpha run -f C:\ProgramData\Anaconda3\envs\rqalpha\Lib\site-packages\rqalpha\examples\ex_mark.py -d C:\Users\LL\.rqalpha\bundle -s 2015-01-01 -e 2018-12-31 --account stock 100000 --plot
```


set pythonpath=C:\ProgramData\Anaconda3\envs\vnpy27\Lib\site-packages\vnpy-1.9.2-py2.7.egg\vnpy\trader\app\algoTrading\algo;C:\ProgramData\Anaconda3\envs\vnpy27\Lib\site-packages\vnpy-1.9.2-py2.7.egg\vnpy\trader\app\ctaStrategy\strategy






conda-env remove --name vnpy27

> set CONDA_FORCE_32BIT=1

conda create --name vnpy27 python=2.7

conda create -n vnpy27 python=2.7

pip install -r requirements.txt
pip install TA_Lib-0.4.17-cp27-cp27m-win32.whl
pip install PyQt4-4.11.4-cp27-cp27m-win32.whl
pip install PySide-1.2.4-cp27-cp27m-win32.whl
pip install enum
pip install typing
pip install zmq
pip install python-qt5

乱码问题
cmd terminal : chcp 65001


vnpy27.code-workspace - office
{
	"folders": [
		{
			"path": "vnpy"
		}
	],
	"settings": {
		"python.pythonPath": "C:\\ProgramData\\Anaconda3\\envs\\vnpy27\\python.exe",		
		"python.linting.pylintEnabled": true,
		"terminal.integrated.env.windows": {
			"PYTHONPATH":"F:\\Gitee\\VNMod\\vnpy;F:\\Gitee\\VNMod\\vnpy\\vnpy\\trader\\app\\algoTrading\\algo;F:\\Gitee\\VNMod\\vnpy\\vnpy\\trader\\app\\ctaStrategy\\strategy"
		}
	},
}
