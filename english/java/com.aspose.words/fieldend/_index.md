---
title: FieldEnd
second_title: Aspose.Words for Java API Reference
description: Represents an end of a Word field in a document.
type: docs
weight: 187
url: /java/com.aspose.words/fieldend/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.Inline](../../com.aspose.words/inline), [com.aspose.words.SpecialChar](../../com.aspose.words/specialchar), [com.aspose.words.FieldChar](../../com.aspose.words/fieldchar)
```
public class FieldEnd extends FieldChar
```

Represents an end of a Word field in a document.

To learn more, visit the [ Working with Fields ][Working with Fields] documentation article.

[FieldEnd](../../com.aspose.words/fieldend) is an inline-level node and represented by the [ControlChar.FIELD\_END\_CHAR](../../com.aspose.words/controlchar\#FIELD-END-CHAR) control character in the document.

[FieldEnd](../../com.aspose.words/fieldend) can only be a child of [Paragraph](../../com.aspose.words/paragraph).

A complete field in a Microsoft Word document is a complex structure consisting of a field start character, field code, field separator character, field result and field end character. Some fields only have field start, field code and field end.

To easily insert a new field into a document, use the [DocumentBuilder.insertField(java.lang.String)](../../com.aspose.words/documentbuilder\#insertField-java.lang.String) method.


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Methods

| Method | Description |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor) | Accepts a visitor. |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [dd()](#dd) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean) | Creates a duplicate of the node. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int) |  |
| [getAncestor(int ancestorType)](#getAncestor-int) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class) | Gets the first ancestor of the specified object type. |
| [getClass()](#getClass) |  |
| [getCustomNodeId()](#getCustomNodeId) | Specifies custom node identifier. |
| [getDirectRunAttr(int fontAttr)](#getDirectRunAttr-int) |  |
| [getDocument()](#getDocument) | Gets the document to which this node belongs. |
| [getDocument_IInline()](#getDocument-IInline) |  |
| [getField()](#getField) | Returns a field for the field char. |
| [getFieldType()](#getFieldType) | Returns the type of the field. |
| [getFont()](#getFont) | Provides access to the font formatting of this object. |
| [getNextSibling()](#getNextSibling) | Gets the node immediately following this node. |
| [getNodeType()](#getNodeType) | Returns [NodeType.FIELD\_END](../../com.aspose.words/nodetype\#FIELD-END). |
| [getParentNode()](#getParentNode) | Gets the immediate parent of this node. |
| [getParentParagraph()](#getParentParagraph) | Retrieves the parent [Paragraph](../../com.aspose.words/paragraph) of this node. |
| [getParentParagraph_IInline()](#getParentParagraph-IInline) |  |
| [getPreviousSibling()](#getPreviousSibling) | Gets the node immediately preceding this node. |
| [getRange()](#getRange) | Returns a [Range](../../com.aspose.words/range) object that represents the portion of a document that is contained in this node. |
| [getText()](#getText) | Gets the special character that this node represents. |
| [hasSeparator()](#hasSeparator) | Returns  true  if this field has a separator. |
| [hashCode()](#hashCode) |  |
| [isComposite()](#isComposite) | Returns  true  if this node can contain other nodes. |
| [isDeleteRevision()](#isDeleteRevision) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [isDirty()](#isDirty) | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isDirty(boolean value)](#isDirty-boolean) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isFormatRevision()](#isFormatRevision) | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled. |
| [isInsertRevision()](#isInsertRevision) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [isLocked()](#isLocked) | Gets whether the parent field is locked (should not recalculate its result). |
| [isLocked(boolean value)](#isLocked-boolean) | Sets whether the parent field is locked (should not recalculate its result). |
| [isMoveFromRevision()](#isMoveFromRevision) | Returns  true  if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [isMoveToRevision()](#isMoveToRevision) | Returns  true  if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node) | Gets next node according to the pre-order tree traversal algorithm. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [remove()](#remove) | Removes itself from the parent. |
| [removeMoveRevisions()](#removeMoveRevisions) |  |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [setCustomNodeId(int value)](#setCustomNodeId-int) | Specifies custom node identifier. |
| [setRunAttr(int fontAttr, Object value)](#setRunAttr-int-java.lang.Object) |  |
| [toString()](#toString) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions) | Exports the content of the node into a string using the specified save options. |
| [toString(int saveFormat)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor}
```
public boolean accept(DocumentVisitor visitor)
```


Accepts a visitor.

Calls [DocumentVisitor.visitFieldEnd(com.aspose.words.FieldEnd)](../../com.aspose.words/documentvisitor\#visitFieldEnd-com.aspose.words.FieldEnd).

For more info see the Visitor design pattern.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | The visitor that will visit the node. |

**Returns:**
boolean - **False** if the visitor requested the enumeration to stop.
### clearRunAttrs() {#clearRunAttrs}
```
public void clearRunAttrs()
```




### dd() {#dd}
```
public void dd()
```




### deepClone(boolean isCloneChildren) {#deepClone-boolean}
```
public Node deepClone(boolean isCloneChildren)
```


Creates a duplicate of the node.

This method serves as a copy constructor for nodes. The cloned node has no parent, but belongs to the same document as the original node.

This method always performs a deep copy of the node. The  isCloneChildren  parameter specifies whether to perform copy all child nodes as well.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| isCloneChildren | boolean | True to recursively clone the subtree under the specified node; false to clone only the node itself. |

**Returns:**
[Node](../../com.aspose.words/node) - The cloned node.
### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### fetchInheritedRunAttr(int fontAttr) {#fetchInheritedRunAttr-int}
```
public Object fetchInheritedRunAttr(int fontAttr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |

**Returns:**
java.lang.Object
### getAncestor(int ancestorType) {#getAncestor-int}
```
public CompositeNode getAncestor(int ancestorType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ancestorType | int |  |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode)
### getAncestor(Class ancestorType) {#getAncestor-java.lang.Class}
```
public CompositeNode getAncestor(Class ancestorType)
```


Gets the first ancestor of the specified object type.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ancestorType | java.lang.Class | The object type of the ancestor to retrieve. |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode) - The ancestor of the specified type or  null  if no ancestor of this type was found.

The ancestor type matches if it is equal to  ancestorType  or derived from  ancestorType .
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getCustomNodeId() {#getCustomNodeId}
```
public int getCustomNodeId()
```


Specifies custom node identifier.

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.

**Returns:**
int - The corresponding  int  value.
### getDirectRunAttr(int fontAttr) {#getDirectRunAttr-int}
```
public Object getDirectRunAttr(int fontAttr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |

**Returns:**
java.lang.Object
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Gets the document to which this node belongs.

The node always belongs to a document even if it has just been created and not yet added to the tree, or if it has been removed from the tree.

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase) - The document to which this node belongs.
### getDocument_IInline() {#getDocument-IInline}
```
public DocumentBase getDocument_IInline()
```




**Returns:**
[DocumentBase](../../com.aspose.words/documentbase)
### getField() {#getField}
```
public Field getField()
```


Returns a field for the field char. A new [Field](../../com.aspose.words/field) object is created each time the method is called.

**Returns:**
[Field](../../com.aspose.words/field) - A field for the field char.
### getFieldType() {#getFieldType}
```
public int getFieldType()
```


Returns the type of the field.

**Returns:**
int - The type of the field. The returned value is one of [FieldType](../../com.aspose.words/fieldtype) constants.
### getFont() {#getFont}
```
public Font getFont()
```


Provides access to the font formatting of this object.

**Returns:**
[Font](../../com.aspose.words/font) - The corresponding [Font](../../com.aspose.words/font) value.
### getNextSibling() {#getNextSibling}
```
public Node getNextSibling()
```


Gets the node immediately following this node. If there is no next node, a  null  is returned.

**Returns:**
[Node](../../com.aspose.words/node) - The node immediately following this node.
### getNodeType() {#getNodeType}
```
public int getNodeType()
```


Returns [NodeType.FIELD\_END](../../com.aspose.words/nodetype\#FIELD-END).

**Returns:**
int - \{[NodeType.FIELD\_END](../../com.aspose.words/nodetype\#FIELD-END). The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### getParentNode() {#getParentNode}
```
public CompositeNode getParentNode()
```


Gets the immediate parent of this node.

If a node has just been created and not yet added to the tree, or if it has been removed from the tree, the parent is  null .

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode) - The immediate parent of this node.
### getParentParagraph() {#getParentParagraph}
```
public Paragraph getParentParagraph()
```


Retrieves the parent [Paragraph](../../com.aspose.words/paragraph) of this node.

**Returns:**
[Paragraph](../../com.aspose.words/paragraph) - The corresponding [Paragraph](../../com.aspose.words/paragraph) value.
### getParentParagraph_IInline() {#getParentParagraph-IInline}
```
public Paragraph getParentParagraph_IInline()
```




**Returns:**
[Paragraph](../../com.aspose.words/paragraph)
### getPreviousSibling() {#getPreviousSibling}
```
public Node getPreviousSibling()
```


Gets the node immediately preceding this node. If there is no preceding node, a  null  is returned.

**Returns:**
[Node](../../com.aspose.words/node) - The node immediately preceding this node.
### getRange() {#getRange}
```
public Range getRange()
```


Returns a [Range](../../com.aspose.words/range) object that represents the portion of a document that is contained in this node.

**Returns:**
[Range](../../com.aspose.words/range) - A [Range](../../com.aspose.words/range) object that represents the portion of a document that is contained in this node.
### getText() {#getText}
```
public String getText()
```


Gets the special character that this node represents.

**Returns:**
java.lang.String - The string that contains the character that this node represents.
### hasSeparator() {#hasSeparator}
```
public boolean hasSeparator()
```


Returns  true  if this field has a separator.

**Returns:**
boolean - \{ true  if this field has a separator.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### isComposite() {#isComposite}
```
public boolean isComposite()
```


Returns  true  if this node can contain other nodes. (31231,6)

**Returns:**
boolean - \{ true  if this node can contain other nodes.
### isDeleteRevision() {#isDeleteRevision}
```
public boolean isDeleteRevision()
```


Returns true if this object was deleted in Microsoft Word while change tracking was enabled.

**Returns:**
boolean - True if this object was deleted in Microsoft Word while change tracking was enabled.
### isDirty() {#isDirty}
```
public boolean isDirty()
```


Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.

**Returns:**
boolean - Whether the current result of the field is no longer correct (stale) due to other modifications made to the document.
### isDirty(boolean value) {#isDirty-boolean}
```
public void isDirty(boolean value)
```


Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |

### isFormatRevision() {#isFormatRevision}
```
public boolean isFormatRevision()
```


Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled.

**Returns:**
boolean - True if formatting of the object was changed in Microsoft Word while change tracking was enabled.
### isInsertRevision() {#isInsertRevision}
```
public boolean isInsertRevision()
```


Returns true if this object was inserted in Microsoft Word while change tracking was enabled.

**Returns:**
boolean - True if this object was inserted in Microsoft Word while change tracking was enabled.
### isLocked() {#isLocked}
```
public boolean isLocked()
```


Gets whether the parent field is locked (should not recalculate its result).

**Returns:**
boolean - Whether the parent field is locked (should not recalculate its result).
### isLocked(boolean value) {#isLocked-boolean}
```
public void isLocked(boolean value)
```


Sets whether the parent field is locked (should not recalculate its result).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether the parent field is locked (should not recalculate its result). |

### isMoveFromRevision() {#isMoveFromRevision}
```
public boolean isMoveFromRevision()
```


Returns  true  if this object was moved (deleted) in Microsoft Word while change tracking was enabled.

**Returns:**
boolean - \{ true  if this object was moved (deleted) in Microsoft Word while change tracking was enabled.
### isMoveToRevision() {#isMoveToRevision}
```
public boolean isMoveToRevision()
```


Returns  true  if this object was moved (inserted) in Microsoft Word while change tracking was enabled.

**Returns:**
boolean - \{ true  if this object was moved (inserted) in Microsoft Word while change tracking was enabled.
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node}
```
public Node nextPreOrder(Node rootNode)
```


Gets next node according to the pre-order tree traversal algorithm.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | The top node (limit) of traversal. |

**Returns:**
[Node](../../com.aspose.words/node) - Next node in pre-order order. Null if reached the  rootNode .
### nodeTypeToString(int nodeType) {#nodeTypeToString-int}
```
public static String nodeTypeToString(int nodeType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node}
```
public Node previousPreOrder(Node rootNode)
```


Gets the previous node according to the pre-order tree traversal algorithm.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | The top node (limit) of traversal. |

**Returns:**
[Node](../../com.aspose.words/node) - Previous node in pre-order order. Null if reached the  rootNode .
### remove() {#remove}
```
public void remove()
```


Removes itself from the parent.

### removeMoveRevisions() {#removeMoveRevisions}
```
public void removeMoveRevisions()
```




### removeRunAttr(int key) {#removeRunAttr-int}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

### setCustomNodeId(int value) {#setCustomNodeId-int}
```
public void setCustomNodeId(int value)
```


Specifies custom node identifier.

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setRunAttr(int fontAttr, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int fontAttr, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |
| value | java.lang.Object |  |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(SaveOptions saveOptions) {#toString-com.aspose.words.SaveOptions}
```
public String toString(SaveOptions saveOptions)
```


Exports the content of the node into a string using the specified save options.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions) | Specifies the options that control how the node is saved. |

**Returns:**
java.lang.String - The content of the node in the specified format.
### toString(int saveFormat) {#toString-int}
```
public String toString(int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

