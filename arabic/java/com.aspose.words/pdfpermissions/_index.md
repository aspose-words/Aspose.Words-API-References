---
title: "PdfPermissions"
linktitle: "PdfPermissions"
second_title: "Aspose.Words لـ Java"
description: "يحدد العمليات المسموح بها للمستخدم على مستند PDF مشفر في جافا."
type: docs
weight: 541
url: /ar/java/com.aspose.words/pdfpermissions/
---

**Inheritance:**
java.lang.Object
```
public class PdfPermissions
```

يحدد العمليات المسموح بها للمستخدم على مستند PDF مشفر.

 **Examples:** 

يوضح كيفية تعيين الصلاحيات على مستند PDF محفوظ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [ALLOW_ALL](#ALLOW-ALL) | يسمح بجميع العمليات على مستند PDF. |
| [CONTENT_COPY](#CONTENT-COPY) | نسخ أو استخراج النص والرسومات من المستند بعمليات أخرى غير تلك التي يتحكم فيها [CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions/\#CONTENT-COPY-FOR-ACCESSIBILITY). |
| [CONTENT_COPY_FOR_ACCESSIBILITY](#CONTENT-COPY-FOR-ACCESSIBILITY) | استخراج النص والرسومات (دعمًا لإمكانية الوصول للمستخدمين ذوي الإعاقة أو لأغراض أخرى). |
| [DISALLOW_ALL](#DISALLOW-ALL) | يمنع جميع العمليات على مستند PDF. |
| [DOCUMENT_ASSEMBLY](#DOCUMENT-ASSEMBLY) | تجميع المستند (إدراج أو تدوير أو حذف الصفحات وإنشاء عناصر مخطط المستند أو صور مصغرة)، حتى إذا كان [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) غير مفعّل. |
| [FILL_IN](#FILL-IN) | ملء حقول النماذج التفاعلية الموجودة (بما في ذلك حقول التوقيع)، حتى إذا كان [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) غير مفعّل. |
| [HIGH_RESOLUTION_PRINTING](#HIGH-RESOLUTION-PRINTING) | طباعة المستند إلى تمثيل يمكن من خلاله إنشاء نسخة رقمية دقيقة من محتوى PDF، استنادًا إلى خوارزمية تعتمد على التنفيذ. |
| [MODIFY_ANNOTATIONS](#MODIFY-ANNOTATIONS) | إضافة أو تعديل تعليقات النص، ملء حقول النماذج التفاعلية، وإذا كان [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) مفعّلاً أيضًا، إنشاء أو تعديل حقول النماذج التفاعلية (بما في ذلك حقول التوقيع). |
| [MODIFY_CONTENTS](#MODIFY-CONTENTS) | تعديل محتوى المستند بعمليات غير تلك التي يتحكم فيها [MODIFY\_ANNOTATIONS](../../com.aspose.words/pdfpermissions/\#MODIFY-ANNOTATIONS)، [FILL\_IN](../../com.aspose.words/pdfpermissions/\#FILL-IN)، و[DOCUMENT\_ASSEMBLY](../../com.aspose.words/pdfpermissions/\#DOCUMENT-ASSEMBLY). |
| [PRINTING](#PRINTING) | طباعة المستند (قد لا تكون بأعلى جودة، اعتمادًا على ما إذا كان [HIGH\_RESOLUTION\_PRINTING](../../com.aspose.words/pdfpermissions/\#HIGH-RESOLUTION-PRINTING) مفعّلاً أيضًا). |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String pdfPermissionsName)](#fromName-java.lang.String) |  |
| [fromNames(Set pdfPermissionsNames)](#fromNames-java.util.Set) |  |
| [getName(int pdfPermissions)](#getName-int) |  |
| [getNames(int pdfPermissions)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfPermissions)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### ALLOW_ALL {#ALLOW-ALL}
```
public static int ALLOW_ALL
```


يسمح بجميع العمليات على مستند PDF.

### CONTENT_COPY {#CONTENT-COPY}
```
public static int CONTENT_COPY
```


نسخ أو استخراج النص والرسومات من المستند بعمليات أخرى غير تلك التي يتحكم فيها [CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions/\#CONTENT-COPY-FOR-ACCESSIBILITY).

### CONTENT_COPY_FOR_ACCESSIBILITY {#CONTENT-COPY-FOR-ACCESSIBILITY}
```
public static int CONTENT_COPY_FOR_ACCESSIBILITY
```


استخراج النص والرسومات (دعمًا لإمكانية الوصول للمستخدمين ذوي الإعاقة أو لأغراض أخرى).

### DISALLOW_ALL {#DISALLOW-ALL}
```
public static int DISALLOW_ALL
```


يمنع جميع العمليات على مستند PDF. هذا هو القيمة الافتراضية.

### DOCUMENT_ASSEMBLY {#DOCUMENT-ASSEMBLY}
```
public static int DOCUMENT_ASSEMBLY
```


تجميع المستند (إدراج أو تدوير أو حذف الصفحات وإنشاء عناصر مخطط المستند أو صور مصغرة)، حتى إذا كان [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) غير مفعّل.

### FILL_IN {#FILL-IN}
```
public static int FILL_IN
```


ملء حقول النماذج التفاعلية الموجودة (بما في ذلك حقول التوقيع)، حتى إذا كان [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) غير مفعّل.

### HIGH_RESOLUTION_PRINTING {#HIGH-RESOLUTION-PRINTING}
```
public static int HIGH_RESOLUTION_PRINTING
```


طباعة المستند إلى تمثيل يمكن من خلاله إنشاء نسخة رقمية دقيقة من محتوى PDF، استنادًا إلى خوارزمية تعتمد على التنفيذ. عندما تكون هذه العلامة غير مفعّلة (و[PRINTING](../../com.aspose.words/pdfpermissions/\#PRINTING) مفعّلة)، يجب أن تقتصر الطباعة على تمثيل منخفض المستوى للمظهر، وربما بجودة منخفضة.

### MODIFY_ANNOTATIONS {#MODIFY-ANNOTATIONS}
```
public static int MODIFY_ANNOTATIONS
```


إضافة أو تعديل تعليقات النص، ملء حقول النماذج التفاعلية، وإذا كان [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) مفعّلاً أيضًا، إنشاء أو تعديل حقول النماذج التفاعلية (بما في ذلك حقول التوقيع).

### MODIFY_CONTENTS {#MODIFY-CONTENTS}
```
public static int MODIFY_CONTENTS
```


تعديل محتوى المستند بعمليات غير تلك التي يتحكم فيها [MODIFY\_ANNOTATIONS](../../com.aspose.words/pdfpermissions/\#MODIFY-ANNOTATIONS)، [FILL\_IN](../../com.aspose.words/pdfpermissions/\#FILL-IN)، و[DOCUMENT\_ASSEMBLY](../../com.aspose.words/pdfpermissions/\#DOCUMENT-ASSEMBLY).

### PRINTING {#PRINTING}
```
public static int PRINTING
```


طباعة المستند (قد لا تكون بأعلى جودة، اعتمادًا على ما إذا كان [HIGH\_RESOLUTION\_PRINTING](../../com.aspose.words/pdfpermissions/\#HIGH-RESOLUTION-PRINTING) مفعّلاً أيضًا).

### length {#length}
```
public static int length
```


### fromName(String pdfPermissionsName) {#fromName-java.lang.String}
```
public static int fromName(String pdfPermissionsName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfPermissionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set pdfPermissionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set pdfPermissionsNames)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfPermissionsNames | java.util.Set |  |

**Returns:**
int
### getName(int pdfPermissions) {#getName-int}
```
public static String getName(int pdfPermissions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfPermissions | int |  |

**Returns:**
java.lang.String
### getNames(int pdfPermissions) {#getNames-int}
```
public static Set getNames(int pdfPermissions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfPermissions | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfPermissions) {#toString-int}
```
public static String toString(int pdfPermissions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfPermissions | int |  |

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
