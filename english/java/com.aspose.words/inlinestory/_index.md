---
title: InlineStory
second_title: Aspose.Words for Java API Reference
description: Base class for inline-level nodes that can contain paragraphs and tables.
type: docs
weight: 350
url: /java/com.aspose.words/inlinestory/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode)
```
public abstract class InlineStory extends CompositeNode
```

Base class for inline-level nodes that can contain paragraphs and tables.

To learn more, visit the **Logical Levels of Nodes in a Document** documentation article.

**InlineStory** is a container for block-level nodes [Paragraph](../../com.aspose.words/paragraph) and [Table](../../com.aspose.words/table).

The classes that derive from **InlineStory** are inline-level nodes that can contain their own text (paragraphs and tables). For example, a **Comment** node contains text of a comment and a **Footnote** contains text of a footnote.
## Constructors

| Constructor | Description |
| --- | --- |
| [InlineStory()](#InlineStory--) |  |
## Methods

| Method | Description |
| --- | --- |
| [getStoryType()](#getStoryType--) | Returns the type of the story. |
| [getParentParagraph()](#getParentParagraph--) | Retrieves the parent [Paragraph](../../com.aspose.words/paragraph) of this node. |
| [getFirstParagraph()](#getFirstParagraph--) | Gets the first paragraph in the story. |
| [getLastParagraph()](#getLastParagraph--) | Gets the last paragraph in the story. |
| [getParagraphs()](#getParagraphs--) | Gets a collection of paragraphs that are immediate children of the story. |
| [getTables()](#getTables--) | Gets a collection of tables that are immediate children of the story. |
| [isInsertRevision()](#isInsertRevision--) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [isDeleteRevision()](#isDeleteRevision--) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [isMoveFromRevision()](#isMoveFromRevision--) | Returns **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [isMoveToRevision()](#isMoveToRevision--) | Returns **true** if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [getFont()](#getFont--) | Provides access to the font formatting of the anchor character of this object. |
| [ensureMinimum()](#ensureMinimum--) | If the last child is not a paragraph, creates and appends one empty paragraph. |
| [getParentParagraph_IInline()](#getParentParagraph-IInline--) |  |
| [getDocument_IInline()](#getDocument-IInline--) |  |
| [getDirectRunAttr(int fontAttr)](#getDirectRunAttr-int-) |  |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int-) |  |
| [setRunAttr(int fontAttr, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [clearRunAttrs()](#clearRunAttrs--) |  |
### InlineStory() {#InlineStory--}
```
public InlineStory()
```


### getStoryType() {#getStoryType--}
```
public abstract int getStoryType()
```


Returns the type of the story.

**Returns:**
int - The type of the story. The returned value is one of [StoryType](../../com.aspose.words/storytype) constants.
### getParentParagraph() {#getParentParagraph--}
```
public Paragraph getParentParagraph()
```


Retrieves the parent [Paragraph](../../com.aspose.words/paragraph) of this node.

**Returns:**
[Paragraph](../../com.aspose.words/paragraph) - The corresponding [Paragraph](../../com.aspose.words/paragraph) value.
### getFirstParagraph() {#getFirstParagraph--}
```
public Paragraph getFirstParagraph()
```


Gets the first paragraph in the story.

**Returns:**
[Paragraph](../../com.aspose.words/paragraph) - The first paragraph in the story.
### getLastParagraph() {#getLastParagraph--}
```
public Paragraph getLastParagraph()
```


Gets the last paragraph in the story.

**Returns:**
[Paragraph](../../com.aspose.words/paragraph) - The last paragraph in the story.
### getParagraphs() {#getParagraphs--}
```
public ParagraphCollection getParagraphs()
```


Gets a collection of paragraphs that are immediate children of the story.

**Returns:**
[ParagraphCollection](../../com.aspose.words/paragraphcollection) - A collection of paragraphs that are immediate children of the story.
### getTables() {#getTables--}
```
public TableCollection getTables()
```


Gets a collection of tables that are immediate children of the story.

**Returns:**
[TableCollection](../../com.aspose.words/tablecollection) - A collection of tables that are immediate children of the story.
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
### getFont() {#getFont--}
```
public Font getFont()
```


Provides access to the font formatting of the anchor character of this object.

**Returns:**
[Font](../../com.aspose.words/font) - The corresponding [Font](../../com.aspose.words/font) value.
### ensureMinimum() {#ensureMinimum--}
```
public void ensureMinimum()
```


If the last child is not a paragraph, creates and appends one empty paragraph.

### getParentParagraph_IInline() {#getParentParagraph-IInline--}
```
public Paragraph getParentParagraph_IInline()
```




**Returns:**
[Paragraph](../../com.aspose.words/paragraph)
### getDocument_IInline() {#getDocument-IInline--}
```
public DocumentBase getDocument_IInline()
```




**Returns:**
[DocumentBase](../../com.aspose.words/documentbase)
### getDirectRunAttr(int fontAttr) {#getDirectRunAttr-int-}
```
public Object getDirectRunAttr(int fontAttr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRunAttr(int fontAttr) {#fetchInheritedRunAttr-int-}
```
public Object fetchInheritedRunAttr(int fontAttr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |

**Returns:**
java.lang.Object
### setRunAttr(int fontAttr, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int fontAttr, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |
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




