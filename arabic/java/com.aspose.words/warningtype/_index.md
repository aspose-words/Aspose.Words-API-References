---
title: "WarningType"
linktitle: "WarningType"
second_title: "Aspose.Words لـ Java"
description: "يحدد نوع التحذير الذي تصدره Aspose.Words أثناء تحميل أو حفظ المستند في Java."
type: docs
weight: 720
url: /ar/java/com.aspose.words/warningtype/
---

**Inheritance:**
java.lang.Object
```
public class WarningType
```

يحدد نوع التحذير الذي تصدره Aspose.Words أثناء تحميل المستند أو حفظه.

 **Examples:** 

يوضح كيفية تعيين الخاصية للعثور على أقرب تطابق للخط المفقود من مصادر الخطوط المتاحة.

```

 // Open a document that contains text formatted with a font that does not exist in any of our font sources.
 Document doc = new Document(getMyDir() + "Missing font.docx");

 // Assign a callback for handling font substitution warnings.
 WarningInfoCollection warningCollector = new WarningInfoCollection();
 doc.setWarningCallback(warningCollector);

 // Set a default font name and enable font substitution.
 FontSettings fontSettings = new FontSettings();
 fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
 fontSettings.getSubstitutionSettings().getFontInfoSubstitution().setEnabled(true);

 // Original font metrics should be used after font substitution.
 doc.getLayoutOptions().setKeepOriginalFontMetrics(true);

 // We will get a font substitution warning if we save a document with a missing font.
 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.EnableFontSubstitution.pdf");

 for (WarningInfo info : warningCollector)
 {
     if (info.getWarningType() == WarningType.FONT_SUBSTITUTION)
         System.out.println(info.getDescription());
 }
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [DATA_LOSS](#DATA-LOSS) | فقدان بيانات عام، بدون رمز محدد. |
| [DATA_LOSS_CATEGORY](#DATA-LOSS-CATEGORY) | قد يكون بعض النص/الحرف/الصورة أو بيانات أخرى مفقودة إما من شجرة المستند بعد التحميل، أو من المستند المُنشأ بعد الحفظ. |
| [FONT_EMBEDDING](#FONT-EMBEDDING) | فقدان معلومات الخط المضمن أثناء حفظ المستند. |
| [FONT_SUBSTITUTION](#FONT-SUBSTITUTION) | تم استبدال الخط. |
| [HINT](#HINT) | ينصح بمشكلة محتملة أو يقترح تحسينًا. |
| [MAJOR_FORMATTING_LOSS](#MAJOR-FORMATTING-LOSS) | فقدان تنسيق رئيسي عام، بدون رمز محدد. |
| [MAJOR_FORMATTING_LOSS_CATEGORY](#MAJOR-FORMATTING-LOSS-CATEGORY) | قد يبدو المستند الناتج أو موقع معين فيه مختلفًا بشكل كبير مقارنة بالمستند الأصلي. |
| [MINOR_FORMATTING_LOSS](#MINOR-FORMATTING-LOSS) | فقدان تنسيق فرعي عام، بدون رمز محدد. |
| [MINOR_FORMATTING_LOSS_CATEGORY](#MINOR-FORMATTING-LOSS-CATEGORY) | قد يبدو المستند الناتج أو موقع معين فيه مختلفًا إلى حد ما مقارنة بالمستند الأصلي. |
| [UNEXPECTED_CONTENT](#UNEXPECTED-CONTENT) | محتوى غير متوقع عام، بدون رمز محدد. |
| [UNEXPECTED_CONTENT_CATEGORY](#UNEXPECTED-CONTENT-CATEGORY) | لم يتم التعرف على بعض المحتوى في المستند المصدر (مثال |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String warningTypeName)](#fromName-java.lang.String) |  |
| [fromNames(Set warningTypeNames)](#fromNames-java.util.Set) |  |
| [getName(int warningType)](#getName-int) |  |
| [getNames(int warningType)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int warningType)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### DATA_LOSS {#DATA-LOSS}
```
public static int DATA_LOSS
```


فقدان بيانات عام، بدون رمز محدد.

### DATA_LOSS_CATEGORY {#DATA-LOSS-CATEGORY}
```
public static int DATA_LOSS_CATEGORY
```


قد يكون بعض النص/الحرف/الصورة أو بيانات أخرى مفقودة إما من شجرة المستند بعد التحميل، أو من المستند المُنشأ بعد الحفظ.

### FONT_EMBEDDING {#FONT-EMBEDDING}
```
public static int FONT_EMBEDDING
```


فقدان معلومات الخط المضمن أثناء حفظ المستند.

### FONT_SUBSTITUTION {#FONT-SUBSTITUTION}
```
public static int FONT_SUBSTITUTION
```


تم استبدال الخط.

### HINT {#HINT}
```
public static int HINT
```


ينصح بمشكلة محتملة أو يقترح تحسينًا.

### MAJOR_FORMATTING_LOSS {#MAJOR-FORMATTING-LOSS}
```
public static int MAJOR_FORMATTING_LOSS
```


فقدان تنسيق رئيسي عام، بدون رمز محدد.

### MAJOR_FORMATTING_LOSS_CATEGORY {#MAJOR-FORMATTING-LOSS-CATEGORY}
```
public static int MAJOR_FORMATTING_LOSS_CATEGORY
```


قد يبدو المستند الناتج أو موقع معين فيه مختلفًا بشكل كبير مقارنة بالمستند الأصلي.

### MINOR_FORMATTING_LOSS {#MINOR-FORMATTING-LOSS}
```
public static int MINOR_FORMATTING_LOSS
```


فقدان تنسيق فرعي عام، بدون رمز محدد.

### MINOR_FORMATTING_LOSS_CATEGORY {#MINOR-FORMATTING-LOSS-CATEGORY}
```
public static int MINOR_FORMATTING_LOSS_CATEGORY
```


قد يبدو المستند الناتج أو موقع معين فيه مختلفًا إلى حد ما مقارنة بالمستند الأصلي.

### UNEXPECTED_CONTENT {#UNEXPECTED-CONTENT}
```
public static int UNEXPECTED_CONTENT
```


محتوى غير متوقع عام، بدون رمز محدد.

### UNEXPECTED_CONTENT_CATEGORY {#UNEXPECTED-CONTENT-CATEGORY}
```
public static int UNEXPECTED_CONTENT_CATEGORY
```


لم يتم التعرف على بعض المحتوى في المستند المصدر (أي غير مدعوم)، قد يسبب ذلك مشاكل أو قد لا يسبب، وقد يؤدي إلى فقدان البيانات/التنسيق.

### length {#length}
```
public static int length
```


### fromName(String warningTypeName) {#fromName-java.lang.String}
```
public static int fromName(String warningTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| warningTypeName | java.lang.String |  |

**Returns:**
int
### fromNames(Set warningTypeNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set warningTypeNames)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| warningTypeNames | java.util.Set |  |

**Returns:**
int
### getName(int warningType) {#getName-int}
```
public static String getName(int warningType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| warningType | int |  |

**Returns:**
java.lang.String
### getNames(int warningType) {#getNames-int}
```
public static Set getNames(int warningType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| warningType | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int warningType) {#toString-int}
```
public static String toString(int warningType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| warningType | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
