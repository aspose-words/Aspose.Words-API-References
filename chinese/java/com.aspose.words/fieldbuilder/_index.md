---
title: 字段Builder
second_title: Aspose.Words for Java API Reference
description: 从字段代码标记参数和开关构建一个字段。
type: docs
weight: 166
url: /zh/java/com.aspose.words/fieldbuilder/
---

**遗产:**
java.lang.Object
```
public class 字段Builder
```

从域代码标记（参数和开关）构建一个域。

要了解更多信息，请访问**Working with 字段**文档文章。
## 构造函数

| 构造函数 | 描述 |
| --- | --- |
| [字段Builder(int field类型)](#字段Builder-int-) | 初始化此类的新实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [addArgument(字段ArgumentBuilder argument)](#addArgument-com.aspose.words.字段ArgumentBuilder-) | 添加一个字段的参数，由[字段ArgumentBuilder](../../com.aspose.words/fieldargumentbuilder)到字段的代码。 |
| [addArgument(字段Builder argument)](#addArgument-com.aspose.words.字段Builder-) | 添加另一个表示的子字段[字段Builder](../../com.aspose.words/fieldbuilder)到字段的代码。 |
| [addArgument(double argument)](#addArgument-double-) | 添加字段的参数。 |
| [addArgument(int argument)](#addArgument-int-) | 添加字段的参数。 |
| [addArgument(String argument)](#addArgument-java.lang.String-) | 添加字段的参数。 |
| [addSwitch(String switchName)](#addSwitch-java.lang.String-) | 添加字段的开关。 |
| [addSwitch(String switchName, double switchArgument)](#addSwitch-java.lang.String-double-) | 添加字段的开关。 |
| [addSwitch(String switchName, int switchArgument)](#addSwitch-java.lang.String-int-) | 添加字段的开关。 |
| [addSwitch(String switchName, String switchArgument)](#addSwitch-java.lang.String-java.lang.String-) | 添加字段的开关。 |
| [buildAndInsert(Inline refNode)](#buildAndInsert-com.aspose.words.Inline-) | 在指定的内联节点之前构建并插入一个字段到文档中。 |
| [buildAndInsert(Paragraph refNode)](#buildAndInsert-com.aspose.words.Paragraph-) | 在文档中构建并插入一个字段到指定段落的末尾。 |
| [buildBlock(DocumentBuilder documentBuilder)](#buildBlock-com.aspose.words.DocumentBuilder-) |  |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### 字段Builder(int field类型) {#字段Builder-int-}
```
public 字段Builder(int field类型)
```


初始化此类的新实例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| field类型 | int |  |

### addArgument(字段ArgumentBuilder argument) {#addArgument-com.aspose.words.字段ArgumentBuilder-}
```
public 字段Builder addArgument(字段ArgumentBuilder argument)
```


添加一个字段的参数，由[字段ArgumentBuilder](../../com.aspose.words/fieldargumentbuilder)到字段的代码。当参数包含不同部分（例如子字段、节点和纯文本）的混合时，将使用此重载。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| argument | [字段ArgumentBuilder](../../com.aspose.words/fieldargumentbuilder) |  |

**退货:**
[字段Builder](../../com.aspose.words/fieldbuilder)
### addArgument(字段Builder argument) {#addArgument-com.aspose.words.字段Builder-}
```
public 字段Builder addArgument(字段Builder argument)
```


添加另一个表示的子字段[字段Builder](../../com.aspose.words/fieldbuilder)到字段的代码。当参数由单个子字段组成时使用此重载。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| argument | [字段Builder](../../com.aspose.words/fieldbuilder) |  |

**退货:**
[字段Builder](../../com.aspose.words/fieldbuilder)
### addArgument(double argument) {#addArgument-double-}
```
public 字段Builder addArgument(double argument)
```


添加字段的参数。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| argument | double | 参数值。 |

**退货:**
[字段Builder](../../com.aspose.words/fieldbuilder)
### addArgument(int argument) {#addArgument-int-}
```
public 字段Builder addArgument(int argument)
```


添加字段的参数。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| argument | int | 参数值。 |

**退货:**
[字段Builder](../../com.aspose.words/fieldbuilder)
### addArgument(String argument) {#addArgument-java.lang.String-}
```
public 字段Builder addArgument(String argument)
```


添加字段的参数。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| argument | java.lang.String | 参数值。 |

**退货:**
[字段Builder](../../com.aspose.words/fieldbuilder)
### addSwitch(String switchName) {#addSwitch-java.lang.String-}
```
public 字段Builder addSwitch(String switchName)
```


添加字段的开关。此重载添加了一个标志（不带参数的开关）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| switchName | java.lang.String | 交换机名称。 |

**退货:**
[字段Builder](../../com.aspose.words/fieldbuilder)
### addSwitch(String switchName, double switchArgument) {#addSwitch-java.lang.String-double-}
```
public 字段Builder addSwitch(String switchName, double switchArgument)
```


添加字段的开关。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| switchName | java.lang.String | 交换机名称。 |
| switchArgument | double | 开关值。 |

**退货:**
[字段Builder](../../com.aspose.words/fieldbuilder)
### addSwitch(String switchName, int switchArgument) {#addSwitch-java.lang.String-int-}
```
public 字段Builder addSwitch(String switchName, int switchArgument)
```


添加字段的开关。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| switchName | java.lang.String | 交换机名称。 |
| switchArgument | int | 开关值。 |

**退货:**
[字段Builder](../../com.aspose.words/fieldbuilder)
### addSwitch(String switchName, String switchArgument) {#addSwitch-java.lang.String-java.lang.String-}
```
public 字段Builder addSwitch(String switchName, String switchArgument)
```


添加字段的开关。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| switchName | java.lang.String | 交换机名称。 |
| switchArgument | java.lang.String | 开关值。 |

**退货:**
[字段Builder](../../com.aspose.words/fieldbuilder)
### buildAndInsert(Inline refNode) {#buildAndInsert-com.aspose.words.Inline-}
```
public 字段 buildAndInsert(Inline refNode)
```


在指定的内联节点之前构建并插入一个字段到文档中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| refNode | [Inline](../../com.aspose.words/inline) |  |

**退货:**
[字段](../../com.aspose.words/field) - 一个[字段](../../com.aspose.words/field)表示插入字段的对象。
### buildAndInsert(Paragraph refNode) {#buildAndInsert-com.aspose.words.Paragraph-}
```
public 字段 buildAndInsert(Paragraph refNode)
```


在文档中构建并插入一个字段到指定段落的末尾。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| refNode | [Paragraph](../../com.aspose.words/paragraph) |  |

**退货:**
[字段](../../com.aspose.words/field) - 一个[字段](../../com.aspose.words/field)表示插入字段的对象。
### buildBlock(DocumentBuilder documentBuilder) {#buildBlock-com.aspose.words.DocumentBuilder-}
```
public void buildBlock(DocumentBuilder documentBuilder)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| documentBuilder | [DocumentBuilder](../../com.aspose.words/documentbuilder) |  |

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
