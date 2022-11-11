---
title: ChartLegendEntry
second_title: Aspose.Words for Java API 参考
description:表示图表图例条目。
type: docs
weight: 64
url: /zh/java/com.aspose.words/chartlegendentry/
---

**遗产:**
java.lang.Object

**All Implemented 界面s:**
java.lang.Cloneable
```
public class ChartLegendEntry implements Cloneable
```

表示图表图例条目。

要了解更多信息，请访问**Working with Charts**文档文章。

图例条目对应于特定的图表系列或趋势线。

条目的文本是系列或趋势线的名称。无法更改文本。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int-) |  |
| [get班级()](#get班级--) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int-) |  |
| [getFont()](#getFont--) | 提供对此图例条目的字体格式的访问。 |
| [hashCode()](#hashCode--) |  |
| [isHidden()](#isHidden--) | 获取一个值，该值指示此条目是否隐藏在图表图例中。 |
| [isHidden(boolean value)](#isHidden-boolean-) | 设置一个值，指示此条目是否隐藏在图表图例中。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearRunAttrs() {#clearRunAttrs--}
```
public void clearRunAttrs()
```




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
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
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
### getFont() {#getFont--}
```
public Font getFont()
```


提供对此图例条目的字体格式的访问。

**退货:**
[Font](../../com.aspose.words/font) - 相应的[Font](../../com.aspose.words/font)价值。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isHidden() {#isHidden--}
```
public boolean isHidden()
```


获取一个值，该值指示此条目是否隐藏在图表图例中。默认值为**false**.当图表图例条目被隐藏时，它不会影响仍显示在图表上的相应图表系列或趋势线。

**退货:**
boolean - 指示此条目是否隐藏在图表图例中的值。
### isHidden(boolean value) {#isHidden-boolean-}
```
public void isHidden(boolean value)
```


设置一个值，指示此条目是否隐藏在图表图例中。默认值为**false**.当图表图例条目被隐藏时，它不会影响仍显示在图表上的相应图表系列或趋势线。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示此条目是否隐藏在图表图例中的值。 |

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

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int key, Object value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

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
