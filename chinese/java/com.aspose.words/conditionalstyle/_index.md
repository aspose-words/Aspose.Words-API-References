---
title: ConditionalStyle
second_title: Aspose.Words for Java API 参考
description:表示应用于具有指定表格样式的表格的某些区域的特殊格式。
type: docs
weight: 89
url: /zh/java/com.aspose.words/conditionalstyle/
---

**遗产:**
java.lang.Object

**All Implemented 界面s:**
java.lang.Cloneable
```
public class ConditionalStyle implements Cloneable
```

表示应用于具有指定表格样式的表格的某些区域的特殊格式。

要了解更多信息，请访问**Working with Tables**文档文章。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [clearFormatting()](#clearFormatting--) | 清除此条件样式的格式。 |
| [clearParaAttrs()](#clearParaAttrs--) |  |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [equals(Object obj)](#equals-java.lang.Object-) |  |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int-) |  |
| [fetchInheritedParaAttr(int key)](#fetchInheritedParaAttr-int-) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int-) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int-) |  |
| [fetchParaAttr(int key)](#fetchParaAttr-int-) |  |
| [getBorders()](#getBorders--) | 获取条件样式的默认单元格边框的集合。 |
| [getBottomPadding()](#getBottomPadding--) | 获取要添加到表格单元格内容下方的空间量（以磅为单位）。 |
| [get班级()](#get班级--) |  |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int-) |  |
| [getDirectParaAttr(int key)](#getDirectParaAttr-int-) |  |
| [getDirectParaAttr(int key, int revisionsView)](#getDirectParaAttr-int-int-) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int-) |  |
| [getFont()](#getFont--) | 获取条件样式的字符格式。 |
| [getLeftPadding()](#getLeftPadding--) | 获取要添加到表格单元格内容左侧的空间量（以磅为单位）。 |
| [getParagraphFormat()](#getParagraphFormat--) | 获取条件样式的段落格式。 |
| [getRightPadding()](#getRightPadding--) | 获取要添加到表格单元格内容右侧的空间量（以磅为单位）。 |
| [getShading()](#getShading--) | 得到一个[Shading](../../com.aspose.words/shading)引用此条件样式的阴影格式的对象。 |
| [getTopPadding()](#getTopPadding--) | 获取要添加到表格单元格内容上方的空间量（以磅为单位）。 |
| [get类型()](#get类型--) | 获取与此条件样式相关的表格区域。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [removeParaAttr(int key)](#removeParaAttr-int-) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object-) |  |
| [setBottomPadding(double value)](#setBottomPadding-double-) | 设置要在表格单元格内容下方添加的空间量（以磅为单位）。 |
| [setLeftPadding(double value)](#setLeftPadding-double-) | 设置要添加到表格单元格内容左侧的空间量（以磅为单位）。 |
| [setParaAttr(int key, Object value)](#setParaAttr-int-java.lang.Object-) |  |
| [setRightPadding(double value)](#setRightPadding-double-) | 设置要添加到表格单元格内容右侧的空间量（以磅为单位）。 |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [setTopPadding(double value)](#setTopPadding-double-) | 设置要在表格单元格内容上方添加的空间量（以磅为单位）。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearFormatting() {#clearFormatting--}
```
public void clearFormatting()
```


清除此条件样式的格式。

### clearParaAttrs() {#clearParaAttrs--}
```
public void clearParaAttrs()
```




### clearRunAttrs() {#clearRunAttrs--}
```
public void clearRunAttrs()
```




### equals(Object obj) {#equals-java.lang.Object-}
```
public boolean equals(Object obj)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| obj | java.lang.Object |  |

**退货:**
布尔值
### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int-}
```
public Object fetchInheritedBorderAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### fetchInheritedParaAttr(int key) {#fetchInheritedParaAttr-int-}
```
public Object fetchInheritedParaAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
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
### fetchInheritedShadingAttr(int key) {#fetchInheritedShadingAttr-int-}
```
public Object fetchInheritedShadingAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### fetchParaAttr(int key) {#fetchParaAttr-int-}
```
public Object fetchParaAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### getBorders() {#getBorders--}
```
public BorderCollection getBorders()
```


获取条件样式的默认单元格边框的集合。

**退货:**
[BorderCollection](../../com.aspose.words/bordercollection) - 条件样式的默认单元格边框的集合。
### getBottomPadding() {#getBottomPadding--}
```
public double getBottomPadding()
```


获取要添加到表格单元格内容下方的空间量（以磅为单位）。

**退货:**
double - 在表格单元格内容下方添加的空间量（以磅为单位）。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int-}
```
public Object getDirectBorderAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### getDirectParaAttr(int key) {#getDirectParaAttr-int-}
```
public Object getDirectParaAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### getDirectParaAttr(int key, int revisionsView) {#getDirectParaAttr-int-int-}
```
public Object getDirectParaAttr(int key, int revisionsView)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**退货:**
java.lang.Object
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


获取条件样式的字符格式。

**退货:**
[Font](../../com.aspose.words/font) - 条件样式的字符格式。
### getLeftPadding() {#getLeftPadding--}
```
public double getLeftPadding()
```


获取要添加到表格单元格内容左侧的空间量（以磅为单位）。

**退货:**
double - 添加到表格单元格内容左侧的空间量（以磅为单位）。
### getParagraphFormat() {#getParagraphFormat--}
```
public ParagraphFormat getParagraphFormat()
```


获取条件样式的段落格式。

**退货:**
[ParagraphFormat](../../com.aspose.words/paragraphformat) - 条件样式的段落格式。
### getRightPadding() {#getRightPadding--}
```
public double getRightPadding()
```


获取要添加到表格单元格内容右侧的空间量（以磅为单位）。

**退货:**
double - 添加到表格单元格内容右侧的空间量（以磅为单位）。
### getShading() {#getShading--}
```
public Shading getShading()
```


得到一个[Shading](../../com.aspose.words/shading)引用此条件样式的阴影格式的对象。

**退货:**
[Shading](../../com.aspose.words/shading) - 一个[Shading](../../com.aspose.words/shading)引用此条件样式的阴影格式的对象。
### getTopPadding() {#getTopPadding--}
```
public double getTopPadding()
```


获取要添加到表格单元格内容上方的空间量（以磅为单位）。

**退货:**
double - 在表格单元格内容上方添加的空间量（以磅为单位）。
### get类型() {#get类型--}
```
public int get类型()
```


获取与此条件样式相关的表格区域。

**退货:**
 int - 与此条件样式相关的表格区域。返回值是以下之一[ConditionalStyle类型](../../com.aspose.words/conditionalstyletype)常数。
### hashCode() {#hashCode--}
```
public int hashCode()
```




**退货:**
整数
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### removeParaAttr(int key) {#removeParaAttr-int-}
```
public void removeParaAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

### removeRunAttr(int key) {#removeRunAttr-int-}
```
public void removeRunAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object-}
```
public void setBorderAttr(int key, Object value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setBottomPadding(double value) {#setBottomPadding-double-}
```
public void setBottomPadding(double value)
```


设置要在表格单元格内容下方添加的空间量（以磅为单位）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 在表格单元格内容下方添加的空间量（以磅为单位）。 |

### setLeftPadding(double value) {#setLeftPadding-double-}
```
public void setLeftPadding(double value)
```


设置要添加到表格单元格内容左侧的空间量（以磅为单位）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 添加到表格单元格内容左侧的空间量（以磅为单位）。 |

### setParaAttr(int key, Object value) {#setParaAttr-int-java.lang.Object-}
```
public void setParaAttr(int key, Object value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setRightPadding(double value) {#setRightPadding-double-}
```
public void setRightPadding(double value)
```


设置要添加到表格单元格内容右侧的空间量（以磅为单位）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 添加到表格单元格内容右侧的空间量（以磅为单位）。 |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int key, Object value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setTopPadding(double value) {#setTopPadding-double-}
```
public void setTopPadding(double value)
```


设置要在表格单元格内容上方添加的空间量（以磅为单位）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 在表格单元格内容上方添加的空间量（以磅为单位）。 |

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
