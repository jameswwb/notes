## 下载数据
1. 启动服务器

```
进入目录：
.\Gitee\VNMod\vnpy\zzmod\dataclaw
启动服务器：
python web_clawhost.py
```

2. 创建任务列表 in.txt

```
任务list： .\ClawWork\list
添加修改所需的任务列表到in.txt， 品种，频率，时间
把in.txt 拖入 .\ClawWork\cmd
```

3. 创建RQ策略 rq_code_003_jqOK.py， G1-G6

```
修改外网ip和端口号，run策略
```

## 导入数据

1. 启动vnpy cmd。

```
拷贝数据到目录 .\vnpy\zzmod\dataext\csv2db， 把数据解压缩到本路径
cmd 进入目录：
.\VNMod\vnpy\zzmod\dataext
设置当前环境变量，cmd下执行： set_python_path.bat
执行 python csv2db.py
```