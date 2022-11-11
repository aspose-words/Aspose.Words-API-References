---
title: OutlineOptions
second_title: Aspose.Words for Java API 参考
description: 允许指定大纲选项。
type: docs
weight: 431
url: /zh/java/com.aspose.words/outlineoptions/
---

**遗产:**
java.lang.Object
```
public class OutlineOptions
```

允许指定大纲选项。

要了解更多信息，请访问**Save a Document**文档文章。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBookmarksOutlineLevels()](#getBookmarksOutlineLevels--) | 允许指定单个书签大纲级别。 |
| [get班级()](#get班级--) |  |
| [getCreateMissingOutlineLevels()](#getCreateMissingOutlineLevels--) | 获取或设置一个值，该值确定在导出文档时是否创建缺少的大纲级别。 |
| [getCreateOutlinesForHeadingsInTables()](#getCreateOutlinesForHeadingsInTables--) | 指定是否为表格内的标题（使用标题样式格式化的段落）创建大纲。 |
| [getDefaultBookmarksOutlineLevel()](#getDefaultBookmarksOutlineLevel--) | 指定文档大纲中显示 Word 书签的默认级别。 |
| [getExpandedOutlineLevels()](#getExpandedOutlineLevels--) | 指定查看文件时在文档大纲中显示展开的级别数。 |
| [getHeadingsOutlineLevels()](#getHeadingsOutlineLevels--) | 指定要包含在文档大纲中的标题级别（使用标题样式格式化的段落）。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setCreateMissingOutlineLevels(boolean value)](#setCreateMissingOutlineLevels-boolean-) | 获取或设置一个值，该值确定在导出文档时是否创建缺少的大纲级别。 |
| [setCreateOutlinesForHeadingsInTables(boolean value)](#setCreateOutlinesForHeadingsInTables-boolean-) | 指定是否为表格内的标题（使用标题样式格式化的段落）创建大纲。 |
| [setDefaultBookmarksOutlineLevel(int value)](#setDefaultBookmarksOutlineLevel-int-) | 指定文档大纲中显示 Word 书签的默认级别。 |
| [setExpandedOutlineLevels(int value)](#setExpandedOutlineLevels-int-) | 指定查看文件时在文档大纲中显示展开的级别数。 |
| [setHeadingsOutlineLevels(int value)](#setHeadingsOutlineLevels-int-) | 指定要包含在文档大纲中的标题级别（使用标题样式格式化的段落）。 |
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
### getBookmarksOutlineLevels() {#getBookmarksOutlineLevels--}
```
public BookmarksOutlineLevelCollection getBookmarksOutlineLevels()
```


允许指定单个书签大纲级别。

如果此集合中未指定书签级别，则[getDefaultBookmarksOutlineLevel()](../../com.aspose.words/outlineoptions\#getDefaultBookmarksOutlineLevel--) / [setDefaultBookmarksOutlineLevel(int)](../../com.aspose.words/outlineoptions\#setDefaultBookmarksOutlineLevel-int-)值被使用。

**退货:**
[BookmarksOutlineLevelCollection](../../com.aspose.words/bookmarksoutlinelevelcollection) - 相应的[BookmarksOutlineLevelCollection](../../com.aspose.words/bookmarksoutlinelevelcollection)价值。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getCreateMissingOutlineLevels() {#getCreateMissingOutlineLevels--}
```
public boolean getCreateMissingOutlineLevels()
```


获取或设置一个值，该值确定在导出文档时是否创建缺少的大纲级别。

此属性的默认值为**false**.

**退货:**
boolean - 对应的布尔值。
### getCreateOutlinesForHeadingsInTables() {#getCreateOutlinesForHeadingsInTables--}
```
public boolean getCreateOutlinesForHeadingsInTables()
```


指定是否为表格内的标题（使用标题样式格式化的段落）创建大纲。

默认值为**false**.

**退货:**
boolean - 对应的布尔值。
### getDefaultBookmarksOutlineLevel() {#getDefaultBookmarksOutlineLevel--}
```
public int getDefaultBookmarksOutlineLevel()
```


指定文档大纲中显示 Word 书签的默认级别。

可以使用指定单个书签级别[getBookmarksOutlineLevels()](../../com.aspose.words/outlineoptions\#getBookmarksOutlineLevels--)财产。

指定 0，Word 书签将不会显示在文档大纲中。指定 1，Word 书签将显示在第 1 级的文档大纲中； 2 表示 2 级，依此类推。

默认值为 0。有效范围为 0 到 9。

**退货:**
int - 对应的 int 值。
### getExpandedOutlineLevels() {#getExpandedOutlineLevels--}
```
public int getExpandedOutlineLevels()
```


指定查看文件时在文档大纲中显示展开的级别数。

请注意，保存到 XPS 时，此选项将不起作用。

指定0，文档大纲将被折叠；指定1，大纲中的第一级项目将被展开，依此类推。

默认值为 0。有效范围为 0 到 9。

**退货:**
int - 对应的 int 值。
### getHeadingsOutlineLevels() {#getHeadingsOutlineLevels--}
```
public int getHeadingsOutlineLevels()
```


指定要包含在文档大纲中的标题级别（使用标题样式格式化的段落）。

指定 0 表示大纲中没有标题；为大纲中的一级标题指定 1，依此类推。

默认值为 0。有效范围为 0 到 9。

**退货:**
int - 对应的 int 值。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setCreateMissingOutlineLevels(boolean value) {#setCreateMissingOutlineLevels-boolean-}
```
public void setCreateMissingOutlineLevels(boolean value)
```


获取或设置一个值，该值确定在导出文档时是否创建缺少的大纲级别。

此属性的默认值为**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setCreateOutlinesForHeadingsInTables(boolean value) {#setCreateOutlinesForHeadingsInTables-boolean-}
```
public void setCreateOutlinesForHeadingsInTables(boolean value)
```


指定是否为表格内的标题（使用标题样式格式化的段落）创建大纲。

默认值为**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setDefaultBookmarksOutlineLevel(int value) {#setDefaultBookmarksOutlineLevel-int-}
```
public void setDefaultBookmarksOutlineLevel(int value)
```


指定文档大纲中显示 Word 书签的默认级别。

可以使用指定单个书签级别[getBookmarksOutlineLevels()](../../com.aspose.words/outlineoptions\#getBookmarksOutlineLevels--)财产。

指定 0，Word 书签将不会显示在文档大纲中。指定 1，Word 书签将显示在第 1 级的文档大纲中； 2 表示 2 级，依此类推。

默认值为 0。有效范围为 0 到 9。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。 |

### setExpandedOutlineLevels(int value) {#setExpandedOutlineLevels-int-}
```
public void setExpandedOutlineLevels(int value)
```


指定查看文件时在文档大纲中显示展开的级别数。

请注意，保存到 XPS 时，此选项将不起作用。

指定0，文档大纲将被折叠；指定1，大纲中的第一级项目将被展开，依此类推。

默认值为 0。有效范围为 0 到 9。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。 |

### setHeadingsOutlineLevels(int value) {#setHeadingsOutlineLevels-int-}
```
public void setHeadingsOutlineLevels(int value)
```


指定要包含在文档大纲中的标题级别（使用标题样式格式化的段落）。

指定 0 表示大纲中没有标题；为大纲中的一级标题指定 1，依此类推。

默认值为 0。有效范围为 0 到 9。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。 |

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
