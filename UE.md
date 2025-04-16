# 一.Dedicated Server启动参数

## 基本参数

1. -server: 以服务器模式运行
2. -log: 启用日志记录
3. -stdout: 将日志输出到标准输出
4. -fullstdoutlog: 完整日志输出
5. -unattended: 无交互模式运行
6. -NoSeekFreeLoading: 禁用 seek-free 加载
7. -NoVerifyGC: 禁用垃圾回收验证

## 网络参数

1. -port=7777: 设置服务器端口 (默认7777)
2. -queryport=27015: 设置查询端口 (默认27015)
3. -beaconport=15000: 设置信标端口
4. -Multihome=IP地址: 指定服务器绑定IP
5. -maxplayers=16: 设置最大玩家数
6. -public: 将服务器设为公开可见
7. -lan: 局域网模式

## 游戏特定

1. -game: 指定游戏模式 (如 -game=FFA)
2. -map=地图名: 指定初始地图 (如 -map=/Game/Maps/TestMap)
3. -servername="服务器名称": 设置服务器名称
4. -password=密码: 设置服务器密码

## 性能相关

1. -USEALLAVAILABLECORES: 使用所有可用核心
2. -corelimit=X: 限制使用核心数
3. -nomansky: 禁用天空效果
4. -nosound: 禁用声音系统
5. -low: 低性能模式

# 二.控制台命令

## 调试

1. stat fps —— 显示帧率
2. stat unit —— 显示包括Draw Call ，游戏逻辑等各种项的消耗
3. stat UnitGraph —— 显示各个参数的实时曲线图
4. stat rhi —— 显示各种GPU上的消耗细则
5. stat game —— 显示当前帧的时间信息
6. stat Engine —— 显示帧数时间，三角面数等
7. stat scenerendering —— 显示Drawcall
8. ShowFlag.Bounds —— 显示包围盒（0关闭，1打开）
9. ShowFlag.Collision—— 显示碰撞盒（0关闭，1打开）
10. r.visualizeOccludedPrimitives —— 查看遮挡剔除（0关闭，1打开）
11. DisableAllScreenMessages/EnableAllScreenMessages —— 关闭/打开屏幕打印信息
12. ke * rendertextures 高分辨率截图
13. HighResShot  —— 以当前viewport分辨率的倍数进行截图（倍数）
14. HighResShot 3840x2160 —— 指定分辨率截图【图片存储位置：\Saved\Screenshots\】
15. stat Hitches —— 或者stat DumpHitches 记录log文件
16. stat startfile / stat stopfile —— 开始/结束统计性能分析  ，用于记录某段时间内的性能分析数据。此时会在路径 Saved/Profiling/UnrealStats 下生成数据文件

## 画面

1. r.vsync 0—— 垂直同步（0关闭，1打开）
2. r.Tonemapper.Sharpen 3 —— 锐化（锐化强度）
3. r.Streaming.PoolSize 4096 —— 显存多少分配给了纹理流送池（显存大小，0表示无上限）
4. r.ScreenPercentage 50 —— 设置渲染分辨率为默认大小的50%
5. r.TonemapperFilm —— 开关后处理效果
6. ShowFlag.PostProcessing —— 开关后期盒子效果
7. r.AOSpecularOcclusionMode —— 可以让 skylight 产生的 DFAO 产生更准确的高光（0关闭，1打开）

## 其他

1. slomo —— 游戏运行速度

# 三.UE c++

## [https://wiki.unrealengine.com/Custom_Blueprint_Node_Creation](https://wiki.unrealengine.com/Custom_Blueprint_Node_Creation)
