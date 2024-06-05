# X-Track - 2.0英寸PCB，嘉立创版本
感谢@FASTSHIFT的开源项目X-TRACK
此版本PCB完全基于 [FASTSHIFT/X-TRACK/2.0-inch](https://github.com/FASTSHIFT/X-TRACK/tree/2.0-inch) 版本微调，**但采用嘉立创DEA专业版绘制，元件编号齐全，方便直接下单(PCB/SMT都可以)**

## 硬件改动基本与2.0跟原版的改动一致
* 使用四层PCB，方便走线，PCB厚度 *1.6mm*
* 主控芯片AT32F403ACGU7 QFN48pin6*6**（注意原2.0用的AT32F403ACGT7 LQFP48pin7\*7）**
* 串口线片更换为 *CP2102*
* IMU更换为 *MPU6050*
* 地磁极更换为 *QMC6310* **(换成QMC6310U了，6310没买到)**
* 增加了电池电量计 *BQ27220*, 由于电量计是ROM-Base, 固件需要通过SD卡持久化保存电量计数据
* PCB接口由原来的焊盘更换为 *GH1.25*, 方便安装
* USB接口更换为Type-C( **不再是沉版** )
* 电源网络使用覆铜覆盖( [电池购买 102540](https://item.taobao.com/item.htm?app=chrome&bxsign=scdybBkYjhS5-5wN6dysk3IziPhKZWXZgGFacQ8cdYp3XgbuXY68H2UpQurpck03-k5IlmZOsP6wRgMMGPT8tV7KoYIe0a03DC4bI4G-hk_sLXDxqF7wBt2DzuhyD0ZpnPH&cpp=1&detailSharePosition=interactBar&iconType=commonIconType&id=679383526179&shareUniqueId=27013702763&share_crt_v=1&shareurl=true&short_name=h.gVvMdhO1mEqdpPx&sourceType=item&sp_tk=Um02b1d4UnRwOHA=&spm=a2159r.13376460.0.0&suid=83164451-E75B-4C16-BD19-544A0A6A66BE&tbSocialPopKey=shareItem&tk=Rm6oWxRtp8p%20HU7632&un=1483307b6e540c44bbeeeafdb2768e28&un_site=0&ut_sk=1.YD%20aNlDmIEkDANL%20jX22x9EX_21380790_1717565213234.Copy.1) )
* 充电芯片挪至PCB背面，可以更好的散热
* GPS模块内部集成了LDO, 因此将GPS模块VCC直接接电池减小*3.3v LDO*负载( [HT1818Z3G5L 购买地址](https://item.taobao.com/item.htm?app=chrome&bxsign=scdosPBHz-UC8G3PDpzw40cH0bmWjczDpw3_44dIF3DU62vNtrFfk6ZiGHI7Q5dvnk1NsBADb-W1ibuI2iycRxdT4HAhFRW32S89E_dpgdiLi-rrwlV6ldsrukCDtvIhiVI&cpp=1&detailSharePosition=interactBar&iconType=commonIconType&id=626662626027&shareUniqueId=27013862433&share_crt_v=1&shareurl=true&short_name=h.gVjrzNpXV8kxsoN&sourceType=item&sp_tk=YVBZQ1d4UnJpWEQ=&spm=a2159r.13376460.0.0&suid=E49A966F-1E25-4F27-BA41-2E764F1C5B88&tbSocialPopKey=shareItem&tk=aPYCWxRriXD%20HU9046&un=1483307b6e540c44bbeeeafdb2768e28&un_site=0&ut_sk=1.YD+aNlDmIEkDANL+jX22x9EX_21380790_1717565213234.Copy.1) )
* 充电指示灯挪至边缘

## 注意事项
* 由于地线和电源线均采用覆铜走线，对烙铁焊接不够友好，建议使用 **低温锡膏** 加 **风枪** 方式焊接。
* 焊接最好使用延长排线加长屏幕排线，方便安装进外壳
* *BQ27220* 电量计是可选项，BGA封装对焊接不够友好，新手不推荐安装
