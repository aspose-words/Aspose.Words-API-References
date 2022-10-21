---
title: Bookmark
second_title: Aspose.Words for Java API Reference
description: Represents a single bookmark.
type: docs
weight: 31
url: /java/com.aspose.words/bookmark/
---

**Inheritance:**
java.lang.Object
```
public class Bookmark
```

Represents a single bookmark.

To learn more, visit the **Working with Bookmarks** documentation article.

[Bookmark](../../com.aspose.words/bookmark) is a "facade" object that encapsulates two nodes [getBookmarkStart()](../../com.aspose.words/bookmark\#getBookmarkStart--) and [getBookmarkEnd()](../../com.aspose.words/bookmark\#getBookmarkEnd--) in a document tree and allows to work with a bookmark as a single object.
## Methods

| Method | Description |
| --- | --- |
| [getName()](#getName--) | Gets the name of the bookmark. |
| [setName(String value)](#setName-java.lang.String-) | Sets the name of the bookmark. |
| [getText()](#getText--) | Gets the text enclosed in the bookmark. |
| [setText(String value)](#setText-java.lang.String-) | Sets the text enclosed in the bookmark. |
| [getBookmarkStart()](#getBookmarkStart--) | Gets the node that represents the start of the bookmark. |
| [getBookmarkEnd()](#getBookmarkEnd--) | Gets the node that represents the end of the bookmark. |
| [isColumn()](#isColumn--) | Returns **true** if this bookmark is a table column bookmark. |
| [getFirstColumn()](#getFirstColumn--) | Gets the zero-based index of the first column of the table column range associated with the bookmark. |
| [getLastColumn()](#getLastColumn--) | Gets the zero-based index of the last column of the table column range associated with the bookmark. |
| [remove()](#remove--) | Removes the bookmark from the document. |
### getName() {#getName--}
```
public String getName()
```


Gets the name of the bookmark. Note that if you change the name of a bookmark to a name that already exists in the document, no error will be given and only the first bookmark will be stored when you save the document.

**Returns:**
java.lang.String - The name of the bookmark.
### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


Sets the name of the bookmark. Note that if you change the name of a bookmark to a name that already exists in the document, no error will be given and only the first bookmark will be stored when you save the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the bookmark. |

### getText() {#getText--}
```
public String getText()
```


Gets the text enclosed in the bookmark.

**Returns:**
java.lang.String - The text enclosed in the bookmark.
### setText(String value) {#setText-java.lang.String-}
```
public void setText(String value)
```


Sets the text enclosed in the bookmark.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The text enclosed in the bookmark. |

### getBookmarkStart() {#getBookmarkStart--}
```
public BookmarkStart getBookmarkStart()
```


Gets the node that represents the start of the bookmark.

**Returns:**
[BookmarkStart](../../com.aspose.words/bookmarkstart) - The node that represents the start of the bookmark.
### getBookmarkEnd() {#getBookmarkEnd--}
```
public BookmarkEnd getBookmarkEnd()
```


Gets the node that represents the end of the bookmark.

**Returns:**
[BookmarkEnd](../../com.aspose.words/bookmarkend) - The node that represents the end of the bookmark.
### isColumn() {#isColumn--}
```
public boolean isColumn()
```


Returns **true** if this bookmark is a table column bookmark.

**Returns:**
boolean - **true** if this bookmark is a table column bookmark.
### getFirstColumn() {#getFirstColumn--}
```
public int getFirstColumn()
```


Gets the zero-based index of the first column of the table column range associated with the bookmark. Returns **-1** if this bookmark is not a table column bookmark.

**Returns:**
int - The zero-based index of the first column of the table column range associated with the bookmark.
### getLastColumn() {#getLastColumn--}
```
public int getLastColumn()
```


Gets the zero-based index of the last column of the table column range associated with the bookmark. Returns **-1** if this bookmark is not a table column bookmark.

**Returns:**
int - The zero-based index of the last column of the table column range associated with the bookmark.
### remove() {#remove--}
```
public void remove()
```


Removes the bookmark from the document. Does not remove text inside the bookmark.

