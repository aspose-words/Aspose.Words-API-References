---
title: BookmarkStart
second_title: Aspose.Words for Java API Reference
description: Represents a start of a bookmark in a Word document.
type: docs
weight: 34
url: /java/com.aspose.words/bookmarkstart/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node)
```
public class BookmarkStart extends Node
```

Represents a start of a bookmark in a Word document.

To learn more, visit the **Working with Bookmarks** documentation article.

A complete bookmark in a Word document consists of a [BookmarkStart](../../com.aspose.words/bookmarkstart) and a matching [BookmarkEnd](../../com.aspose.words/bookmarkend) with the same bookmark name.

[BookmarkStart](../../com.aspose.words/bookmarkstart) and [BookmarkEnd](../../com.aspose.words/bookmarkend) are just markers inside a document that specify where the bookmark starts and ends.

Use the [getBookmark()](../../com.aspose.words/bookmarkstart\#getBookmark--) class as a "facade" to work with a bookmark as a single object.
## Constructors

| Constructor | Description |
| --- | --- |
| [BookmarkStart(DocumentBase doc, String name)](#BookmarkStart-com.aspose.words.DocumentBase-java.lang.String-) | Initializes a new instance of the [BookmarkStart](../../com.aspose.words/bookmarkstart) class. |
## Methods

| Method | Description |
| --- | --- |
| [getNodeType()](#getNodeType--) | Returns [NodeType.BOOKMARK\_START](../../com.aspose.words/nodetype\#BOOKMARK-START). |
| [getBookmark()](#getBookmark--) | Gets the facade object that encapsulates this bookmark start and end. |
| [getDisplacedByCustomXml()](#getDisplacedByCustomXml--) |  |
| [setDisplacedByCustomXml(int value)](#setDisplacedByCustomXml-int-) |  |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
| [getText()](#getText--) | Returns an empty string. |
| [getName()](#getName--) | Gets the bookmark name. |
| [setName(String value)](#setName-java.lang.String-) | Sets the bookmark name. |
### BookmarkStart(DocumentBase doc, String name) {#BookmarkStart-com.aspose.words.DocumentBase-java.lang.String-}
```
public BookmarkStart(DocumentBase doc, String name)
```


Initializes a new instance of the [BookmarkStart](../../com.aspose.words/bookmarkstart) class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) | The owner document. |
| name | java.lang.String | The name of the bookmark. Cannot be null. |

### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns [NodeType.BOOKMARK\_START](../../com.aspose.words/nodetype\#BOOKMARK-START).

**Returns:**
int - \{[NodeType.BOOKMARK\_START](../../com.aspose.words/nodetype\#BOOKMARK-START). The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### getBookmark() {#getBookmark--}
```
public Bookmark getBookmark()
```


Gets the facade object that encapsulates this bookmark start and end.

**Returns:**
[Bookmark](../../com.aspose.words/bookmark) - The facade object that encapsulates this bookmark start and end.
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

Calls [DocumentVisitor.visitBookmarkStart(com.aspose.words.BookmarkStart)](../../com.aspose.words/documentvisitor\#visitBookmarkStart-com.aspose.words.BookmarkStart-).

For more info see the Visitor design pattern.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | The visitor that will visit the node. |

**Returns:**
boolean - False if the visitor requested the enumeration to stop.
### getText() {#getText--}
```
public String getText()
```


Returns an empty string.

**Returns:**
java.lang.String - An empty string.
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

