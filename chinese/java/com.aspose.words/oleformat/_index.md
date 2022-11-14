---
title: OleFormat
second_title: Aspose.Words for Java API 参考
description: 提供对 OLE 对象或 ActiveX 控件的数据的访问。
type: docs
weight: 425
url: /zh/java/com.aspose.words/oleformat/
---

**遗产:**
java.lang.Object
```
public class OleFormat
```

提供对 OLE 对象或 ActiveX 控件的数据的访问。

要了解更多信息，请访问**Working with Ole Objects**文档文章。

使用[Shape.getOleFormat()](../../com.aspose.words/shape\#getOleFormat--)属性来访问 OLE 对象的数据。您不创建的实例[OleFormat](../../com.aspose.words/oleformat)直接上课。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAutoUpdate()](#getAutoUpdate--) | 指定到 OLE 对象的链接是否在 Microsoft Word 中自动更新。 |
| [getClass()](#getClass--) |  |
| [getClsid()](#getClsid--) | 获取 OLE 对象的 CLSID。 |
| [getIconCaption()](#getIconCaption--) | 获取 OLE 对象的图标标题。 |
| [getOleControl()](#getOleControl--) | 获取[getOleControl()](../../com.aspose.words/oleformat\#getOleControl--)如果此 OLE 对象是 ActiveX 控件，则为对象。 |
| [getOleEntry(String oleEntryName)](#getOleEntry-java.lang.String-) |  |
| [getOleIcon()](#getOleIcon--) | 获取 OLE 对象的绘制方面。 |
| [getOlePackage()](#getOlePackage--) | 提供访问权限[OlePackage](../../com.aspose.words/olepackage)如果 OLE 对象是 OLE 包。 |
| [getProgId()](#getProgId--) | 获取 OLE 对象的 ProgID。 |
| [getRawData()](#getRawData--) | 获取 OLE 对象原始数据。 |
| [getSourceFullName()](#getSourceFullName--) | 获取链接的 OLE 对象的源文件的路径和名称。 |
| [getSourceItem()](#getSourceItem--) | 获取一个字符串，该字符串用于标识正在链接的源文件部分。 |
| [getSuggestedExtension()](#getSuggestedExtension--) | 如果要将当前嵌入对象保存到文件中，则获取建议的文件扩展名。 |
| [getSuggestedFileName()](#getSuggestedFileName--) | 如果要将当前嵌入对象保存到文件中，则获取建议的文件名。 |
| [hashCode()](#hashCode--) |  |
| [isLink()](#isLink--) | 如果 OLE 对象已链接（当[getSourceFullName()](../../com.aspose.words/oleformat\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat\#setSourceFullName-java.lang.String-)指定）。 |
| [isLocked()](#isLocked--) | 指定是否锁定到 OLE 对象的链接以防止更新。 |
| [isLocked(boolean value)](#isLocked-boolean-) | 指定是否锁定到 OLE 对象的链接以防止更新。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [save(OutputStream stream)](#save-java.io.OutputStream-) |  |
| [save(String fileName)](#save-java.lang.String-) | 将嵌入对象的数据保存到具有指定名称的文件中。 |
| [setAutoUpdate(boolean value)](#setAutoUpdate-boolean-) | 指定到 OLE 对象的链接是否在 Microsoft Word 中自动更新。 |
| [setProgId(String value)](#setProgId-java.lang.String-) | 设置 OLE 对象的 ProgID。 |
| [setSourceFullName(String value)](#setSourceFullName-java.lang.String-) | 为链接的 OLE 对象设置源文件的路径和名称。 |
| [setSourceItem(String value)](#setSourceItem-java.lang.String-) | 设置一个字符串，用于标识正在链接的源文件部分。 |
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
### getAutoUpdate() {#getAutoUpdate--}
```
public boolean getAutoUpdate()
```


指定到 OLE 对象的链接是否在 Microsoft Word 中自动更新。

默认值为**false**.

**退货:**
boolean - 对应的布尔值。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getClsid() {#getClsid--}
```
public UUID getClsid()
```


获取 OLE 对象的 CLSID。

**退货:**
java.util.UUID - OLE 对象的 CLSID。
### getIconCaption() {#getIconCaption--}
```
public String getIconCaption()
```


获取 OLE 对象的图标标题。

如果 OLE 对象未嵌入为图标或无法检索标题，则返回空字符串。

**退货:**
java.lang.String - OLE 对象的图标标题。
### getOleControl() {#getOleControl--}
```
public OleControl getOleControl()
```


获取[getOleControl()](../../com.aspose.words/oleformat\#getOleControl--)如果此 OLE 对象是 ActiveX 控件，则为对象。否则此属性为空。

**退货:**
[OleControl](../../com.aspose.words/olecontrol) -\{[getOleControl()](../../com.aspose.words/oleformat\#getOleControl--)如果此 OLE 对象是 ActiveX 控件，则为对象。
### getOleEntry(String oleEntryName) {#getOleEntry-java.lang.String-}
```
public byte[] getOleEntry(String oleEntryName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| oleEntryName | java.lang.String |  |

**退货:**
字节[]
### getOleIcon() {#getOleIcon--}
```
public boolean getOleIcon()
```


获取 OLE 对象的绘制方面。什么时候**true**，OLE 对象显示为图标。什么时候**false**，OLE 对象显示为内容。

Aspose.Words 不允许设置此属性以避免混淆。如果您能够在 Aspose.Words 中更改绘图方面，Microsoft Word 仍会以其原始绘图方面显示 OLE 对象，直到您在 Microsoft Word 中编辑或更新 OLE 对象。

**退货:**
boolean - OLE 对象的绘制方面。
### getOlePackage() {#getOlePackage--}
```
public OlePackage getOlePackage()
```


提供访问权限[OlePackage](../../com.aspose.words/olepackage)如果 OLE 对象是 OLE 包。否则返回 null。 OLE 包是一项遗留技术，它允许将 Windows 系统的 OLE 注册表中不存在的任何文件格式包装到通用包中，从而允许将几乎任何内容嵌入到文档中。看[OlePackage](../../com.aspose.words/olepackage)键入以获取更多信息。

**退货:**
[OlePackage](../../com.aspose.words/olepackage) - 相应的[OlePackage](../../com.aspose.words/olepackage)价值。
### getProgId() {#getProgId--}
```
public String getProgId()
```


获取 OLE 对象的 ProgID。

ProgID 属性并不总是存在于 Microsoft Word 文档中，因此不能依赖。

不能为空。

默认值为空字符串。

**退货:**
java.lang.String - OLE 对象的 ProgID。
### getRawData() {#getRawData--}
```
public byte[] getRawData()
```


获取 OLE 对象原始数据。

**退货:**
字节[]
### getSourceFullName() {#getSourceFullName--}
```
public String getSourceFullName()
```


获取链接的 OLE 对象的源文件的路径和名称。

默认值为空字符串。

如果[getSourceFullName()](../../com.aspose.words/oleformat\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat\#setSourceFullName-java.lang.String-)不是空字符串，则 OLE 对象已链接。

**退货:**
java.lang.String - 链接的 OLE 对象的源文件的路径和名称。
### getSourceItem() {#getSourceItem--}
```
public String getSourceItem()
```


获取一个字符串，该字符串用于标识正在链接的源文件部分。

默认值为空字符串。

例如，如果源文件是 Microsoft Excel 工作簿，则[getSourceItem()](../../com.aspose.words/oleformat\#getSourceItem--) / [setSourceItem(java.lang.String)](../../com.aspose.words/oleformat\#setSourceItem-java.lang.String-)如果 OLE 对象仅包含工作表中的几个单元格，则属性可能会返回“Workbook1!R3C1:R4C2”。

**退货:**
java.lang.String - 用于标识正在链接的源文件部分的字符串。
### getSuggestedExtension() {#getSuggestedExtension--}
```
public String getSuggestedExtension()
```


如果要将当前嵌入对象保存到文件中，则获取建议的文件扩展名。

**退货:**
java.lang.String - 如果要将当前嵌入对象保存到文件中，建议的文件扩展名。
### getSuggestedFileName() {#getSuggestedFileName--}
```
public String getSuggestedFileName()
```


如果要将当前嵌入对象保存到文件中，则获取建议的文件名。

**退货:**
java.lang.String - 如果要将当前嵌入对象保存到文件中，建议的文件名。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isLink() {#isLink--}
```
public boolean isLink()
```


如果 OLE 对象已链接（当[getSourceFullName()](../../com.aspose.words/oleformat\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat\#setSourceFullName-java.lang.String-)指定）。

**退货:**
 boolean - 如果 OLE 对象已链接，则为真（当[getSourceFullName()](../../com.aspose.words/oleformat\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat\#setSourceFullName-java.lang.String-)指定）。
### isLocked() {#isLocked--}
```
public boolean isLocked()
```


指定是否锁定到 OLE 对象的链接以防止更新。

默认值为**false**.

**退货:**
boolean - 对应的布尔值。
### isLocked(boolean value) {#isLocked-boolean-}
```
public void isLocked(boolean value)
```


指定是否锁定到 OLE 对象的链接以防止更新。

默认值为**false**.

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




### save(OutputStream stream) {#save-java.io.OutputStream-}
```
public void save(OutputStream stream)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | java.io.OutputStream |  |

### save(String fileName) {#save-java.lang.String-}
```
public void save(String fileName)
```


将嵌入对象的数据保存到具有指定名称的文件中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 保存 OLE 对象数据的文件的名称。 |

### setAutoUpdate(boolean value) {#setAutoUpdate-boolean-}
```
public void setAutoUpdate(boolean value)
```


指定到 OLE 对象的链接是否在 Microsoft Word 中自动更新。

默认值为**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setProgId(String value) {#setProgId-java.lang.String-}
```
public void setProgId(String value)
```


设置 OLE 对象的 ProgID。

ProgID 属性并不总是存在于 Microsoft Word 文档中，因此不能依赖。

不能为空。

默认值为空字符串。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | OLE 对象的 ProgID。 |

### setSourceFullName(String value) {#setSourceFullName-java.lang.String-}
```
public void setSourceFullName(String value)
```


为链接的 OLE 对象设置源文件的路径和名称。

默认值为空字符串。

如果[getSourceFullName()](../../com.aspose.words/oleformat\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat\#setSourceFullName-java.lang.String-)不是空字符串，则 OLE 对象已链接。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 链接的 OLE 对象的源文件的路径和名称。 |

### setSourceItem(String value) {#setSourceItem-java.lang.String-}
```
public void setSourceItem(String value)
```


设置一个字符串，用于标识正在链接的源文件部分。

默认值为空字符串。

例如，如果源文件是 Microsoft Excel 工作簿，则[getSourceItem()](../../com.aspose.words/oleformat\#getSourceItem--) / [setSourceItem(java.lang.String)](../../com.aspose.words/oleformat\#setSourceItem-java.lang.String-)如果 OLE 对象仅包含工作表中的几个单元格，则属性可能会返回“Workbook1!R3C1:R4C2”。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 用于标识正在链接的源文件部分的字符串。 |

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
