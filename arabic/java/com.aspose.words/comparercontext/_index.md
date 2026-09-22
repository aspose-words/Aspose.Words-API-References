---
title: "ComparerContext"
linktitle: "ComparerContext"
second_title: "Aspose.Words لـ Java"
description: "سياق مقارنة المستندات في Java."
type: docs
weight: 115
url: /ar/java/com.aspose.words/comparercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class ComparerContext extends ProcessorContext
```

سياق مقارنة المستندات

 **Examples:** 

يوضح كيفية مقارنة المستندات ببساطة باستخدام السياق.

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

يوضح كيفية مقارنة المستندات من الدفق باستخدام السياق.

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
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [ComparerContext()](#ComparerContext) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getAcceptRevisions()](#getAcceptRevisions) | يشير إلى ما إذا كان يجب قبول التعديلات في المستندات قبل مقارنتها. |
| [getAuthor()](#getAuthor) | المؤلف الذي سيُعيّن للتعديلات التي تم إنشاؤها أثناء مقارنة المستندات. |
| [getCompareOptions()](#getCompareOptions) | الخيارات المستخدمة عند مقارنة المستندات. |
| [getDateTime()](#getDateTime) | التاريخ والوقت المعينان للتعديلات التي تم إنشاؤها أثناء مقارنة المستندات. |
| [getFontSettings()](#getFontSettings) | إعدادات الخط المستخدمة بواسطة المعالج. |
| [getLayoutOptions()](#getLayoutOptions) | خيارات تخطيط المستند المستخدمة بواسطة المعالج. |
| [getWarningCallback()](#getWarningCallback) | دالة رد النداء للتحذير المستخدمة بواسطة المعالج. |
| [setAcceptRevisions(boolean value)](#setAcceptRevisions-boolean) | يشير إلى ما إذا كان يجب قبول التعديلات في المستندات قبل مقارنتها. |
| [setAuthor(String value)](#setAuthor-java.lang.String) | المؤلف الذي سيُعيّن للتعديلات التي تم إنشاؤها أثناء مقارنة المستندات. |
| [setDateTime(Date value)](#setDateTime-java.util.Date) | التاريخ والوقت المعينان للتعديلات التي تم إنشاؤها أثناء مقارنة المستندات. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | إعدادات الخط المستخدمة بواسطة المعالج. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | دالة رد النداء للتحذير المستخدمة بواسطة المعالج. |
### ComparerContext() {#ComparerContext}
```
public ComparerContext()
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

### getAcceptRevisions() {#getAcceptRevisions}
```
public boolean getAcceptRevisions()
```


يشير إلى ما إذا كان يجب قبول التعديلات في المستندات قبل مقارنتها. إذا كانت المستندات المقارنة تحتوي على تعديلات وتم تعيين هذه العلامة إلى false، فسيقوم المعالج برفض التعديلات. القيمة الافتراضية هي true .

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getAuthor() {#getAuthor}
```
public String getAuthor()
```


المؤلف الذي سيُعيّن للتعديلات التي تم إنشاؤها أثناء مقارنة المستندات.

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getCompareOptions() {#getCompareOptions}
```
public CompareOptions getCompareOptions()
```


الخيارات المستخدمة عند مقارنة المستندات.

 **Examples:** 

يوضح كيفية مقارنة المستندات ببساطة باستخدام السياق.

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

يوضح كيفية مقارنة المستندات من الدفق باستخدام السياق.

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


التاريخ والوقت المعينان للتعديلات التي تم إنشاؤها أثناء مقارنة المستندات.

**Returns:**
java.util.Date - القيمة المقابلة لـ java.util.Date.
### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


إعدادات الخط المستخدمة بواسطة المعالج.

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getLayoutOptions() {#getLayoutOptions}
```
public LayoutOptions getLayoutOptions()
```


خيارات تخطيط المستند المستخدمة بواسطة المعالج.

**Returns:**
[LayoutOptions](../../com.aspose.words/layoutoptions/) - The corresponding [LayoutOptions](../../com.aspose.words/layoutoptions/) value.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


دالة رد النداء للتحذير المستخدمة بواسطة المعالج.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setAcceptRevisions(boolean value) {#setAcceptRevisions-boolean}
```
public void setAcceptRevisions(boolean value)
```


يشير إلى ما إذا كان يجب قبول التعديلات في المستندات قبل مقارنتها. إذا كانت المستندات المقارنة تحتوي على تعديلات وتم تعيين هذه العلامة إلى false، فسيقوم المعالج برفض التعديلات. القيمة الافتراضية هي true .

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setAuthor(String value) {#setAuthor-java.lang.String}
```
public void setAuthor(String value)
```


المؤلف الذي سيُعيّن للتعديلات التي تم إنشاؤها أثناء مقارنة المستندات.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

### setDateTime(Date value) {#setDateTime-java.util.Date}
```
public void setDateTime(Date value)
```


التاريخ والوقت المعينان للتعديلات التي تم إنشاؤها أثناء مقارنة المستندات.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.util.Date | القيمة المقابلة لـ java.util.Date. |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


إعدادات الخط المستخدمة بواسطة المعالج.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | القيمة المقابلة لـ [FontSettings](../../com.aspose.words/fontsettings/). |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


دالة رد النداء للتحذير المستخدمة بواسطة المعالج.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | القيمة المقابلة لـ [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

