---
title: "SplitterContext"
linktitle: "SplitterContext"
second_title: "Aspose.Words لـ Java"
description: "سياق مقسم المستند في Java."
type: docs
weight: 632
url: /ar/java/com.aspose.words/splittercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class SplitterContext extends ProcessorContext
```

سياق مقسّم المستند.

 **Examples:** 

يعرض كيفية تقسيم المستند إلى صفحات باستخدام السياق.

```

 String doc = getMyDir() + "Big document.docx";

 SplitterContext splitterContext = new SplitterContext();
 splitterContext.getSplitOptions().setSplitCriteria(SplitCriteria.PAGE);

 Splitter.create(splitterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.SplitContextDocument.docx")
         .execute();
 
```

يعرض كيفية تقسيم المستند من الدفق إلى صفحات باستخدام السياق.

```

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Big document.docx")) {
     SplitterContext splitterContext = new SplitterContext();
     splitterContext.getSplitOptions().setSplitCriteria(SplitCriteria.PAGE);

     ArrayList pages = new ArrayList<>();
     Splitter.create(splitterContext)
             .from(streamIn)
             .toOutput(pages, SaveFormat.DOCX)
             .execute();
 }
 
```
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [SplitterContext()](#SplitterContext) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getFontSettings()](#getFontSettings) | إعدادات الخط المستخدمة بواسطة المعالج. |
| [getLayoutOptions()](#getLayoutOptions) | خيارات تخطيط المستند المستخدمة بواسطة المعالج. |
| [getSplitOptions()](#getSplitOptions) | خيارات تقسيم المستند. |
| [getWarningCallback()](#getWarningCallback) | دالة رد النداء للتحذير المستخدمة بواسطة المعالج. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | إعدادات الخط المستخدمة بواسطة المعالج. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | دالة رد النداء للتحذير المستخدمة بواسطة المعالج. |
### SplitterContext() {#SplitterContext}
```
public SplitterContext()
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

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
### getSplitOptions() {#getSplitOptions}
```
public SplitOptions getSplitOptions()
```


خيارات تقسيم المستند.

 **Examples:** 

يعرض كيفية تقسيم المستند إلى صفحات باستخدام السياق.

```

 String doc = getMyDir() + "Big document.docx";

 SplitterContext splitterContext = new SplitterContext();
 splitterContext.getSplitOptions().setSplitCriteria(SplitCriteria.PAGE);

 Splitter.create(splitterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.SplitContextDocument.docx")
         .execute();
 
```

يعرض كيفية تقسيم المستند من الدفق إلى صفحات باستخدام السياق.

```

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Big document.docx")) {
     SplitterContext splitterContext = new SplitterContext();
     splitterContext.getSplitOptions().setSplitCriteria(SplitCriteria.PAGE);

     ArrayList pages = new ArrayList<>();
     Splitter.create(splitterContext)
             .from(streamIn)
             .toOutput(pages, SaveFormat.DOCX)
             .execute();
 }
 
```

**Returns:**
[SplitOptions](../../com.aspose.words/splitoptions/) - The corresponding [SplitOptions](../../com.aspose.words/splitoptions/) value.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


دالة رد النداء للتحذير المستخدمة بواسطة المعالج.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
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

