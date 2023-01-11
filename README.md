# Android studio Connection refused: connect

studio 编译报这个错的时候，八九不离十是手欠去设置过代理，别问我怎么知道，我就是那个手欠过的人。
即使你编译看见报Error:Connection refused: connect 
这个错去把什么代理改回来、注释掉、更改grade版本，翻墙、把网线都没有用，再编译studio 仍然会报

```
Error:Connection refused: connect

```

因为你手动设置过一次代理后studio 就会在C盘里面生成一个代理文件，而后studio 每次编译都会去读取C盘路径的文件

![2781551-2c28ed0c3f74712a](https://user-images.githubusercontent.com/13359093/211734743-5cc9f65b-c6f0-4fba-80f9-4b0e2b450a15.png)

就问studio 这波操作惊不惊喜，刺不刺激。

# 方法
# 第一、关掉代理 No proxy给打勾上：

![2781551-b6b4118a0076de6a](https://user-images.githubusercontent.com/13359093/211734839-5e5adcd8-a39c-401e-bf6a-f830118a5c37.png)

# 第二、删除 C:\Users\pc.gradle 路径下面的 gradle.properties文件

![2781551-6a8e36386c8c48d1](https://user-images.githubusercontent.com/13359093/211734893-77e22d4e-0728-446a-9251-d2cd9ec6691a.png)

# 第二,   是重重重点！！！！！

删除掉再重新编译，绝对是没什么问题。
