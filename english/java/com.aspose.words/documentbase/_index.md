---
title: DocumentBase
second_title: Aspose.Words for Java API Reference
description: Provides the abstract base class for a main document and a glossary document of a Word document.
type: docs
weight: 121
url: /java/com.aspose.words/documentbase/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode)
```
public abstract class DocumentBase extends CompositeNode
```

Provides the abstract base class for a main document and a glossary document of a Word document.

To learn more, visit the **Aspose.Words Document Object Model (DOM)** documentation article.

Aspose.Words represents a Word document as a tree of nodes. [DocumentBase](../../com.aspose.words/documentbase) is a root node of the tree that contains all other nodes of the document.

[DocumentBase](../../com.aspose.words/documentbase) also stores document-wide information such as [getStyles()](../../com.aspose.words/documentbase\#getStyles--) and [getLists()](../../com.aspose.words/documentbase\#getLists--) that the tree nodes might refer to.
## Methods

| Method | Description |
| --- | --- |
| [importNode(Node srcNode, boolean isImportChildren)](#importNode-com.aspose.words.Node-boolean-) | Imports a node from another document to the current document. |
| [importNode(Node srcNode, boolean isImportChildren, int importFormatMode)](#importNode-com.aspose.words.Node-boolean-int-) |  |
| [getDocument()](#getDocument--) |  |
| [getNodeChangingCallback()](#getNodeChangingCallback--) | Called when a node is inserted or removed in the document. |
| [setNodeChangingCallback(INodeChangingCallback value)](#setNodeChangingCallback-com.aspose.words.INodeChangingCallback-) | Called when a node is inserted or removed in the document. |
| [getResourceLoadingCallback()](#getResourceLoadingCallback--) | Allows to control how external resources are loaded. |
| [setResourceLoadingCallback(IResourceLoadingCallback value)](#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback-) | Allows to control how external resources are loaded. |
| [getFontInfos()](#getFontInfos--) | Provides access to properties of fonts used in this document. |
| [getStyles()](#getStyles--) | Returns a collection of styles defined in the document. |
| [getLists()](#getLists--) | Provides access to the list formatting used in the document. |
| [getWarningCallback()](#getWarningCallback--) | Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback-) | Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss. |
| [getBackgroundShape()](#getBackgroundShape--) | Gets the background shape of the document. |
| [setBackgroundShape(Shape value)](#setBackgroundShape-com.aspose.words.Shape-) | Sets the background shape of the document. |
| [getPageColor()](#getPageColor--) | Gets the page color of the document. |
| [setPageColor(Color value)](#setPageColor-java.awt.Color-) | Sets the page color of the document. |
### importNode(Node srcNode, boolean isImportChildren) {#importNode-com.aspose.words.Node-boolean-}
```
public Node importNode(Node srcNode, boolean isImportChildren)
```


Imports a node from another document to the current document.

Imports a node from another document to the current document.

This method uses the [ImportFormatMode.USE\_DESTINATION\_STYLES](../../com.aspose.words/importformatmode\#USE-DESTINATION-STYLES) option to resolve formatting.

Importing a node creates a copy of the source node belonging to the importing document. The returned node has no parent. The source node is not altered or removed from the original document.

Before a node from another document can be inserted into this document, it must be imported. During import, document-specific properties such as references to styles and lists are translated from the original to the importing document. After the node was imported, it can be inserted into the appropriate place in the document using [CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertBefore-com.aspose.words.Node--com.aspose.words.Node-) or [CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertAfter-com.aspose.words.Node--com.aspose.words.Node-).

If the source node already belongs to the destination document, then simply a deep clone of the source node is created.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcNode | [Node](../../com.aspose.words/node) | The node being imported. |
| isImportChildren | boolean | True to import all child nodes recursively; otherwise, false. |

**Returns:**
[Node](../../com.aspose.words/node) - The cloned node that belongs to the current document.
### importNode(Node srcNode, boolean isImportChildren, int importFormatMode) {#importNode-com.aspose.words.Node-boolean-int-}
```
public Node importNode(Node srcNode, boolean isImportChildren, int importFormatMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcNode | [Node](../../com.aspose.words/node) |  |
| isImportChildren | boolean |  |
| importFormatMode | int |  |

**Returns:**
[Node](../../com.aspose.words/node)
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


Gets the document to which this node belongs.

The node always belongs to a document even if it has just been created and not yet added to the tree, or if it has been removed from the tree.

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase)
### getNodeChangingCallback() {#getNodeChangingCallback--}
```
public INodeChangingCallback getNodeChangingCallback()
```


Called when a node is inserted or removed in the document.

**Returns:**
[INodeChangingCallback](../../com.aspose.words/inodechangingcallback) - The corresponding [INodeChangingCallback](../../com.aspose.words/inodechangingcallback) value.
### setNodeChangingCallback(INodeChangingCallback value) {#setNodeChangingCallback-com.aspose.words.INodeChangingCallback-}
```
public void setNodeChangingCallback(INodeChangingCallback value)
```


Called when a node is inserted or removed in the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [INodeChangingCallback](../../com.aspose.words/inodechangingcallback) | The corresponding [INodeChangingCallback](../../com.aspose.words/inodechangingcallback) value. |

### getResourceLoadingCallback() {#getResourceLoadingCallback--}
```
public IResourceLoadingCallback getResourceLoadingCallback()
```


Allows to control how external resources are loaded.

**Returns:**
[IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) - The corresponding [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) value.
### setResourceLoadingCallback(IResourceLoadingCallback value) {#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback-}
```
public void setResourceLoadingCallback(IResourceLoadingCallback value)
```


Allows to control how external resources are loaded.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) | The corresponding [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) value. |

### getFontInfos() {#getFontInfos--}
```
public FontInfoCollection getFontInfos()
```


Provides access to properties of fonts used in this document.

This collection of font definitions is loaded as is from the document. Font definitions might be optional, missing or incomplete in some documents.

Do not rely on this collection to ascertain that a particular font is used in the document. You should only use this collection to get information about fonts that might be used in the document.

**Returns:**
[FontInfoCollection](../../com.aspose.words/fontinfocollection) - The corresponding [FontInfoCollection](../../com.aspose.words/fontinfocollection) value.
### getStyles() {#getStyles--}
```
public StyleCollection getStyles()
```


Returns a collection of styles defined in the document.

For more information see the description of the [StyleCollection](../../com.aspose.words/stylecollection) class.

**Returns:**
[StyleCollection](../../com.aspose.words/stylecollection) - A collection of styles defined in the document.
### getLists() {#getLists--}
```
public ListCollection getLists()
```


Provides access to the list formatting used in the document.

For more information see the description of the [ListCollection](../../com.aspose.words/listcollection) class.

**Returns:**
[ListCollection](../../com.aspose.words/listcollection) - The corresponding [ListCollection](../../com.aspose.words/listcollection) value.
### getWarningCallback() {#getWarningCallback--}
```
public IWarningCallback getWarningCallback()
```


Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss. Document may generate warnings at any stage of its existence, so it's important to setup warning callback as early as possible to avoid the warnings loss. E.g. such properties as [Document.getPageCount()](../../com.aspose.words/document\#getPageCount--) actually build the document layout which is used later for rendering, and the layout warnings may be lost if warning callback is specified just for the rendering calls later.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback) value.
### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback-}
```
public void setWarningCallback(IWarningCallback value)
```


Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss. Document may generate warnings at any stage of its existence, so it's important to setup warning callback as early as possible to avoid the warnings loss. E.g. such properties as [Document.getPageCount()](../../com.aspose.words/document\#getPageCount--) actually build the document layout which is used later for rendering, and the layout warnings may be lost if warning callback is specified just for the rendering calls later.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback) | The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback) value. |

### getBackgroundShape() {#getBackgroundShape--}
```
public Shape getBackgroundShape()
```


Gets the background shape of the document. Can be null.

Microsoft Word allows only a shape that has its [ShapeBase.getShapeType()](../../com.aspose.words/shapebase\#getShapeType--) property equal to [ShapeType.RECTANGLE](../../com.aspose.words/shapetype\#RECTANGLE) to be used as a background shape for a document.

Microsoft Word supports only the fill properties of a background shape. All other properties are ignored.

Setting this property to a non-null value will also set the [ViewOptions.getDisplayBackgroundShape()](../../com.aspose.words/viewoptions\#getDisplayBackgroundShape--) / [ViewOptions.setDisplayBackgroundShape(boolean)](../../com.aspose.words/viewoptions\#setDisplayBackgroundShape-boolean-) to true.

**Returns:**
[Shape](../../com.aspose.words/shape) - The background shape of the document.
### setBackgroundShape(Shape value) {#setBackgroundShape-com.aspose.words.Shape-}
```
public void setBackgroundShape(Shape value)
```


Sets the background shape of the document. Can be null.

Microsoft Word allows only a shape that has its [ShapeBase.getShapeType()](../../com.aspose.words/shapebase\#getShapeType--) property equal to [ShapeType.RECTANGLE](../../com.aspose.words/shapetype\#RECTANGLE) to be used as a background shape for a document.

Microsoft Word supports only the fill properties of a background shape. All other properties are ignored.

Setting this property to a non-null value will also set the [ViewOptions.getDisplayBackgroundShape()](../../com.aspose.words/viewoptions\#getDisplayBackgroundShape--) / [ViewOptions.setDisplayBackgroundShape(boolean)](../../com.aspose.words/viewoptions\#setDisplayBackgroundShape-boolean-) to true.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [Shape](../../com.aspose.words/shape) | The background shape of the document. |

### getPageColor() {#getPageColor--}
```
public Color getPageColor()
```


Gets the page color of the document. This property is a simpler version of [getBackgroundShape()](../../com.aspose.words/documentbase\#getBackgroundShape--) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase\#setBackgroundShape-com.aspose.words.Shape-).

This property provides a simple way to specify a solid page color for the document. Setting this property creates and sets an appropriate [getBackgroundShape()](../../com.aspose.words/documentbase\#getBackgroundShape--) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase\#setBackgroundShape-com.aspose.words.Shape-).

If the page color is not set (e.g. there is no background shape in the document) returns a zero color.

**Returns:**
java.awt.Color - The page color of the document.
### setPageColor(Color value) {#setPageColor-java.awt.Color-}
```
public void setPageColor(Color value)
```


Sets the page color of the document. This property is a simpler version of [getBackgroundShape()](../../com.aspose.words/documentbase\#getBackgroundShape--) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase\#setBackgroundShape-com.aspose.words.Shape-).

This property provides a simple way to specify a solid page color for the document. Setting this property creates and sets an appropriate [getBackgroundShape()](../../com.aspose.words/documentbase\#getBackgroundShape--) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase\#setBackgroundShape-com.aspose.words.Shape-).

If the page color is not set (e.g. there is no background shape in the document) returns a zero color.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The page color of the document. |

