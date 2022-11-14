---
title: ReplacingArgs
second_title: Aspose.Words for Java API 参考
description: 为自定义替换操作提供数据。
type: docs
weight: 476
url: /zh/java/com.aspose.words/replacingargs/
---

**遗产:**
java.lang.Object
```
public class ReplacingArgs
```

为自定义替换操作提供数据。

要了解更多信息，请访问**Find and Replace**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getGroupIndex()](#getGroupIndex--) | 通过索引标识在[getMatch()](../../com.aspose.words/replacingargs\#getMatch--)那将被替换为[getReplacement()](../../com.aspose.words/replacingargs\#getReplacement--) / [setReplacement(java.lang.String)](../../com.aspose.words/replacingargs\#setReplacement-java.lang.String-)细绳。 |
| [getMatch()](#getMatch--) |  java.util.regex.Matcher 由单个正则表达式匹配产生**Replace**. |
| [getMatchNode()](#getMatchNode--) | 获取包含匹配开始的节点。 |
| [getMatchOffset()](#getMatchOffset--) | 从包含匹配开头的节点的开头获取匹配的从零开始的起始位置。 |
| [getReplacement()](#getReplacement--) | 获取替换字符串。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setGroupIndex(int value)](#setGroupIndex-int-) | 通过索引标识在[getMatch()](../../com.aspose.words/replacingargs\#getMatch--)那将被替换为[getReplacement()](../../com.aspose.words/replacingargs\#getReplacement--) / [setReplacement(java.lang.String)](../../com.aspose.words/replacingargs\#setReplacement-java.lang.String-)细绳。 |
| [setReplacement(String value)](#setReplacement-java.lang.String-) | 设置替换字符串。 |
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getGroupIndex() {#getGroupIndex--}
```
public int getGroupIndex()
```


通过索引标识在[getMatch()](../../com.aspose.words/replacingargs\#getMatch--)那将被替换为[getReplacement()](../../com.aspose.words/replacingargs\#getReplacement--) / [setReplacement(java.lang.String)](../../com.aspose.words/replacingargs\#setReplacement-java.lang.String-)细绳。

默认为零。

**退货:**
int - 对应的 int 值。
### getMatch() {#getMatch--}
```
public Matcher getMatch()
```


 java.util.regex.Matcher 由单个正则表达式匹配产生**Replace**.

Matcher.start() 从查找和替换范围的开头获取匹配的从零开始的起始位置。

**退货:**
java.util.regex.Matcher - 相应的 java.util.regex.Matcher 值。
### getMatchNode() {#getMatchNode--}
```
public Node getMatchNode()
```


获取包含匹配开始的节点。

**退货:**
[Node](../../com.aspose.words/node) - 包含匹配开始的节点。
### getMatchOffset() {#getMatchOffset--}
```
public int getMatchOffset()
```


从包含匹配开头的节点的开头获取匹配的从零开始的起始位置。

**退货:**
int - 从包含匹配开始的节点开始的匹配从零开始的起始位置。
### getReplacement() {#getReplacement--}
```
public String getReplacement()
```


获取替换字符串。

**退货:**
java.lang.String - 替换字符串。
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




### setGroupIndex(int value) {#setGroupIndex-int-}
```
public void setGroupIndex(int value)
```


通过索引标识在[getMatch()](../../com.aspose.words/replacingargs\#getMatch--)那将被替换为[getReplacement()](../../com.aspose.words/replacingargs\#getReplacement--) / [setReplacement(java.lang.String)](../../com.aspose.words/replacingargs\#setReplacement-java.lang.String-)细绳。

默认为零。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。 |

### setReplacement(String value) {#setReplacement-java.lang.String-}
```
public void setReplacement(String value)
```


设置替换字符串。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 替换字符串。 |

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
