# 控制台命令
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
