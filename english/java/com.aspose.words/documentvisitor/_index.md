---
title: DocumentVisitor
second_title: Aspose.Words for Java API Reference
description: Base class for custom document visitors.
type: docs
weight: 132
url: /java/com.aspose.words/documentvisitor/
---

**Inheritance:**
java.lang.Object
```
public abstract class DocumentVisitor
```

Base class for custom document visitors.

To learn more, visit the **Aspose.Words Document Object Model (DOM)** documentation article.

With **DocumentVisitor** you can define and execute custom operations that require enumeration over the document tree.

For example, Aspose.Words uses **DocumentVisitor** internally for saving **Document** in various formats and for other operations like finding fields or bookmarks over a fragment of a document.

To use **DocumentVisitor**:

1.  Create a class derived from **DocumentVisitor**.
2.  Override and provide implementations for some or all of the VisitXXX methods to perform some custom operations.
3.  Call [Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node\#accept-com.aspose.words.DocumentVisitor-) on the **Node** that you want to start the enumeration from.

**DocumentVisitor** provides default implementations for all of the VisitXXX methods to make it easier to create new document visitors as only the methods required for the particular visitor need to be overridden. It is not necessary to override all of the visitor methods.

For more information see the Visitor design pattern.
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [visitAbsolutePositionTab(AbsolutePositionTab tab)](#visitAbsolutePositionTab-com.aspose.words.AbsolutePositionTab-) | Called when a [AbsolutePositionTab](../../com.aspose.words/absolutepositiontab) node is encountered in the document. |
| [visitBodyEnd(Body body)](#visitBodyEnd-com.aspose.words.Body-) | Called when enumeration of the main text story in a section has ended. |
| [visitBodyStart(Body body)](#visitBodyStart-com.aspose.words.Body-) | Called when enumeration of the main text story in a section has started. |
| [visitBookmarkEnd(BookmarkEnd bookmarkEnd)](#visitBookmarkEnd-com.aspose.words.BookmarkEnd-) | Called when an end of a bookmark is encountered in the document. |
| [visitBookmarkStart(BookmarkStart bookmarkStart)](#visitBookmarkStart-com.aspose.words.BookmarkStart-) | Called when a start of a bookmark is encountered in the document. |
| [visitBuildingBlockEnd(BuildingBlock block)](#visitBuildingBlockEnd-com.aspose.words.BuildingBlock-) | Called when enumeration of a building block has ended. |
| [visitBuildingBlockStart(BuildingBlock block)](#visitBuildingBlockStart-com.aspose.words.BuildingBlock-) | Called when enumeration of a building block has started. |
| [visitCellEnd(Cell cell)](#visitCellEnd-com.aspose.words.Cell-) | Called when enumeration of a table cell has ended. |
| [visitCellStart(Cell cell)](#visitCellStart-com.aspose.words.Cell-) | Called when enumeration of a table cell has started. |
| [visitCommentEnd(Comment comment)](#visitCommentEnd-com.aspose.words.Comment-) | Called when enumeration of a comment text has ended. |
| [visitCommentRangeEnd(CommentRangeEnd commentRangeEnd)](#visitCommentRangeEnd-com.aspose.words.CommentRangeEnd-) | Called when the end of a commented range of text is encountered. |
| [visitCommentRangeStart(CommentRangeStart commentRangeStart)](#visitCommentRangeStart-com.aspose.words.CommentRangeStart-) | Called when the start of a commented range of text is encountered. |
| [visitCommentStart(Comment comment)](#visitCommentStart-com.aspose.words.Comment-) | Called when enumeration of a comment text has started. |
| [visitDocumentEnd(Document doc)](#visitDocumentEnd-com.aspose.words.Document-) | Called when enumeration of the document has finished. |
| [visitDocumentStart(Document doc)](#visitDocumentStart-com.aspose.words.Document-) | Called when enumeration of the document has started. |
| [visitEditableRangeEnd(EditableRangeEnd editableRangeEnd)](#visitEditableRangeEnd-com.aspose.words.EditableRangeEnd-) | Called when an end of an editable range is encountered in the document. |
| [visitEditableRangeStart(EditableRangeStart editableRangeStart)](#visitEditableRangeStart-com.aspose.words.EditableRangeStart-) | Called when a start of an editable range is encountered in the document. |
| [visitFieldEnd(FieldEnd fieldEnd)](#visitFieldEnd-com.aspose.words.FieldEnd-) | Called when a field ends in the document. |
| [visitFieldSeparator(FieldSeparator fieldSeparator)](#visitFieldSeparator-com.aspose.words.FieldSeparator-) | Called when a field separator is encountered in the document. |
| [visitFieldStart(FieldStart fieldStart)](#visitFieldStart-com.aspose.words.FieldStart-) | Called when a field starts in the document. |
| [visitFootnoteEnd(Footnote footnote)](#visitFootnoteEnd-com.aspose.words.Footnote-) | Called when enumeration of a footnote or endnote text has ended. |
| [visitFootnoteStart(Footnote footnote)](#visitFootnoteStart-com.aspose.words.Footnote-) | Called when enumeration of a footnote or endnote text has started. |
| [visitFormField(FormField formField)](#visitFormField-com.aspose.words.FormField-) | Called when a form field is encountered in the document. |
| [visitGlossaryDocumentEnd(GlossaryDocument glossary)](#visitGlossaryDocumentEnd-com.aspose.words.GlossaryDocument-) | Called when enumeration of a glossary document has ended. |
| [visitGlossaryDocumentStart(GlossaryDocument glossary)](#visitGlossaryDocumentStart-com.aspose.words.GlossaryDocument-) | Called when enumeration of a glossary document has started. |
| [visitGroupShapeEnd(GroupShape groupShape)](#visitGroupShapeEnd-com.aspose.words.GroupShape-) | Called when enumeration of a group shape has ended. |
| [visitGroupShapeStart(GroupShape groupShape)](#visitGroupShapeStart-com.aspose.words.GroupShape-) | Called when enumeration of a group shape has started. |
| [visitHeaderFooterEnd(HeaderFooter headerFooter)](#visitHeaderFooterEnd-com.aspose.words.HeaderFooter-) | Called when enumeration of a header or footer in a section has ended. |
| [visitHeaderFooterStart(HeaderFooter headerFooter)](#visitHeaderFooterStart-com.aspose.words.HeaderFooter-) | Called when enumeration of a header or footer in a section has started. |
| [visitOfficeMathEnd(OfficeMath officeMath)](#visitOfficeMathEnd-com.aspose.words.OfficeMath-) | Called when enumeration of a Office Math object has ended. |
| [visitOfficeMathStart(OfficeMath officeMath)](#visitOfficeMathStart-com.aspose.words.OfficeMath-) | Called when enumeration of a Office Math object has started. |
| [visitParagraphEnd(Paragraph paragraph)](#visitParagraphEnd-com.aspose.words.Paragraph-) | Called when enumeration of a paragraph has ended. |
| [visitParagraphStart(Paragraph paragraph)](#visitParagraphStart-com.aspose.words.Paragraph-) | Called when enumeration of a paragraph has started. |
| [visitRowEnd(Row row)](#visitRowEnd-com.aspose.words.Row-) | Called when enumeration of a table row has ended. |
| [visitRowStart(Row row)](#visitRowStart-com.aspose.words.Row-) | Called when enumeration of a table row has started. |
| [visitRun(Run run)](#visitRun-com.aspose.words.Run-) | Called when a run of text in the is encountered. |
| [visitSectionEnd(Section section)](#visitSectionEnd-com.aspose.words.Section-) | Called when enumeration of a section has ended. |
| [visitSectionStart(Section section)](#visitSectionStart-com.aspose.words.Section-) | Called when enumeration of a section has started. |
| [visitShapeEnd(Shape shape)](#visitShapeEnd-com.aspose.words.Shape-) | Called when enumeration of a shape has ended. |
| [visitShapeStart(Shape shape)](#visitShapeStart-com.aspose.words.Shape-) | Called when enumeration of a shape has started. |
| [visitSmartTagEnd(SmartTag smartTag)](#visitSmartTagEnd-com.aspose.words.SmartTag-) | Called when enumeration of a smart tag has ended. |
| [visitSmartTagStart(SmartTag smartTag)](#visitSmartTagStart-com.aspose.words.SmartTag-) | Called when enumeration of a smart tag has started. |
| [visitSpecialChar(SpecialChar specialChar)](#visitSpecialChar-com.aspose.words.SpecialChar-) | Called when a [SpecialChar](../../com.aspose.words/specialchar) node is encountered in the document. |
| [visitStructuredDocumentTagEnd(StructuredDocumentTag sdt)](#visitStructuredDocumentTagEnd-com.aspose.words.StructuredDocumentTag-) | Called when enumeration of a structured document tag has ended. |
| [visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)](#visitStructuredDocumentTagRangeEnd-com.aspose.words.StructuredDocumentTagRangeEnd-) |  |
| [visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)](#visitStructuredDocumentTagRangeStart-com.aspose.words.StructuredDocumentTagRangeStart-) |  |
| [visitStructuredDocumentTagStart(StructuredDocumentTag sdt)](#visitStructuredDocumentTagStart-com.aspose.words.StructuredDocumentTag-) | Called when enumeration of a structured document tag has started. |
| [visitSubDocument(SubDocument subDocument)](#visitSubDocument-com.aspose.words.SubDocument-) | Called when a subDocument is encountered. |
| [visitTableEnd(Table table)](#visitTableEnd-com.aspose.words.Table-) | Called when enumeration of a table has ended. |
| [visitTableStart(Table table)](#visitTableStart-com.aspose.words.Table-) | Called when enumeration of a table has started. |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
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




**Returns:**
java.lang.String
### visitAbsolutePositionTab(AbsolutePositionTab tab) {#visitAbsolutePositionTab-com.aspose.words.AbsolutePositionTab-}
```
public int visitAbsolutePositionTab(AbsolutePositionTab tab)
```


Called when a [AbsolutePositionTab](../../com.aspose.words/absolutepositiontab) node is encountered in the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tab | [AbsolutePositionTab](../../com.aspose.words/absolutepositiontab) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitBodyEnd(Body body) {#visitBodyEnd-com.aspose.words.Body-}
```
public int visitBodyEnd(Body body)
```


Called when enumeration of the main text story in a section has ended.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| body | [Body](../../com.aspose.words/body) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitBodyStart(Body body) {#visitBodyStart-com.aspose.words.Body-}
```
public int visitBodyStart(Body body)
```


Called when enumeration of the main text story in a section has started.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| body | [Body](../../com.aspose.words/body) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitBookmarkEnd(BookmarkEnd bookmarkEnd) {#visitBookmarkEnd-com.aspose.words.BookmarkEnd-}
```
public int visitBookmarkEnd(BookmarkEnd bookmarkEnd)
```


Called when an end of a bookmark is encountered in the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkEnd | [BookmarkEnd](../../com.aspose.words/bookmarkend) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitBookmarkStart(BookmarkStart bookmarkStart) {#visitBookmarkStart-com.aspose.words.BookmarkStart-}
```
public int visitBookmarkStart(BookmarkStart bookmarkStart)
```


Called when a start of a bookmark is encountered in the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkStart | [BookmarkStart](../../com.aspose.words/bookmarkstart) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitBuildingBlockEnd(BuildingBlock block) {#visitBuildingBlockEnd-com.aspose.words.BuildingBlock-}
```
public int visitBuildingBlockEnd(BuildingBlock block)
```


Called when enumeration of a building block has ended.

Note: A building block node and its children are not visited when you execute a Visitor over a [Document](../../com.aspose.words/document). If you want to execute a Visitor over a building block, you need to execute the visitor over [GlossaryDocument](../../com.aspose.words/glossarydocument) or call [BuildingBlock.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/buildingblock\#accept-com.aspose.words.DocumentVisitor-).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| block | [BuildingBlock](../../com.aspose.words/buildingblock) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitBuildingBlockStart(BuildingBlock block) {#visitBuildingBlockStart-com.aspose.words.BuildingBlock-}
```
public int visitBuildingBlockStart(BuildingBlock block)
```


Called when enumeration of a building block has started.

Note: A building block node and its children are not visited when you execute a Visitor over a [Document](../../com.aspose.words/document). If you want to execute a Visitor over a building block, you need to execute the visitor over [GlossaryDocument](../../com.aspose.words/glossarydocument) or call [BuildingBlock.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/buildingblock\#accept-com.aspose.words.DocumentVisitor-).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| block | [BuildingBlock](../../com.aspose.words/buildingblock) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitCellEnd(Cell cell) {#visitCellEnd-com.aspose.words.Cell-}
```
public int visitCellEnd(Cell cell)
```


Called when enumeration of a table cell has ended.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| cell | [Cell](../../com.aspose.words/cell) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitCellStart(Cell cell) {#visitCellStart-com.aspose.words.Cell-}
```
public int visitCellStart(Cell cell)
```


Called when enumeration of a table cell has started.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| cell | [Cell](../../com.aspose.words/cell) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitCommentEnd(Comment comment) {#visitCommentEnd-com.aspose.words.Comment-}
```
public int visitCommentEnd(Comment comment)
```


Called when enumeration of a comment text has ended.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| comment | [Comment](../../com.aspose.words/comment) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitCommentRangeEnd(CommentRangeEnd commentRangeEnd) {#visitCommentRangeEnd-com.aspose.words.CommentRangeEnd-}
```
public int visitCommentRangeEnd(CommentRangeEnd commentRangeEnd)
```


Called when the end of a commented range of text is encountered.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| commentRangeEnd | [CommentRangeEnd](../../com.aspose.words/commentrangeend) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitCommentRangeStart(CommentRangeStart commentRangeStart) {#visitCommentRangeStart-com.aspose.words.CommentRangeStart-}
```
public int visitCommentRangeStart(CommentRangeStart commentRangeStart)
```


Called when the start of a commented range of text is encountered.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| commentRangeStart | [CommentRangeStart](../../com.aspose.words/commentrangestart) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitCommentStart(Comment comment) {#visitCommentStart-com.aspose.words.Comment-}
```
public int visitCommentStart(Comment comment)
```


Called when enumeration of a comment text has started.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| comment | [Comment](../../com.aspose.words/comment) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitDocumentEnd(Document doc) {#visitDocumentEnd-com.aspose.words.Document-}
```
public int visitDocumentEnd(Document doc)
```


Called when enumeration of the document has finished.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitDocumentStart(Document doc) {#visitDocumentStart-com.aspose.words.Document-}
```
public int visitDocumentStart(Document doc)
```


Called when enumeration of the document has started.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitEditableRangeEnd(EditableRangeEnd editableRangeEnd) {#visitEditableRangeEnd-com.aspose.words.EditableRangeEnd-}
```
public int visitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
```


Called when an end of an editable range is encountered in the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| editableRangeEnd | [EditableRangeEnd](../../com.aspose.words/editablerangeend) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitEditableRangeStart(EditableRangeStart editableRangeStart) {#visitEditableRangeStart-com.aspose.words.EditableRangeStart-}
```
public int visitEditableRangeStart(EditableRangeStart editableRangeStart)
```


Called when a start of an editable range is encountered in the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| editableRangeStart | [EditableRangeStart](../../com.aspose.words/editablerangestart) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitFieldEnd(FieldEnd fieldEnd) {#visitFieldEnd-com.aspose.words.FieldEnd-}
```
public int visitFieldEnd(FieldEnd fieldEnd)
```


Called when a field ends in the document.

For more info see [visitFieldStart(com.aspose.words.FieldStart)](../../com.aspose.words/documentvisitor\#visitFieldStart-com.aspose.words.FieldStart-)

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldEnd | [FieldEnd](../../com.aspose.words/fieldend) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitFieldSeparator(FieldSeparator fieldSeparator) {#visitFieldSeparator-com.aspose.words.FieldSeparator-}
```
public int visitFieldSeparator(FieldSeparator fieldSeparator)
```


Called when a field separator is encountered in the document.

The field separator separates field code from field value in the document. Note that some fields have only field code and do not have field separator and field value.

For more info see [visitFieldStart(com.aspose.words.FieldStart)](../../com.aspose.words/documentvisitor\#visitFieldStart-com.aspose.words.FieldStart-)

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldSeparator | [FieldSeparator](../../com.aspose.words/fieldseparator) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitFieldStart(FieldStart fieldStart) {#visitFieldStart-com.aspose.words.FieldStart-}
```
public int visitFieldStart(FieldStart fieldStart)
```


Called when a field starts in the document.

A field in a Word document consists of a field code and field value.

For example, a field that displays a page number can be represented as follows:

[FieldStart]PAGE[FieldSeparator]98[FieldEnd]

The field separator separates field code from field value in the document. Note that some fields have only field code and do not have field separator and field value.

Fields can be nested.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldStart | [FieldStart](../../com.aspose.words/fieldstart) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitFootnoteEnd(Footnote footnote) {#visitFootnoteEnd-com.aspose.words.Footnote-}
```
public int visitFootnoteEnd(Footnote footnote)
```


Called when enumeration of a footnote or endnote text has ended.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| footnote | [Footnote](../../com.aspose.words/footnote) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitFootnoteStart(Footnote footnote) {#visitFootnoteStart-com.aspose.words.Footnote-}
```
public int visitFootnoteStart(Footnote footnote)
```


Called when enumeration of a footnote or endnote text has started.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| footnote | [Footnote](../../com.aspose.words/footnote) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitFormField(FormField formField) {#visitFormField-com.aspose.words.FormField-}
```
public int visitFormField(FormField formField)
```


Called when a form field is encountered in the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| formField | [FormField](../../com.aspose.words/formfield) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitGlossaryDocumentEnd(GlossaryDocument glossary) {#visitGlossaryDocumentEnd-com.aspose.words.GlossaryDocument-}
```
public int visitGlossaryDocumentEnd(GlossaryDocument glossary)
```


Called when enumeration of a glossary document has ended.

Note: A glossary document node and its children are not visited when you execute a Visitor over a [Document](../../com.aspose.words/document). If you want to execute a Visitor over a glossary document, you need to call [GlossaryDocument.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/glossarydocument\#accept-com.aspose.words.DocumentVisitor-).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| glossary | [GlossaryDocument](../../com.aspose.words/glossarydocument) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitGlossaryDocumentStart(GlossaryDocument glossary) {#visitGlossaryDocumentStart-com.aspose.words.GlossaryDocument-}
```
public int visitGlossaryDocumentStart(GlossaryDocument glossary)
```


Called when enumeration of a glossary document has started.

Note: A glossary document node and its children are not visited when you execute a Visitor over a [Document](../../com.aspose.words/document). If you want to execute a Visitor over a glossary document, you need to call [GlossaryDocument.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/glossarydocument\#accept-com.aspose.words.DocumentVisitor-).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| glossary | [GlossaryDocument](../../com.aspose.words/glossarydocument) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitGroupShapeEnd(GroupShape groupShape) {#visitGroupShapeEnd-com.aspose.words.GroupShape-}
```
public int visitGroupShapeEnd(GroupShape groupShape)
```


Called when enumeration of a group shape has ended.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| groupShape | [GroupShape](../../com.aspose.words/groupshape) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitGroupShapeStart(GroupShape groupShape) {#visitGroupShapeStart-com.aspose.words.GroupShape-}
```
public int visitGroupShapeStart(GroupShape groupShape)
```


Called when enumeration of a group shape has started.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| groupShape | [GroupShape](../../com.aspose.words/groupshape) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitHeaderFooterEnd(HeaderFooter headerFooter) {#visitHeaderFooterEnd-com.aspose.words.HeaderFooter-}
```
public int visitHeaderFooterEnd(HeaderFooter headerFooter)
```


Called when enumeration of a header or footer in a section has ended.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| headerFooter | [HeaderFooter](../../com.aspose.words/headerfooter) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitHeaderFooterStart(HeaderFooter headerFooter) {#visitHeaderFooterStart-com.aspose.words.HeaderFooter-}
```
public int visitHeaderFooterStart(HeaderFooter headerFooter)
```


Called when enumeration of a header or footer in a section has started.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| headerFooter | [HeaderFooter](../../com.aspose.words/headerfooter) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitOfficeMathEnd(OfficeMath officeMath) {#visitOfficeMathEnd-com.aspose.words.OfficeMath-}
```
public int visitOfficeMathEnd(OfficeMath officeMath)
```


Called when enumeration of a Office Math object has ended.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| officeMath | [OfficeMath](../../com.aspose.words/officemath) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitOfficeMathStart(OfficeMath officeMath) {#visitOfficeMathStart-com.aspose.words.OfficeMath-}
```
public int visitOfficeMathStart(OfficeMath officeMath)
```


Called when enumeration of a Office Math object has started.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| officeMath | [OfficeMath](../../com.aspose.words/officemath) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitParagraphEnd(Paragraph paragraph) {#visitParagraphEnd-com.aspose.words.Paragraph-}
```
public int visitParagraphEnd(Paragraph paragraph)
```


Called when enumeration of a paragraph has ended.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| paragraph | [Paragraph](../../com.aspose.words/paragraph) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitParagraphStart(Paragraph paragraph) {#visitParagraphStart-com.aspose.words.Paragraph-}
```
public int visitParagraphStart(Paragraph paragraph)
```


Called when enumeration of a paragraph has started.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| paragraph | [Paragraph](../../com.aspose.words/paragraph) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitRowEnd(Row row) {#visitRowEnd-com.aspose.words.Row-}
```
public int visitRowEnd(Row row)
```


Called when enumeration of a table row has ended.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| row | [Row](../../com.aspose.words/row) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitRowStart(Row row) {#visitRowStart-com.aspose.words.Row-}
```
public int visitRowStart(Row row)
```


Called when enumeration of a table row has started.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| row | [Row](../../com.aspose.words/row) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitRun(Run run) {#visitRun-com.aspose.words.Run-}
```
public int visitRun(Run run)
```


Called when a run of text in the is encountered.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| run | [Run](../../com.aspose.words/run) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitSectionEnd(Section section) {#visitSectionEnd-com.aspose.words.Section-}
```
public int visitSectionEnd(Section section)
```


Called when enumeration of a section has ended.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| section | [Section](../../com.aspose.words/section) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitSectionStart(Section section) {#visitSectionStart-com.aspose.words.Section-}
```
public int visitSectionStart(Section section)
```


Called when enumeration of a section has started.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| section | [Section](../../com.aspose.words/section) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitShapeEnd(Shape shape) {#visitShapeEnd-com.aspose.words.Shape-}
```
public int visitShapeEnd(Shape shape)
```


Called when enumeration of a shape has ended.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| shape | [Shape](../../com.aspose.words/shape) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitShapeStart(Shape shape) {#visitShapeStart-com.aspose.words.Shape-}
```
public int visitShapeStart(Shape shape)
```


Called when enumeration of a shape has started.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| shape | [Shape](../../com.aspose.words/shape) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitSmartTagEnd(SmartTag smartTag) {#visitSmartTagEnd-com.aspose.words.SmartTag-}
```
public int visitSmartTagEnd(SmartTag smartTag)
```


Called when enumeration of a smart tag has ended.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| smartTag | [SmartTag](../../com.aspose.words/smarttag) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitSmartTagStart(SmartTag smartTag) {#visitSmartTagStart-com.aspose.words.SmartTag-}
```
public int visitSmartTagStart(SmartTag smartTag)
```


Called when enumeration of a smart tag has started.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| smartTag | [SmartTag](../../com.aspose.words/smarttag) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitSpecialChar(SpecialChar specialChar) {#visitSpecialChar-com.aspose.words.SpecialChar-}
```
public int visitSpecialChar(SpecialChar specialChar)
```


Called when a [SpecialChar](../../com.aspose.words/specialchar) node is encountered in the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| specialChar | [SpecialChar](../../com.aspose.words/specialchar) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants. This method is not be called for generic control characters (see [ControlChar](../../com.aspose.words/controlchar)) that can be present in the document.
### visitStructuredDocumentTagEnd(StructuredDocumentTag sdt) {#visitStructuredDocumentTagEnd-com.aspose.words.StructuredDocumentTag-}
```
public int visitStructuredDocumentTagEnd(StructuredDocumentTag sdt)
```


Called when enumeration of a structured document tag has ended.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sdt | [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd) {#visitStructuredDocumentTagRangeEnd-com.aspose.words.StructuredDocumentTagRangeEnd-}
```
public int visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sdtRangeEnd | [StructuredDocumentTagRangeEnd](../../com.aspose.words/structureddocumenttagrangeend) |  |

**Returns:**
int
### visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart) {#visitStructuredDocumentTagRangeStart-com.aspose.words.StructuredDocumentTagRangeStart-}
```
public int visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sdtRangeStart | [StructuredDocumentTagRangeStart](../../com.aspose.words/structureddocumenttagrangestart) |  |

**Returns:**
int
### visitStructuredDocumentTagStart(StructuredDocumentTag sdt) {#visitStructuredDocumentTagStart-com.aspose.words.StructuredDocumentTag-}
```
public int visitStructuredDocumentTagStart(StructuredDocumentTag sdt)
```


Called when enumeration of a structured document tag has started.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sdt | [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitSubDocument(SubDocument subDocument) {#visitSubDocument-com.aspose.words.SubDocument-}
```
public int visitSubDocument(SubDocument subDocument)
```


Called when a subDocument is encountered.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| subDocument | [SubDocument](../../com.aspose.words/subdocument) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitTableEnd(Table table) {#visitTableEnd-com.aspose.words.Table-}
```
public int visitTableEnd(Table table)
```


Called when enumeration of a table has ended.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| table | [Table](../../com.aspose.words/table) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### visitTableStart(Table table) {#visitTableStart-com.aspose.words.Table-}
```
public int visitTableStart(Table table)
```


Called when enumeration of a table has started.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| table | [Table](../../com.aspose.words/table) | The object that is being visited. |

**Returns:**
int - A [VisitorAction](../../com.aspose.words/visitoraction) value that specifies how to continue the enumeration. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction) constants.
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

