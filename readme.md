# Linux-Add-Fonts

## 字体准备

下载所需要的字体文件：***.ttf文件

**安装方法**：

（1）本repo下提供Times New Roman的ttf文件

（2）window系统下的’C:\Windows\Fonts‘可以找到其他字体

（3）http://xiazaiziti.com/

## 字体安装

通过python查看matplotlib字体缓存和字体安装路径

```Python
import matplotlib as mpl
print(mpl.get_cachedir())
print(mpl.matplotlib_fname())
>>/home/user/.cache/matplotlib
>>/home/user/anaconda3/envs/python/lib/python3.10/site-packages/matplotlib/mpl-data/matplotlibrc
```

将.ttf文件复制到： **/home/user/anaconda3/envs/python/lib/python3.10/site-packages/matplotlib/mpl-data/matplotlibrc/fonts/ttf**中。

接下来，清楚matplotlib缓存：

```bash
rm -rf /home/user/.cache/matplotlib
```

## 在matplotlib中使用字体

```python
import matplotlib.pyplot as plt
plt.rcParams['font.family'] = 'Times New Roman'
```