---
title: Forms2OleControl
second_title: Aspose.Words for Java API 参考
description:表示 Microsoft Forms 2.0 OLE 控件。
type: docs
weight: 298
url: /zh/java/com.aspose.words/forms2olecontrol/
---

**遗产:**
java.lang.Object, [com.aspose.words.OleControl](../../com.aspose.words/olecontrol)
```
public abstract class Forms2OleControl extends OleControl
```

表示 Microsoft Forms 2.0 OLE 控件。

要了解更多信息，请访问**Working with Ole Objects**文档文章。
## 构造函数s

| 构造函数 | 描述 |
| --- | --- |
| [Forms2OleControl()](#Forms2OleControl--) |  |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getCaption()](#getCaption--) | 获取控件的 Caption 属性。 |
| [getChildNodes()](#getChildNodes--) | 获取直接子控件的集合。 |
| [get班级()](#get班级--) |  |
| [getEnabled()](#getEnabled--) | 如果控件处于启用状态，则返回 true。 |
| [getName()](#getName--) | 获取 ActiveX 控件的名称。 |
| [get类型()](#get类型--) | 获取 Forms 2.0 控件的类型。 |
| [getValue()](#getValue--) | 获取通常表示控件状态的基础 Value 属性。 |
| [hashCode()](#hashCode--) |  |
| [isForms2OleControl()](#isForms2OleControl--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### Forms2OleControl() {#Forms2OleControl--}
```
public Forms2OleControl()
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
### getCaption() {#getCaption--}
```
public String getCaption()
```


获取控件的 Caption 属性。默认值为空字符串。

**退货:**
java.lang.String - 控件的 Caption 属性。
### getChildNodes() {#getChildNodes--}
```
public Forms2OleControlCollection getChildNodes()
```


获取直接子控件的集合。退货**null**如果这个控件不能有孩子。

**退货:**
[Forms2OleControlCollection](../../com.aspose.words/forms2olecontrolcollection) - 直接子控件的集合。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getEnabled() {#getEnabled--}
```
public boolean getEnabled()
```


如果控件处于启用状态，则返回 true。

**退货:**
boolean - 如果控件处于启用状态，则为真。
### getName() {#getName--}
```
public String getName()
```


获取 ActiveX 控件的名称。

**退货:**
java.lang.String - ActiveX 控件的名称。
### get类型() {#get类型--}
```
public int get类型()
```


获取 Forms 2.0 控件的类型。

**退货:**
 int - Forms 2.0 控件的类型。返回值是以下之一[Forms2OleControl类型](../../com.aspose.words/forms2olecontroltype)常数。
### getValue() {#getValue--}
```
public String getValue()
```


获取通常表示控件状态的基础 Value 属性。例如，选中选项按钮的值为“1”，而未选中的选项按钮值为“0”。默认值为空字符串。

**退货:**
java.lang.String - 通常表示控件状态的基础值属性。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isForms2OleControl() {#isForms2OleControl--}
```
public boolean isForms2OleControl()
```


如果控件是[Forms2OleControl](../../com.aspose.words/forms2olecontrol).

**退货:**
布尔值
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




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
