---
title: Rule
second_title: Aspose.Words for Java API 参考
description:指示执行 a 时发生的操作。
type: docs
weight: 36
url: /zh/java/com.aspose.words.net.system.data/rule/
---

**遗产:**
java.lang.Object, java.lang.Enum
```
public enum Rule extends Enum<System.Data.Rule>
```

表示当一个[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint)被强制执行。
## 字段

| 字段 | 描述 |
| --- | --- |
| [CASCADE](#CASCADE) | 删除或更新相关行。 |
| [NONE](#NONE) | 未对相关行执行任何操作。 |
| [SET_DEFAULT](#SET-DEFAULT) | 将相关行中的值设置为包含在[DataColumn.getDefaultValue()](../../com.aspose.words.net.system.data/datacolumn\#getDefaultValue--) / [DataColumn.setDefaultValue(java.lang.Object)](../../com.aspose.words.net.system.data/datacolumn\#setDefaultValue-java.lang.Object-)财产。 |
| [SET_NULL](#SET-NULL) | 将相关行中的值设置为 DBNull。 |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [<T>valueOf(班级<T> arg0, String arg1)](#-T-valueOf-java.lang.班级-T--java.lang.String-) |  |
| [compareTo(E arg0)](#compareTo-E-) |  |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getDeclaring班级()](#getDeclaring班级--) |  |
| [hashCode()](#hashCode--) |  |
| [name()](#name--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [ordinal()](#ordinal--) |  |
| [toString()](#toString--) |  |
| [valueOf(String name)](#valueOf-java.lang.String-) |  |
| [values()](#values--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### CASCADE {#CASCADE}
```
public static final System.Data.Rule CASCADE
```


删除或更新相关行。这是默认设置。

### NONE {#NONE}
```
public static final System.Data.Rule NONE
```


未对相关行执行任何操作。

### SET_DEFAULT {#SET-DEFAULT}
```
public static final System.Data.Rule SET_DEFAULT
```


将相关行中的值设置为包含在[DataColumn.getDefaultValue()](../../com.aspose.words.net.system.data/datacolumn\#getDefaultValue--) / [DataColumn.setDefaultValue(java.lang.Object)](../../com.aspose.words.net.system.data/datacolumn\#setDefaultValue-java.lang.Object-)财产。

### SET_NULL {#SET-NULL}
```
public static final System.Data.Rule SET_NULL
```


将相关行中的值设置为 DBNull。

### <T>valueOf(班级<T> arg0, String arg1) {#-T-valueOf-java.lang.班级-T--java.lang.String-}
```
public static T <T>valueOf(班级<T> arg0, String arg1)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.班级<T> |  |
| arg1 | java.lang.String |  |

**退货:**
吨
### compareTo(E arg0) {#compareTo-E-}
```
public final int compareTo(E arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | E |  |

**退货:**
整数
### equals(Object arg0) {#equals-java.lang.Object-}
```
public final boolean equals(Object arg0)
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
### getDeclaring班级() {#getDeclaring班级--}
```
public final 班级<E> getDeclaring班级()
```




**退货:**
java.lang.类<E>
### hashCode() {#hashCode--}
```
public final int hashCode()
```




**退货:**
整数
### name() {#name--}
```
public final String name()
```




**退货:**
java.lang.String
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### ordinal() {#ordinal--}
```
public final int ordinal()
```




**退货:**
整数
### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### valueOf(String name) {#valueOf-java.lang.String-}
```
public static System.Data.Rule valueOf(String name)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String |  |

**退货:**
[Rule](../../com.aspose.words.net.system.data/rule)
### values() {#values--}
```
public static System.Data.Rule[] values()
```




**退货:**
com.aspose.words.net.System.Data.Rule[]
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
