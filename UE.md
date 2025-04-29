# 一.Dedicated Server启动参数

## 通用

| 名称                                    | 标记或键值对 | 说明                                                                           |
| --------------------------------------- | ------------ | ------------------------------------------------------------------------------ |
| -log                                    | 标记         | 在客户端或服务器运行时显示日志窗口。                                           |
| -game                                   | 标记         | 用于启动游戏客户端的模式标记。                                                 |
| -server                                 | 标记         | 用于启动专用服务器的模式标记。                                                 |
| -newconsole                             | 标记         | 将服务器日志封装在窗口中，该窗口可访问控制台，为你的专用服务器运行控制台命令。 |
| -notimeouts                             | 标记         | 在客户端目标行上使用，防止客户端在尝试连接到服务器时超时。                     |
| -windowed                               | 标记         | 在窗口模式下启动客户端。与 -ResX=horizontal_res -ResY=vertical_res 一起使用。  |
| -fullscreen                             | 标记         | 在全屏模式下启动客户端。                                                       |
| -ResX=horizontal_res -ResY=vertical_res | 键值对       | 指定客户端的水平（X）和垂直（Y）分辨率大小。示例： -ResX=1920 -ResY=1080       |

## 渲染和GPU

| 名称                                  | 标记或键值对 | 说明                                                                                                                                   |
| ------------------------------------- | ------------ | -------------------------------------------------------------------------------------------------------------------------------------- |
| -d3d11                                | 标记         | 在DirectX 11 RHI中运行编辑器。                                                                                                         |
| -d3d12                                | 标记         | 在DirectX 12 RHI中运行编辑器。                                                                                                         |
| -vulkan                               | 标记         | 在Vulkan RHI中运行编辑器。                                                                                                             |
| -D3Ddebug                             | 标记         | 用于在DirectX RHI中显示隐藏的问题和详细日志记录的调试层。                                                                              |
| -VulkanDebug                          | 标记         | 用于在Vulkan RHI中显示隐藏的问题和详细日志记录的调试层。                                                                               |
| -gpuCrashDebugging                    | 标记         | 为DirectX 12上的NVIDIA GPU启用事后日志记录，或在AMD和NVIDIA的Vulkan中启用等效的日志记录。                                              |
| -rhiValidation                        | 标记         | 位于RHI层上方的调试层，用于捕获低级别RHI问题。适用于所有平台，在测试和发布版本配置中不可用。                                           |
| -DumpGPU                              | 标记         | 按可以检查以供调试的格式，将当前帧的所有内部资源转储到磁盘。这应该在每次遇到渲染崩溃时执行。                                           |
| -gpuValidation                        | 标记         | 适用于DirectX 12和Vulkan。将工具添加到着色器代码，通过GPU上的其他验证提供有关挂起的更多信息。                                          |
| -ForceRHIBypass                       | 标记         | 与 -NoRHIThread 一起使用。RHI调用与渲染器一起内联运行，而不是排队以后执行。                                                            |
| -NoRHIThread                          | 标记         | 与 -ForceRHIBypass 一起使用。与渲染线程上正在执行的RHI调用一起运行，而不是排队到单独的RHI线程中。                                      |
| -noshaderworker                       | 标记         | 在不进行分布式着色器编译的情况下运行编辑器。每个着色器会逐一编译，以便找出单个着色器的问题。这会导致在运行时速度显著变慢。             |
| -ddc=NoShared                         | 键值对       | 在不利用派生数据缓存（DDC）中的已编译二进制信息的情况下运行编辑器。这包括网络DDC上缓存的所有信息、缓存的动画、材质、纹理、材质函数等。 |
| -ddc=cold                             | 键值对       | 与 -ddc=NoShared 相同，只是本地DDC也会被忽略。适合用于测试以诊断或排除DDC问题。                                                        |
| -logcmds="LogDerivedDataCacheVerbose" | 键值对       | 提供更详细的DDC日志记录。                                                                                                              |

## CPU和内存

| 名称         | 标记或键值对 | 说明                                                   |
| ------------ | ------------ | ------------------------------------------------------ |
| -StompMAlloc | 标记         | 检查以确保传入的内存分配不会覆盖已经在使用的内存地址。 |

## 调试

| 名字                | 标志 或 键值对 | 描述                                               |
| ------------------- | -------------- | -------------------------------------------------- |
| -DebugCoreRedirects | 标志           | 在UE日志中添加额外信息，以帮助识别核心重定向问题。 |

# 二.控制台命令

## 调试

| 命令                                             | 说明                                                                                                               |
| ------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ |
| stat fps                                         | 显示帧率                                                                                                           |
| stat unit                                        | 显示包括Draw Call ，游戏逻辑等各种项的消耗                                                                         |
| stat UnitGraph                                   | 显示各个参数的实时曲线图                                                                                           |
| stat rhi                                         | 显示各种GPU上的消耗细则                                                                                            |
| stat game                                        | 显示当前帧的时间信息                                                                                               |
| stat Engine                                      | 显示帧数时间，三角面数等                                                                                           |
| stat scenerendering                              | 显示Drawcall                                                                                                       |
| ShowFlag.Bounds                                  | 显示包围盒（0关闭，1打开）                                                                                         |
| ShowFlag.Collision                               | 显示碰撞盒（0关闭，1打开）                                                                                         |
| r.visualizeOccludedPrimitives                    | 查看遮挡剔除（0关闭，1打开）                                                                                       |
| DisableAllScreenMessages/EnableAllScreenMessages | 关闭/打开屏幕打印信息                                                                                              |
| ke * rendertextures                              | 高分辨率截图                                                                                                       |
| HighResShot                                      | 以当前viewport分辨率的倍数进行截图（倍数）                                                                         |
| HighResShot 3840x2160                            | 指定分辨率截图【图片存储位置：\Saved\Screenshots\】                                                                |
| stat Hitches                                     | 或者stat DumpHitches 记录log文件                                                                                   |
| stat startfile / stat stopfile                   | 开始/结束统计性能分析  ，用于记录某段时间内的性能分析数据。此时会在路径 Saved/Profiling/UnrealStats 下生成数据文件 |

## 画面

| 命令                      | 说明                                                         |
| ------------------------- | ------------------------------------------------------------ |
| r.vsync 0                 | 垂直同步（0关闭，1打开）                                     |
| r.Tonemapper.Sharpen 3    | 锐化（锐化强度）                                             |
| r.Streaming.PoolSize 4096 | 显存多少分配给了纹理流送池（显存大小，0表示无上限）          |
| r.ScreenPercentage 50     | 设置渲染分辨率为默认大小的50%                                |
| r.TonemapperFilm          | 开关后处理效果                                               |
| ShowFlag.PostProcessing   | 开关后期盒子效果                                             |
| r.AOSpecularOcclusionMode | 可以让 skylight 产生的 DFAO 产生更准确的高光（0关闭，1打开） |

## 其他

| 命令  | 说明         |  |
| ----- | ------------ | - |
| slomo | 游戏运行速度 |  |

# 三.UE c++

## [https://wiki.unrealengine.com/Custom_Blueprint_Node_Creation](https://wiki.unrealengine.com/Custom_Blueprint_Node_Creation)
