---
title: MetafileRenderingOptions
second_title: Aspose.Words for Java API 参考
description: 允许指定额外的图元文件呈现选项。
type: docs
weight: 397
url: /zh/java/com.aspose.words/metafilerenderingoptions/
---

**遗产：**
java.lang.Object
```
public class MetafileRenderingOptions
```

允许指定额外的图元文件呈现选项。

要了解更多信息，请访问**Handling Windows Metafiles**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getEmfPlusDualRenderingMode()](#getEmfPlusDualRenderingMode--) | 获取一个值，该值确定应如何呈现 EMF+ Dual 图元文件。 |
| [getEmulateRasterOperations()](#getEmulateRasterOperations--) | 获取一个值，该值确定是否应模拟光栅操作。 |
| [getRenderingMode()](#getRenderingMode--) | 获取一个值，该值确定应如何呈现图元文件图像。 |
| [getScaleWmfFontsToMetafileSize()](#getScaleWmfFontsToMetafileSize--) | 获取一个值，该值确定是否根据页面上的图元文件大小缩放 WMF 图元文件中的字体。 |
| [getUseEmfEmbeddedToWmf()](#getUseEmfEmbeddedToWmf--) | 获取一个值，该值确定应如何呈现具有嵌入式 EMF 图元文件的 WMF 图元文件。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setEmfPlusDualRenderingMode(int value)](#setEmfPlusDualRenderingMode-int-) | 设置一个值，确定应如何呈现 EMF+ Dual 图元文件。 |
| [setEmulateRasterOperations(boolean value)](#setEmulateRasterOperations-boolean-) | 设置一个值，确定是否应模拟光栅操作。 |
| [setRenderingMode(int value)](#setRenderingMode-int-) | 设置一个值，确定应如何呈现图元文件图像。 |
| [setScaleWmfFontsToMetafileSize(boolean value)](#setScaleWmfFontsToMetafileSize-boolean-) | 设置一个值，确定是否根据页面上的图元文件大小缩放 WMF 图元文件中的字体。 |
| [setUseEmfEmbeddedToWmf(boolean value)](#setUseEmfEmbeddedToWmf-boolean-) | 设置一个值，确定应如何呈现具有嵌入式 EMF 图元文件的 WMF 图元文件。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货：**
布尔值
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getEmfPlusDualRenderingMode() {#getEmfPlusDualRenderingMode--}
```
public int getEmfPlusDualRenderingMode()
```


获取一个值，该值确定应如何呈现 EMF+ Dual 图元文件。

EMF+ Dual 图元文件包含 EMF+ 和 EMF 部分。 MS Word 和 GDI+ 始终呈现 EMF+ 部分。 Aspose.Words 目前不完全支持所有 EMF+ 记录，在某些情况下，EMF 部分的渲染结果看起来比 EMF+ 部分的渲染结果更好。

仅当图元文件呈现为矢量图形时才使用此选项。图元文件呈现为位图时，始终使用 EMF+ 部分。

默认值为[EmfPlusDualRenderingMode.EMF\_PLUS\_WITH\_FALLBACK](../../com.aspose.words/emfplusdualrenderingmode\#EMF-PLUS-WITH-FALLBACK).

**退货：**
 int - 决定 EMF+ Dual 图元文件应如何呈现的值。返回值是其中之一[EmfPlusDualRenderingMode](../../com.aspose.words/emfplusdualrenderingmode)常数。
### getEmulateRasterOperations() {#getEmulateRasterOperations--}
```
public boolean getEmulateRasterOperations()
```


获取一个值，该值确定是否应模拟光栅操作。

可以在图元文件中使用特定的光栅操作。它们不能直接渲染为矢量图形。模拟光栅操作需要对生成的矢量图形进行部分光栅化，这可能会影响元文件渲染性能。

当此值设置为 true 时，Aspose.Words 模拟光栅操作。生成的输出可能会部分光栅化并且性能可能会变慢。

当此值设置为 false 时，Aspose.Words 不会模拟光栅操作。当 Aspose.Words 在元文件中遇到光栅操作时，它会回退到使用操作系统将元文件渲染为位图。

仅当图元文件呈现为矢量图形时才使用此选项。

默认值是true 。

**退货：**
boolean - 确定是否应模拟光栅操作的值。
### getRenderingMode() {#getRenderingMode--}
```
public int getRenderingMode()
```


获取一个值，该值确定应如何呈现图元文件图像。

默认值取决于保存格式。对于图像它是[MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode\#BITMAP).对于其他格式，它是[MetafileRenderingMode.VECTOR\_WITH\_FALLBACK](../../com.aspose.words/metafilerenderingmode\#VECTOR-WITH-FALLBACK).

**退货：**
int - 确定应如何呈现元文件图像的值。返回值是其中之一[MetafileRenderingMode](../../com.aspose.words/metafilerenderingmode)常数。
### getScaleWmfFontsToMetafileSize() {#getScaleWmfFontsToMetafileSize--}
```
public boolean getScaleWmfFontsToMetafileSize()
```


获取一个值，该值确定是否根据页面上的图元文件大小缩放 WMF 图元文件中的字体。

当 WMF 图元文件在 MS Word 中显示时，字体可能会根据页面上的实际图元文件大小进行缩放。

当此值设置为 true 时，Aspose.Words 根据页面上的图元文件大小模拟字体缩放。

当此值设置为 false 时，Aspose.Words 显示字体，因为图元文件被渲染为其默认大小。

仅当图元文件呈现为矢量图形时才使用此选项。

默认值是true 。

**退货：**
布尔值 - 一个值，用于确定是否根据页面上的图元文件大小缩放 WMF 图元文件中的字体。
### getUseEmfEmbeddedToWmf() {#getUseEmfEmbeddedToWmf--}
```
public boolean getUseEmfEmbeddedToWmf()
```


获取一个值，该值确定应如何呈现具有嵌入式 EMF 图元文件的 WMF 图元文件。

WMF 图元文件可以包含嵌入的 EMF 数据。 MS Word 在大多数情况下使用嵌入式 EMF 数据。 GDI+ 始终使用 WMF 数据。

当此值设置为 true 时，Aspose.Words 在渲染时使用嵌入的 EMF 数据。

当此值设置为 false 时，Aspose.Words 在渲染时使用 WMF 数据。

仅当图元文件呈现为矢量图形时才使用此选项。当图元文件呈现为位图时，始终使用 WMF 数据。

默认值是true 。

**退货：**
布尔值 - 确定应如何呈现具有嵌入式 EMF 图元文件的 WMF 图元文件的值。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setEmfPlusDualRenderingMode(int value) {#setEmfPlusDualRenderingMode-int-}
```
public void setEmfPlusDualRenderingMode(int value)
```


设置一个值，确定应如何呈现 EMF+ Dual 图元文件。

EMF+ Dual 图元文件包含 EMF+ 和 EMF 部分。 MS Word 和 GDI+ 始终呈现 EMF+ 部分。 Aspose.Words 目前不完全支持所有 EMF+ 记录，在某些情况下，EMF 部分的渲染结果看起来比 EMF+ 部分的渲染结果更好。

仅当图元文件呈现为矢量图形时才使用此选项。图元文件呈现为位图时，始终使用 EMF+ 部分。

默认值为[EmfPlusDualRenderingMode.EMF\_PLUS\_WITH\_FALLBACK](../../com.aspose.words/emfplusdualrenderingmode\#EMF-PLUS-WITH-FALLBACK).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 确定应如何呈现 EMF+ Dual 图元文件的值。该值必须是其中之一[EmfPlusDualRenderingMode](../../com.aspose.words/emfplusdualrenderingmode)常数。 |

### setEmulateRasterOperations(boolean value) {#setEmulateRasterOperations-boolean-}
```
public void setEmulateRasterOperations(boolean value)
```


设置一个值，确定是否应模拟光栅操作。

可以在图元文件中使用特定的光栅操作。它们不能直接渲染为矢量图形。模拟光栅操作需要对生成的矢量图形进行部分光栅化，这可能会影响元文件渲染性能。

当此值设置为 true 时，Aspose.Words 模拟光栅操作。生成的输出可能会部分光栅化并且性能可能会变慢。

当此值设置为 false 时，Aspose.Words 不会模拟光栅操作。当 Aspose.Words 在元文件中遇到光栅操作时，它会回退到使用操作系统将元文件渲染为位图。

仅当图元文件呈现为矢量图形时才使用此选项。

默认值是true 。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 确定是否应模拟光栅操作的值。 |

### setRenderingMode(int value) {#setRenderingMode-int-}
```
public void setRenderingMode(int value)
```


设置一个值，确定应如何呈现图元文件图像。

默认值取决于保存格式。对于图像它是[MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode\#BITMAP).对于其他格式，它是[MetafileRenderingMode.VECTOR\_WITH\_FALLBACK](../../com.aspose.words/metafilerenderingmode\#VECTOR-WITH-FALLBACK).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 确定应如何呈现图元文件图像的值。该值必须是其中之一[MetafileRenderingMode](../../com.aspose.words/metafilerenderingmode)常数。 |

### setScaleWmfFontsToMetafileSize(boolean value) {#setScaleWmfFontsToMetafileSize-boolean-}
```
public void setScaleWmfFontsToMetafileSize(boolean value)
```


设置一个值，确定是否根据页面上的图元文件大小缩放 WMF 图元文件中的字体。

当 WMF 图元文件在 MS Word 中显示时，字体可能会根据页面上的实际图元文件大小进行缩放。

当此值设置为 true 时，Aspose.Words 根据页面上的图元文件大小模拟字体缩放。

当此值设置为 false 时，Aspose.Words 显示字体，因为图元文件被渲染为其默认大小。

仅当图元文件呈现为矢量图形时才使用此选项。

默认值是true 。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个值，确定是否根据页面上的图元文件大小缩放 WMF 图元文件中的字体。 |

### setUseEmfEmbeddedToWmf(boolean value) {#setUseEmfEmbeddedToWmf-boolean-}
```
public void setUseEmfEmbeddedToWmf(boolean value)
```


设置一个值，确定应如何呈现具有嵌入式 EMF 图元文件的 WMF 图元文件。

WMF 图元文件可以包含嵌入的 EMF 数据。 MS Word 在大多数情况下使用嵌入式 EMF 数据。 GDI+ 始终使用 WMF 数据。

当此值设置为 true 时，Aspose.Words 在渲染时使用嵌入的 EMF 数据。

当此值设置为 false 时，Aspose.Words 在渲染时使用 WMF 数据。

仅当图元文件呈现为矢量图形时才使用此选项。当图元文件呈现为位图时，始终使用 WMF 数据。

默认值是true 。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 确定应如何呈现具有嵌入式 EMF 图元文件的 WMF 图元文件的值。 |

### toString() {#toString--}
```
public String toString()
```




**退货：**
java.lang.字符串
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
