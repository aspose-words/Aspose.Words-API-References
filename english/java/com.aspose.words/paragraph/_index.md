---
title: Paragraph
linktitle: Paragraph
second_title: Aspose.Words for Java API Reference
description: Represents a paragraph of text in Java.
type: docs
weight: 449
url: /java/com.aspose.words/paragraph/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node/), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode/)
```
public class Paragraph extends CompositeNode
```

Represents a paragraph of text.

To learn more, visit the [ Working with Paragraphs ][Working with Paragraphs] documentation article.

[Paragraph](../../com.aspose.words/paragraph/) is a block-level node and can be a child of classes derived from [Story](../../com.aspose.words/story/) or [InlineStory](../../com.aspose.words/inlinestory/).

[Paragraph](../../com.aspose.words/paragraph/) can contain any number of inline-level nodes and bookmarks.

The complete list of child nodes that can occur inside a paragraph consists of [BookmarkStart](../../com.aspose.words/bookmarkstart/), [BookmarkEnd](../../com.aspose.words/bookmarkend/), [FieldStart](../../com.aspose.words/fieldstart/), [FieldSeparator](../../com.aspose.words/fieldseparator/), [FieldEnd](../../com.aspose.words/fieldend/), [FormField](../../com.aspose.words/formfield/), [Comment](../../com.aspose.words/comment/), [Footnote](../../com.aspose.words/footnote/), [Run](../../com.aspose.words/run/), [SpecialChar](../../com.aspose.words/specialchar/), [Shape](../../com.aspose.words/shape/), [GroupShape](../../com.aspose.words/groupshape/), [SmartTag](../../com.aspose.words/smarttag/).

A valid paragraph in Microsoft Word always ends with a paragraph break character and a minimal valid paragraph consists just of a paragraph break. The [Paragraph](../../com.aspose.words/paragraph/) class automatically appends the appropriate paragraph break character at the end and this character is not part of the child nodes of the [Paragraph](../../com.aspose.words/paragraph/), therefore a [Paragraph](../../com.aspose.words/paragraph/) can be empty.

Do not include the end of paragraph [ControlChar.PARAGRAPH\_BREAK](../../com.aspose.words/controlchar/\#PARAGRAPH-BREAK) or end of cell [ControlChar.CELL](../../com.aspose.words/controlchar/\#CELL) characters inside the text of the paragraph as it might make the paragraph invalid when the document is opened in Microsoft Word.


[Working with Paragraphs]: https://docs.aspose.com/words/java/working-with-paragraphs/
## Constructors

| Constructor | Description |
| --- | --- |
| [Paragraph(DocumentBase doc)](#Paragraph-com.aspose.words.DocumentBase) | Initializes a new instance of the [Paragraph](../../com.aspose.words/paragraph/) class. |
## Methods

| Method | Description |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor) | Accepts a visitor. |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node) | Adds the specified node to the end of the list of child nodes for this node. |
| [appendField(int fieldType, boolean updateField)](#appendField-int-boolean) |  |
| [appendField(String fieldCode)](#appendField-java.lang.String) | Appends a field to this paragraph. |
| [appendField(String fieldCode, String fieldValue)](#appendField-java.lang.String-java.lang.String) | Appends a field to this paragraph. |
| [clearParaAttrs()](#clearParaAttrs) |  |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [dd()](#dd) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean) | Creates a duplicate of the node. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fetchInheritedParaAttr(int key)](#fetchInheritedParaAttr-int) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int) |  |
| [fetchParaAttr(int key)](#fetchParaAttr-int) |  |
| [getAncestor(int ancestorType)](#getAncestor-int) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class) | Gets the first ancestor of the specified object type. |
| [getBreakIsStyleSeparator()](#getBreakIsStyleSeparator) | True if this paragraph break is a Style Separator. |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean) |  |
| [getChildNodes()](#getChildNodes) | Gets all immediate child nodes of this node. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean) |  |
| [getClass()](#getClass) |  |
| [getContainer()](#getContainer) |  |
| [getCount()](#getCount) | Gets the number of immediate children of this node. |
| [getCurrentNode()](#getCurrentNode) |  |
| [getCustomNodeId()](#getCustomNodeId) | Specifies custom node identifier. |
| [getDirectParaAttr(int key)](#getDirectParaAttr-int) |  |
| [getDirectParaAttr(int key, int revisionsView)](#getDirectParaAttr-int-int) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getDocument()](#getDocument) | Gets the document to which this node belongs. |
| [getEffectiveTabStops()](#getEffectiveTabStops) | Returns array of all tab stops applied to this paragraph, including applied indirectly by styles or lists. |
| [getFirstChild()](#getFirstChild) | Gets the first child of the node. |
| [getFrameFormat()](#getFrameFormat) | Provides access to the frame formatting properties. |
| [getLastChild()](#getLastChild) | Gets the last child of the node. |
| [getListFormat()](#getListFormat) | Provides access to the list formatting properties of the paragraph. |
| [getListLabel()](#getListLabel) | Gets a [getListLabel()](../../com.aspose.words/paragraph/\#getListLabel) object that provides access to list numbering value and formatting for this paragraph. |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node) |  |
| [getNextSibling()](#getNextSibling) | Gets the node immediately following this node. |
| [getNodeType()](#getNodeType) | Returns [NodeType.PARAGRAPH](../../com.aspose.words/nodetype/\#PARAGRAPH). |
| [getParagraphBreakFont()](#getParagraphBreakFont) | Provides access to the font formatting of the paragraph break character. |
| [getParagraphFormat()](#getParagraphFormat) | Provides access to the paragraph formatting properties. |
| [getParentNode()](#getParentNode) | Gets the immediate parent of this node. |
| [getParentSection()](#getParentSection) | Retrieves the parent [Section](../../com.aspose.words/section/) of the paragraph. |
| [getParentStory()](#getParentStory) | Retrieves the parent section-level story that can be [Body](../../com.aspose.words/body/) or [HeaderFooter](../../com.aspose.words/headerfooter/). |
| [getPreviousSibling()](#getPreviousSibling) | Gets the node immediately preceding this node. |
| [getRange()](#getRange) | Returns a [Range](../../com.aspose.words/range/) object that represents the portion of a document that is contained in this node. |
| [getRuns()](#getRuns) | Provides access to the typed collection of pieces of text inside the paragraph. |
| [getText()](#getText) | Gets the text of this paragraph including the end of paragraph character. |
| [hasChildNodes()](#hasChildNodes) | Returns  true  if this node has any child nodes. |
| [hashCode()](#hashCode) |  |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node) | Returns the index of the specified child node in the child node array. |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node) | Inserts the specified node immediately after the specified reference node. |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node) | Inserts the specified node immediately before the specified reference node. |
| [insertField(int fieldType, boolean updateField, Node refNode, boolean isAfter)](#insertField-int-boolean-com.aspose.words.Node-boolean) |  |
| [insertField(String fieldCode, Node refNode, boolean isAfter)](#insertField-java.lang.String-com.aspose.words.Node-boolean) | Inserts a field into this paragraph. |
| [insertField(String fieldCode, String fieldValue, Node refNode, boolean isAfter)](#insertField-java.lang.String-java.lang.String-com.aspose.words.Node-boolean) | Inserts a field into this paragraph. |
| [isComposite()](#isComposite) | Returns  true  as this node can have child nodes. |
| [isDeleteRevision()](#isDeleteRevision) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [isEndOfCell()](#isEndOfCell) | True if this paragraph is the last paragraph in a [Cell](../../com.aspose.words/cell/); false otherwise. |
| [isEndOfDocument()](#isEndOfDocument) | True if this paragraph is the last paragraph in the last section of the document. |
| [isEndOfHeaderFooter()](#isEndOfHeaderFooter) | True if this paragraph is the last paragraph in the [HeaderFooter](../../com.aspose.words/headerfooter/) (main text story) of a [Section](../../com.aspose.words/section/); false otherwise. |
| [isEndOfSection()](#isEndOfSection) | True if this paragraph is the last paragraph in the [Body](../../com.aspose.words/body/) (main text story) of a [Section](../../com.aspose.words/section/); false otherwise. |
| [isFormatRevision()](#isFormatRevision) | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled. |
| [isInCell()](#isInCell) | True if this paragraph is an immediate child of [Cell](../../com.aspose.words/cell/); false otherwise. |
| [isInsertRevision()](#isInsertRevision) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [isListItem()](#isListItem) | True when the paragraph is an item in a bulleted or numbered list in original revision. |
| [isMoveFromRevision()](#isMoveFromRevision) | Returns  true  if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [isMoveToRevision()](#isMoveToRevision) | Returns  true  if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [iterator()](#iterator) | Provides support for the for each style iteration over the child nodes of this node. |
| [joinRunsWithSameFormatting()](#joinRunsWithSameFormatting) | Joins runs with the same formatting in the paragraph. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node) | Gets next node according to the pre-order tree traversal algorithm. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [prependChild(Node newChild)](#prependChild-com.aspose.words.Node) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [remove()](#remove) | Removes itself from the parent. |
| [removeAllChildren()](#removeAllChildren) | Removes all the child nodes of the current node. |
| [removeChild(Node oldChild)](#removeChild-com.aspose.words.Node) | Removes the specified child node. |
| [removeMoveRevisions()](#removeMoveRevisions) |  |
| [removeParaAttr(int key)](#removeParaAttr-int) |  |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [removeSmartTags()](#removeSmartTags) | Removes all [SmartTag](../../com.aspose.words/smarttag/) descendant nodes of the current node. |
| [selectNodes(String xpath)](#selectNodes-java.lang.String) | Selects a list of nodes matching the XPath expression. |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String) | Selects the first [Node](../../com.aspose.words/node/) that matches the XPath expression. |
| [setCustomNodeId(int value)](#setCustomNodeId-int) | Specifies custom node identifier. |
| [setParaAttr(int key, Object value)](#setParaAttr-int-java.lang.Object) |  |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object) |  |
| [toString()](#toString) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions) | Exports the content of the node into a string using the specified save options. |
| [toString(int saveFormat)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### Paragraph(DocumentBase doc) {#Paragraph-com.aspose.words.DocumentBase}
```
public Paragraph(DocumentBase doc)
```


Initializes a new instance of the [Paragraph](../../com.aspose.words/paragraph/) class.

When [Paragraph](../../com.aspose.words/paragraph/) is created, it belongs to the specified document, but is not yet part of the document and [Node.getParentNode()](../../com.aspose.words/node/\#getParentNode) is  null .

To append [Paragraph](../../com.aspose.words/paragraph/) to the document use [CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertAfter-com.aspose.words.Node--com.aspose.words.Node) or [CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertBefore-com.aspose.words.Node--com.aspose.words.Node) on the story where you want the paragraph inserted.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase/) | The owner document. |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor}
```
public boolean accept(DocumentVisitor visitor)
```


Accepts a visitor.

Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../com.aspose.words/documentvisitor/).

For more info see the Visitor design pattern.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | The visitor that will visit the nodes. |

**Returns:**
boolean - True if all nodes were visited; false if [DocumentVisitor](../../com.aspose.words/documentvisitor/) stopped the operation before visiting all nodes. Calls [DocumentVisitor.visitParagraphStart(com.aspose.words.Paragraph)](../../com.aspose.words/documentvisitor/\#visitParagraphStart-com.aspose.words.Paragraph), then calls [Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node/\#accept-com.aspose.words.DocumentVisitor) for all child nodes of the paragraph and calls [DocumentVisitor.visitParagraphEnd(com.aspose.words.Paragraph)](../../com.aspose.words/documentvisitor/\#visitParagraphEnd-com.aspose.words.Paragraph) at the end.
### appendChild(Node newChild) {#appendChild-com.aspose.words.Node}
```
public Node appendChild(Node newChild)
```


Adds the specified node to the end of the list of child nodes for this node.

If the  newChild  is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | The node to add. |

**Returns:**
[Node](../../com.aspose.words/node/) - The node added.
### appendField(int fieldType, boolean updateField) {#appendField-int-boolean}
```
public Field appendField(int fieldType, boolean updateField)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldType | int |  |
| updateField | boolean |  |

**Returns:**
[Field](../../com.aspose.words/field/)
### appendField(String fieldCode) {#appendField-java.lang.String}
```
public Field appendField(String fieldCode)
```


Appends a field to this paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | java.lang.String | The field code to append (without curly braces). |

**Returns:**
[Field](../../com.aspose.words/field/) - A [Field](../../com.aspose.words/field/) object that represents the appended field.
### appendField(String fieldCode, String fieldValue) {#appendField-java.lang.String-java.lang.String}
```
public Field appendField(String fieldCode, String fieldValue)
```


Appends a field to this paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | java.lang.String | The field code to append (without curly braces). |
| fieldValue | java.lang.String | The field value to append. Pass  null  for fields that do not have a value. |

**Returns:**
[Field](../../com.aspose.words/field/) - A [Field](../../com.aspose.words/field/) object that represents the appended field.
### clearParaAttrs() {#clearParaAttrs}
```
public void clearParaAttrs()
```




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
[Node](../../com.aspose.words/node/) - The cloned node.
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
### fetchInheritedParaAttr(int key) {#fetchInheritedParaAttr-int}
```
public Object fetchInheritedParaAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRunAttr(int key) {#fetchInheritedRunAttr-int}
```
public Object fetchInheritedRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchParaAttr(int key) {#fetchParaAttr-int}
```
public Object fetchParaAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

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
[CompositeNode](../../com.aspose.words/compositenode/)
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
[CompositeNode](../../com.aspose.words/compositenode/) - The ancestor of the specified type or  null  if no ancestor of this type was found.

The ancestor type matches if it is equal to  ancestorType  or derived from  ancestorType .
### getBreakIsStyleSeparator() {#getBreakIsStyleSeparator}
```
public boolean getBreakIsStyleSeparator()
```


True if this paragraph break is a Style Separator. A style separator allows one paragraph to consist of parts that have different paragraph styles.

**Returns:**
boolean - The corresponding  boolean  value.
### getChild(int nodeType, int index, boolean isDeep) {#getChild-int-int-boolean}
```
public Node getChild(int nodeType, int index, boolean isDeep)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | int |  |
| index | int |  |
| isDeep | boolean |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### getChildNodes() {#getChildNodes}
```
public NodeCollection getChildNodes()
```


Gets all immediate child nodes of this node.

Note, [getChildNodes()](../../com.aspose.words/compositenode/\#getChildNodes) is equivalent to calling **M:Aspose.Words.CompositeNode.GetChildNodes(Aspose.Words.NodeType,System.Boolean)** with arguments ( [NodeType.ANY](../../com.aspose.words/nodetype/\#ANY),  false ) and creates and returns a new collection every time it is accessed.

If there are no child nodes, this property returns an empty collection.

**Returns:**
[NodeCollection](../../com.aspose.words/nodecollection/) - All immediate child nodes of this node.
### getChildNodes(int nodeType, boolean isDeep) {#getChildNodes-int-boolean}
```
public NodeCollection getChildNodes(int nodeType, boolean isDeep)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | int |  |
| isDeep | boolean |  |

**Returns:**
[NodeCollection](../../com.aspose.words/nodecollection/)
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getContainer() {#getContainer}
```
public CompositeNode getContainer()
```




**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/)
### getCount() {#getCount}
```
public int getCount()
```


Gets the number of immediate children of this node.

**Returns:**
int - The number of immediate children of this node.
### getCurrentNode() {#getCurrentNode}
```
public Node getCurrentNode()
```




**Returns:**
[Node](../../com.aspose.words/node/)
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
### getDirectParaAttr(int key) {#getDirectParaAttr-int}
```
public Object getDirectParaAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectParaAttr(int key, int revisionsView) {#getDirectParaAttr-int-int}
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
### getDirectRunAttr(int key) {#getDirectRunAttr-int}
```
public Object getDirectRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key, int revisionsView) {#getDirectRunAttr-int-int}
```
public Object getDirectRunAttr(int key, int revisionsView)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Gets the document to which this node belongs.

The node always belongs to a document even if it has just been created and not yet added to the tree, or if it has been removed from the tree.

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/) - The document to which this node belongs.
### getEffectiveTabStops() {#getEffectiveTabStops}
```
public TabStop[] getEffectiveTabStops()
```


Returns array of all tab stops applied to this paragraph, including applied indirectly by styles or lists.

**Returns:**
com.aspose.words.TabStop[]
### getFirstChild() {#getFirstChild}
```
public Node getFirstChild()
```


Gets the first child of the node. If there is no first child node, a  null  is returned.

**Returns:**
[Node](../../com.aspose.words/node/) - The first child of the node.
### getFrameFormat() {#getFrameFormat}
```
public FrameFormat getFrameFormat()
```


Provides access to the frame formatting properties.

**Returns:**
[FrameFormat](../../com.aspose.words/frameformat/) - The corresponding [FrameFormat](../../com.aspose.words/frameformat/) value.
### getLastChild() {#getLastChild}
```
public Node getLastChild()
```


Gets the last child of the node. If there is no last child node, a  null  is returned.

**Returns:**
[Node](../../com.aspose.words/node/) - The last child of the node.
### getListFormat() {#getListFormat}
```
public ListFormat getListFormat()
```


Provides access to the list formatting properties of the paragraph.

**Returns:**
[ListFormat](../../com.aspose.words/listformat/) - The corresponding [ListFormat](../../com.aspose.words/listformat/) value.
### getListLabel() {#getListLabel}
```
public ListLabel getListLabel()
```


Gets a [getListLabel()](../../com.aspose.words/paragraph/\#getListLabel) object that provides access to list numbering value and formatting for this paragraph.

**Returns:**
[ListLabel](../../com.aspose.words/listlabel/) - A [getListLabel()](../../com.aspose.words/paragraph/\#getListLabel) object that provides access to list numbering value and formatting for this paragraph.
### getNextMatchingNode(Node curNode) {#getNextMatchingNode-com.aspose.words.Node}
```
public Node getNextMatchingNode(Node curNode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node/) |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### getNextSibling() {#getNextSibling}
```
public Node getNextSibling()
```


Gets the node immediately following this node. If there is no next node, a  null  is returned.

**Returns:**
[Node](../../com.aspose.words/node/) - The node immediately following this node.
### getNodeType() {#getNodeType}
```
public int getNodeType()
```


Returns [NodeType.PARAGRAPH](../../com.aspose.words/nodetype/\#PARAGRAPH).

**Returns:**
int - \{[NodeType.PARAGRAPH](../../com.aspose.words/nodetype/\#PARAGRAPH). The returned value is one of [NodeType](../../com.aspose.words/nodetype/) constants.
### getParagraphBreakFont() {#getParagraphBreakFont}
```
public Font getParagraphBreakFont()
```


Provides access to the font formatting of the paragraph break character.

**Returns:**
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getParagraphFormat() {#getParagraphFormat}
```
public ParagraphFormat getParagraphFormat()
```


Provides access to the paragraph formatting properties.

**Returns:**
[ParagraphFormat](../../com.aspose.words/paragraphformat/) - The corresponding [ParagraphFormat](../../com.aspose.words/paragraphformat/) value.
### getParentNode() {#getParentNode}
```
public CompositeNode getParentNode()
```


Gets the immediate parent of this node.

If a node has just been created and not yet added to the tree, or if it has been removed from the tree, the parent is  null .

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/) - The immediate parent of this node.
### getParentSection() {#getParentSection}
```
public Section getParentSection()
```


Retrieves the parent [Section](../../com.aspose.words/section/) of the paragraph.

**Returns:**
[Section](../../com.aspose.words/section/) - The corresponding [Section](../../com.aspose.words/section/) value.
### getParentStory() {#getParentStory}
```
public Story getParentStory()
```


Retrieves the parent section-level story that can be [Body](../../com.aspose.words/body/) or [HeaderFooter](../../com.aspose.words/headerfooter/).

**Returns:**
[Story](../../com.aspose.words/story/) - The corresponding [Story](../../com.aspose.words/story/) value.
### getPreviousSibling() {#getPreviousSibling}
```
public Node getPreviousSibling()
```


Gets the node immediately preceding this node. If there is no preceding node, a  null  is returned.

**Returns:**
[Node](../../com.aspose.words/node/) - The node immediately preceding this node.
### getRange() {#getRange}
```
public Range getRange()
```


Returns a [Range](../../com.aspose.words/range/) object that represents the portion of a document that is contained in this node.

**Returns:**
[Range](../../com.aspose.words/range/) - A [Range](../../com.aspose.words/range/) object that represents the portion of a document that is contained in this node.
### getRuns() {#getRuns}
```
public RunCollection getRuns()
```


Provides access to the typed collection of pieces of text inside the paragraph.

**Returns:**
[RunCollection](../../com.aspose.words/runcollection/) - The corresponding [RunCollection](../../com.aspose.words/runcollection/) value.
### getText() {#getText}
```
public String getText()
```


Gets the text of this paragraph including the end of paragraph character.

The text of all child nodes is concatenated and the end of paragraph character is appended as follows:

 *  If the paragraph is the last paragraph of [Body](../../com.aspose.words/body/), then [ControlChar.SECTION\_BREAK](../../com.aspose.words/controlchar/\#SECTION-BREAK) (\\x000c) is appended.
 *  If the paragraph is the last paragraph of [Cell](../../com.aspose.words/cell/), then [ControlChar.CELL](../../com.aspose.words/controlchar/\#CELL) (\\x0007) is appended.
 *  For all other paragraphs [ControlChar.PARAGRAPH\_BREAK](../../com.aspose.words/controlchar/\#PARAGRAPH-BREAK) (\\r) is appended.

The returned string includes all control and special characters as described in [ControlChar](../../com.aspose.words/controlchar/).

**Returns:**
java.lang.String
### hasChildNodes() {#hasChildNodes}
```
public boolean hasChildNodes()
```


Returns  true  if this node has any child nodes.

**Returns:**
boolean - \{ true  if this node has any child nodes.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### indexOf(Node child) {#indexOf-com.aspose.words.Node}
```
public int indexOf(Node child)
```


Returns the index of the specified child node in the child node array. Returns -1 if the node is not found in the child nodes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| child | [Node](../../com.aspose.words/node/) |  |

**Returns:**
int
### insertAfter(Node newChild, Node refChild) {#insertAfter-com.aspose.words.Node-com.aspose.words.Node}
```
public Node insertAfter(Node newChild, Node refChild)
```


Inserts the specified node immediately after the specified reference node.

If  refChild  is  null , inserts  newChild  at the beginning of the list of child nodes.

If the  newChild  is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | The [Node](../../com.aspose.words/node/) to insert. |
| refChild | [Node](../../com.aspose.words/node/) | The [Node](../../com.aspose.words/node/) that is the reference node. The  newChild  is placed after the  refChild . |

**Returns:**
[Node](../../com.aspose.words/node/) - The inserted node.
### insertBefore(Node newChild, Node refChild) {#insertBefore-com.aspose.words.Node-com.aspose.words.Node}
```
public Node insertBefore(Node newChild, Node refChild)
```


Inserts the specified node immediately before the specified reference node.

If  refChild  is  null , inserts  newChild  at the end of the list of child nodes.

If the  newChild  is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | The [Node](../../com.aspose.words/node/) to insert. |
| refChild | [Node](../../com.aspose.words/node/) | The [Node](../../com.aspose.words/node/) that is the reference node. The  newChild  is placed before this node. |

**Returns:**
[Node](../../com.aspose.words/node/) - The inserted node.
### insertField(int fieldType, boolean updateField, Node refNode, boolean isAfter) {#insertField-int-boolean-com.aspose.words.Node-boolean}
```
public Field insertField(int fieldType, boolean updateField, Node refNode, boolean isAfter)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldType | int |  |
| updateField | boolean |  |
| refNode | [Node](../../com.aspose.words/node/) |  |
| isAfter | boolean |  |

**Returns:**
[Field](../../com.aspose.words/field/)
### insertField(String fieldCode, Node refNode, boolean isAfter) {#insertField-java.lang.String-com.aspose.words.Node-boolean}
```
public Field insertField(String fieldCode, Node refNode, boolean isAfter)
```


Inserts a field into this paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | java.lang.String | The field code to insert (without curly braces). |
| refNode | [Node](../../com.aspose.words/node/) | Reference node inside this paragraph (if  refNode  is  null , then appends to the end of the paragraph). |
| isAfter | boolean | Whether to insert the field after or before reference node. |

**Returns:**
[Field](../../com.aspose.words/field/) - A [Field](../../com.aspose.words/field/) object that represents the inserted field.
### insertField(String fieldCode, String fieldValue, Node refNode, boolean isAfter) {#insertField-java.lang.String-java.lang.String-com.aspose.words.Node-boolean}
```
public Field insertField(String fieldCode, String fieldValue, Node refNode, boolean isAfter)
```


Inserts a field into this paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | java.lang.String | The field code to insert (without curly braces). |
| fieldValue | java.lang.String | The field value to insert. Pass  null  for fields that do not have a value. |
| refNode | [Node](../../com.aspose.words/node/) | Reference node inside this paragraph (if  refNode  is  null , then appends to the end of the paragraph). |
| isAfter | boolean | Whether to insert the field after or before reference node. |

**Returns:**
[Field](../../com.aspose.words/field/) - A [Field](../../com.aspose.words/field/) object that represents the inserted field.
### isComposite() {#isComposite}
```
public boolean isComposite()
```


Returns  true  as this node can have child nodes.

**Returns:**
boolean - \{ true  as this node can have child nodes.
### isDeleteRevision() {#isDeleteRevision}
```
public boolean isDeleteRevision()
```


Returns true if this object was deleted in Microsoft Word while change tracking was enabled.

**Returns:**
boolean - True if this object was deleted in Microsoft Word while change tracking was enabled.
### isEndOfCell() {#isEndOfCell}
```
public boolean isEndOfCell()
```


True if this paragraph is the last paragraph in a [Cell](../../com.aspose.words/cell/); false otherwise.

**Returns:**
boolean - The corresponding  boolean  value.
### isEndOfDocument() {#isEndOfDocument}
```
public boolean isEndOfDocument()
```


True if this paragraph is the last paragraph in the last section of the document.

**Returns:**
boolean - The corresponding  boolean  value.
### isEndOfHeaderFooter() {#isEndOfHeaderFooter}
```
public boolean isEndOfHeaderFooter()
```


True if this paragraph is the last paragraph in the [HeaderFooter](../../com.aspose.words/headerfooter/) (main text story) of a [Section](../../com.aspose.words/section/); false otherwise.

**Returns:**
boolean - The corresponding  boolean  value.
### isEndOfSection() {#isEndOfSection}
```
public boolean isEndOfSection()
```


True if this paragraph is the last paragraph in the [Body](../../com.aspose.words/body/) (main text story) of a [Section](../../com.aspose.words/section/); false otherwise.

**Returns:**
boolean - The corresponding  boolean  value.
### isFormatRevision() {#isFormatRevision}
```
public boolean isFormatRevision()
```


Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled.

**Returns:**
boolean - True if formatting of the object was changed in Microsoft Word while change tracking was enabled.
### isInCell() {#isInCell}
```
public boolean isInCell()
```


True if this paragraph is an immediate child of [Cell](../../com.aspose.words/cell/); false otherwise.

**Returns:**
boolean - The corresponding  boolean  value.
### isInsertRevision() {#isInsertRevision}
```
public boolean isInsertRevision()
```


Returns true if this object was inserted in Microsoft Word while change tracking was enabled.

**Returns:**
boolean - True if this object was inserted in Microsoft Word while change tracking was enabled.
### isListItem() {#isListItem}
```
public boolean isListItem()
```


True when the paragraph is an item in a bulleted or numbered list in original revision.

**Returns:**
boolean - The corresponding  boolean  value.
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
### iterator() {#iterator}
```
public Iterator iterator()
```


Provides support for the for each style iteration over the child nodes of this node.

**Returns:**
java.util.Iterator
### joinRunsWithSameFormatting() {#joinRunsWithSameFormatting}
```
public int joinRunsWithSameFormatting()
```


Joins runs with the same formatting in the paragraph.

**Returns:**
int - Number of joins performed. When **N** adjacent runs are being joined they count as **N - 1** joins.
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node}
```
public Node nextPreOrder(Node rootNode)
```


Gets next node according to the pre-order tree traversal algorithm.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node/) | The top node (limit) of traversal. |

**Returns:**
[Node](../../com.aspose.words/node/) - Next node in pre-order order. Null if reached the  rootNode .
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




### prependChild(Node newChild) {#prependChild-com.aspose.words.Node}
```
public Node prependChild(Node newChild)
```


Adds the specified node to the beginning of the list of child nodes for this node.

If the  newChild  is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | The node to add. |

**Returns:**
[Node](../../com.aspose.words/node/) - The node added.
### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node}
```
public Node previousPreOrder(Node rootNode)
```


Gets the previous node according to the pre-order tree traversal algorithm.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node/) | The top node (limit) of traversal. |

**Returns:**
[Node](../../com.aspose.words/node/) - Previous node in pre-order order. Null if reached the  rootNode .
### remove() {#remove}
```
public void remove()
```


Removes itself from the parent.

### removeAllChildren() {#removeAllChildren}
```
public void removeAllChildren()
```


Removes all the child nodes of the current node.

### removeChild(Node oldChild) {#removeChild-com.aspose.words.Node}
```
public Node removeChild(Node oldChild)
```


Removes the specified child node.

The parent of  oldChild  is set to  null  after the node is removed.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| oldChild | [Node](../../com.aspose.words/node/) | The node to remove. |

**Returns:**
[Node](../../com.aspose.words/node/) - The removed node.
### removeMoveRevisions() {#removeMoveRevisions}
```
public void removeMoveRevisions()
```




### removeParaAttr(int key) {#removeParaAttr-int}
```
public void removeParaAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

### removeRunAttr(int key) {#removeRunAttr-int}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

### removeSmartTags() {#removeSmartTags}
```
public void removeSmartTags()
```


Removes all [SmartTag](../../com.aspose.words/smarttag/) descendant nodes of the current node. This method does not remove the content of the smart tags.

### selectNodes(String xpath) {#selectNodes-java.lang.String}
```
public NodeList selectNodes(String xpath)
```


Selects a list of nodes matching the XPath expression.

Only expressions with element names are supported at the moment. Expressions that use attribute names are not supported.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xpath | java.lang.String | The XPath expression. |

**Returns:**
[NodeList](../../com.aspose.words/nodelist/) - A list of nodes matching the XPath query.
### selectSingleNode(String xpath) {#selectSingleNode-java.lang.String}
```
public Node selectSingleNode(String xpath)
```


Selects the first [Node](../../com.aspose.words/node/) that matches the XPath expression.

Only expressions with element names are supported at the moment. Expressions that use attribute names are not supported.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xpath | java.lang.String | The XPath expression. |

**Returns:**
[Node](../../com.aspose.words/node/) - The first [Node](../../com.aspose.words/node/) that matches the XPath query or  null  if no matching node is found.
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

### setParaAttr(int key, Object value) {#setParaAttr-int-java.lang.Object}
```
public void setParaAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
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
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Specifies the options that control how the node is saved. |

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

