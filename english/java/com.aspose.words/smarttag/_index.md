---
title: SmartTag
second_title: Aspose.Words for Java API Reference
description: This element specifies the presence of a smart tag around one or more inline structures runs images fieldsetc. within a paragraph.
type: docs
weight: 526
url: /java/com.aspose.words/smarttag/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode)
```
public class SmartTag extends CompositeNode
```

This element specifies the presence of a smart tag around one or more inline structures (runs, images, fields,etc.) within a paragraph.

To learn more, visit the **Structured Document Tags or Content Control** documentation article.

Smart tags is a kind of custom XML markup. Smart tags provide a facility for embedding customer-defined semantics into the document via the ability to provide a basic namespace/name for a run or set of runs within a document.

[SmartTag](../../com.aspose.words/smarttag) can be a child of a [Paragraph](../../com.aspose.words/paragraph) or another [SmartTag](../../com.aspose.words/smarttag) node.

The complete list of child nodes that can occur inside a smart tag consists of [BookmarkStart](../../com.aspose.words/bookmarkstart), [BookmarkEnd](../../com.aspose.words/bookmarkend), [FieldStart](../../com.aspose.words/fieldstart), [FieldSeparator](../../com.aspose.words/fieldseparator), [FieldEnd](../../com.aspose.words/fieldend), [FormField](../../com.aspose.words/formfield), [Comment](../../com.aspose.words/comment), [Footnote](../../com.aspose.words/footnote), [Run](../../com.aspose.words/run), [SpecialChar](../../com.aspose.words/specialchar), [Shape](../../com.aspose.words/shape), [GroupShape](../../com.aspose.words/groupshape), [CommentRangeStart](../../com.aspose.words/commentrangestart), [CommentRangeEnd](../../com.aspose.words/commentrangeend), [SmartTag](../../com.aspose.words/smarttag).
## Constructors

| Constructor | Description |
| --- | --- |
| [SmartTag(DocumentBase doc)](#SmartTag-com.aspose.words.DocumentBase-) | Initializes a new instance of the [SmartTag](../../com.aspose.words/smarttag) class. |
## Methods

| Method | Description |
| --- | --- |
| [getNodeType()](#getNodeType--) | Returns **NodeType.SmartTag**. |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
| [getElement()](#getElement--) | Specifies the name of the smart tag within the document. |
| [setElement(String value)](#setElement-java.lang.String-) | Specifies the name of the smart tag within the document. |
| [getUri()](#getUri--) | Specifies the namespace URI of the smart tag. |
| [setUri(String value)](#setUri-java.lang.String-) | Specifies the namespace URI of the smart tag. |
| [getProperties()](#getProperties--) | A collection of the smart tag properties. |
| [getLevel_IMarkupNode()](#getLevel-IMarkupNode--) |  |
### SmartTag(DocumentBase doc) {#SmartTag-com.aspose.words.DocumentBase-}
```
public SmartTag(DocumentBase doc)
```


Initializes a new instance of the [SmartTag](../../com.aspose.words/smarttag) class.

When you create a new node, you need to specify a document to which the node belongs. A node cannot exist without a document because it depends on the document-wide structures such as lists and styles. Although a node always belongs to a document, a node might or might not be a part of the document tree.

When a node is created, it belongs to a document, but is not yet part of the document tree and [Node.getParentNode()](../../com.aspose.words/node\#getParentNode--) is null. To insert a node into the document, use the [CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertAfter-com.aspose.words.Node--com.aspose.words.Node-) or [CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertBefore-com.aspose.words.Node--com.aspose.words.Node-) methods on the parent node.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) | The owner document. |

### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns **NodeType.SmartTag**.

**Returns:**
int - **NodeType.SmartTag**. The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
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
boolean - True if all nodes were visited; false if DocumentVisitor stopped the operation before visiting all nodes. Calls [DocumentVisitor.visitSmartTagStart(com.aspose.words.SmartTag)](../../com.aspose.words/documentvisitor\#visitSmartTagStart-com.aspose.words.SmartTag-), then calls [Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node\#accept-com.aspose.words.DocumentVisitor-) for all child nodes of the smart tag and calls [DocumentVisitor.visitSmartTagEnd(com.aspose.words.SmartTag)](../../com.aspose.words/documentvisitor\#visitSmartTagEnd-com.aspose.words.SmartTag-) at the end.
### getElement() {#getElement--}
```
public String getElement()
```


Specifies the name of the smart tag within the document.

Cannot be null.

Default is empty string.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setElement(String value) {#setElement-java.lang.String-}
```
public void setElement(String value)
```


Specifies the name of the smart tag within the document.

Cannot be null.

Default is empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getUri() {#getUri--}
```
public String getUri()
```


Specifies the namespace URI of the smart tag.

Cannot be null.

Default is empty string.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setUri(String value) {#setUri-java.lang.String-}
```
public void setUri(String value)
```


Specifies the namespace URI of the smart tag.

Cannot be null.

Default is empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getProperties() {#getProperties--}
```
public CustomXmlPropertyCollection getProperties()
```


A collection of the smart tag properties.

Cannot be null.

**Returns:**
[CustomXmlPropertyCollection](../../com.aspose.words/customxmlpropertycollection) - The corresponding [CustomXmlPropertyCollection](../../com.aspose.words/customxmlpropertycollection) value.
### getLevel_IMarkupNode() {#getLevel-IMarkupNode--}
```
public int getLevel_IMarkupNode()
```




**Returns:**
int
