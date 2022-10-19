---
title: OfficeMath
second_title: Aspose.Words for Java API Reference
description: Represents an Office Math object such as function equation matrix or alike.
type: docs
weight: 420
url: /java/com.aspose.words/officemath/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode)
```
public class OfficeMath extends CompositeNode
```

Represents an Office Math object such as function, equation, matrix or alike. Can contain child elements including runs of mathematical text, bookmarks, comments, other [OfficeMath](../../com.aspose.words/officemath) instances and some other nodes.

To learn more, visit the **Working with OfficeMath** documentation article.

In this version of Aspose.Words, [OfficeMath](../../com.aspose.words/officemath) nodes do not provide public methods and properties to create or modify a OfficeMath object. In this version you are not able to instantiate **N:Aspose.Words.Math** nodes or modify existing except deleting them.

[OfficeMath](../../com.aspose.words/officemath) can only be a child of [Paragraph](../../com.aspose.words/paragraph).
## Methods

| Method | Description |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
| [getMathRenderer()](#getMathRenderer--) | Creates and returns an object that can be used to render this equation into an image. |
| [getDirectRunAttr(int fontAttr)](#getDirectRunAttr-int-) |  |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int-) |  |
| [setRunAttr(int fontAttr, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [getNodeType()](#getNodeType--) | Returns **NodeType.OfficeMath**. |
| [getParentParagraph()](#getParentParagraph--) | Retrieves the parent [Paragraph](../../com.aspose.words/paragraph) of this node. |
| [getParentParagraph_IInline()](#getParentParagraph-IInline--) |  |
| [getDocument_IInline()](#getDocument-IInline--) |  |
| [getMathObjectType()](#getMathObjectType--) | Gets type [getMathObjectType()](../../com.aspose.words/officemath\#getMathObjectType--) of this Office Math object. |
| [getEquationXmlEncoding()](#getEquationXmlEncoding--) | Gets/sets an encoding that was used to encode equation XML, if this office math object is read from equation XML. |
| [setEquationXmlEncoding(Charset value)](#setEquationXmlEncoding-java.nio.charset.Charset-) | Gets/sets an encoding that was used to encode equation XML, if this office math object is read from equation XML. |
| [getJustification()](#getJustification--) | Gets/sets Office Math justification. |
| [setJustification(int value)](#setJustification-int-) | Gets/sets Office Math justification. |
| [getDisplayType()](#getDisplayType--) | Gets/sets Office Math display format type which represents whether an equation is displayed inline with the text or displayed on its own line. |
| [setDisplayType(int value)](#setDisplayType-int-) | Gets/sets Office Math display format type which represents whether an equation is displayed inline with the text or displayed on its own line. |
| [removeMoveRevisions()](#removeMoveRevisions--) |  |
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
boolean - True if all nodes were visited; false if DocumentVisitor stopped the operation before visiting all nodes. Calls [DocumentVisitor.visitOfficeMathStart(com.aspose.words.OfficeMath)](../../com.aspose.words/documentvisitor\#visitOfficeMathStart-com.aspose.words.OfficeMath-), then calls [Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node\#accept-com.aspose.words.DocumentVisitor-) for all child nodes of the Office Math and calls [DocumentVisitor.visitOfficeMathEnd(com.aspose.words.OfficeMath)](../../com.aspose.words/documentvisitor\#visitOfficeMathEnd-com.aspose.words.OfficeMath-) at the end.
### getMathRenderer() {#getMathRenderer--}
```
public OfficeMathRenderer getMathRenderer()
```


Creates and returns an object that can be used to render this equation into an image.

This method just invokes the [OfficeMathRenderer](../../com.aspose.words/officemathrenderer) constructor and passes this object as a parameter.

**Returns:**
[OfficeMathRenderer](../../com.aspose.words/officemathrenderer) - The renderer object for this equation.
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




### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns **NodeType.OfficeMath**.

**Returns:**
int - **NodeType.OfficeMath**. The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### getParentParagraph() {#getParentParagraph--}
```
public Paragraph getParentParagraph()
```


Retrieves the parent [Paragraph](../../com.aspose.words/paragraph) of this node.

**Returns:**
[Paragraph](../../com.aspose.words/paragraph) - The corresponding [Paragraph](../../com.aspose.words/paragraph) value.
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
### getMathObjectType() {#getMathObjectType--}
```
public int getMathObjectType()
```


Gets type [getMathObjectType()](../../com.aspose.words/officemath\#getMathObjectType--) of this Office Math object.

**Returns:**
int - Type [getMathObjectType()](../../com.aspose.words/officemath\#getMathObjectType--) of this Office Math object. The returned value is one of [MathObjectType](../../com.aspose.words/mathobjecttype) constants.
### getEquationXmlEncoding() {#getEquationXmlEncoding--}
```
public Charset getEquationXmlEncoding()
```


Gets/sets an encoding that was used to encode equation XML, if this office math object is read from equation XML. We use the encoding on saving a document to write in same encoding that it was read.

**Returns:**
java.nio.charset.Charset - The corresponding java.nio.charset.Charset value.
### setEquationXmlEncoding(Charset value) {#setEquationXmlEncoding-java.nio.charset.Charset-}
```
public void setEquationXmlEncoding(Charset value)
```


Gets/sets an encoding that was used to encode equation XML, if this office math object is read from equation XML. We use the encoding on saving a document to write in same encoding that it was read.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.nio.charset.Charset | The corresponding java.nio.charset.Charset value. |

### getJustification() {#getJustification--}
```
public int getJustification()
```


Gets/sets Office Math justification.

Justification cannot be set to the Office Math with display format type [OfficeMathDisplayType.INLINE](../../com.aspose.words/officemathdisplaytype\#INLINE).

Inline justification cannot be set to the Office Math with display format type [OfficeMathDisplayType.DISPLAY](../../com.aspose.words/officemathdisplaytype\#DISPLAY).

Corresponding [getDisplayType()](../../com.aspose.words/officemath\#getDisplayType--) / [setDisplayType(int)](../../com.aspose.words/officemath\#setDisplayType-int-) has to be set before setting Office Math justification.

**Returns:**
int - The corresponding  int  value. The returned value is one of [OfficeMathJustification](../../com.aspose.words/officemathjustification) constants.
### setJustification(int value) {#setJustification-int-}
```
public void setJustification(int value)
```


Gets/sets Office Math justification.

Justification cannot be set to the Office Math with display format type [OfficeMathDisplayType.INLINE](../../com.aspose.words/officemathdisplaytype\#INLINE).

Inline justification cannot be set to the Office Math with display format type [OfficeMathDisplayType.DISPLAY](../../com.aspose.words/officemathdisplaytype\#DISPLAY).

Corresponding [getDisplayType()](../../com.aspose.words/officemath\#getDisplayType--) / [setDisplayType(int)](../../com.aspose.words/officemath\#setDisplayType-int-) has to be set before setting Office Math justification.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [OfficeMathJustification](../../com.aspose.words/officemathjustification) constants. |

### getDisplayType() {#getDisplayType--}
```
public int getDisplayType()
```


Gets/sets Office Math display format type which represents whether an equation is displayed inline with the text or displayed on its own line.

Display format type has effect for top level Office Math only.

Returned display format type is always [OfficeMathDisplayType.INLINE](../../com.aspose.words/officemathdisplaytype\#INLINE) for nested Office Math.

**Returns:**
int - The corresponding  int  value. The returned value is one of [OfficeMathDisplayType](../../com.aspose.words/officemathdisplaytype) constants.
### setDisplayType(int value) {#setDisplayType-int-}
```
public void setDisplayType(int value)
```


Gets/sets Office Math display format type which represents whether an equation is displayed inline with the text or displayed on its own line.

Display format type has effect for top level Office Math only.

Returned display format type is always [OfficeMathDisplayType.INLINE](../../com.aspose.words/officemathdisplaytype\#INLINE) for nested Office Math.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [OfficeMathDisplayType](../../com.aspose.words/officemathdisplaytype) constants. |

### removeMoveRevisions() {#removeMoveRevisions--}
```
public void removeMoveRevisions()
```




