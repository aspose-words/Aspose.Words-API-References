---
title: "ReplacerContext"
linktitle: "ReplacerContext"
second_title: "Aspose.Words لـ Java"
description: "سياق عملية البحث/الاستبدال في Java."
type: docs
weight: 568
url: /ar/java/com.aspose.words/replacercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class ReplacerContext extends ProcessorContext
```

سياق عملية البحث/الاستبدال.

 **Examples:** 

يوضح كيفية استبدال السلسلة في المستند باستخدام السياق.

```

 // There is a several ways to replace string in the document:
 String doc = getMyDir() + "Footer.docx";
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 ReplacerContext replacerContext = new ReplacerContext();
 replacerContext.setReplacement(pattern, replacement);
 replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

 Replacer.create(replacerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ReplaceContext.docx")
         .execute();
 
```

يوضح كيفية استبدال السلسلة في المستند باستخدام المستندات من الدفق باستخدام السياق.

```

 // There is a several ways to replace string in the document using documents from the stream:
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Footer.docx")) {
     ReplacerContext replacerContext = new ReplacerContext();
     replacerContext.setReplacement(pattern, replacement);
     replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ReplaceContextStream.docx")) {
         Replacer.create(replacerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

يوضح كيفية استبدال السلسلة باستخدام تعبير عادي في المستند باستخدام السياق.

```

 // There is a several ways to replace string with regex in the document:
 String doc = getMyDir() + "Footer.docx";
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 ReplacerContext replacerContext = new ReplacerContext();
 replacerContext.setReplacement(pattern, replacement);
 replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

 Replacer.create(replacerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ReplaceContextRegex.docx")
         .execute();
 
```

يوضح كيفية استبدال السلسلة باستخدام تعبير عادي في المستند باستخدام المستندات من الدفق باستخدام السياق.

```

 // There is a several ways to replace string with regex in the document using documents from the stream:
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Replace regex.docx")) {
     ReplacerContext replacerContext = new ReplacerContext();
     replacerContext.setReplacement(pattern, replacement);
     replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ReplaceContextStreamRegex.docx")) {
         Replacer.create(replacerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [ReplacerContext()](#ReplacerContext) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getFindReplaceOptions()](#getFindReplaceOptions) | خيارات البحث/الاستبدال. |
| [getFontSettings()](#getFontSettings) | إعدادات الخط المستخدمة بواسطة المعالج. |
| [getLayoutOptions()](#getLayoutOptions) | خيارات تخطيط المستند المستخدمة بواسطة المعالج. |
| [getWarningCallback()](#getWarningCallback) | دالة رد النداء للتحذير المستخدمة بواسطة المعالج. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | إعدادات الخط المستخدمة بواسطة المعالج. |
| [setReplacement(String pattern, String replacement)](#setReplacement-java.lang.String-java.lang.String) | يضبط النمط والاستبدال المستخدمين في عملية البحث/الاستبدال. |
| [setReplacement(Pattern pattern, String replacement)](#setReplacement-java.util.regex.Pattern-java.lang.String) | يضبط النمط والاستبدال المستخدمين في عملية البحث/الاستبدال. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | دالة رد النداء للتحذير المستخدمة بواسطة المعالج. |
### ReplacerContext() {#ReplacerContext}
```
public ReplacerContext()
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

### getFindReplaceOptions() {#getFindReplaceOptions}
```
public FindReplaceOptions getFindReplaceOptions()
```


خيارات البحث/الاستبدال.

 **Examples:** 

يوضح كيفية استبدال السلسلة في المستند باستخدام السياق.

```

 // There is a several ways to replace string in the document:
 String doc = getMyDir() + "Footer.docx";
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 ReplacerContext replacerContext = new ReplacerContext();
 replacerContext.setReplacement(pattern, replacement);
 replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

 Replacer.create(replacerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ReplaceContext.docx")
         .execute();
 
```

يوضح كيفية استبدال السلسلة في المستند باستخدام المستندات من الدفق باستخدام السياق.

```

 // There is a several ways to replace string in the document using documents from the stream:
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Footer.docx")) {
     ReplacerContext replacerContext = new ReplacerContext();
     replacerContext.setReplacement(pattern, replacement);
     replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ReplaceContextStream.docx")) {
         Replacer.create(replacerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

يوضح كيفية استبدال السلسلة باستخدام تعبير عادي في المستند باستخدام السياق.

```

 // There is a several ways to replace string with regex in the document:
 String doc = getMyDir() + "Footer.docx";
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 ReplacerContext replacerContext = new ReplacerContext();
 replacerContext.setReplacement(pattern, replacement);
 replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

 Replacer.create(replacerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ReplaceContextRegex.docx")
         .execute();
 
```

يوضح كيفية استبدال السلسلة باستخدام تعبير عادي في المستند باستخدام المستندات من الدفق باستخدام السياق.

```

 // There is a several ways to replace string with regex in the document using documents from the stream:
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Replace regex.docx")) {
     ReplacerContext replacerContext = new ReplacerContext();
     replacerContext.setReplacement(pattern, replacement);
     replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ReplaceContextStreamRegex.docx")) {
         Replacer.create(replacerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Returns:**
[FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) - The corresponding [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) value.
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
### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


إعدادات الخط المستخدمة بواسطة المعالج.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | القيمة المقابلة لـ [FontSettings](../../com.aspose.words/fontsettings/). |

### setReplacement(String pattern, String replacement) {#setReplacement-java.lang.String-java.lang.String}
```
public void setReplacement(String pattern, String replacement)
```


يضبط النمط والاستبدال المستخدمين في عملية البحث/الاستبدال.

 **Remarks:** 

استخدام هذه الطريقة يتجاوز النمط والاستبدال المحددين مسبقًا.

 **Examples:** 

يوضح كيفية استبدال السلسلة في المستند باستخدام السياق.

```

 // There is a several ways to replace string in the document:
 String doc = getMyDir() + "Footer.docx";
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 ReplacerContext replacerContext = new ReplacerContext();
 replacerContext.setReplacement(pattern, replacement);
 replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

 Replacer.create(replacerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ReplaceContext.docx")
         .execute();
 
```

يوضح كيفية استبدال السلسلة في المستند باستخدام المستندات من الدفق باستخدام السياق.

```

 // There is a several ways to replace string in the document using documents from the stream:
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Footer.docx")) {
     ReplacerContext replacerContext = new ReplacerContext();
     replacerContext.setReplacement(pattern, replacement);
     replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ReplaceContextStream.docx")) {
         Replacer.create(replacerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| نمط | java.lang.String |  |
| استبدال | java.lang.String |  |

### setReplacement(Pattern pattern, String replacement) {#setReplacement-java.util.regex.Pattern-java.lang.String}
```
public void setReplacement(Pattern pattern, String replacement)
```


يضبط النمط والاستبدال المستخدمين في عملية البحث/الاستبدال.

 **Remarks:** 

استخدام هذه الطريقة يتجاوز النمط والاستبدال المحددين مسبقًا.

 **Examples:** 

يوضح كيفية استبدال السلسلة باستخدام تعبير عادي في المستند باستخدام السياق.

```

 // There is a several ways to replace string with regex in the document:
 String doc = getMyDir() + "Footer.docx";
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 ReplacerContext replacerContext = new ReplacerContext();
 replacerContext.setReplacement(pattern, replacement);
 replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

 Replacer.create(replacerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ReplaceContextRegex.docx")
         .execute();
 
```

يوضح كيفية استبدال السلسلة باستخدام تعبير عادي في المستند باستخدام المستندات من الدفق باستخدام السياق.

```

 // There is a several ways to replace string with regex in the document using documents from the stream:
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Replace regex.docx")) {
     ReplacerContext replacerContext = new ReplacerContext();
     replacerContext.setReplacement(pattern, replacement);
     replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ReplaceContextStreamRegex.docx")) {
         Replacer.create(replacerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| نمط | java.util.regex.Pattern |  |
| استبدال | java.lang.String |  |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


دالة رد النداء للتحذير المستخدمة بواسطة المعالج.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | القيمة المقابلة لـ [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

