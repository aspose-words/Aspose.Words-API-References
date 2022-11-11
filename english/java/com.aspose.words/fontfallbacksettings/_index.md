---
title: FontFallbackSettings
second_title: Aspose.Words for Java API 参考
description: 指定字体回退机制设置。
type: docs
weight: 277
url: /zh/java/com.aspose.words/fontfallbacksettings/
---

**遗产:**
java.lang.Object
```
public class FontFallbackSettings
```

指定字体回退机制设置。

要了解更多信息，请访问**Working with Fonts**文档文章。

默认情况下，后备设置使用模仿 Microsoft Word 后备的预定义设置进行初始化。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [buildAutomatic()](#buildAutomatic--) | 通过扫描可用字体自动构建后备设置。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [hashCode()](#hashCode--) |  |
| [load(InputStream stream)](#load-java.io.InputStream-) |  |
| [load(String fileName)](#load-java.lang.String-) | 从 XML 文件加载字体回退设置。 |
| [loadMsOfficeFallbackSettings()](#loadMsOfficeFallbackSettings--) | 加载模拟 Microsoft Word 后备并使用 Microsoft Office 字体的预定义后备设置。 |
| [loadNotoFallbackSettings()](#loadNotoFallbackSettings--) | 加载使用 Google Noto 字体的预定义后备设置。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [save(OutputStream outputStream)](#save-java.io.OutputStream-) |  |
| [save(String fileName)](#save-java.lang.String-) | 将当前的后备设置保存到文件。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### buildAutomatic() {#buildAutomatic--}
```
public void buildAutomatic()
```


通过扫描可用字体自动构建后备设置。此方法可能会产生非最佳的回退设置。字体由[ Unicode Character Range ][Unicode Character Range]字段而不是实际字形的存在。 Unicode 范围也被单独检查，与单一语言/脚本相关的几个范围可能使用不同的后备字体。


[Unicode Character Range]: https://docs.microsoft.com/en-us/typography/opentype/spec/os2#ur

### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
布尔值
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### load(InputStream stream) {#load-java.io.InputStream-}
```
public void load(InputStream stream)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### load(String fileName) {#load-java.lang.String-}
```
public void load(String fileName)
```


从 XML 文件加载字体回退设置。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 输入文件名。 |

### loadMsOfficeFallbackSettings() {#loadMsOfficeFallbackSettings--}
```
public void loadMsOfficeFallbackSettings()
```


加载模拟 Microsoft Word 后备并使用 Microsoft Office 字体的预定义后备设置。

### loadNotoFallbackSettings() {#loadNotoFallbackSettings--}
```
public void loadNotoFallbackSettings()
```


加载使用 Google Noto 字体的预定义后备设置。

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### save(OutputStream outputStream) {#save-java.io.OutputStream-}
```
public void save(OutputStream outputStream)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |

### save(String fileName) {#save-java.lang.String-}
```
public void save(String fileName)
```


将当前的后备设置保存到文件。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 输出文件名。 |

### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
