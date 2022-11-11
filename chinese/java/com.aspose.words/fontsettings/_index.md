---
title: FontSettings
second_title: Aspose.Words for Java API Reference
description: 指定文档的字体设置。
type: docs
weight: 286
url: /zh/java/com.aspose.words/fontsettings/
---

**遗产:**
java.lang.Object
```
public class FontSettings
```

指定文档的字体设置。

要了解更多信息，请访问**Working with Fonts**文档文章。

 Aspose.Words 使用字体设置来解析文档中的字体。字体主要在构建文档布局或呈现为固定页面格式时得到解决。但是在加载某些格式时，Aspose.Words 也可能需要解析字体。例如，在加载 HTML 文档时，Aspose.Words 可能会解析字体以执行字体回退。所以建议你在字体设置中设置[LoadOptions](../../com.aspose.words/loadoptions)加载文档时。或者至少在构建布局或将文档呈现为固定页面格式之前。

默认情况下，所有文档都使用单个静态字体设置实例。它可以通过[getDefaultInstance()](../../com.aspose.words/fontsettings\#getDefaultInstance--)财产。

随时从任何线程更改字体设置都是安全的。但建议您在处理某些使用此设置的文档时不要更改字体设置。这可能会导致相同的字体在文档的不同部分以不同的方式解析。
## 构造函数

| 构造函数 | 描述 |
| --- | --- |
| [FontSettings()](#FontSettings--) | 初始化此类的新实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getDefaultInstance()](#getDefaultInstance--) | 静态默认字体设置。 |
| [getFallbackSettings()](#getFallbackSettings--) | 与字体回退机制相关的设置。 |
| [getFontsSources()](#getFontsSources--) | 获取数组的副本，其中包含 Aspose.Words 查找 True类型 字体的源列表。 |
| [getSubstitutionSettings()](#getSubstitutionSettings--) | 与字体替换机制相关的设置。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [resetFontSources()](#resetFontSources--) | 将字体源重置为系统默认值。 |
| [saveSearchCache(OutputStream outputStream)](#saveSearchCache-java.io.OutputStream-) |  |
| [setFontsFolder(String fontFolder, boolean recursive)](#setFontsFolder-java.lang.String-boolean-) | 设置 Aspose.Words 在渲染文档或嵌入字体时查找 True类型 字体的文件夹。 |
| [setFontsFolders(String[] fontsFolders, boolean recursive)](#setFontsFolders-java.lang.String---boolean-) | 设置 Aspose.Words 在渲染文档或嵌入字体时查找 True类型 字体的文件夹。 |
| [setFontsSources(FontSourceBase[] sources)](#setFontsSources-com.aspose.words.FontSourceBase---) | 设置 Aspose.Words 在渲染文档或嵌入字体时查找 True类型 字体的来源。 |
| [setFontsSources(FontSourceBase[] sources, InputStream cacheInputStream)](#setFontsSources-com.aspose.words.FontSourceBase---java.io.InputStream-) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### FontSettings() {#FontSettings--}
```
public FontSettings()
```


初始化此类的新实例。

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
### getDefaultInstance() {#getDefaultInstance--}
```
public static FontSettings getDefaultInstance()
```


静态默认字体设置。默认情况下，此实例在文档中使用，除非[Document.getFontSettings()](../../com.aspose.words/document\#getFontSettings--) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document\#setFontSettings-com.aspose.words.FontSettings-)被指定。

**退货:**
[FontSettings](../../com.aspose.words/fontsettings) - 相应的[FontSettings](../../com.aspose.words/fontsettings)价值。
### getFallbackSettings() {#getFallbackSettings--}
```
public FontFallbackSettings getFallbackSettings()
```


与字体回退机制相关的设置。

**退货:**
[FontFallbackSettings](../../com.aspose.words/fontfallbacksettings) - 相应的[FontFallbackSettings](../../com.aspose.words/fontfallbacksettings)价值。
### getFontsSources() {#getFontsSources--}
```
public FontSourceBase[] getFontsSources()
```


获取数组的副本，其中包含 Aspose.Words 查找 True类型 字体的源列表。

返回值是 Aspose.Words 使用的数据的副本。如果您更改返回数组中的条目，它将不会影响文档呈现。要指定新字体源，请使用[setFontsSources(com.aspose.words.FontSourceBase[])](../../com.aspose.words/fontsettings\#setFontsSources-com.aspose.words.FontSourceBase---)方法。

**退货:**
com.aspose.words.FontSourceBase[] - 当前字体源的副本。
### getSubstitutionSettings() {#getSubstitutionSettings--}
```
public FontSubstitutionSettings getSubstitutionSettings()
```


与字体替换机制相关的设置。

**退货:**
[FontSubstitutionSettings](../../com.aspose.words/fontsubstitutionsettings) - 相应的[FontSubstitutionSettings](../../com.aspose.words/fontsubstitutionsettings)价值。
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




### resetFontSources() {#resetFontSources--}
```
public void resetFontSources()
```


将字体源重置为系统默认值。

### saveSearchCache(OutputStream outputStream) {#saveSearchCache-java.io.OutputStream-}
```
public void saveSearchCache(OutputStream outputStream)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |

### setFontsFolder(String fontFolder, boolean recursive) {#setFontsFolder-java.lang.String-boolean-}
```
public void setFontsFolder(String fontFolder, boolean recursive)
```


设置 Aspose.Words 在渲染文档或嵌入字体时查找 True类型 字体的文件夹。这是一个快捷方式[setFontsFolders(java.lang.String[], boolean)](../../com.aspose.words/fontsettings\#setFontsFolders-java.lang.String----boolean-)仅设置一个字体目录。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontFolder | java.lang.String | 包含 True类型 字体的文件夹。 |
| recursive | boolean | True 以递归方式扫描指定文件夹中的字体。 |

### setFontsFolders(String[] fontsFolders, boolean recursive) {#setFontsFolders-java.lang.String---boolean-}
```
public void setFontsFolders(String[] fontsFolders, boolean recursive)
```


设置 Aspose.Words 在渲染文档或嵌入字体时查找 True类型 字体的文件夹。

默认情况下，Aspose.Words 会查找安装到系统中的字体。

设置此属性会重置所有先前加载的字体的缓存。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontsFolders | java.lang.String[] | 包含 True类型 字体的文件夹数组。 |
| recursive | boolean | True 以递归方式扫描指定文件夹中的字体。 |

### setFontsSources(FontSourceBase[] sources) {#setFontsSources-com.aspose.words.FontSourceBase---}
```
public void setFontsSources(FontSourceBase[] sources)
```


设置 Aspose.Words 在渲染文档或嵌入字体时查找 True类型 字体的来源。

默认情况下，Aspose.Words 会查找安装到系统中的字体。

设置此属性会重置所有先前加载的字体的缓存。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| sources | [FontSourceBase\[\]](../../com.aspose.words/fontsourcebase) | 包含 True类型 字体的源数组。 |

### setFontsSources(FontSourceBase[] sources, InputStream cacheInputStream) {#setFontsSources-com.aspose.words.FontSourceBase---java.io.InputStream-}
```
public void setFontsSources(FontSourceBase[] sources, InputStream cacheInputStream)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| sources | [FontSourceBase\[\]](../../com.aspose.words/fontsourcebase) |  |
| cacheInputStream | java.io.InputStream |  |

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
