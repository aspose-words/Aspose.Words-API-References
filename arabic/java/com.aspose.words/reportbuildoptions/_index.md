---
title: "ReportBuildOptions"
linktitle: "ReportBuildOptions"
second_title: "Aspose.Words لـ Java"
description: "يحدد الخيارات التي تتحكم في سلوك ReportingEngine أثناء إنشاء تقرير في جافا."
type: docs
weight: 570
url: /ar/java/com.aspose.words/reportbuildoptions/
---

**Inheritance:**
java.lang.Object
```
public class ReportBuildOptions
```

يحدد الخيارات التي تتحكم في سلوك [ReportingEngine](../../com.aspose.words/reportingengine/) أثناء إنشاء تقرير.
## الحقول

| حقل | الوصف |
| --- | --- |
| [ALLOW_MISSING_MEMBERS](#ALLOW-MISSING-MEMBERS) | يحدد أن الأعضاء المفقودة في الكائن يجب أن تُعامل كقواعد null بواسطة المحرك. |
| [INLINE_ERROR_MESSAGES](#INLINE-ERROR-MESSAGES) | يحدد أن المحرك يجب أن يدمج رسائل أخطاء صياغة القالب داخل مستندات الإخراج. |
| [NONE](#NONE) | يحدد الخيارات الافتراضية. |
| [REMOVE_EMPTY_PARAGRAPHS](#REMOVE-EMPTY-PARAGRAPHS) | يحدد أن المحرك يجب أن يزيل الفقرات التي تصبح فارغة بعد إزالة علامات صياغة القالب أو استبدالها بقيم فارغة. |
| [RESPECT_JPEG_EXIF_ORIENTATION](#RESPECT-JPEG-EXIF-ORIENTATION) | يحدد أن المحرك يجب أن يستخدم قيم توجيه الصورة EXIF \\u200b\\u200bimage لتدوير الصور JPEG المدخلة بشكل مناسب. |
| [UPDATE_FIELDS_SYNTAX_AWARE](#UPDATE-FIELDS-SYNTAX-AWARE) | يحدد أن المحرك يجب أن يتجاهل صياغة القالب في نتائج الحقول ويحدّث الحقول بعد بناء التقرير. |
| [USE_LEGACY_HEADER_FOOTER_VISITING](#USE-LEGACY-HEADER-FOOTER-VISITING) | يحدد أن المحرك يجب أن يزور عقد الأطفال للقسم (الرؤوس، التذييلات، الأجسام) بترتيب متوافق مع إصدارات Aspose.Words السابقة للنسخة 21.9. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String reportBuildOptionsName)](#fromName-java.lang.String) |  |
| [fromNames(Set reportBuildOptionsNames)](#fromNames-java.util.Set) |  |
| [getName(int reportBuildOptions)](#getName-int) |  |
| [getNames(int reportBuildOptions)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int reportBuildOptions)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### ALLOW_MISSING_MEMBERS {#ALLOW-MISSING-MEMBERS}
```
public static int ALLOW_MISSING_MEMBERS
```


يحدد أن أعضاء الكائن المفقودة يجب أن تُعامل كقيمة null من قبل المحرك. يؤثر هذا الخيار فقط على الوصول إلى أعضاء الكائن المثيل (أي غير ثابت) وطرق الامتداد. إذا لم يتم تعيين هذا الخيار، يرمي المحرك استثناءً عند مواجهة عضو كائن مفقود.

### INLINE_ERROR_MESSAGES {#INLINE-ERROR-MESSAGES}
```
public static int INLINE_ERROR_MESSAGES
```


يحدد أن المحرك يجب أن يدمج رسائل أخطاء بناء القالب في مستندات الإخراج. إذا لم يتم تعيين هذا الخيار، يرمي المحرك استثناءً عند مواجهة خطأ بناء.

### NONE {#NONE}
```
public static int NONE
```


يحدد الخيارات الافتراضية.

### REMOVE_EMPTY_PARAGRAPHS {#REMOVE-EMPTY-PARAGRAPHS}
```
public static int REMOVE_EMPTY_PARAGRAPHS
```


يحدد أن المحرك يجب أن يزيل الفقرات التي تصبح فارغة بعد إزالة علامات صياغة القالب أو استبدالها بقيم فارغة.

### RESPECT_JPEG_EXIF_ORIENTATION {#RESPECT-JPEG-EXIF-ORIENTATION}
```
public static int RESPECT_JPEG_EXIF_ORIENTATION
```


يحدد أن المحرك يجب أن يستخدم قيم توجيه الصورة EXIF \\u200b\\u200bimage لتدوير الصور JPEG المدخلة بشكل مناسب.

### UPDATE_FIELDS_SYNTAX_AWARE {#UPDATE-FIELDS-SYNTAX-AWARE}
```
public static int UPDATE_FIELDS_SYNTAX_AWARE
```


يحدد أن المحرك يجب أن يتجاهل صياغة القالب في نتائج الحقول ويحدّث الحقول بعد بناء التقرير.

### USE_LEGACY_HEADER_FOOTER_VISITING {#USE-LEGACY-HEADER-FOOTER-VISITING}
```
public static int USE_LEGACY_HEADER_FOOTER_VISITING
```


يحدد أن المحرك يجب أن يزور عقد الأطفال للقسم (الرؤوس، التذييلات، الأجسام) بترتيب متوافق مع إصدارات Aspose.Words السابقة للنسخة 21.9.

 **Remarks:** 

بشكل افتراضي، يعامل المحرك الرؤوس والتذييلات كما لو كانت مرتبطة بفواصل الأقسام. أي، عند زيارة عقد الأطفال للقسم، يتم زيارة الجسم أولاً ثم تُزار الرؤوس والتذييلات. يتوافق هذا مع سلوك Microsoft Word عند النسخ واللصق أو إزالة محتويات متعددة الأقسام ويُنتج نتائج أكثر صحة في معظم السيناريوهات.

قبل Aspose.Words 21.9، كان المحرك يستخدم ترتيب زيارة آخر: كانت تُزار عقد الأطفال للقسم بالترتيب الذي تظهر به في المستند. طبّق هذه القيمة على [ReportingEngine.getOptions()](../../com.aspose.words/reportingengine/\#getOptions) / [ReportingEngine.setOptions(int)](../../com.aspose.words/reportingengine/\#setOptions-int) إذا كان التوافق مع الإصدارات القديمة من Aspose.Words مطلوبًا.

### length {#length}
```
public static int length
```


### fromName(String reportBuildOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String reportBuildOptionsName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| reportBuildOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set reportBuildOptionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set reportBuildOptionsNames)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| reportBuildOptionsNames | java.util.Set |  |

**Returns:**
int
### getName(int reportBuildOptions) {#getName-int}
```
public static String getName(int reportBuildOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| reportBuildOptions | int |  |

**Returns:**
java.lang.String
### getNames(int reportBuildOptions) {#getNames-int}
```
public static Set getNames(int reportBuildOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| reportBuildOptions | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int reportBuildOptions) {#toString-int}
```
public static String toString(int reportBuildOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| reportBuildOptions | int |  |

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
