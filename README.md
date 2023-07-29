# ccurent
一个电流控制模块，对电流进行修改且去除mi_thermal文件的模块。（测试机型：K50ultra、k60pro，理论可行机型：miui-120W（非120W需要修改电流参数））
#
## 主要原理
控制电流，实现电流的合理陡降和缓降。
带日志版本：电流实时大小写入日志文件为/data/adb/modules/charge/log.txt，便于查看当前写入状态。
#
## 电流放置方案
夏日模式：0
夏日电流控制规则为，40度以下13A，40到44度电流用一个二次函数来拟合，44度到46度7.5A，46到49度用一个二次函数拟合，49度以上0A。
![F554B200AC54C64FB75E1F12BFFDE404](https://user-images.githubusercontent.com/86546035/224915630-2793d2f3-3ee1-4c3b-818a-63096a54b2fe.jpg)
![9E04FD32509AA3A43008004AC0896A03](https://user-images.githubusercontent.com/86546035/224915650-bd27ad0e-8f0d-42a2-9777-0ad0e789bb19.jpg)

冬日模式：1。
夏日电流控制规则为，40度以下20A，40到44度电流用一个二次函数来拟合，44度到46度7.5A，46到49度用一个二次函数拟合，49度以上0A。


