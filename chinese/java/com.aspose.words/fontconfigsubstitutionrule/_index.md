---
title: FontConfigSubstitutionRule
second_title: Aspose.Words for Java API 参考
description: 字体配置替换规则。
type: docs
weight: 276
url: /zh/java/com.aspose.words/fontconfigsubstitutionrule/
---

**遗产:**
java.lang.Object, [com.aspose.words.FontSubstitutionRule](../../com.aspose.words/fontsubstitutionrule)
```
public class FontConfigSubstitutionRule extends FontSubstitutionRule
```

字体配置替换规则。

要了解更多信息，请访问**Working with Fonts**文档文章。

如果原始字体不可用，此规则使用 Linux（和其他类 Unix）平台上的 fontconfig 实用程序来获取替换。

如果 fontconfig 实用程序不可用，则此规则将被忽略。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getEnabled()](#getEnabled--) | 指定是否启用规则。 |
| [hashCode()](#hashCode--) |  |
| [isFontConfigAvailable()](#isFontConfigAvailable--) | 检查 fontconfig 实用程序是否可用。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [resetCache()](#resetCache--) | 重置 fontconfig 调用结果的缓存。 |
| [setEnabled(boolean value)](#setEnabled-boolean-) | 指定是否启用规则。 |
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
### getEnabled() {#getEnabled--}
```
public boolean getEnabled()
```


指定是否启用规则。

**退货:**
boolean - 对应的布尔值。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isFontConfigAvailable() {#isFontConfigAvailable--}
```
public boolean isFontConfigAvailable()
```


检查 fontconfig 实用程序是否可用。

**退货:**
布尔值
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### resetCache() {#resetCache--}
```
public void resetCache()
```


重置 fontconfig 调用结果的缓存。

### setEnabled(boolean value) {#setEnabled-boolean-}
```
public void setEnabled(boolean value)
```


指定是否启用规则。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

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
