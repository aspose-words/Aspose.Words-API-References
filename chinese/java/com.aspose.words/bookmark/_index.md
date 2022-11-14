---
title: Bookmark
second_title: Aspose.Words for Java API 参考
description: 表示单个书签。
type: docs
weight: 31
url: /zh/java/com.aspose.words/bookmark/
---

**遗产:**
java.lang.Object
```
public class Bookmark
```

代表单个书签。

要了解更多信息，请访问**Working with Bookmarks**文档文章。

[Bookmark](../../com.aspose.words/bookmark)是一个封装了两个节点的“门面”对象[getBookmarkStart()](../../com.aspose.words/bookmark\#getBookmarkStart--)和[getBookmarkEnd()](../../com.aspose.words/bookmark\#getBookmarkEnd--)在文档树中，并允许将书签作为单个对象使用。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBookmarkEnd()](#getBookmarkEnd--) | 获取表示书签结束的节点。 |
| [getBookmarkStart()](#getBookmarkStart--) | 获取表示书签开始的节点。 |
| [getClass()](#getClass--) |  |
| [getFirstColumn()](#getFirstColumn--) | 获取与书签关联的表列范围的第一列的从零开始的索引。 |
| [getLastColumn()](#getLastColumn--) | 获取与书签关联的表列范围的最后一列的从零开始的索引。 |
| [getName()](#getName--) | 获取书签的名称。 |
| [getText()](#getText--) | 获取书签中包含的文本。 |
| [hashCode()](#hashCode--) |  |
| [isColumn()](#isColumn--) | 退货**true**如果此书签是表格列书签。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | 从文档中删除书签。 |
| [setName(String value)](#setName-java.lang.String-) | 设置书签的名称。 |
| [setText(String value)](#setText-java.lang.String-) | 设置书签中包含的文本。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
布尔值
### getBookmarkEnd() {#getBookmarkEnd--}
```
public BookmarkEnd getBookmarkEnd()
```


获取表示书签结束的节点。

**退货:**
[BookmarkEnd](../../com.aspose.words/bookmarkend) - 代表书签结束的节点。
### getBookmarkStart() {#getBookmarkStart--}
```
public BookmarkStart getBookmarkStart()
```


获取表示书签开始的节点。

**退货:**
[BookmarkStart](../../com.aspose.words/bookmarkstart) - 表示书签开始的节点。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getFirstColumn() {#getFirstColumn--}
```
public int getFirstColumn()
```


获取与书签关联的表列范围的第一列的从零开始的索引。退货**-1**如果此书签不是表格列书签。

**退货:**
int - 与书签关联的表列范围的第一列的从零开始的索引。
### getLastColumn() {#getLastColumn--}
```
public int getLastColumn()
```


获取与书签关联的表列范围的最后一列的从零开始的索引。退货**-1**如果此书签不是表格列书签。

**退货:**
int - 与书签关联的表列范围的最后一列的从零开始的索引。
### getName() {#getName--}
```
public String getName()
```


获取书签名称。请注意，如果将书签的名称更改为文档中已存在的名称，则不会报错，并且在保存文档时只会存储第一个书签。

**退货:**
java.lang.String - 书签名称。
### getText() {#getText--}
```
public String getText()
```


获取书签中包含的文本。

**退货:**
java.lang.String - 书签中包含的文本。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isColumn() {#isColumn--}
```
public boolean isColumn()
```


退货**true**如果此书签是表格列书签。

**退货:**
布尔值 -**true**如果此书签是表格列书签。
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


从文档中删除书签。不删除书签内的文本。

### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


设置书签名称。请注意，如果将书签的名称更改为文档中已存在的名称，则不会报错，并且在保存文档时只会存储第一个书签。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 书签名称。 |

### setText(String value) {#setText-java.lang.String-}
```
public void setText(String value)
```


设置书签中包含的文本。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 书签中包含的文本。 |

### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
