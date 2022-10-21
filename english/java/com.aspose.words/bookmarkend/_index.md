---
title: BookmarkEnd
second_title: Aspose.Words for Java API Reference
description: Represents an end of a bookmark in a Word document.
type: docs
weight: 33
url: /java/com.aspose.words/bookmarkend/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node)
```
public class BookmarkEnd extends Node
```

Represents an end of a bookmark in a Word document.

To learn more, visit the **Working with Bookmarks** documentation article.

A complete bookmark in a Word document consists of a [BookmarkStart](../../com.aspose.words/bookmarkstart) and a matching [BookmarkEnd](../../com.aspose.words/bookmarkend) with the same bookmark name.

[BookmarkStart](../../com.aspose.words/bookmarkstart) and [BookmarkEnd](../../com.aspose.words/bookmarkend) are just markers inside a document that specify where the bookmark starts and ends.

Use the [Bookmark](../../com.aspose.words/bookmark) class as a "facade" to work with a bookmark as a single object.
## Constructors

| Constructor | Description |
| --- | --- |
| [BookmarkEnd(DocumentBase doc, String name)](#BookmarkEnd-com.aspose.words.DocumentBase-java.lang.String-) | Initializes a new instance of the [BookmarkEnd](../../com.aspose.words/bookmarkend) class. |
## Methods

| Method | Description |
| --- | --- |
| [getNodeType()](#getNodeType--) | Returns [NodeType.BOOKMARK\_END](../../com.aspose.words/nodetype\#BOOKMARK-END). |
| [getDisplacedByCustomXml()](#getDisplacedByCustomXml--) |  |
| [setDisplacedByCustomXml(int value)](#setDisplacedByCustomXml-int-) |  |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
| [getName()](#getName--) | Gets the bookmark name. |
| [setName(String value)](#setName-java.lang.String-) | Sets the bookmark name. |
### BookmarkEnd(DocumentBase doc, String name) {#BookmarkEnd-com.aspose.words.DocumentBase-java.lang.String-}
```
public BookmarkEnd(DocumentBase doc, String name)
```


Initializes a new instance of the [BookmarkEnd](../../com.aspose.words/bookmarkend) class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) | The owner document. |
| name | java.lang.String | The name of the bookmark. Cannot be null. |

### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns [NodeType.BOOKMARK\_END](../../com.aspose.words/nodetype\#BOOKMARK-END).

**Returns:**
int - \{[NodeType.BOOKMARK\_END](../../com.aspose.words/nodetype\#BOOKMARK-END). The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### getDisplacedByCustomXml() {#getDisplacedByCustomXml--}
```
public int getDisplacedByCustomXml()
```




**Returns:**
int
### setDisplacedByCustomXml(int value) {#setDisplacedByCustomXml-int-}
```
public void setDisplacedByCustomXml(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public boolean accept(DocumentVisitor visitor)
```


Accepts a visitor.

Calls [DocumentVisitor.visitBookmarkEnd(com.aspose.words.BookmarkEnd)](../../com.aspose.words/documentvisitor\#visitBookmarkEnd-com.aspose.words.BookmarkEnd-).

For more info see the Visitor design pattern.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | The visitor that will visit the node. |

**Returns:**
boolean - False if the visitor requested the enumeration to stop.
### getName() {#getName--}
```
public String getName()
```


Gets the bookmark name.

Cannot be null.

**Returns:**
java.lang.String - The bookmark name.
### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


Sets the bookmark name.

Cannot be null.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The bookmark name. |

