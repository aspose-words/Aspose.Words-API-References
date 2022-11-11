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
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBookmarkEnd()](#getBookmarkEnd--) | Gets the node that represents the end of the bookmark. |
| [getBookmarkStart()](#getBookmarkStart--) | Gets the node that represents the start of the bookmark. |
| [getClass()](#getClass--) |  |
| [getFirstColumn()](#getFirstColumn--) | Gets the zero-based index of the first column of the table column range associated with the bookmark. |
| [getLastColumn()](#getLastColumn--) | Gets the zero-based index of the last column of the table column range associated with the bookmark. |
| [getName()](#getName--) | Gets the name of the bookmark. |
| [getText()](#getText--) | Gets the text enclosed in the bookmark. |
| [hashCode()](#hashCode--) |  |
| [isColumn()](#isColumn--) | Returns **true** if this bookmark is a table column bookmark. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | Removes the bookmark from the document. |
| [setName(String value)](#setName-java.lang.String-) | Sets the name of the bookmark. |
| [setText(String value)](#setText-java.lang.String-) | Sets the text enclosed in the bookmark. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getBookmarkEnd() {#getBookmarkEnd--}
```
public BookmarkEnd getBookmarkEnd()
```


Gets the node that represents the end of the bookmark.

**Returns:**
[BookmarkEnd](../../com.aspose.words/bookmarkend) - The node that represents the end of the bookmark.
### getBookmarkStart() {#getBookmarkStart--}
```
public BookmarkStart getBookmarkStart()
```


Gets the node that represents the start of the bookmark.

**Returns:**
[BookmarkStart](../../com.aspose.words/bookmarkstart) - The node that represents the start of the bookmark.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
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
### getName() {#getName--}
```
public String getName()
```


Gets the name of the bookmark. Note that if you change the name of a bookmark to a name that already exists in the document, no error will be given and only the first bookmark will be stored when you save the document.

**Returns:**
java.lang.String - The name of the bookmark.
### getText() {#getText--}
```
public String getText()
```


Gets the text enclosed in the bookmark.

**Returns:**
java.lang.String - The text enclosed in the bookmark.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### isColumn() {#isColumn--}
```
public boolean isColumn()
```


Returns **true** if this bookmark is a table column bookmark.

**Returns:**
boolean - **true** if this bookmark is a table column bookmark.
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### remove() {#remove--}
```
public void remove()
```


Removes the bookmark from the document. Does not remove text inside the bookmark.

### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


Sets the name of the bookmark. Note that if you change the name of a bookmark to a name that already exists in the document, no error will be given and only the first bookmark will be stored when you save the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the bookmark. |

### setText(String value) {#setText-java.lang.String-}
```
public void setText(String value)
```


Sets the text enclosed in the bookmark.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The text enclosed in the bookmark. |

### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

