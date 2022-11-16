---
title: NodeType
second_title: Aspose.Words for Java API 参考
description: 指定 Word 文档节点的类型。
type: docs
weight: 408
url: /zh/java/com.aspose.words/nodetype/
---

**遗产：**
java.lang.Object
```
public class NodeType
```

指定 Word 文档节点的类型。
## 字段

| 场地 | 描述 |
| --- | --- |
| [ANY](#ANY) | 指示所有节点类型。 |
| [BODY](#BODY) | 一个[Body](../../com.aspose.words/body)包含部分正文的对象（正文故事）。 |
| [BOOKMARK_END](#BOOKMARK-END) | 书签标记的结尾。 |
| [BOOKMARK_START](#BOOKMARK-START) | 书签标记的开始。 |
| [BUILDING_BLOCK](#BUILDING-BLOCK) | 词汇表文档中的构建块（例如 |
| [CELL](#CELL) | 表行的一个单元格。 |
| [COMMENT](#COMMENT) | Word 文档中的评论。 |
| [COMMENT_RANGE_END](#COMMENT-RANGE-END) | 表示注释范围结束的标记节点。 |
| [COMMENT_RANGE_START](#COMMENT-RANGE-START) | 表示注释范围开始的标记节点。 |
| [DOCUMENT](#DOCUMENT) | 一个[Document](../../com.aspose.words/document)对象，作为文档树的根，提供对整个 Word 文档的访问。 |
| [EDITABLE_RANGE_END](#EDITABLE-RANGE-END) | 可编辑范围的末端。 |
| [EDITABLE_RANGE_START](#EDITABLE-RANGE-START) | 可编辑范围的开始。 |
| [FIELD_END](#FIELD-END) | 指定 Word 字段结尾的特殊字符。 |
| [FIELD_SEPARATOR](#FIELD-SEPARATOR) | 将域代码与域结果分隔开的特殊字符。 |
| [FIELD_START](#FIELD-START) | 一个特殊字符，用于指定 Word 字段的开头。 |
| [FOOTNOTE](#FOOTNOTE) | Word 文档中的脚注或尾注。 |
| [FORM_FIELD](#FORM-FIELD) | 一个表单域。 |
| [GLOSSARY_DOCUMENT](#GLOSSARY-DOCUMENT) | 主文档中的词汇表文档。 |
| [GROUP_SHAPE](#GROUP-SHAPE) | 一组形状、图像、OLE 对象或其他组形状。 |
| [HEADER_FOOTER](#HEADER-FOOTER) | 一个[HeaderFooter](../../com.aspose.words/headerfooter)包含节内特定页眉或页脚文本的对象。 |
| [MOVE_FROM_RANGE_END](#MOVE-FROM-RANGE-END) | MoveFrom 范围的结束。 |
| [MOVE_FROM_RANGE_START](#MOVE-FROM-RANGE-START) | MoveFrom 范围的开始。 |
| [MOVE_TO_RANGE_END](#MOVE-TO-RANGE-END) | MoveTo 范围的结束。 |
| [MOVE_TO_RANGE_START](#MOVE-TO-RANGE-START) | MoveTo 范围的开始。 |
| [NULL](#NULL) | 保留供 Aspose.Words 内部使用。 |
| [OFFICE_MATH](#OFFICE-MATH) | Office Math 对象。 |
| [PARAGRAPH](#PARAGRAPH) | 一段文字。 |
| [ROW](#ROW) | 一排桌子。 |
| [RUN](#RUN) | 一段文字。 |
| [SECTION](#SECTION) | 一个[Section](../../com.aspose.words/section)对应于 Word 文档中的一个部分的对象。 |
| [SHAPE](#SHAPE) | 绘图对象，例如 OfficeArt 形状、图像或 OLE 对象。 |
| [SMART_TAG](#SMART-TAG) | 围绕段落中一个或多个内联结构（运行、图像、字段等）的智能标记 |
| [SPECIAL_CHAR](#SPECIAL-CHAR) | 不是更具体的特殊字符类型之一的特殊字符。 |
| [STRUCTURED_DOCUMENT_TAG](#STRUCTURED-DOCUMENT-TAG) | 允许定义特定于客户的信息及其表示方式。 |
| [STRUCTURED_DOCUMENT_TAG_RANGE_END](#STRUCTURED-DOCUMENT-TAG-RANGE-END) | 的结束**ranged**接受多节内容的结构化文档标签。 |
| [STRUCTURED_DOCUMENT_TAG_RANGE_START](#STRUCTURED-DOCUMENT-TAG-RANGE-START) | 的开始**ranged**接受多节内容的结构化文档标签。 |
| [SUB_DOCUMENT](#SUB-DOCUMENT) | 一个子文档节点，它是指向另一个文档的链接。 |
| [SYSTEM](#SYSTEM) | 保留供 Aspose.Words 内部使用。 |
| [TABLE](#TABLE) | 一个[Table](../../com.aspose.words/table)表示 Word 文档中表格的对象。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String nodeTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int nodeType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int nodeType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ANY {#ANY}
```
public static int ANY
```


指示所有节点类型。允许选择所有孩子。

### BODY {#BODY}
```
public static int BODY
```


一个[Body](../../com.aspose.words/body)包含部分正文的对象（正文故事）。

一个[Body](../../com.aspose.words/body)节点可以有[Paragraph](../../com.aspose.words/paragraph)和[Table](../../com.aspose.words/table)节点。

### BOOKMARK_END {#BOOKMARK-END}
```
public static int BOOKMARK_END
```


书签标记的结尾。

### BOOKMARK_START {#BOOKMARK-START}
```
public static int BOOKMARK_START
```


书签标记的开始。

### BUILDING_BLOCK {#BUILDING-BLOCK}
```
public static int BUILDING_BLOCK
```


词汇表文档中的构建块（例如，词汇表文档条目）。

### CELL {#CELL}
```
public static int CELL
```


表行的一个单元格。

一个[Cell](../../com.aspose.words/cell)节点可以有[Paragraph](../../com.aspose.words/paragraph)和[Table](../../com.aspose.words/table)节点。

### COMMENT {#COMMENT}
```
public static int COMMENT
```


Word 文档中的评论。

一个[Comment](../../com.aspose.words/comment)节点可以有[Paragraph](../../com.aspose.words/paragraph)和[Table](../../com.aspose.words/table)节点。

### COMMENT_RANGE_END {#COMMENT-RANGE-END}
```
public static int COMMENT_RANGE_END
```


表示注释范围结束的标记节点。

### COMMENT_RANGE_START {#COMMENT-RANGE-START}
```
public static int COMMENT_RANGE_START
```


表示注释范围开始的标记节点。

### DOCUMENT {#DOCUMENT}
```
public static int DOCUMENT
```


一个[Document](../../com.aspose.words/document)对象，作为文档树的根，提供对整个 Word 文档的访问。

一个[Document](../../com.aspose.words/document)节点可以有[Section](../../com.aspose.words/section)节点。

### EDITABLE_RANGE_END {#EDITABLE-RANGE-END}
```
public static int EDITABLE_RANGE_END
```


可编辑范围的末端。

### EDITABLE_RANGE_START {#EDITABLE-RANGE-START}
```
public static int EDITABLE_RANGE_START
```


可编辑范围的开始。

### FIELD_END {#FIELD-END}
```
public static int FIELD_END
```


指定 Word 字段结尾的特殊字符。

### FIELD_SEPARATOR {#FIELD-SEPARATOR}
```
public static int FIELD_SEPARATOR
```


将域代码与域结果分隔开的特殊字符。

### FIELD_START {#FIELD-START}
```
public static int FIELD_START
```


一个特殊字符，用于指定 Word 字段的开头。

### FOOTNOTE {#FOOTNOTE}
```
public static int FOOTNOTE
```


Word 文档中的脚注或尾注。

一个[Footnote](../../com.aspose.words/footnote)节点可以有[Paragraph](../../com.aspose.words/paragraph)和[Table](../../com.aspose.words/table)节点。

### FORM_FIELD {#FORM-FIELD}
```
public static int FORM_FIELD
```


一个表单域。

### GLOSSARY_DOCUMENT {#GLOSSARY-DOCUMENT}
```
public static int GLOSSARY_DOCUMENT
```


主文档中的词汇表文档。

### GROUP_SHAPE {#GROUP-SHAPE}
```
public static int GROUP_SHAPE
```


一组形状、图像、OLE 对象或其他组形状。

一个[GroupShape](../../com.aspose.words/groupshape)节点可以包含其他[Shape](../../com.aspose.words/shape)和[GroupShape](../../com.aspose.words/groupshape)节点。

### HEADER_FOOTER {#HEADER-FOOTER}
```
public static int HEADER_FOOTER
```


一个[HeaderFooter](../../com.aspose.words/headerfooter)包含节内特定页眉或页脚文本的对象。

一个[HeaderFooter](../../com.aspose.words/headerfooter)节点可以有[Paragraph](../../com.aspose.words/paragraph)和[Table](../../com.aspose.words/table)节点。

### MOVE_FROM_RANGE_END {#MOVE-FROM-RANGE-END}
```
public static int MOVE_FROM_RANGE_END
```


MoveFrom 范围的结束。

### MOVE_FROM_RANGE_START {#MOVE-FROM-RANGE-START}
```
public static int MOVE_FROM_RANGE_START
```


MoveFrom 范围的开始。

### MOVE_TO_RANGE_END {#MOVE-TO-RANGE-END}
```
public static int MOVE_TO_RANGE_END
```


MoveTo 范围的结束。

### MOVE_TO_RANGE_START {#MOVE-TO-RANGE-START}
```
public static int MOVE_TO_RANGE_START
```


MoveTo 范围的开始。

### NULL {#NULL}
```
public static int NULL
```


保留供 Aspose.Words 内部使用。

### OFFICE_MATH {#OFFICE-MATH}
```
public static int OFFICE_MATH
```


Office Math 对象。可以是方程、函数、矩阵或其他数学对象之一。可以是数学对象的集合，也可以包含一些非数学对象，例如文本运行。

### PARAGRAPH {#PARAGRAPH}
```
public static int PARAGRAPH
```


一段文字。

一个[Paragraph](../../com.aspose.words/paragraph)节点是内联级别元素的容器[Run](../../com.aspose.words/run), [FieldStart](../../com.aspose.words/fieldstart), [FieldSeparator](../../com.aspose.words/fieldseparator), [FieldEnd](../../com.aspose.words/fieldend), [FormField](../../com.aspose.words/formfield), [Shape](../../com.aspose.words/shape), [GroupShape](../../com.aspose.words/groupshape), [Footnote](../../com.aspose.words/footnote), [Comment](../../com.aspose.words/comment), [SpecialChar](../../com.aspose.words/specialchar)， 也[BookmarkStart](../../com.aspose.words/bookmarkstart)和[BookmarkEnd](../../com.aspose.words/bookmarkend).

### ROW {#ROW}
```
public static int ROW
```


一排桌子。

一个[Row](../../com.aspose.words/row)节点可以有[Cell](../../com.aspose.words/cell)节点。

### RUN {#RUN}
```
public static int RUN
```


一段文字。

### SECTION {#SECTION}
```
public static int SECTION
```


一个[Section](../../com.aspose.words/section)对应于 Word 文档中的一个部分的对象。

一个[Section](../../com.aspose.words/section)节点可以有**Body**和**HeaderFooter**节点。

### SHAPE {#SHAPE}
```
public static int SHAPE
```


绘图对象，例如 OfficeArt 形状、图像或 OLE 对象。

一个[Shape](../../com.aspose.words/shape)节点可以包含[Paragraph](../../com.aspose.words/paragraph)和[Table](../../com.aspose.words/table)节点。

### SMART_TAG {#SMART-TAG}
```
public static int SMART_TAG
```


围绕段落中一个或多个内联结构（运行、图像、字段等）的智能标记

### SPECIAL_CHAR {#SPECIAL-CHAR}
```
public static int SPECIAL_CHAR
```


不是更具体的特殊字符类型之一的特殊字符。

### STRUCTURED_DOCUMENT_TAG {#STRUCTURED-DOCUMENT-TAG}
```
public static int STRUCTURED_DOCUMENT_TAG
```


允许定义特定于客户的信息及其表示方式。

### STRUCTURED_DOCUMENT_TAG_RANGE_END {#STRUCTURED-DOCUMENT-TAG-RANGE-END}
```
public static int STRUCTURED_DOCUMENT_TAG_RANGE_END
```


的结束**ranged**接受多节内容的结构化文档标签。

### STRUCTURED_DOCUMENT_TAG_RANGE_START {#STRUCTURED-DOCUMENT-TAG-RANGE-START}
```
public static int STRUCTURED_DOCUMENT_TAG_RANGE_START
```


的开始**ranged**接受多节内容的结构化文档标签。

### SUB_DOCUMENT {#SUB-DOCUMENT}
```
public static int SUB_DOCUMENT
```


一个子文档节点，它是指向另一个文档的链接。

### SYSTEM {#SYSTEM}
```
public static int SYSTEM
```


保留供 Aspose.Words 内部使用。

### TABLE {#TABLE}
```
public static int TABLE
```


一个[Table](../../com.aspose.words/table)表示 Word 文档中表格的对象。

一个[Table](../../com.aspose.words/table)节点可以有[Row](../../com.aspose.words/row)节点。

### length {#length}
```
public static int length
```


### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货：**
布尔值
### fromName(String nodeTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String nodeTypeName)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| nodeTypeName | java.lang.String |  |

**退货：**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getName(int nodeType) {#getName-int-}
```
public static String getName(int nodeType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| nodeType | int |  |

**退货：**
java.lang.字符串
### getValues() {#getValues--}
```
public static int[] getValues()
```




**退货：**
整数[]
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
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




**退货：**
java.lang.字符串
### toString(int nodeType) {#toString-int-}
```
public static String toString(int nodeType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| nodeType | int |  |

**退货：**
java.lang.字符串
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
