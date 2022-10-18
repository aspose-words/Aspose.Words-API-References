---
title: GroupShape
second_title: Aspose.Words for Java API Reference
description: Represents a group of shapes in a document.
type: docs
weight: 314
url: /java/com.aspose.words/groupshape/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode), [com.aspose.words.ShapeBase](../../com.aspose.words/shapebase)
```
public class GroupShape extends ShapeBase
```

Represents a group of shapes in a document.

To learn more, visit the **How to Add Group Shape into a Word Document** documentation article.

A [GroupShape](../../com.aspose.words/groupshape) is a composite node and can have [Shape](../../com.aspose.words/shape) and [GroupShape](../../com.aspose.words/groupshape) nodes as children.

Each [GroupShape](../../com.aspose.words/groupshape) defines a new coordinate system for its child shapes. The coordinate system is defined using the [ShapeBase.getCoordSize()](../../com.aspose.words/shapebase\#getCoordSize--) / [ShapeBase.setCoordSize(java.awt.Dimension)](../../com.aspose.words/shapebase\#setCoordSize-java.awt.Dimension-) and [ShapeBase.getCoordOrigin()](../../com.aspose.words/shapebase\#getCoordOrigin--) / [ShapeBase.setCoordOrigin(java.awt.Point)](../../com.aspose.words/shapebase\#setCoordOrigin-java.awt.Point-) properties.
## Constructors

| Constructor | Description |
| --- | --- |
| [GroupShape(DocumentBase doc)](#GroupShape-com.aspose.words.DocumentBase-) | Creates a new group shape. |
## Methods

| Method | Description |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
| [getNodeType()](#getNodeType--) | Returns [NodeType.GROUP\_SHAPE](../../com.aspose.words/nodetype\#GROUP-SHAPE). |
### GroupShape(DocumentBase doc) {#GroupShape-com.aspose.words.DocumentBase-}
```
public GroupShape(DocumentBase doc)
```


Creates a new group shape.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) | The owner document.

By default, the shape is floating and has default location and size.

You should specify desired shape properties after you created a shape. |

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
boolean - True if all nodes were visited; false if DocumentVisitor stopped the operation before visiting all nodes. Calls [DocumentVisitor.visitGroupShapeStart(com.aspose.words.GroupShape)](../../com.aspose.words/documentvisitor\#visitGroupShapeStart-com.aspose.words.GroupShape-), then calls [Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node\#accept-com.aspose.words.DocumentVisitor-) for all child shapes of this group shape and calls [DocumentVisitor.visitGroupShapeEnd(com.aspose.words.GroupShape)](../../com.aspose.words/documentvisitor\#visitGroupShapeEnd-com.aspose.words.GroupShape-) at the end.
### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns [NodeType.GROUP\_SHAPE](../../com.aspose.words/nodetype\#GROUP-SHAPE).

**Returns:**
int - \{[NodeType.GROUP\_SHAPE](../../com.aspose.words/nodetype\#GROUP-SHAPE). The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
