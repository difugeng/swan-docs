---
title: 相机组件控制
header: develop
nav: api
sidebar: media_cameracontext
---



createCameraContext
---
**解释：**创建并返回 camera 上下文 `cameraContext`对象，cameraContext 与页面的 camera 组件绑定，一个页面只能有一个 camera，通过它可以操作对应的组件。

**参数：**无

**cameraContext 对象的方法列表：**

|方法 | 参数  |说明|
|---- | ---- | ---- |
|takePhoto |  Object|  拍照，可指定质量，成功则返回图片。|
|startRecord |Object  |开始录像|
|stopRecord | Object | 结束录像，成功则返回封面与视频。|


**takePhoto 的 Object 参数列表：**

|参数  |类型 | 必填 | 说明|
|---- | ---- | ---- |---- |
|quality |String  |否  | 成像质量，值为high, normal, low，默认normal。|
|success| Function |   否  | 接口调用成功的回调函数 ，res = { tempImagePath }。|
|fail  |  Function  |  否 |  接口调用失败的回调函数|
|complete |   Function  |  否  | 接口调用结束的回调函数（调用成功、失败都会执行）|


**startRecord 的 Object 参数列表：**

|参数 | 类型 | 必填 | 说明|
|---- | ---- | ---- |---- |
|success |Function  |  否 |  接口调用成功的回调函数|
|fail  |  Function |   否  | 接口调用失败的回调函数|
|complete   | Function |   否  | 接口调用结束的回调函数（调用成功、失败都会执行）|


**stopRecord 的 Object 参数列表：**

|参数 | 类型  |必填  |说明|
|---- | ---- | ---- |---- |
|success |Function   | 否  | 接口调用成功的回调函数 ，res = { tempThumbPath, tempVideoPath }。|
|fail |   Function |   否  | 接口调用失败的回调函数|
|complete   | Function   | 否  | 接口调用结束的回调函数（调用成功、失败都会执行）|
