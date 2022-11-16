---
title: IStructuredDocumentTag
second_title: Aspose.Words for Java API 参考
description: 为 和 定义公共数据的接口。
type: docs
weight: 658
url: /zh/java/com.aspose.words/istructureddocumenttag/
---
```
public interface IStructuredDocumentTag
```

定义通用数据的接口[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)和[StructuredDocumentTagRangeStart](../../com.aspose.words/structureddocumenttagrangestart).
## 方法

| 方法 | 描述 |
| --- | --- |
| [getColor()](#getColor--) | 获取结构化文档标签的颜色。 |
| [getId()](#getId--) | 为此指定一个唯一的只读持久数字 Id**SDT**. |
| [getLevel()](#getLevel--) | 获取此级别**SDT**发生在文档树中。 |
| [getLockContentControl()](#getLockContentControl--) | 当设置为 true 时，此属性将禁止用户删除此**SDT**. |
| [getLockContents()](#getLockContents--) | 当设置为 true 时，此属性将禁止用户编辑此文件的内容**SDT**. |
| [getPlaceholder()](#getPlaceholder--) | 获取[BuildingBlock](../../com.aspose.words/buildingblock)包含应在此 SDT 运行内容为空时显示的占位符文本，关联的映射 XML 元素为空，如通过[getXmlMapping()](../../com.aspose.words/istructureddocumenttag\#getXmlMapping--)元素或[isShowingPlaceholderText()](../../com.aspose.words/istructureddocumenttag\#isShowingPlaceholderText--) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/istructureddocumenttag\#isShowingPlaceholderText-boolean-)元素为真。 |
| [getPlaceholderName()](#getPlaceholderName--) | 获取或设置名称[BuildingBlock](../../com.aspose.words/buildingblock)包含占位符文本。 |
| [getSdtType()](#getSdtType--) | 获取 this 的类型**Structured document tag**. |
| [getTag()](#getTag--) | 指定与当前 SDT 节点关联的标签。 |
| [getTitle()](#getTitle--) | 指定与此关联的友好名称**SDT**. |
| [getWordOpenXML()](#getWordOpenXML--) | 获取一个字符串，该字符串表示包含在[SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC)格式。 |
| [getXmlMapping()](#getXmlMapping--) | 获取一个对象，该对象表示此结构化文档标记到当前文档的自定义 XML 部分中的 XML 数据的映射。 |
| [isRanged()](#isRanged--) | 如果此实例是范围结构化文档标记，则返回 true。 |
| [isShowingPlaceholderText()](#isShowingPlaceholderText--) | 指定此内容是否**SDT**应被解释为包含占位符文本（与 SDT 中的常规文本内容相反）。 |
| [isShowingPlaceholderText(boolean value)](#isShowingPlaceholderText-boolean-) | 指定此内容是否**SDT**应被解释为包含占位符文本（与 SDT 中的常规文本内容相反）。 |
| [setColor(Color value)](#setColor-java.awt.Color-) | 设置结构化文档标签的颜色。 |
| [setLockContentControl(boolean value)](#setLockContentControl-boolean-) | 当设置为 true 时，此属性将禁止用户删除此**SDT**. |
| [setLockContents(boolean value)](#setLockContents-boolean-) | 当设置为 true 时，此属性将禁止用户编辑此文件的内容**SDT**. |
| [setPlaceholderName(String value)](#setPlaceholderName-java.lang.String-) | 获取或设置名称[BuildingBlock](../../com.aspose.words/buildingblock)包含占位符文本。 |
| [setTag(String value)](#setTag-java.lang.String-) | 指定与当前 SDT 节点关联的标签。 |
| [setTitle(String value)](#setTitle-java.lang.String-) | 指定与此关联的友好名称**SDT**. |
| [structuredDocumentTagNode()](#structuredDocumentTagNode--) | 返回实现此接口的 Node 对象。 |
### getColor() {#getColor--}
```
public abstract Color getColor()
```


获取结构化文档标签的颜色。

**退货：**
java.awt.Color - 结构化文档标签的颜色。
### getId() {#getId--}
```
public abstract int getId()
```


为此指定一个唯一的只读持久数字 Id**SDT**.

**退货：**
int - 相应的 int 值。
### getLevel() {#getLevel--}
```
public abstract int getLevel()
```


获取此级别**SDT**发生在文档树中。

**退货：**
 int - 这个级别**SDT**发生在文档树中。返回值是其中之一[MarkupLevel](../../com.aspose.words/markuplevel)常数。
### getLockContentControl() {#getLockContentControl--}
```
public abstract boolean getLockContentControl()
```


当设置为 true 时，此属性将禁止用户删除此**SDT**.

**退货：**
boolean - 相应的布尔值。
### getLockContents() {#getLockContents--}
```
public abstract boolean getLockContents()
```


当设置为 true 时，此属性将禁止用户编辑此文件的内容**SDT**.

**退货：**
boolean - 相应的布尔值。
### getPlaceholder() {#getPlaceholder--}
```
public abstract BuildingBlock getPlaceholder()
```


获取[BuildingBlock](../../com.aspose.words/buildingblock)包含应在此 SDT 运行内容为空时显示的占位符文本，关联的映射 XML 元素为空，如通过[getXmlMapping()](../../com.aspose.words/istructureddocumenttag\#getXmlMapping--)元素或[isShowingPlaceholderText()](../../com.aspose.words/istructureddocumenttag\#isShowingPlaceholderText--) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/istructureddocumenttag\#isShowingPlaceholderText-boolean-)元素为真。可以为空，表示占位符不适用于此 Sdt。

**退货：**
[BuildingBlock](../../com.aspose.words/buildingblock) - 这[BuildingBlock](../../com.aspose.words/buildingblock)包含应在此 SDT 运行内容为空时显示的占位符文本，关联的映射 XML 元素为空，如通过[getXmlMapping()](../../com.aspose.words/istructureddocumenttag\#getXmlMapping--)元素或[isShowingPlaceholderText()](../../com.aspose.words/istructureddocumenttag\#isShowingPlaceholderText--) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/istructureddocumenttag\#isShowingPlaceholderText-boolean-)元素为真。
### getPlaceholderName() {#getPlaceholderName--}
```
public abstract String getPlaceholderName()
```


获取或设置名称[BuildingBlock](../../com.aspose.words/buildingblock)包含占位符文本。

具有此名称的 BuildingBlock[BuildingBlock.getName()](../../com.aspose.words/buildingblock\#getName--) / [BuildingBlock.setName(java.lang.String)](../../com.aspose.words/buildingblock\#setName-java.lang.String-)必须出现在[Document.getGlossaryDocument()](../../com.aspose.words/document\#getGlossaryDocument--) / [Document.setGlossaryDocument(com.aspose.words.GlossaryDocument)](../../com.aspose.words/document\#setGlossaryDocument-com.aspose.words.GlossaryDocument-)否则会出现 java.lang.IllegalStateException。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getSdtType() {#getSdtType--}
```
public abstract int getSdtType()
```


获取 this 的类型**Structured document tag**.

**退货：**
 int - 这个的类型**Structured document tag** .返回值是其中之一[SdtType](../../com.aspose.words/sdttype)常数。
### getTag() {#getTag--}
```
public abstract String getTag()
```


指定与当前 SDT 节点关联的标签。不能为空。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getTitle() {#getTitle--}
```
public abstract String getTitle()
```


指定与此关联的友好名称**SDT**.不能为空。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getWordOpenXML() {#getWordOpenXML--}
```
public abstract String getWordOpenXML()
```


获取一个字符串，该字符串表示包含在[SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC)格式。

**退货：**
 java.lang.String - 一个字符串，表示包含在[SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC)格式。
### getXmlMapping() {#getXmlMapping--}
```
public abstract XmlMapping getXmlMapping()
```


获取一个对象，该对象表示此结构化文档标记到当前文档的自定义 XML 部分中的 XML 数据的映射。您可以使用[XmlMapping.setMapping(com.aspose.words.CustomXmlPart, java.lang.String, java.lang.String)](../../com.aspose.words/xmlmapping\#setMapping-com.aspose.words.CustomXmlPart--java.lang.String--java.lang.String-)此对象的方法将结构化文档标记映射到 XML 数据。

**退货：**
[XmlMapping](../../com.aspose.words/xmlmapping) - 表示此结构化文档标记到当前文档的自定义 XML 部分中的 XML 数据的映射的对象。
### isRanged() {#isRanged--}
```
public abstract boolean isRanged()
```


如果此实例是范围结构化文档标记，则返回 true。

**退货：**
布尔值
### isShowingPlaceholderText() {#isShowingPlaceholderText--}
```
public abstract boolean isShowingPlaceholderText()
```


指定此内容是否**SDT**应被解释为包含占位符文本（与 SDT 中的常规文本内容相反）。

如果设置为 true，则在打开此文档时应恢复此状态（显示占位符文本）。

**退货：**
boolean - 相应的布尔值。
### isShowingPlaceholderText(boolean value) {#isShowingPlaceholderText-boolean-}
```
public abstract void isShowingPlaceholderText(boolean value)
```


指定此内容是否**SDT**应被解释为包含占位符文本（与 SDT 中的常规文本内容相反）。

如果设置为 true，则在打开此文档时应恢复此状态（显示占位符文本）。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setColor(Color value) {#setColor-java.awt.Color-}
```
public abstract void setColor(Color value)
```


设置结构化文档标签的颜色。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color | 结构化文档标签的颜色。 |

### setLockContentControl(boolean value) {#setLockContentControl-boolean-}
```
public abstract void setLockContentControl(boolean value)
```


当设置为 true 时，此属性将禁止用户删除此**SDT**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setLockContents(boolean value) {#setLockContents-boolean-}
```
public abstract void setLockContents(boolean value)
```


当设置为 true 时，此属性将禁止用户编辑此文件的内容**SDT**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setPlaceholderName(String value) {#setPlaceholderName-java.lang.String-}
```
public abstract void setPlaceholderName(String value)
```


获取或设置名称[BuildingBlock](../../com.aspose.words/buildingblock)包含占位符文本。

具有此名称的 BuildingBlock[BuildingBlock.getName()](../../com.aspose.words/buildingblock\#getName--) / [BuildingBlock.setName(java.lang.String)](../../com.aspose.words/buildingblock\#setName-java.lang.String-)必须出现在[Document.getGlossaryDocument()](../../com.aspose.words/document\#getGlossaryDocument--) / [Document.setGlossaryDocument(com.aspose.words.GlossaryDocument)](../../com.aspose.words/document\#setGlossaryDocument-com.aspose.words.GlossaryDocument-)否则会出现 java.lang.IllegalStateException。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setTag(String value) {#setTag-java.lang.String-}
```
public abstract void setTag(String value)
```


指定与当前 SDT 节点关联的标签。不能为空。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setTitle(String value) {#setTitle-java.lang.String-}
```
public abstract void setTitle(String value)
```


指定与此关联的友好名称**SDT**.不能为空。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### structuredDocumentTagNode() {#structuredDocumentTagNode--}
```
public abstract Node structuredDocumentTagNode()
```


返回实现此接口的 Node 对象。

**退货：**
[Node](../../com.aspose.words/node)