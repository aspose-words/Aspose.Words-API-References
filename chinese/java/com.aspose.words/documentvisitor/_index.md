---
title: DocumentVisitor
second_title: Aspose.Words for Java API 参考
description: 自定义文档访问者的基类。
type: docs
weight: 132
url: /zh/java/com.aspose.words/documentvisitor/
---

**遗产：**
java.lang.Object
```
public abstract class DocumentVisitor
```

自定义文档访问者的基类。

要了解更多信息，请访问**Aspose.Words Document Object Model (DOM)**文档文章。

和**DocumentVisitor**您可以定义和执行需要对文档树进行枚举的自定义操作。

例如，Aspose.Words 使用**DocumentVisitor**内部用于保存**Document**以各种格式和其他操作，如在文档的片段上查找字段或书签。

使用**DocumentVisitor**:

1.  创建一个派生自的类**DocumentVisitor**.
2.  覆盖并提供部分或全部 VisitXXX 方法的实现，以执行一些自定义操作。
3.  称呼[Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node\#accept-com.aspose.words.DocumentVisitor-)在**Node**您要从中开始枚举。

**DocumentVisitor**为所有 VisitXXX 方法提供默认实现，以便更轻松地创建新的文档访问者，因为只有特定访问者所需的方法需要被覆盖。没有必要覆盖所有的访问者方法。

有关更多信息，请参阅访问者设计模式。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [visitAbsolutePositionTab(AbsolutePositionTab tab)](#visitAbsolutePositionTab-com.aspose.words.AbsolutePositionTab-) | 当一个[AbsolutePositionTab](../../com.aspose.words/absolutepositiontab)在文档中遇到节点。 |
| [visitBodyEnd(Body body)](#visitBodyEnd-com.aspose.words.Body-) | 当一节中主要文本故事的枚举结束时调用。 |
| [visitBodyStart(Body body)](#visitBodyStart-com.aspose.words.Body-) | 当一节中的主要文本故事的枚举开始时调用。 |
| [visitBookmarkEnd(BookmarkEnd bookmarkEnd)](#visitBookmarkEnd-com.aspose.words.BookmarkEnd-) | 在文档中遇到书签结尾时调用。 |
| [visitBookmarkStart(BookmarkStart bookmarkStart)](#visitBookmarkStart-com.aspose.words.BookmarkStart-) | 在文档中遇到书签开始时调用。 |
| [visitBuildingBlockEnd(BuildingBlock block)](#visitBuildingBlockEnd-com.aspose.words.BuildingBlock-) | 当构建块的枚举结束时调用。 |
| [visitBuildingBlockStart(BuildingBlock block)](#visitBuildingBlockStart-com.aspose.words.BuildingBlock-) | 在开始枚举构建块时调用。 |
| [visitCellEnd(Cell cell)](#visitCellEnd-com.aspose.words.Cell-) | 当表格单元格的枚举结束时调用。 |
| [visitCellStart(Cell cell)](#visitCellStart-com.aspose.words.Cell-) | 在开始枚举表格单元格时调用。 |
| [visitCommentEnd(Comment comment)](#visitCommentEnd-com.aspose.words.Comment-) | 当评论文本的枚举结束时调用。 |
| [visitCommentRangeEnd(CommentRangeEnd commentRangeEnd)](#visitCommentRangeEnd-com.aspose.words.CommentRangeEnd-) | 当遇到注释文本范围的结尾时调用。 |
| [visitCommentRangeStart(CommentRangeStart commentRangeStart)](#visitCommentRangeStart-com.aspose.words.CommentRangeStart-) | 当遇到注释文本范围的开头时调用。 |
| [visitCommentStart(Comment comment)](#visitCommentStart-com.aspose.words.Comment-) | 当注释文本的枚举开始时调用。 |
| [visitDocumentEnd(Document doc)](#visitDocumentEnd-com.aspose.words.Document-) | 当文档的枚举完成时调用。 |
| [visitDocumentStart(Document doc)](#visitDocumentStart-com.aspose.words.Document-) | 当文档的枚举开始时调用。 |
| [visitEditableRangeEnd(EditableRangeEnd editableRangeEnd)](#visitEditableRangeEnd-com.aspose.words.EditableRangeEnd-) | 在文档中遇到可编辑范围的结尾时调用。 |
| [visitEditableRangeStart(EditableRangeStart editableRangeStart)](#visitEditableRangeStart-com.aspose.words.EditableRangeStart-) | 在文档中遇到可编辑范围的开始时调用。 |
| [visitFieldEnd(FieldEnd fieldEnd)](#visitFieldEnd-com.aspose.words.FieldEnd-) | 当字段在文档中结束时调用。 |
| [visitFieldSeparator(FieldSeparator fieldSeparator)](#visitFieldSeparator-com.aspose.words.FieldSeparator-) | 在文档中遇到字段分隔符时调用。 |
| [visitFieldStart(FieldStart fieldStart)](#visitFieldStart-com.aspose.words.FieldStart-) | 当文档中的字段开始时调用。 |
| [visitFootnoteEnd(Footnote footnote)](#visitFootnoteEnd-com.aspose.words.Footnote-) | 当脚注或尾注文本的枚举结束时调用。 |
| [visitFootnoteStart(Footnote footnote)](#visitFootnoteStart-com.aspose.words.Footnote-) | 当开始枚举脚注或尾注文本时调用。 |
| [visitFormField(FormField formField)](#visitFormField-com.aspose.words.FormField-) | 在文档中遇到表单域时调用。 |
| [visitGlossaryDocumentEnd(GlossaryDocument glossary)](#visitGlossaryDocumentEnd-com.aspose.words.GlossaryDocument-) | 在词汇表文档的枚举结束时调用。 |
| [visitGlossaryDocumentStart(GlossaryDocument glossary)](#visitGlossaryDocumentStart-com.aspose.words.GlossaryDocument-) | 在词汇表文档的枚举开始时调用。 |
| [visitGroupShapeEnd(GroupShape groupShape)](#visitGroupShapeEnd-com.aspose.words.GroupShape-) | 当组形状的枚举结束时调用。 |
| [visitGroupShapeStart(GroupShape groupShape)](#visitGroupShapeStart-com.aspose.words.GroupShape-) | 当组形状枚举开始时调用。 |
| [visitHeaderFooterEnd(HeaderFooter headerFooter)](#visitHeaderFooterEnd-com.aspose.words.HeaderFooter-) | 当节中页眉或页脚的枚举结束时调用。 |
| [visitHeaderFooterStart(HeaderFooter headerFooter)](#visitHeaderFooterStart-com.aspose.words.HeaderFooter-) | 当节中的页眉或页脚枚举开始时调用。 |
| [visitOfficeMathEnd(OfficeMath officeMath)](#visitOfficeMathEnd-com.aspose.words.OfficeMath-) | 在 Office Math 对象的枚举结束时调用。 |
| [visitOfficeMathStart(OfficeMath officeMath)](#visitOfficeMathStart-com.aspose.words.OfficeMath-) | 在开始枚举 Office Math 对象时调用。 |
| [visitParagraphEnd(Paragraph paragraph)](#visitParagraphEnd-com.aspose.words.Paragraph-) | 当段落枚举结束时调用。 |
| [visitParagraphStart(Paragraph paragraph)](#visitParagraphStart-com.aspose.words.Paragraph-) | 当开始枚举段落时调用。 |
| [visitRowEnd(Row row)](#visitRowEnd-com.aspose.words.Row-) | 当表行的枚举结束时调用。 |
| [visitRowStart(Row row)](#visitRowStart-com.aspose.words.Row-) | 当表行的枚举开始时调用。 |
| [visitRun(Run run)](#visitRun-com.aspose.words.Run-) | 遇到 中的一段文本时调用。 |
| [visitSectionEnd(Section section)](#visitSectionEnd-com.aspose.words.Section-) | 当部分枚举结束时调用。 |
| [visitSectionStart(Section section)](#visitSectionStart-com.aspose.words.Section-) | 当一个部分的枚举开始时调用。 |
| [visitShapeEnd(Shape shape)](#visitShapeEnd-com.aspose.words.Shape-) | 当形状的枚举结束时调用。 |
| [visitShapeStart(Shape shape)](#visitShapeStart-com.aspose.words.Shape-) | 在开始枚举形状时调用。 |
| [visitSmartTagEnd(SmartTag smartTag)](#visitSmartTagEnd-com.aspose.words.SmartTag-) | 当智能标签的枚举结束时调用。 |
| [visitSmartTagStart(SmartTag smartTag)](#visitSmartTagStart-com.aspose.words.SmartTag-) | 当智能标签的枚举开始时调用。 |
| [visitSpecialChar(SpecialChar specialChar)](#visitSpecialChar-com.aspose.words.SpecialChar-) | 当一个[SpecialChar](../../com.aspose.words/specialchar)在文档中遇到节点。 |
| [visitStructuredDocumentTagEnd(StructuredDocumentTag sdt)](#visitStructuredDocumentTagEnd-com.aspose.words.StructuredDocumentTag-) | 当结构化文档标签的枚举结束时调用。 |
| [visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)](#visitStructuredDocumentTagRangeEnd-com.aspose.words.StructuredDocumentTagRangeEnd-) |  |
| [visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)](#visitStructuredDocumentTagRangeStart-com.aspose.words.StructuredDocumentTagRangeStart-) |  |
| [visitStructuredDocumentTagStart(StructuredDocumentTag sdt)](#visitStructuredDocumentTagStart-com.aspose.words.StructuredDocumentTag-) | 当结构化文档标签的枚举开始时调用。 |
| [visitSubDocument(SubDocument subDocument)](#visitSubDocument-com.aspose.words.SubDocument-) | 遇到子文档时调用。 |
| [visitTableEnd(Table table)](#visitTableEnd-com.aspose.words.Table-) | 当表的枚举结束时调用。 |
| [visitTableStart(Table table)](#visitTableStart-com.aspose.words.Table-) | 当表的枚举开始时调用。 |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
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
### visitAbsolutePositionTab(AbsolutePositionTab tab) {#visitAbsolutePositionTab-com.aspose.words.AbsolutePositionTab-}
```
public int visitAbsolutePositionTab(AbsolutePositionTab tab)
```


当一个[AbsolutePositionTab](../../com.aspose.words/absolutepositiontab)在文档中遇到节点。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| tab | [AbsolutePositionTab](../../com.aspose.words/absolutepositiontab) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitBodyEnd(Body body) {#visitBodyEnd-com.aspose.words.Body-}
```
public int visitBodyEnd(Body body)
```


当一节中主要文本故事的枚举结束时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| body | [Body](../../com.aspose.words/body) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitBodyStart(Body body) {#visitBodyStart-com.aspose.words.Body-}
```
public int visitBodyStart(Body body)
```


当一节中的主要文本故事的枚举开始时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| body | [Body](../../com.aspose.words/body) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitBookmarkEnd(BookmarkEnd bookmarkEnd) {#visitBookmarkEnd-com.aspose.words.BookmarkEnd-}
```
public int visitBookmarkEnd(BookmarkEnd bookmarkEnd)
```


在文档中遇到书签结尾时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| bookmarkEnd | [BookmarkEnd](../../com.aspose.words/bookmarkend) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitBookmarkStart(BookmarkStart bookmarkStart) {#visitBookmarkStart-com.aspose.words.BookmarkStart-}
```
public int visitBookmarkStart(BookmarkStart bookmarkStart)
```


在文档中遇到书签开始时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| bookmarkStart | [BookmarkStart](../../com.aspose.words/bookmarkstart) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitBuildingBlockEnd(BuildingBlock block) {#visitBuildingBlockEnd-com.aspose.words.BuildingBlock-}
```
public int visitBuildingBlockEnd(BuildingBlock block)
```


当构建块的枚举结束时调用。

注意：当您对构建块节点执行访问者时，不会访问构建块节点及其子节点[Document](../../com.aspose.words/document).如果要在构建块上执行访问者，则需要执行访问者[GlossaryDocument](../../com.aspose.words/glossarydocument)或致电[BuildingBlock.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/buildingblock\#accept-com.aspose.words.DocumentVisitor-).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| block | [BuildingBlock](../../com.aspose.words/buildingblock) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitBuildingBlockStart(BuildingBlock block) {#visitBuildingBlockStart-com.aspose.words.BuildingBlock-}
```
public int visitBuildingBlockStart(BuildingBlock block)
```


在开始枚举构建块时调用。

注意：当您对构建块节点执行访问者时，不会访问构建块节点及其子节点[Document](../../com.aspose.words/document).如果要在构建块上执行访问者，则需要执行访问者[GlossaryDocument](../../com.aspose.words/glossarydocument)或致电[BuildingBlock.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/buildingblock\#accept-com.aspose.words.DocumentVisitor-).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| block | [BuildingBlock](../../com.aspose.words/buildingblock) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitCellEnd(Cell cell) {#visitCellEnd-com.aspose.words.Cell-}
```
public int visitCellEnd(Cell cell)
```


当表格单元格的枚举结束时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| cell | [Cell](../../com.aspose.words/cell) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitCellStart(Cell cell) {#visitCellStart-com.aspose.words.Cell-}
```
public int visitCellStart(Cell cell)
```


在开始枚举表格单元格时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| cell | [Cell](../../com.aspose.words/cell) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitCommentEnd(Comment comment) {#visitCommentEnd-com.aspose.words.Comment-}
```
public int visitCommentEnd(Comment comment)
```


当评论文本的枚举结束时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| comment | [Comment](../../com.aspose.words/comment) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitCommentRangeEnd(CommentRangeEnd commentRangeEnd) {#visitCommentRangeEnd-com.aspose.words.CommentRangeEnd-}
```
public int visitCommentRangeEnd(CommentRangeEnd commentRangeEnd)
```


当遇到注释文本范围的结尾时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| commentRangeEnd | [CommentRangeEnd](../../com.aspose.words/commentrangeend) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitCommentRangeStart(CommentRangeStart commentRangeStart) {#visitCommentRangeStart-com.aspose.words.CommentRangeStart-}
```
public int visitCommentRangeStart(CommentRangeStart commentRangeStart)
```


当遇到注释文本范围的开头时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| commentRangeStart | [CommentRangeStart](../../com.aspose.words/commentrangestart) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitCommentStart(Comment comment) {#visitCommentStart-com.aspose.words.Comment-}
```
public int visitCommentStart(Comment comment)
```


当注释文本的枚举开始时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| comment | [Comment](../../com.aspose.words/comment) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitDocumentEnd(Document doc) {#visitDocumentEnd-com.aspose.words.Document-}
```
public int visitDocumentEnd(Document doc)
```


当文档的枚举完成时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitDocumentStart(Document doc) {#visitDocumentStart-com.aspose.words.Document-}
```
public int visitDocumentStart(Document doc)
```


当文档的枚举开始时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitEditableRangeEnd(EditableRangeEnd editableRangeEnd) {#visitEditableRangeEnd-com.aspose.words.EditableRangeEnd-}
```
public int visitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
```


在文档中遇到可编辑范围的结尾时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| editableRangeEnd | [EditableRangeEnd](../../com.aspose.words/editablerangeend) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitEditableRangeStart(EditableRangeStart editableRangeStart) {#visitEditableRangeStart-com.aspose.words.EditableRangeStart-}
```
public int visitEditableRangeStart(EditableRangeStart editableRangeStart)
```


在文档中遇到可编辑范围的开始时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| editableRangeStart | [EditableRangeStart](../../com.aspose.words/editablerangestart) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitFieldEnd(FieldEnd fieldEnd) {#visitFieldEnd-com.aspose.words.FieldEnd-}
```
public int visitFieldEnd(FieldEnd fieldEnd)
```


当字段在文档中结束时调用。

有关更多信息，请参阅[visitFieldStart(com.aspose.words.FieldStart)](../../com.aspose.words/documentvisitor\#visitFieldStart-com.aspose.words.FieldStart-)

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldEnd | [FieldEnd](../../com.aspose.words/fieldend) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitFieldSeparator(FieldSeparator fieldSeparator) {#visitFieldSeparator-com.aspose.words.FieldSeparator-}
```
public int visitFieldSeparator(FieldSeparator fieldSeparator)
```


在文档中遇到字段分隔符时调用。

字段分隔符将文档中的字段代码与字段值分开。请注意，有些字段只有字段代码，没有字段分隔符和字段值。

有关更多信息，请参阅[visitFieldStart(com.aspose.words.FieldStart)](../../com.aspose.words/documentvisitor\#visitFieldStart-com.aspose.words.FieldStart-)

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldSeparator | [FieldSeparator](../../com.aspose.words/fieldseparator) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitFieldStart(FieldStart fieldStart) {#visitFieldStart-com.aspose.words.FieldStart-}
```
public int visitFieldStart(FieldStart fieldStart)
```


当文档中的字段开始时调用。

Word 文档中的字段由字段代码和字段值组成。

例如，显示页码的字段可以表示如下：

[FieldStart]PAGE[字段分隔符]98[FieldEnd]

字段分隔符将文档中的字段代码与字段值分开。请注意，有些字段只有字段代码，没有字段分隔符和字段值。

字段可以嵌套。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldStart | [FieldStart](../../com.aspose.words/fieldstart) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitFootnoteEnd(Footnote footnote) {#visitFootnoteEnd-com.aspose.words.Footnote-}
```
public int visitFootnoteEnd(Footnote footnote)
```


当脚注或尾注文本的枚举结束时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| footnote | [Footnote](../../com.aspose.words/footnote) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitFootnoteStart(Footnote footnote) {#visitFootnoteStart-com.aspose.words.Footnote-}
```
public int visitFootnoteStart(Footnote footnote)
```


当开始枚举脚注或尾注文本时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| footnote | [Footnote](../../com.aspose.words/footnote) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitFormField(FormField formField) {#visitFormField-com.aspose.words.FormField-}
```
public int visitFormField(FormField formField)
```


在文档中遇到表单域时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| formField | [FormField](../../com.aspose.words/formfield) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitGlossaryDocumentEnd(GlossaryDocument glossary) {#visitGlossaryDocumentEnd-com.aspose.words.GlossaryDocument-}
```
public int visitGlossaryDocumentEnd(GlossaryDocument glossary)
```


在词汇表文档的枚举结束时调用。

注意：当您对词汇表文档节点执行访问者时，不会访问词汇表文档节点及其子节点[Document](../../com.aspose.words/document).如果要对词汇表文档执行访问者，则需要调用[GlossaryDocument.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/glossarydocument\#accept-com.aspose.words.DocumentVisitor-).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| glossary | [GlossaryDocument](../../com.aspose.words/glossarydocument) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitGlossaryDocumentStart(GlossaryDocument glossary) {#visitGlossaryDocumentStart-com.aspose.words.GlossaryDocument-}
```
public int visitGlossaryDocumentStart(GlossaryDocument glossary)
```


在词汇表文档的枚举开始时调用。

注意：当您对词汇表文档节点执行访问者时，不会访问词汇表文档节点及其子节点[Document](../../com.aspose.words/document).如果要对词汇表文档执行访问者，则需要调用[GlossaryDocument.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/glossarydocument\#accept-com.aspose.words.DocumentVisitor-).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| glossary | [GlossaryDocument](../../com.aspose.words/glossarydocument) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitGroupShapeEnd(GroupShape groupShape) {#visitGroupShapeEnd-com.aspose.words.GroupShape-}
```
public int visitGroupShapeEnd(GroupShape groupShape)
```


当组形状的枚举结束时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| groupShape | [GroupShape](../../com.aspose.words/groupshape) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitGroupShapeStart(GroupShape groupShape) {#visitGroupShapeStart-com.aspose.words.GroupShape-}
```
public int visitGroupShapeStart(GroupShape groupShape)
```


当组形状枚举开始时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| groupShape | [GroupShape](../../com.aspose.words/groupshape) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitHeaderFooterEnd(HeaderFooter headerFooter) {#visitHeaderFooterEnd-com.aspose.words.HeaderFooter-}
```
public int visitHeaderFooterEnd(HeaderFooter headerFooter)
```


当节中页眉或页脚的枚举结束时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| headerFooter | [HeaderFooter](../../com.aspose.words/headerfooter) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitHeaderFooterStart(HeaderFooter headerFooter) {#visitHeaderFooterStart-com.aspose.words.HeaderFooter-}
```
public int visitHeaderFooterStart(HeaderFooter headerFooter)
```


当节中的页眉或页脚枚举开始时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| headerFooter | [HeaderFooter](../../com.aspose.words/headerfooter) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitOfficeMathEnd(OfficeMath officeMath) {#visitOfficeMathEnd-com.aspose.words.OfficeMath-}
```
public int visitOfficeMathEnd(OfficeMath officeMath)
```


在 Office Math 对象的枚举结束时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| officeMath | [OfficeMath](../../com.aspose.words/officemath) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitOfficeMathStart(OfficeMath officeMath) {#visitOfficeMathStart-com.aspose.words.OfficeMath-}
```
public int visitOfficeMathStart(OfficeMath officeMath)
```


在开始枚举 Office Math 对象时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| officeMath | [OfficeMath](../../com.aspose.words/officemath) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitParagraphEnd(Paragraph paragraph) {#visitParagraphEnd-com.aspose.words.Paragraph-}
```
public int visitParagraphEnd(Paragraph paragraph)
```


当段落枚举结束时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| paragraph | [Paragraph](../../com.aspose.words/paragraph) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitParagraphStart(Paragraph paragraph) {#visitParagraphStart-com.aspose.words.Paragraph-}
```
public int visitParagraphStart(Paragraph paragraph)
```


当开始枚举段落时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| paragraph | [Paragraph](../../com.aspose.words/paragraph) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitRowEnd(Row row) {#visitRowEnd-com.aspose.words.Row-}
```
public int visitRowEnd(Row row)
```


当表行的枚举结束时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| row | [Row](../../com.aspose.words/row) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitRowStart(Row row) {#visitRowStart-com.aspose.words.Row-}
```
public int visitRowStart(Row row)
```


当表行的枚举开始时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| row | [Row](../../com.aspose.words/row) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitRun(Run run) {#visitRun-com.aspose.words.Run-}
```
public int visitRun(Run run)
```


遇到 中的一段文本时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| run | [Run](../../com.aspose.words/run) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitSectionEnd(Section section) {#visitSectionEnd-com.aspose.words.Section-}
```
public int visitSectionEnd(Section section)
```


当部分枚举结束时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| section | [Section](../../com.aspose.words/section) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitSectionStart(Section section) {#visitSectionStart-com.aspose.words.Section-}
```
public int visitSectionStart(Section section)
```


当一个部分的枚举开始时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| section | [Section](../../com.aspose.words/section) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitShapeEnd(Shape shape) {#visitShapeEnd-com.aspose.words.Shape-}
```
public int visitShapeEnd(Shape shape)
```


当形状的枚举结束时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| shape | [Shape](../../com.aspose.words/shape) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitShapeStart(Shape shape) {#visitShapeStart-com.aspose.words.Shape-}
```
public int visitShapeStart(Shape shape)
```


在开始枚举形状时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| shape | [Shape](../../com.aspose.words/shape) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitSmartTagEnd(SmartTag smartTag) {#visitSmartTagEnd-com.aspose.words.SmartTag-}
```
public int visitSmartTagEnd(SmartTag smartTag)
```


当智能标签的枚举结束时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| smartTag | [SmartTag](../../com.aspose.words/smarttag) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitSmartTagStart(SmartTag smartTag) {#visitSmartTagStart-com.aspose.words.SmartTag-}
```
public int visitSmartTagStart(SmartTag smartTag)
```


当智能标签的枚举开始时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| smartTag | [SmartTag](../../com.aspose.words/smarttag) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitSpecialChar(SpecialChar specialChar) {#visitSpecialChar-com.aspose.words.SpecialChar-}
```
public int visitSpecialChar(SpecialChar specialChar)
```


当一个[SpecialChar](../../com.aspose.words/specialchar)在文档中遇到节点。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| specialChar | [SpecialChar](../../com.aspose.words/specialchar) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。通用控制字符不会调用此方法（请参阅[ControlChar](../../com.aspose.words/controlchar)可以出现在文档中。
### visitStructuredDocumentTagEnd(StructuredDocumentTag sdt) {#visitStructuredDocumentTagEnd-com.aspose.words.StructuredDocumentTag-}
```
public int visitStructuredDocumentTagEnd(StructuredDocumentTag sdt)
```


当结构化文档标签的枚举结束时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| sdt | [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd) {#visitStructuredDocumentTagRangeEnd-com.aspose.words.StructuredDocumentTagRangeEnd-}
```
public int visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| sdtRangeEnd | [StructuredDocumentTagRangeEnd](../../com.aspose.words/structureddocumenttagrangeend) |  |

**退货：**
整数
### visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart) {#visitStructuredDocumentTagRangeStart-com.aspose.words.StructuredDocumentTagRangeStart-}
```
public int visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| sdtRangeStart | [StructuredDocumentTagRangeStart](../../com.aspose.words/structureddocumenttagrangestart) |  |

**退货：**
整数
### visitStructuredDocumentTagStart(StructuredDocumentTag sdt) {#visitStructuredDocumentTagStart-com.aspose.words.StructuredDocumentTag-}
```
public int visitStructuredDocumentTagStart(StructuredDocumentTag sdt)
```


当结构化文档标签的枚举开始时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| sdt | [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitSubDocument(SubDocument subDocument) {#visitSubDocument-com.aspose.words.SubDocument-}
```
public int visitSubDocument(SubDocument subDocument)
```


遇到子文档时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| subDocument | [SubDocument](../../com.aspose.words/subdocument) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitTableEnd(Table table) {#visitTableEnd-com.aspose.words.Table-}
```
public int visitTableEnd(Table table)
```


当表的枚举结束时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| table | [Table](../../com.aspose.words/table) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
### visitTableStart(Table table) {#visitTableStart-com.aspose.words.Table-}
```
public int visitTableStart(Table table)
```


当表的枚举开始时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| table | [Table](../../com.aspose.words/table) | 正在访问的对象。 |

**退货：**
诠释 - A[VisitorAction](../../com.aspose.words/visitoraction)指定如何继续枚举的值。返回值是其中之一[VisitorAction](../../com.aspose.words/visitoraction)常数。
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
