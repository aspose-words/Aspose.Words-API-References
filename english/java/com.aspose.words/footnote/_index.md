---
title: Footnote
second_title: Aspose.Words for Java API Reference
description: Represents a container for text of a footnote or endnote.
type: docs
weight: 291
url: /java/com.aspose.words/footnote/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode), [com.aspose.words.InlineStory](../../com.aspose.words/inlinestory)
```
public class Footnote extends InlineStory
```

Represents a container for text of a footnote or endnote.

To learn more, visit the **Working with Footnote and Endnote** documentation article.

The **Footnote** class is used to represent both footnotes and endnotes in a Word document.

**Footnote** is an inline-level node and can only be a child of **Paragraph**.

**Footnote** can contain **Paragraph** and **Table** child nodes.
## Constructors

| Constructor | Description |
| --- | --- |
| [Footnote(DocumentBase doc, int footnoteType)](#Footnote-com.aspose.words.DocumentBase-int-) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [getNodeType()](#getNodeType--) | Returns **NodeType.Footnote**. |
| [getStoryType()](#getStoryType--) | Returns **StoryType.Footnotes** or **StoryType.Endnotes**. |
| [getFootnoteType()](#getFootnoteType--) | Returns a value that specifies whether this is a footnote or endnote. |
| [isAuto()](#isAuto--) | Holds a value that specifies whether this is a auto-numbered footnote or footnote with user defined custom reference mark. |
| [isAuto(boolean value)](#isAuto-boolean-) | Holds a value that specifies whether this is a auto-numbered footnote or footnote with user defined custom reference mark. |
| [getReferenceMark()](#getReferenceMark--) | Gets/sets custom reference mark to be used for this footnote. |
| [setReferenceMark(String value)](#setReferenceMark-java.lang.String-) | Gets/sets custom reference mark to be used for this footnote. |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
| [removeMoveRevisions()](#removeMoveRevisions--) |  |
### Footnote(DocumentBase doc, int footnoteType) {#Footnote-com.aspose.words.DocumentBase-int-}
```
public Footnote(DocumentBase doc, int footnoteType)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) |  |
| footnoteType | int |  |

### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns **NodeType.Footnote**.

**Returns:**
int - **NodeType.Footnote**. The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### getStoryType() {#getStoryType--}
```
public int getStoryType()
```


Returns **StoryType.Footnotes** or **StoryType.Endnotes**.

**Returns:**
int - **StoryType.Footnotes** or **StoryType.Endnotes**. The returned value is one of [StoryType](../../com.aspose.words/storytype) constants.
### getFootnoteType() {#getFootnoteType--}
```
public int getFootnoteType()
```


Returns a value that specifies whether this is a footnote or endnote.

**Returns:**
int - A value that specifies whether this is a footnote or endnote. The returned value is one of [FootnoteType](../../com.aspose.words/footnotetype) constants.
### isAuto() {#isAuto--}
```
public boolean isAuto()
```


Holds a value that specifies whether this is a auto-numbered footnote or footnote with user defined custom reference mark. [getReferenceMark()](../../com.aspose.words/footnote\#getReferenceMark--) / [setReferenceMark(java.lang.String)](../../com.aspose.words/footnote\#setReferenceMark-java.lang.String-) initialized with empty string if IsAuto set to false.

**Returns:**
boolean - The corresponding  boolean  value.
### isAuto(boolean value) {#isAuto-boolean-}
```
public void isAuto(boolean value)
```


Holds a value that specifies whether this is a auto-numbered footnote or footnote with user defined custom reference mark. [getReferenceMark()](../../com.aspose.words/footnote\#getReferenceMark--) / [setReferenceMark(java.lang.String)](../../com.aspose.words/footnote\#setReferenceMark-java.lang.String-) initialized with empty string if IsAuto set to false.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getReferenceMark() {#getReferenceMark--}
```
public String getReferenceMark()
```


Gets/sets custom reference mark to be used for this footnote. Default value is **empty string**, meaning auto-numbered footnotes are used.

If this property is set to **empty string** or null, then [isAuto()](../../com.aspose.words/footnote\#isAuto--) / [isAuto(boolean)](../../com.aspose.words/footnote\#isAuto-boolean-) property will automatically be set to true, if set to anything else then [isAuto()](../../com.aspose.words/footnote\#isAuto--) / [isAuto(boolean)](../../com.aspose.words/footnote\#isAuto-boolean-) will be set to false.

RTF-format can only store 1 symbol as custom reference mark, so upon export only the first symbol will be written others will be discard.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setReferenceMark(String value) {#setReferenceMark-java.lang.String-}
```
public void setReferenceMark(String value)
```


Gets/sets custom reference mark to be used for this footnote. Default value is **empty string**, meaning auto-numbered footnotes are used.

If this property is set to **empty string** or null, then [isAuto()](../../com.aspose.words/footnote\#isAuto--) / [isAuto(boolean)](../../com.aspose.words/footnote\#isAuto-boolean-) property will automatically be set to true, if set to anything else then [isAuto()](../../com.aspose.words/footnote\#isAuto--) / [isAuto(boolean)](../../com.aspose.words/footnote\#isAuto-boolean-) will be set to false.

RTF-format can only store 1 symbol as custom reference mark, so upon export only the first symbol will be written others will be discard.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

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
boolean - True if all nodes were visited; false if DocumentVisitor stopped the operation before visiting all nodes. Calls DocumentVisitor.VisitFootnoteStart, then calls Accept for all child nodes of the footnote and calls DocumentVisitor.VisitFootnoteEnd at the end.
### removeMoveRevisions() {#removeMoveRevisions--}
```
public void removeMoveRevisions()
```




