---
title: Paragraph
second_title: Aspose.Words for Java API Reference
description: Represents a paragraph of text.
type: docs
weight: 443
url: /java/com.aspose.words/paragraph/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode)
```
public class Paragraph extends CompositeNode
```

Represents a paragraph of text.

To learn more, visit the **Working with Paragraphs** documentation article.

[Paragraph](../../com.aspose.words/paragraph) is a block-level node and can be a child of classes derived from [Story](../../com.aspose.words/story) or [InlineStory](../../com.aspose.words/inlinestory).

[Paragraph](../../com.aspose.words/paragraph) can contain any number of inline-level nodes and bookmarks.

The complete list of child nodes that can occur inside a paragraph consists of [BookmarkStart](../../com.aspose.words/bookmarkstart), [BookmarkEnd](../../com.aspose.words/bookmarkend), [FieldStart](../../com.aspose.words/fieldstart), [FieldSeparator](../../com.aspose.words/fieldseparator), [FieldEnd](../../com.aspose.words/fieldend), [FormField](../../com.aspose.words/formfield), [Comment](../../com.aspose.words/comment), [Footnote](../../com.aspose.words/footnote), [Run](../../com.aspose.words/run), [SpecialChar](../../com.aspose.words/specialchar), [Shape](../../com.aspose.words/shape), [GroupShape](../../com.aspose.words/groupshape), [SmartTag](../../com.aspose.words/smarttag).

A valid paragraph in Microsoft Word always ends with a paragraph break character and a minimal valid paragraph consists just of a paragraph break. The **Paragraph** class automatically appends the appropriate paragraph break character at the end and this character is not part of the child nodes of the **Paragraph**, therefore a **Paragraph** can be empty.

Do not include the end of paragraph [ControlChar.PARAGRAPH\_BREAK](../../com.aspose.words/controlchar\#PARAGRAPH-BREAK) or end of cell [ControlChar.CELL](../../com.aspose.words/controlchar\#CELL) characters inside the text of the paragraph as it might make the paragraph invalid when the document is opened in Microsoft Word.
## Constructors

| Constructor | Description |
| --- | --- |
| [Paragraph(DocumentBase doc)](#Paragraph-com.aspose.words.DocumentBase-) | Initializes a new instance of the **Paragraph** class. |
## Methods

| Method | Description |
| --- | --- |
| [getNodeType()](#getNodeType--) | Returns **NodeType.Paragraph**. |
| [getParentStory()](#getParentStory--) | Retrieves the parent section-level story that can be [Body](../../com.aspose.words/body) or [HeaderFooter](../../com.aspose.words/headerfooter). |
| [getParentSection()](#getParentSection--) | Retrieves the parent [Section](../../com.aspose.words/section) of the paragraph. |
| [isInCell()](#isInCell--) | True if this paragraph is an immediate child of [Cell](../../com.aspose.words/cell); false otherwise. |
| [isEndOfCell()](#isEndOfCell--) | True if this paragraph is the last paragraph in a [Cell](../../com.aspose.words/cell); false otherwise. |
| [getBreakIsStyleSeparator()](#getBreakIsStyleSeparator--) | True if this paragraph break is a Style Separator. |
| [isEndOfSection()](#isEndOfSection--) | True if this paragraph is the last paragraph in the **Body** (main text story) of a **Section**; false otherwise. |
| [isEndOfHeaderFooter()](#isEndOfHeaderFooter--) | True if this paragraph is the last paragraph in the **HeaderFooter** (main text story) of a **Section**; false otherwise. |
| [isEndOfDocument()](#isEndOfDocument--) | True if this paragraph is the last paragraph in the last section of the document. |
| [getParagraphFormat()](#getParagraphFormat--) | Provides access to the paragraph formatting properties. |
| [getListFormat()](#getListFormat--) | Provides access to the list formatting properties of the paragraph. |
| [getFrameFormat()](#getFrameFormat--) | Provides access to the paragraph formatting properties. |
| [getListLabel()](#getListLabel--) | Gets a [getListLabel()](../../com.aspose.words/paragraph\#getListLabel--) object that provides access to list numbering value and formatting for this paragraph. |
| [getRuns()](#getRuns--) | Provides access to the typed collection of pieces of text inside the paragraph. |
| [getParagraphBreakFont()](#getParagraphBreakFont--) | Provides access to the font formatting of the paragraph break character. |
| [isInsertRevision()](#isInsertRevision--) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [isDeleteRevision()](#isDeleteRevision--) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [isMoveFromRevision()](#isMoveFromRevision--) | Returns **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [isMoveToRevision()](#isMoveToRevision--) | Returns **true** if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [isFormatRevision()](#isFormatRevision--) | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled. |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
| [getText()](#getText--) | Gets the text of this paragraph including the end of paragraph character. |
| [getDirectParaAttr(int key)](#getDirectParaAttr-int-) |  |
| [getDirectParaAttr(int key, int revisionsView)](#getDirectParaAttr-int-int-) |  |
| [fetchInheritedParaAttr(int key)](#fetchInheritedParaAttr-int-) |  |
| [fetchParaAttr(int key)](#fetchParaAttr-int-) |  |
| [setParaAttr(int key, Object value)](#setParaAttr-int-java.lang.Object-) |  |
| [removeParaAttr(int key)](#removeParaAttr-int-) |  |
| [clearParaAttrs()](#clearParaAttrs--) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int-) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int-) |  |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [removeMoveRevisions()](#removeMoveRevisions--) |  |
| [isListItem()](#isListItem--) | True when the paragraph is an item in a bulleted or numbered list in original revision. |
| [getEffectiveTabStops()](#getEffectiveTabStops--) | Returns array of all tab stops applied to this paragraph, including applied indirectly by styles or lists. |
| [joinRunsWithSameFormatting()](#joinRunsWithSameFormatting--) | Joins runs with the same formatting in the paragraph. |
| [appendField(int fieldType, boolean updateField)](#appendField-int-boolean-) |  |
| [appendField(String fieldCode)](#appendField-java.lang.String-) | Appends a Word field to this paragraph. |
| [appendField(String fieldCode, String fieldValue)](#appendField-java.lang.String-java.lang.String-) | Appends a Word field to this paragraph. |
| [insertField(int fieldType, boolean updateField, Node refNode, boolean isAfter)](#insertField-int-boolean-com.aspose.words.Node-boolean-) |  |
| [insertField(String fieldCode, Node refNode, boolean isAfter)](#insertField-java.lang.String-com.aspose.words.Node-boolean-) | Inserts a Word field into this paragraph. |
| [insertField(String fieldCode, String fieldValue, Node refNode, boolean isAfter)](#insertField-java.lang.String-java.lang.String-com.aspose.words.Node-boolean-) | Inserts a Word field into this paragraph. |
### Paragraph(DocumentBase doc) {#Paragraph-com.aspose.words.DocumentBase-}
```
public Paragraph(DocumentBase doc)
```


Initializes a new instance of the **Paragraph** class.

When **Paragraph** is created, it belongs to the specified document, but is not yet part of the document and **ParentNode** is null.

To append **Paragraph** to the document use InsertAfter or InsertBefore on the story where you want the paragraph inserted.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) | The owner document. |

### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns **NodeType.Paragraph**.

**Returns:**
int - **NodeType.Paragraph**. The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### getParentStory() {#getParentStory--}
```
public Story getParentStory()
```


Retrieves the parent section-level story that can be [Body](../../com.aspose.words/body) or [HeaderFooter](../../com.aspose.words/headerfooter).

**Returns:**
[Story](../../com.aspose.words/story) - The corresponding [Story](../../com.aspose.words/story) value.
### getParentSection() {#getParentSection--}
```
public Section getParentSection()
```


Retrieves the parent [Section](../../com.aspose.words/section) of the paragraph.

**Returns:**
[Section](../../com.aspose.words/section) - The corresponding [Section](../../com.aspose.words/section) value.
### isInCell() {#isInCell--}
```
public boolean isInCell()
```


True if this paragraph is an immediate child of [Cell](../../com.aspose.words/cell); false otherwise.

**Returns:**
boolean - The corresponding  boolean  value.
### isEndOfCell() {#isEndOfCell--}
```
public boolean isEndOfCell()
```


True if this paragraph is the last paragraph in a [Cell](../../com.aspose.words/cell); false otherwise.

**Returns:**
boolean - The corresponding  boolean  value.
### getBreakIsStyleSeparator() {#getBreakIsStyleSeparator--}
```
public boolean getBreakIsStyleSeparator()
```


True if this paragraph break is a Style Separator. A style separator allows one paragraph to consist of parts that have different paragraph styles.

**Returns:**
boolean - The corresponding  boolean  value.
### isEndOfSection() {#isEndOfSection--}
```
public boolean isEndOfSection()
```


True if this paragraph is the last paragraph in the **Body** (main text story) of a **Section**; false otherwise.

**Returns:**
boolean - The corresponding  boolean  value.
### isEndOfHeaderFooter() {#isEndOfHeaderFooter--}
```
public boolean isEndOfHeaderFooter()
```


True if this paragraph is the last paragraph in the **HeaderFooter** (main text story) of a **Section**; false otherwise.

**Returns:**
boolean - The corresponding  boolean  value.
### isEndOfDocument() {#isEndOfDocument--}
```
public boolean isEndOfDocument()
```


True if this paragraph is the last paragraph in the last section of the document.

**Returns:**
boolean - The corresponding  boolean  value.
### getParagraphFormat() {#getParagraphFormat--}
```
public ParagraphFormat getParagraphFormat()
```


Provides access to the paragraph formatting properties.

**Returns:**
[ParagraphFormat](../../com.aspose.words/paragraphformat) - The corresponding [ParagraphFormat](../../com.aspose.words/paragraphformat) value.
### getListFormat() {#getListFormat--}
```
public ListFormat getListFormat()
```


Provides access to the list formatting properties of the paragraph.

**Returns:**
[ListFormat](../../com.aspose.words/listformat) - The corresponding [ListFormat](../../com.aspose.words/listformat) value.
### getFrameFormat() {#getFrameFormat--}
```
public FrameFormat getFrameFormat()
```


Provides access to the paragraph formatting properties.

**Returns:**
[FrameFormat](../../com.aspose.words/frameformat) - The corresponding [FrameFormat](../../com.aspose.words/frameformat) value.
### getListLabel() {#getListLabel--}
```
public ListLabel getListLabel()
```


Gets a [getListLabel()](../../com.aspose.words/paragraph\#getListLabel--) object that provides access to list numbering value and formatting for this paragraph.

**Returns:**
[ListLabel](../../com.aspose.words/listlabel) - A [getListLabel()](../../com.aspose.words/paragraph\#getListLabel--) object that provides access to list numbering value and formatting for this paragraph.
### getRuns() {#getRuns--}
```
public RunCollection getRuns()
```


Provides access to the typed collection of pieces of text inside the paragraph.

**Returns:**
[RunCollection](../../com.aspose.words/runcollection) - The corresponding [RunCollection](../../com.aspose.words/runcollection) value.
### getParagraphBreakFont() {#getParagraphBreakFont--}
```
public Font getParagraphBreakFont()
```


Provides access to the font formatting of the paragraph break character.

**Returns:**
[Font](../../com.aspose.words/font) - The corresponding [Font](../../com.aspose.words/font) value.
### isInsertRevision() {#isInsertRevision--}
```
public boolean isInsertRevision()
```


Returns true if this object was inserted in Microsoft Word while change tracking was enabled.

**Returns:**
boolean - True if this object was inserted in Microsoft Word while change tracking was enabled.
### isDeleteRevision() {#isDeleteRevision--}
```
public boolean isDeleteRevision()
```


Returns true if this object was deleted in Microsoft Word while change tracking was enabled.

**Returns:**
boolean - True if this object was deleted in Microsoft Word while change tracking was enabled.
### isMoveFromRevision() {#isMoveFromRevision--}
```
public boolean isMoveFromRevision()
```


Returns **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled.

**Returns:**
boolean - **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled.
### isMoveToRevision() {#isMoveToRevision--}
```
public boolean isMoveToRevision()
```


Returns **true** if this object was moved (inserted) in Microsoft Word while change tracking was enabled.

**Returns:**
boolean - **true** if this object was moved (inserted) in Microsoft Word while change tracking was enabled.
### isFormatRevision() {#isFormatRevision--}
```
public boolean isFormatRevision()
```


Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled.

**Returns:**
boolean - True if formatting of the object was changed in Microsoft Word while change tracking was enabled.
### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public boolean accept(DocumentVisitor visitor)
```


Accepts a visitor.

Enumerates over this node and all of its children. Each node calls a corresponding method on DocumentVisitor.

For more info see the Visitor design pattern.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | The visitor that will visit the nodes. |

**Returns:**
boolean - True if all nodes were visited; false if DocumentVisitor stopped the operation before visiting all nodes. Calls DocumentVisitor.VisitParagraphStart, then calls Accept for all child nodes of the paragraph and calls DocumentVisitor.VisitParagraphEnd at the end.
### getText() {#getText--}
```
public String getText()
```


Gets the text of this paragraph including the end of paragraph character.

The text of all child nodes is concatenated and the end of paragraph character is appended as follows:

 *  If the paragraph is the last paragraph of [Body](../../com.aspose.words/body), then [ControlChar.SECTION\_BREAK](../../com.aspose.words/controlchar\#SECTION-BREAK) (\\x000c) is appended.
 *  If the paragraph is the last paragraph of [Cell](../../com.aspose.words/cell), then [ControlChar.CELL](../../com.aspose.words/controlchar\#CELL) (\\x0007) is appended.
 *  For all other paragraphs [ControlChar.PARAGRAPH\_BREAK](../../com.aspose.words/controlchar\#PARAGRAPH-BREAK) (\\r) is appended.

The returned string includes all control and special characters as described in [ControlChar](../../com.aspose.words/controlchar).

**Returns:**
java.lang.String
### getDirectParaAttr(int key) {#getDirectParaAttr-int-}
```
public Object getDirectParaAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectParaAttr(int key, int revisionsView) {#getDirectParaAttr-int-int-}
```
public Object getDirectParaAttr(int key, int revisionsView)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### fetchInheritedParaAttr(int key) {#fetchInheritedParaAttr-int-}
```
public Object fetchInheritedParaAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchParaAttr(int key) {#fetchParaAttr-int-}
```
public Object fetchParaAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### setParaAttr(int key, Object value) {#setParaAttr-int-java.lang.Object-}
```
public void setParaAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### removeParaAttr(int key) {#removeParaAttr-int-}
```
public void removeParaAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

### clearParaAttrs() {#clearParaAttrs--}
```
public void clearParaAttrs()
```




### getDirectRunAttr(int key) {#getDirectRunAttr-int-}
```
public Object getDirectRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRunAttr(int key) {#fetchInheritedRunAttr-int-}
```
public Object fetchInheritedRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### removeRunAttr(int key) {#removeRunAttr-int-}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

### clearRunAttrs() {#clearRunAttrs--}
```
public void clearRunAttrs()
```




### removeMoveRevisions() {#removeMoveRevisions--}
```
public void removeMoveRevisions()
```




### isListItem() {#isListItem--}
```
public boolean isListItem()
```


True when the paragraph is an item in a bulleted or numbered list in original revision.

**Returns:**
boolean - The corresponding  boolean  value.
### getEffectiveTabStops() {#getEffectiveTabStops--}
```
public TabStop[] getEffectiveTabStops()
```


Returns array of all tab stops applied to this paragraph, including applied indirectly by styles or lists.

**Returns:**
com.aspose.words.TabStop[]
### joinRunsWithSameFormatting() {#joinRunsWithSameFormatting--}
```
public int joinRunsWithSameFormatting()
```


Joins runs with the same formatting in the paragraph.

**Returns:**
int - Number of joins performed. When **N** adjacent runs are being joined they count as **N - 1** joins.
### appendField(int fieldType, boolean updateField) {#appendField-int-boolean-}
```
public Field appendField(int fieldType, boolean updateField)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldType | int |  |
| updateField | boolean |  |

**Returns:**
[Field](../../com.aspose.words/field)
### appendField(String fieldCode) {#appendField-java.lang.String-}
```
public Field appendField(String fieldCode)
```


Appends a Word field to this paragraph.  Appends a field to this paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | java.lang.String | The field code to append (without curly braces). |

**Returns:**
[Field](../../com.aspose.words/field) - A [Field](../../com.aspose.words/field) object that represents the appended field.
### appendField(String fieldCode, String fieldValue) {#appendField-java.lang.String-java.lang.String-}
```
public Field appendField(String fieldCode, String fieldValue)
```


Appends a Word field to this paragraph.  Appends a field to this paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | java.lang.String | The field code to append (without curly braces). |
| fieldValue | java.lang.String | The field value to append. Pass null for fields that do not have a value. |

**Returns:**
[Field](../../com.aspose.words/field) - A [Field](../../com.aspose.words/field) object that represents the appended field.
### insertField(int fieldType, boolean updateField, Node refNode, boolean isAfter) {#insertField-int-boolean-com.aspose.words.Node-boolean-}
```
public Field insertField(int fieldType, boolean updateField, Node refNode, boolean isAfter)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldType | int |  |
| updateField | boolean |  |
| refNode | [Node](../../com.aspose.words/node) |  |
| isAfter | boolean |  |

**Returns:**
[Field](../../com.aspose.words/field)
### insertField(String fieldCode, Node refNode, boolean isAfter) {#insertField-java.lang.String-com.aspose.words.Node-boolean-}
```
public Field insertField(String fieldCode, Node refNode, boolean isAfter)
```


Inserts a Word field into this paragraph.  Inserts a field into this paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | java.lang.String | The field code to insert (without curly braces). |
| refNode | [Node](../../com.aspose.words/node) | Reference node inside this paragraph (if refNode is null, then appends to the end of the paragraph). |
| isAfter | boolean | Whether to insert the field after or before reference node. |

**Returns:**
[Field](../../com.aspose.words/field) - A [Field](../../com.aspose.words/field) object that represents the inserted field.
### insertField(String fieldCode, String fieldValue, Node refNode, boolean isAfter) {#insertField-java.lang.String-java.lang.String-com.aspose.words.Node-boolean-}
```
public Field insertField(String fieldCode, String fieldValue, Node refNode, boolean isAfter)
```


Inserts a Word field into this paragraph.  Inserts a field into this paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | java.lang.String | The field code to insert (without curly braces). |
| fieldValue | java.lang.String | The field value to insert. Pass null for fields that do not have a value. |
| refNode | [Node](../../com.aspose.words/node) | Reference node inside this paragraph (if refNode is null, then appends to the end of the paragraph). |
| isAfter | boolean | Whether to insert the field after or before reference node. |

**Returns:**
[Field](../../com.aspose.words/field) - A [Field](../../com.aspose.words/field) object that represents the inserted field.
