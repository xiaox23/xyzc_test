# xyzc_test

```
# 检查USB的权限
ls -l /dev/ttyUSB*
crw-rw---- 1 root dialout 188, 1 3月  26 14:07 /dev/ttyUSB1

# 给USB权限
sudo chmod 777 /dev/ttyUSB1

# 再次检查USB权限
ls -l /dev/ttyUSB*
crwxrwxrwx 1 root dialout 188, 1 3月  26 14:07 /dev/ttyUSB1
```

## absolute_move.py
测试绝对移动的脚本。

## calibrate.py
标定脚本，暂未标定。

## control.py
xyzc平台的控制函数。

## get_info.py
获取平台xyzc轴的位置信息，速度信息，判断平台有没有移动。

## home.py
根据不同的输入，让xyzc回到零点。

当输入为`1`时，采用回机械零的方法。

当输入为`2`时，采用回绝对值零的方法。

## absolute_move.py
测试相对移动的脚本，但是相对移动不能为0，不然会出bug。

## move_control.py
育锋的code。