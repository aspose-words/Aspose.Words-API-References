---
title: TableSubstitutionRule
second_title: Aspose.Words for Java API Reference
description: 表格字体替换规则。
type: docs
weight: 554
url: /zh/java/com.aspose.words/tablesubstitutionrule/
---

**遗产:**
java.lang.Object, [com.aspose.words.FontSubstitutionRule](../../com.aspose.words/fontsubstitutionrule)
```
public class TableSubstitutionRule extends FontSubstitutionRule
```

表格字体替换规则。

要了解更多信息，请访问**Working with Fonts**文档文章。

如果原始字体不可用，此规则定义要使用的替代字体名称列表。将检查替代品的字体名称和[FontInfo.getAltName()](../../com.aspose.words/fontinfo\#getAltName--) / [FontInfo.setAltName(java.lang.String)](../../com.aspose.words/fontinfo\#setAltName-java.lang.String-)（如果有的话）。
## 方法

| 方法 | 描述 |
| --- | --- |
| [addSubstitutes(String originalFontName, String[] substituteFontNames)](#addSubstitutes-java.lang.String-java.lang.String...-) | 为给定的原始字体名称添加替代字体名称。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getEnabled()](#getEnabled--) | 指定是否启用规则。 |
| [getSubstitutes(String originalFontName)](#getSubstitutes-java.lang.String-) | 返回包含指定原始字体名称的替代字体名称的数组。 |
| [hashCode()](#hashCode--) |  |
| [load(InputStream stream)](#load-java.io.InputStream-) |  |
| [load(String fileName)](#load-java.lang.String-) | 从 XML 文件加载表替换设置。 |
| [loadAndroidSettings()](#loadAndroidSettings--) | 为 Linux 平台加载预定义的表替换设置。 |
| [loadLinuxSettings()](#loadLinuxSettings--) | 为 Linux 平台加载预定义的表替换设置。 |
| [loadWindowsSettings()](#loadWindowsSettings--) | 为 Windows 平台加载预定义的表替换设置。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [save(OutputStream outputStream)](#save-java.io.OutputStream-) |  |
| [save(String fileName)](#save-java.lang.String-) | 将当前表替换设置保存到文件。 |
| [setEnabled(boolean value)](#setEnabled-boolean-) | 指定是否启用规则。 |
| [setSubstitutes(String originalFontName, String[] substituteFontNames)](#setSubstitutes-java.lang.String-java.lang.String...-) | 覆盖给定原始字体名称的替代字体名称。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### addSubstitutes(String originalFontName, String[] substituteFontNames) {#addSubstitutes-java.lang.String-java.lang.String...-}
```
public void addSubstitutes(String originalFontName, String[] substituteFontNames)
```


为给定的原始字体名称添加替代字体名称。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| originalFontName | java.lang.String | 原始字体名称。 |
| substituteFontNames | java.lang.String[] | 替代字体名称列表。 |

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
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getEnabled() {#getEnabled--}
```
public boolean getEnabled()
```


指定是否启用规则。

**退货:**
boolean - 对应的布尔值。
### getSubstitutes(String originalFontName) {#getSubstitutes-java.lang.String-}
```
public Iterable getSubstitutes(String originalFontName)
```


返回包含指定原始字体名称的替代字体名称的数组。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| originalFontName | java.lang.String | 原始字体名称。 |

**退货:**
java.lang.Iterable - 替代字体名称列表。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### load(InputStream stream) {#load-java.io.InputStream-}
```
public void load(InputStream stream)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### load(String fileName) {#load-java.lang.String-}
```
public void load(String fileName)
```


从 XML 文件加载表替换设置。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 输入文件名。 |

### loadAndroidSettings() {#loadAndroidSettings--}
```
public void loadAndroidSettings()
```


为 Linux 平台加载预定义的表替换设置。

### loadLinuxSettings() {#loadLinuxSettings--}
```
public void loadLinuxSettings()
```


为 Linux 平台加载预定义的表替换设置。

### loadWindowsSettings() {#loadWindowsSettings--}
```
public void loadWindowsSettings()
```


为 Windows 平台加载预定义的表替换设置。

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### save(OutputStream outputStream) {#save-java.io.OutputStream-}
```
public void save(OutputStream outputStream)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |

### save(String fileName) {#save-java.lang.String-}
```
public void save(String fileName)
```


将当前表替换设置保存到文件。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 输出文件名。 |

### setEnabled(boolean value) {#setEnabled-boolean-}
```
public void setEnabled(boolean value)
```


指定是否启用规则。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setSubstitutes(String originalFontName, String[] substituteFontNames) {#setSubstitutes-java.lang.String-java.lang.String...-}
```
public void setSubstitutes(String originalFontName, String[] substituteFontNames)
```


覆盖给定原始字体名称的替代字体名称。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| originalFontName | java.lang.String | 原始字体名称。 |
| substituteFontNames | java.lang.String[] | 替代字体名称列表。 |

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
