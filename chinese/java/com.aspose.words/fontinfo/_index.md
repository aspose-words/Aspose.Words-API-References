---
title: FontInfo
second_title: Aspose.Words for Java API 参考
description:指定有关文档中使用的字体的信息。
type: docs
weight: 280
url: /zh/java/com.aspose.words/fontinfo/
---

**遗产:**
java.lang.Object

**All Implemented 界面s:**
java.lang.Cloneable
```
public class FontInfo implements Cloneable
```

指定有关文档中使用的字体的信息。

要了解更多信息，请访问**Working with Fonts**文档文章。

您不直接创建此类的实例。使用[DocumentBase.getFontInfos()](../../com.aspose.words/documentbase\#getFontInfos--)属性来访问文档中定义的字体集合。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAltName()](#getAltName--) | 获取字体的备用名称。 |
| [getCharset()](#getCharset--) | 获取字体的字符集。 |
| [get班级()](#get班级--) |  |
| [getEmbeddedFont(int format, int style)](#getEmbeddedFont-int-int-) |  |
| [getEmbeddedFontAsOpen类型(int style)](#getEmbeddedFontAsOpen类型-int-) |  |
| [getFamily()](#getFamily--) | 获取此字体所属的字体系列。 |
| [getName()](#getName--) | 获取字体的名称。 |
| [getPanose()](#getPanose--) | 获取 PANOSE 字体分类号。 |
| [getPitch()](#getPitch--) | 间距指示字体是固定间距、按比例间隔还是依赖于默认设置。 |
| [hashCode()](#hashCode--) |  |
| [isTrue类型()](#isTrue类型--) | 指示此字体是 True类型 或 Open类型 字体，而不是光栅或矢量字体。 |
| [isTrue类型(boolean value)](#isTrue类型-boolean-) | 指示此字体是 True类型 或 Open类型 字体，而不是光栅或矢量字体。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAltName(String value)](#setAltName-java.lang.String-) | 设置字体的备用名称。 |
| [setCharset(int value)](#setCharset-int-) | 设置字体的字符集。 |
| [setFamily(int value)](#setFamily-int-) | 设置此字体所属的字体系列。 |
| [setPanose(byte[] value)](#setPanose-byte---) | 设置 PANOSE 字体分类号。 |
| [setPitch(int value)](#setPitch-int-) | 间距指示字体是固定间距、按比例间隔还是依赖于默认设置。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
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
### getAltName() {#getAltName--}
```
public String getAltName()
```


获取字体的备用名称。

不能为 null 。可以是空字符串。

**退货:**
java.lang.String - 字体的备用名称。
### getCharset() {#getCharset--}
```
public int getCharset()
```


获取字体的字符集。

**退货:**
int - 字体的字符集。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getEmbeddedFont(int format, int style) {#getEmbeddedFont-int-int-}
```
public byte[] getEmbeddedFont(int format, int style)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| format | int |  |
| style | int |  |

**退货:**
字节[]
### getEmbeddedFontAsOpen类型(int style) {#getEmbeddedFontAsOpen类型-int-}
```
public byte[] getEmbeddedFontAsOpen类型(int style)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| style | int |  |

**退货:**
字节[]
### getFamily() {#getFamily--}
```
public int getFamily()
```


获取此字体所属的字体系列。

**退货:**
 int - 此字体所属的字体系列。返回值是以下之一[FontFamily](../../com.aspose.words/fontfamily)常数。
### getName() {#getName--}
```
public String getName()
```


获取字体的名称。

不能为 null 。可以是空字符串。

**退货:**
java.lang.String - 字体的名称。
### getPanose() {#getPanose--}
```
public byte[] getPanose()
```


获取 PANOSE 字体分类号。

PANOSE 是对字体关键视觉特征（例如对比度、粗细和衬线样式）的紧凑型 10 字节描述。数字代表家庭种类、衬线样式、重量、比例、对比度、笔画变化、手臂样式、字母形式、中线和 X 高度。

可以为 null 。

**退货:**
字节[] - PANOSE 字体分类号。
### getPitch() {#getPitch--}
```
public int getPitch()
```


间距指示字体是固定间距、按比例间隔还是依赖于默认设置。

**退货:**
int - 对应的 int 值。返回值是以下之一[FontPitch](../../com.aspose.words/fontpitch)常数。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isTrue类型() {#isTrue类型--}
```
public boolean isTrue类型()
```


指示此字体是 True类型 或 Open类型 字体，而不是光栅或矢量字体。默认为真。

**退货:**
boolean - 对应的布尔值。
### isTrue类型(boolean value) {#isTrue类型-boolean-}
```
public void isTrue类型(boolean value)
```


指示此字体是 True类型 或 Open类型 字体，而不是光栅或矢量字体。默认为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setAltName(String value) {#setAltName-java.lang.String-}
```
public void setAltName(String value)
```


设置字体的备用名称。

不能为 null 。可以是空字符串。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 字体的备用名称。 |

### setCharset(int value) {#setCharset-int-}
```
public void setCharset(int value)
```


设置字体的字符集。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 字体的字符集。 |

### setFamily(int value) {#setFamily-int-}
```
public void setFamily(int value)
```


设置此字体所属的字体系列。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 此字体所属的字体系列。该值必须是以下之一[FontFamily](../../com.aspose.words/fontfamily)常数。 |

### setPanose(byte[] value) {#setPanose-byte---}
```
public void setPanose(byte[] value)
```


设置 PANOSE 字体分类号。

PANOSE 是对字体关键视觉特征（例如对比度、粗细和衬线样式）的紧凑型 10 字节描述。数字代表家庭种类、衬线样式、重量、比例、对比度、笔画变化、手臂样式、字母形式、中线和 X 高度。

可以为 null 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | byte[] | PANOSE 字体分类号。 |

### setPitch(int value) {#setPitch-int-}
```
public void setPitch(int value)
```


间距指示字体是固定间距、按比例间隔还是依赖于默认设置。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[FontPitch](../../com.aspose.words/fontpitch)常数。 |

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
