---
title: "ComparerContext"
linktitle: "ComparerContext"
second_title: "Aspose.Words for Java"
description: "Java 中的文档比较器上下文。"
type: docs
weight: 115
url: /zh/java/com.aspose.words/comparercontext/
---

**Inheritance:**
java.lang.Object，[com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class ComparerContext extends ProcessorContext
```

文档比较器上下文

 **Examples:** 

展示如何使用上下文简单比较文档。

```

 // There is a several ways to compare documents:
 String firstDoc = getMyDir() + "Table column bookmarks.docx";
 String secondDoc = getMyDir() + "Table column bookmarks.doc";

 ComparerContext comparerContext = new ComparerContext();
 comparerContext.getCompareOptions().setIgnoreCaseChanges(true);
 comparerContext.setAuthor("Author");
 comparerContext.setDateTime(new Date());

 Comparer.create(comparerContext)
         .from(firstDoc)
         .from(secondDoc)
         .to(getArtifactsDir() + "LowCode.CompareContextDocuments.docx")
         .execute();
 
```

展示如何使用上下文从流中比较文档。

```

 // There is a several ways to compare documents from the stream:
 try (FileInputStream firstStreamIn = new FileInputStream(getMyDir() + "Table column bookmarks.docx")) {
     try (FileInputStream secondStreamIn = new FileInputStream(getMyDir() + "Table column bookmarks.doc")) {
         ComparerContext comparerContext = new ComparerContext();
         comparerContext.getCompareOptions().setIgnoreCaseChanges(true);
         comparerContext.setAuthor("Author");
         comparerContext.setDateTime(new Date());

         try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.CompareContextStreamDocuments.docx")) {
             Comparer.create(comparerContext)
                     .from(firstStreamIn)
                     .from(secondStreamIn)
                     .to(streamOut, SaveFormat.DOCX)
                     .execute();
         }
     }
 }
 
```
## 构造函数

| 构造函数 | 描述 |
| --- | --- |
| [ComparerContext()](#ComparerContext) | 初始化此类的新实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [getAcceptRevisions()](#getAcceptRevisions) | 指示在比较文档之前是否接受文档中的修订。 |
| [getAuthor()](#getAuthor) | 在文档比较期间创建的修订要分配的作者。 |
| [getCompareOptions()](#getCompareOptions) | 比较文档时使用的选项。 |
| [getDateTime()](#getDateTime) | 在文档比较期间创建的修订分配的日期和时间。 |
| [getFontSettings()](#getFontSettings) | 处理器使用的字体设置。 |
| [getLayoutOptions()](#getLayoutOptions) | 处理器使用的文档布局选项。 |
| [getWarningCallback()](#getWarningCallback) | 处理器使用的警告回调。 |
| [setAcceptRevisions(boolean value)](#setAcceptRevisions-boolean) | 指示在比较文档之前是否接受文档中的修订。 |
| [setAuthor(String value)](#setAuthor-java.lang.String) | 在文档比较期间创建的修订要分配的作者。 |
| [setDateTime(Date value)](#setDateTime-java.util.Date) | 在文档比较期间创建的修订分配的日期和时间。 |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | 处理器使用的字体设置。 |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | 处理器使用的警告回调。 |
### ComparerContext() {#ComparerContext}
```
public ComparerContext()
```


初始化此类的新实例。

### getAcceptRevisions() {#getAcceptRevisions}
```
public boolean getAcceptRevisions()
```


指示在比较文档之前是否接受文档中的修订。如果比较的文档包含修订且此标志设置为 false，处理器将拒绝修订。默认值为 true。

**Returns:**
boolean - 相应的 boolean 值。
### getAuthor() {#getAuthor}
```
public String getAuthor()
```


在文档比较期间创建的修订要分配的作者。

**Returns:**
java.lang.String - 相应的 java.lang.String 值。
### getCompareOptions() {#getCompareOptions}
```
public CompareOptions getCompareOptions()
```


比较文档时使用的选项。

 **Examples:** 

展示如何使用上下文简单比较文档。

```

 // There is a several ways to compare documents:
 String firstDoc = getMyDir() + "Table column bookmarks.docx";
 String secondDoc = getMyDir() + "Table column bookmarks.doc";

 ComparerContext comparerContext = new ComparerContext();
 comparerContext.getCompareOptions().setIgnoreCaseChanges(true);
 comparerContext.setAuthor("Author");
 comparerContext.setDateTime(new Date());

 Comparer.create(comparerContext)
         .from(firstDoc)
         .from(secondDoc)
         .to(getArtifactsDir() + "LowCode.CompareContextDocuments.docx")
         .execute();
 
```

展示如何使用上下文从流中比较文档。

```

 // There is a several ways to compare documents from the stream:
 try (FileInputStream firstStreamIn = new FileInputStream(getMyDir() + "Table column bookmarks.docx")) {
     try (FileInputStream secondStreamIn = new FileInputStream(getMyDir() + "Table column bookmarks.doc")) {
         ComparerContext comparerContext = new ComparerContext();
         comparerContext.getCompareOptions().setIgnoreCaseChanges(true);
         comparerContext.setAuthor("Author");
         comparerContext.setDateTime(new Date());

         try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.CompareContextStreamDocuments.docx")) {
             Comparer.create(comparerContext)
                     .from(firstStreamIn)
                     .from(secondStreamIn)
                     .to(streamOut, SaveFormat.DOCX)
                     .execute();
         }
     }
 }
 
```

**Returns:**
[CompareOptions](../../com.aspose.words/compareoptions/) - The corresponding [CompareOptions](../../com.aspose.words/compareoptions/) value.
### getDateTime() {#getDateTime}
```
public Date getDateTime()
```


在文档比较期间创建的修订分配的日期和时间。

**Returns:**
java.util.Date - 对应的 java.util.Date 值。
### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


处理器使用的字体设置。

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getLayoutOptions() {#getLayoutOptions}
```
public LayoutOptions getLayoutOptions()
```


处理器使用的文档布局选项。

**Returns:**
[LayoutOptions](../../com.aspose.words/layoutoptions/) - The corresponding [LayoutOptions](../../com.aspose.words/layoutoptions/) value.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


处理器使用的警告回调。

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setAcceptRevisions(boolean value) {#setAcceptRevisions-boolean}
```
public void setAcceptRevisions(boolean value)
```


指示在比较文档之前是否接受文档中的修订。如果比较的文档包含修订且此标志设置为 false，处理器将拒绝修订。默认值为 true。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 相应的 boolean 值。 |

### setAuthor(String value) {#setAuthor-java.lang.String}
```
public void setAuthor(String value)
```


在文档比较期间创建的修订要分配的作者。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setDateTime(Date value) {#setDateTime-java.util.Date}
```
public void setDateTime(Date value)
```


在文档比较期间创建的修订分配的日期和时间。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | java.util.Date | 对应的 java.util.Date 值。 |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


处理器使用的字体设置。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | 对应的[FontSettings](../../com.aspose.words/fontsettings/)值。 |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


处理器使用的警告回调。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | 对应的[IWarningCallback](../../com.aspose.words/iwarningcallback/)值。 |

