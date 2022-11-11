---
title: ListLevel
second_title: Aspose.Words for Java API 参考
description:定义列表级别的格式。
type: docs
weight: 372
url: /zh/java/com.aspose.words/listlevel/
---

**遗产:**
java.lang.Object

**All Implemented 界面s:**
java.lang.Cloneable
```
public class ListLevel implements Cloneable
```

定义列表级别的格式。

要了解更多信息，请访问**Working with Lists**文档文章。

您不创建此类的对象。创建列表时会自动创建列表级对象。您访问[ListLevel](../../com.aspose.words/listlevel)对象通过[ListLevelCollection](../../com.aspose.words/listlevelcollection)收藏。

使用的属性[ListLevel](../../com.aspose.words/listlevel)为各个列表级别指定列表格式。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [createPictureBullet()](#createPictureBullet--) | 为当前列表级别创建图片项目符号形状。 |
| [deletePictureBullet()](#deletePictureBullet--) | 删除当前列表级别的图片项目符号。 |
| [equals(ListLevel level)](#equals-com.aspose.words.ListLevel-) | 与指定的 ListLevel 进行比较。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int-) |  |
| [getAlignment()](#getAlignment--) | 获取列表项的实际数量的对齐方式。 |
| [get班级()](#get班级--) |  |
| [getCustomNumberStyleFormat()](#getCustomNumberStyleFormat--) | 获取此列表级别的自定义数字样式格式。 |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int-) |  |
| [getEffectiveValue(int index, int numberStyle, String customNumberStyleFormat)](#getEffectiveValue-int-int-java.lang.String-) |  |
| [getFont()](#getFont--) | 指定用于列表标签的字符格式。 |
| [getImageData()](#getImageData--) | 返回当前列表级别的图片子弹形状的图像数据。 |
| [getLinkedStyle()](#getLinkedStyle--) | 获取链接到此列表级别的段落样式。 |
| [getNumberFormat()](#getNumberFormat--) | 获取列表级别的数字格式。 |
| [getNumberPosition()](#getNumberPosition--) | 获取列表级别的数字或项目符号的位置（以磅为单位）。 |
| [getNumberStyle()](#getNumberStyle--) | 获取此列表级别的数字样式。 |
| [getRestartAfterLevel()](#getRestartAfterLevel--) | 获取在指定列表级别重新开始编号之前必须出现的列表级别。 |
| [getStartAt()](#getStartAt--) | 获取此列表级别的起始编号。 |
| [getTabPosition()](#getTabPosition--) | 获取列表级别的制表符位置（以磅为单位）。 |
| [getTextPosition()](#getTextPosition--) | 获取列表级别的第二行换行文本的位置（以磅为单位）。 |
| [getTrailingCharacter()](#getTrailingCharacter--) | 获取在列表级别的数字之后插入的字符。 |
| [hashCode()](#hashCode--) |  |
| [isLegal()](#isLegal--) | 如果关卡将所有继承的数字转换为阿拉伯语，则为真，如果保留其数字样式，则为假。 |
| [isLegal(boolean value)](#isLegal-boolean-) | 如果关卡将所有继承的数字转换为阿拉伯语，则为真，如果保留其数字样式，则为假。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [setAlignment(int value)](#setAlignment-int-) | 设置列表项的实际数量的对齐方式。 |
| [setLinkedStyle(Style value)](#setLinkedStyle-com.aspose.words.Style-) | 设置链接到此列表级别的段落样式。 |
| [setNumberFormat(String value)](#setNumberFormat-java.lang.String-) | 设置列表级别的数字格式。 |
| [setNumberPosition(double value)](#setNumberPosition-double-) | 设置列表级别的数字或项目符号的位置（以磅为单位）。 |
| [setNumberStyle(int value)](#setNumberStyle-int-) | 设置此列表级别的编号样式。 |
| [setRestartAfterLevel(int value)](#setRestartAfterLevel-int-) | 设置在指定列表级别重新开始编号之前必须出现的列表级别。 |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [setStartAt(int value)](#setStartAt-int-) | 设置此列表级别的起始编号。 |
| [setTabPosition(double value)](#setTabPosition-double-) | 设置列表级别的制表符位置（以磅为单位）。 |
| [setTextPosition(double value)](#setTextPosition-double-) | 设置列表级别的第二行换行文本的位置（以磅为单位）。 |
| [setTrailingCharacter(int value)](#setTrailingCharacter-int-) | 设置在列表级别的数字之后插入的字符。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearRunAttrs() {#clearRunAttrs--}
```
public void clearRunAttrs()
```




### createPictureBullet() {#createPictureBullet--}
```
public void createPictureBullet()
```


为当前列表级别创建图片项目符号形状。请注意，NumberStyle 将设置为 Bullet 和 NumberFormat 为“\\xF0B7" 以正确显示图片子弹。红十字图像将在创建时设置为图片子弹图像。要更改它，请使用[getImageData()](../../com.aspose.words/listlevel\#getImageData--).

### deletePictureBullet() {#deletePictureBullet--}
```
public void deletePictureBullet()
```


删除当前列表级别的图片项目符号。默认项目符号将在删除后显示。

### equals(ListLevel level) {#equals-com.aspose.words.ListLevel-}
```
public boolean equals(ListLevel level)
```


与指定的 ListLevel 进行比较。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| level | [ListLevel](../../com.aspose.words/listlevel) |  |

**退货:**
布尔值
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
### fetchInheritedRunAttr(int key) {#fetchInheritedRunAttr-int-}
```
public Object fetchInheritedRunAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### getAlignment() {#getAlignment--}
```
public int getAlignment()
```


获取列表项的实际数量的对齐方式。

列表标签相对于[getNumberPosition()](../../com.aspose.words/listlevel\#getNumberPosition--) / [setNumberPosition(double)](../../com.aspose.words/listlevel\#setNumberPosition-double-)财产。

**退货:**
int - 列表项的实际数量的理由。返回值是以下之一[ListLevelAlignment](../../com.aspose.words/listlevelalignment)常数。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getCustomNumberStyleFormat() {#getCustomNumberStyleFormat--}
```
public String getCustomNumberStyleFormat()
```


获取此列表级别的自定义数字样式格式。例如：“a, �,\\u011d，...”。

**退货:**
java.lang.String - 此列表级别的自定义数字样式格式。
### getDirectRunAttr(int key) {#getDirectRunAttr-int-}
```
public Object getDirectRunAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### getEffectiveValue(int index, int numberStyle, String customNumberStyleFormat) {#getEffectiveValue-int-int-java.lang.String-}
```
public static String getEffectiveValue(int index, int numberStyle, String customNumberStyleFormat)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int |  |
| numberStyle | int |  |
| customNumberStyleFormat | java.lang.String |  |

**退货:**
java.lang.String
### getFont() {#getFont--}
```
public Font getFont()
```


指定用于列表标签的字符格式。

**退货:**
[Font](../../com.aspose.words/font) - 相应的[Font](../../com.aspose.words/font)价值。
### getImageData() {#getImageData--}
```
public ImageData getImageData()
```


返回当前列表级别的图片子弹形状的图像数据。如果此级别未定义图片项目符号，则返回 null。在为非图片子弹形状设置新图像之前，请使用[createPictureBullet()](../../com.aspose.words/listlevel\#createPictureBullet--)先说方法。

**退货:**
[ImageData](../../com.aspose.words/imagedata) - 当前列表级别的图片子弹形状的图像数据。
### getLinkedStyle() {#getLinkedStyle--}
```
public Style getLinkedStyle()
```


获取链接到此列表级别的段落样式。

当列表级别未链接到段落样式时，此属性为 null。该属性可以设置为空。

**退货:**
[Style](../../com.aspose.words/style) 链接到此列表级别的段落样式。
### getNumberFormat() {#getNumberFormat--}
```
public String getNumberFormat()
```


获取列表级别的数字格式。

在普通文本字符中，字符串可以包含占位符字符\\x0000 到\\x0008 表示来自相应列表级别的数字。

例如，字符串“\\x0000。\\x0001)" 将生成一个类似于 "1.5)" 的列表标签。数字 "1" 是第一级列表的当前数字，数字 "5" 是第二级列表的当前数字。

不允许为 Null，但表示没有数字的空字符串是有效的。

**退货:**
java.lang.String - 列表级别的数字格式。
### getNumberPosition() {#getNumberPosition--}
```
public double getNumberPosition()
```


获取列表级别的数字或项目符号的位置（以磅为单位）。

[getNumberPosition()](../../com.aspose.words/listlevel\#getNumberPosition--) / [setNumberPosition(double)](../../com.aspose.words/listlevel\#setNumberPosition-double-)对应段落的 LeftIndent 加上 FirstLineIndent。

**退货:**
double - 列表级别的数字或项目符号的位置（以磅为单位）。
### getNumberStyle() {#getNumberStyle--}
```
public int getNumberStyle()
```


获取此列表级别的数字样式。

**退货:**
 int - 此列表级别的数字样式。返回值是以下之一[NumberStyle](../../com.aspose.words/numberstyle)常数。
### getRestartAfterLevel() {#getRestartAfterLevel--}
```
public int getRestartAfterLevel()
```


获取在指定列表级别重新开始编号之前必须出现的列表级别。

-1 的值表示将继续编号。

**退货:**
int - 在指定列表级别重新开始编号之前必须出现的列表级别。
### getStartAt() {#getStartAt--}
```
public int getStartAt()
```


获取此列表级别的起始编号。

默认值为 1。

**退货:**
int - 此列表级别的起始编号。
### getTabPosition() {#getTabPosition--}
```
public double getTabPosition()
```


获取列表级别的制表符位置（以磅为单位）。

仅在以下情况下生效[getTrailingCharacter()](../../com.aspose.words/listlevel\#getTrailingCharacter--) / [setTrailingCharacter(int)](../../com.aspose.words/listlevel\#setTrailingCharacter-int-)是一个标签。

**退货:**
double - 列表级别的制表符位置（以磅为单位）。
### getTextPosition() {#getTextPosition--}
```
public double getTextPosition()
```


获取列表级别的第二行换行文本的位置（以磅为单位）。

[getTextPosition()](../../com.aspose.words/listlevel\#getTextPosition--) / [setTextPosition(double)](../../com.aspose.words/listlevel\#setTextPosition-double-)对应段落的 LeftIndent。

**退货:**
double - 列表级别的第二行换行文本的位置（以磅为单位）。
### getTrailingCharacter() {#getTrailingCharacter--}
```
public int getTrailingCharacter()
```


获取在列表级别的数字之后插入的字符。

**退货:**
 int - 在列表级别的数字之后插入的字符。返回值是以下之一[ListTrailingCharacter](../../com.aspose.words/listtrailingcharacter)常数。
### hashCode() {#hashCode--}
```
public int hashCode()
```




**退货:**
整数
### isLegal() {#isLegal--}
```
public boolean isLegal()
```


如果关卡将所有继承的数字转换为阿拉伯语，则为真，如果保留其数字样式，则为假。

**退货:**
boolean - 对应的布尔值。
### isLegal(boolean value) {#isLegal-boolean-}
```
public void isLegal(boolean value)
```


如果关卡将所有继承的数字转换为阿拉伯语，则为真，如果保留其数字样式，则为假。

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




### removeRunAttr(int key) {#removeRunAttr-int-}
```
public void removeRunAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

### setAlignment(int value) {#setAlignment-int-}
```
public void setAlignment(int value)
```


设置列表项的实际数量的对齐方式。

列表标签相对于[getNumberPosition()](../../com.aspose.words/listlevel\#getNumberPosition--) / [setNumberPosition(double)](../../com.aspose.words/listlevel\#setNumberPosition-double-)财产。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 列表项的实际数量的理由。该值必须是以下之一[ListLevelAlignment](../../com.aspose.words/listlevelalignment)常数。 |

### setLinkedStyle(Style value) {#setLinkedStyle-com.aspose.words.Style-}
```
public void setLinkedStyle(Style value)
```


设置链接到此列表级别的段落样式。

当列表级别未链接到段落样式时，此属性为 null。该属性可以设置为空。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style) | 链接到此列表级别的段落样式。 |

### setNumberFormat(String value) {#setNumberFormat-java.lang.String-}
```
public void setNumberFormat(String value)
```


设置列表级别的数字格式。

在普通文本字符中，字符串可以包含占位符字符\\x0000 到\\x0008 表示来自相应列表级别的数字。

例如，字符串“\\x0000。\\x0001)" 将生成一个类似于 "1.5)" 的列表标签。数字 "1" 是第一级列表的当前数字，数字 "5" 是第二级列表的当前数字。

不允许为 Null，但表示没有数字的空字符串是有效的。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 列表级别的数字格式。 |

### setNumberPosition(double value) {#setNumberPosition-double-}
```
public void setNumberPosition(double value)
```


设置列表级别的数字或项目符号的位置（以磅为单位）。

[getNumberPosition()](../../com.aspose.words/listlevel\#getNumberPosition--) / [setNumberPosition(double)](../../com.aspose.words/listlevel\#setNumberPosition-double-)对应段落的 LeftIndent 加上 FirstLineIndent。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 列表级别的数字或项目符号的位置（以磅为单位）。 |

### setNumberStyle(int value) {#setNumberStyle-int-}
```
public void setNumberStyle(int value)
```


设置此列表级别的编号样式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 此列表级别的编号样式。该值必须是以下之一[NumberStyle](../../com.aspose.words/numberstyle)常数。 |

### setRestartAfterLevel(int value) {#setRestartAfterLevel-int-}
```
public void setRestartAfterLevel(int value)
```


设置在指定列表级别重新开始编号之前必须出现的列表级别。

-1 的值表示将继续编号。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 在指定的列表级别重新开始编号之前必须出现的列表级别。 |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int key, Object value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setStartAt(int value) {#setStartAt-int-}
```
public void setStartAt(int value)
```


设置此列表级别的起始编号。

默认值为 1。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 此列表级别的起始编号。 |

### setTabPosition(double value) {#setTabPosition-double-}
```
public void setTabPosition(double value)
```


设置列表级别的制表符位置（以磅为单位）。

仅在以下情况下生效[getTrailingCharacter()](../../com.aspose.words/listlevel\#getTrailingCharacter--) / [setTrailingCharacter(int)](../../com.aspose.words/listlevel\#setTrailingCharacter-int-)是一个标签。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 列表级别的制表符位置（以磅为单位）。 |

### setTextPosition(double value) {#setTextPosition-double-}
```
public void setTextPosition(double value)
```


设置列表级别的第二行换行文本的位置（以磅为单位）。

[getTextPosition()](../../com.aspose.words/listlevel\#getTextPosition--) / [setTextPosition(double)](../../com.aspose.words/listlevel\#setTextPosition-double-)对应段落的 LeftIndent。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 列表级别的第二行换行文本的位置（以磅为单位）。 |

### setTrailingCharacter(int value) {#setTrailingCharacter-int-}
```
public void setTrailingCharacter(int value)
```


设置在列表级别的数字之后插入的字符。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 在列表级别的数字之后插入的字符。该值必须是以下之一[ListTrailingCharacter](../../com.aspose.words/listtrailingcharacter)常数。 |

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
