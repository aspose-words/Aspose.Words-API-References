---
title: "PdfCompliance"
linktitle: "PdfCompliance"
second_title: "Aspose.Words لـ Java"
description: "يحدد مستوى الامتثال لمعايير PDF في Java."
type: docs
weight: 529
url: /ar/java/com.aspose.words/pdfcompliance/
---

**Inheritance:**
java.lang.Object
```
public class PdfCompliance
```

يحدد مستوى الامتثال لمعايير PDF.

 **Examples:** 

يوضح كيفية ضبط مستوى الامتثال لمعايير PDF للمستندات PDF المحفوظة.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 // Note that some PdfSaveOptions are prohibited when saving to one of the standards and automatically fixed.
 // Use IWarningCallback to know which options are automatically fixed.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Set the "Compliance" property to "PdfCompliance.PdfA1b" to comply with the "PDF/A-1b" standard,
 // which aims to preserve the visual appearance of the document as Aspose.Words convert it to PDF.
 // Set the "Compliance" property to "PdfCompliance.Pdf17" to comply with the "1.7" standard.
 // Set the "Compliance" property to "PdfCompliance.PdfA1a" to comply with the "PDF/A-1a" standard,
 // which complies with "PDF/A-1b" as well as preserving the document structure of the original document.
 // Set the "Compliance" property to "PdfCompliance.PdfUa1" to comply with the "PDF/UA-1" (ISO 14289-1) standard,
 // which aims to define represent electronic documents in PDF that allow the file to be accessible.
 // Set the "Compliance" property to "PdfCompliance.Pdf20" to comply with the "PDF 2.0" (ISO 32000-2) standard.
 // Set the "Compliance" property to "PdfCompliance.PdfA4" to comply with the "PDF/A-4" (ISO 19004:2020) standard,
 // which preserving document static visual appearance over time.
 // Set the "Compliance" property to "PdfCompliance.PdfA4Ua2" to comply with both PDF/A-4 (ISO 19005-4:2020)
 // and PDF/UA-2 (ISO 14289-2:2024) standards.
 // Set the "Compliance" property to "PdfCompliance.PdfUa2" to comply with the PDF/UA-2 (ISO 14289-2:2024) standard.
 // This helps with making documents searchable but may significantly increase the size of already large documents.
 saveOptions.setCompliance(pdfCompliance);

 doc.save(getArtifactsDir() + "PdfSaveOptions.Compliance.pdf", saveOptions);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [PDF_17](#PDF-17) | سيطابق ملف الإخراج معيار PDF 1.7 (ISO 32000-1). |
| [PDF_20](#PDF-20) | سيطابق ملف الإخراج معيار PDF 2.0 (ISO 32000-2). |
| [PDF_A_1_A](#PDF-A-1-A) | ملف الإخراج سيتوافق مع معيار PDF/A-1a (ISO 19005-1). |
| [PDF_A_1_B](#PDF-A-1-B) | ملف الإخراج سيتوافق مع معيار PDF/A-1b (ISO 19005-1). |
| [PDF_A_2_A](#PDF-A-2-A) | ملف الإخراج سيتوافق مع معيار PDF/A-2a (ISO 19005-2). |
| [PDF_A_2_U](#PDF-A-2-U) | ملف الإخراج سيتوافق مع معيار PDF/A-2u (ISO 19005-2). |
| [PDF_A_3_A](#PDF-A-3-A) | ملف الإخراج سيتوافق مع معيار PDF/A-3a (ISO 19005-3). |
| [PDF_A_3_U](#PDF-A-3-U) | ملف الإخراج سيتوافق مع معيار PDF/A-3u (ISO 19005-3). |
| [PDF_A_4](#PDF-A-4) | ملف الإخراج سيتوافق مع معيار PDF/A-4 (ISO 19005-4:2020). |
| [PDF_A_4_F](#PDF-A-4-F) | ملف الإخراج سيتوافق مع معيار PDF/A-4f (ISO 19005-4:2020). |
| [PDF_A_4_UA_2](#PDF-A-4-UA-2) | ملف الإخراج سيتوافق مع كل من معيار PDF/A-4 (ISO 19005-4:2020) ومعيار PDF/UA-2 (ISO 14289-2:2024). |
| [PDF_UA_1](#PDF-UA-1) | ملف الإخراج سيتوافق مع معيار PDF/UA-1 (ISO 14289-1). |
| [PDF_UA_2](#PDF-UA-2) | ملف الإخراج سيتوافق مع معيار PDF/UA-2 (ISO 14289-2:2024). |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String pdfComplianceName)](#fromName-java.lang.String) |  |
| [getName(int pdfCompliance)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfCompliance)](#toString-int) |  |
### PDF_17 {#PDF-17}
```
public static int PDF_17
```


سيطابق ملف الإخراج معيار PDF 1.7 (ISO 32000-1).

### PDF_20 {#PDF-20}
```
public static int PDF_20
```


سيطابق ملف الإخراج معيار PDF 2.0 (ISO 32000-2).

### PDF_A_1_A {#PDF-A-1-A}
```
public static int PDF_A_1_A
```


ملف الإخراج سيتوافق مع معيار PDF/A-1a (ISO 19005-1). يتضمن هذا المستوى جميع متطلبات PDF/A-1b ويتطلب إضافيًا تضمين بنية المستند (المعروفة أيضًا باسم \"الموسومة\"), بهدف ضمان إمكانية البحث في محتوى المستند وإعادة استخدامه.

 **Remarks:** 

لاحظ أن تصدير بنية المستند يزيد بشكل كبير من استهلاك الذاكرة، خاصةً للوثائق الكبيرة.

### PDF_A_1_B {#PDF-A-1-B}
```
public static int PDF_A_1_B
```


ملف الإخراج سيتوافق مع معيار PDF/A-1b (ISO 19005-1). هدف PDF/A-1b هو ضمان إعادة إنتاج موثوقة للمظهر البصري للمستند.

### PDF_A_2_A {#PDF-A-2-A}
```
public static int PDF_A_2_A
```


ملف الإخراج سيتوافق مع معيار PDF/A-2a (ISO 19005-2). يتضمن هذا المستوى جميع متطلبات PDF/A-2u ويتطلب إضافيًا تضمين بنية المستند (المعروفة أيضًا باسم \"الموسومة\"), بهدف ضمان إمكانية البحث في محتوى المستند وإعادة استخدامه.

 **Remarks:** 

لاحظ أن تصدير بنية المستند يزيد بشكل كبير من استهلاك الذاكرة، خاصةً للوثائق الكبيرة.

### PDF_A_2_U {#PDF-A-2-U}
```
public static int PDF_A_2_U
```


ملف الإخراج سيتوافق مع معيار PDF/A-2u (ISO 19005-2). هدف PDF/A-2u هو الحفاظ على المظهر البصري الثابت للمستند بمرور الوقت، بغض النظر عن الأدوات والأنظمة المستخدمة لإنشاء الملفات أو تخزينها أو عرضها. بالإضافة إلى ذلك، يمكن استخراج أي نص موجود في المستند بشكل موثوق كسلسلة من نقاط كود Unicode.

### PDF_A_3_A {#PDF-A-3-A}
```
public static int PDF_A_3_A
```


ملف الإخراج سيتوافق مع معيار PDF/A-3a (ISO 19005-3). يتضمن هذا المستوى جميع متطلبات PDF/A-3u ويتطلب إضافيًا تضمين بنية المستند (المعروفة أيضًا باسم \"الموسومة\"), بهدف ضمان إمكانية البحث في محتوى المستند وإعادة استخدامه.

 **Remarks:** 

لاحظ أن تصدير بنية المستند يزيد بشكل كبير من استهلاك الذاكرة، خاصةً للوثائق الكبيرة.

### PDF_A_3_U {#PDF-A-3-U}
```
public static int PDF_A_3_U
```


ملف الإخراج سيتوافق مع معيار PDF/A-3u (ISO 19005-3). هدف PDF/A-3u (كما هو الحال مع PDF/A-2u) هو الحفاظ على المظهر البصري الثابت للمستند بمرور الوقت، بغض النظر عن الأدوات والأنظمة المستخدمة لإنشاء الملفات أو تخزينها أو عرضها. بالإضافة إلى ذلك، يمكن استخراج أي نص موجود في المستند بشكل موثوق كسلسلة من نقاط كود Unicode. بالإضافة إلى PDF/A-2u، يسمح PDF/A-3u بضم مرفقات إلى مستند PDF.

### PDF_A_4 {#PDF-A-4}
```
public static int PDF_A_4
```


ملف الإخراج سيتوافق مع معيار PDF/A-4 (ISO 19005-4:2020). هدف PDF/A-4 هو الحفاظ على المظهر البصري الثابت للمستند بمرور الوقت، بغض النظر عن الأدوات والأنظمة المستخدمة لإنشاء الملفات أو تخزينها أو عرضها. بالإضافة إلى ذلك، يمكن استخراج أي نص موجود في المستند بشكل موثوق كسلسلة من نقاط كود Unicode.

### PDF_A_4_F {#PDF-A-4-F}
```
public static int PDF_A_4_F
```


ملف الإخراج سيتوافق مع معيار PDF/A-4f (ISO 19005-4:2020). يتضمن هذا المستوى جميع متطلبات PDF/A-4 ويتطلب إضافيًا السماح بضم مرفقات إلى مستند PDF.

### PDF_A_4_UA_2 {#PDF-A-4-UA-2}
```
public static int PDF_A_4_UA_2
```


ملف الإخراج سيتوافق مع كل من معيار PDF/A-4 (ISO 19005-4:2020) ومعيار PDF/UA-2 (ISO 14289-2:2024). هدف PDF/A-4 هو الحفاظ على المظهر البصري الثابت للمستند بمرور الوقت، بغض النظر عن الأدوات والأنظمة المستخدمة لإنشاء الملفات أو تخزينها أو عرضها. الغرض الأساسي من PDF/UA هو تعريف كيفية تمثيل المستندات الإلكترونية بتنسيق PDF بطريقة تجعل الملف قابلاً للوصول.

 **Remarks:** 

لاحظ أن تصدير بنية المستند يزيد بشكل كبير من استهلاك الذاكرة، خاصةً للوثائق الكبيرة.

### PDF_UA_1 {#PDF-UA-1}
```
public static int PDF_UA_1
```


سيتم الامتثال لملف الإخراج لمعيار PDF/UA-1 (ISO 14289-1). الغرض الأساسي من PDF/UA هو تعريف كيفية تمثيل المستندات الإلكترونية بتنسيق PDF بطريقة تسمح بأن يكون الملف قابلاً للوصول.

 **Remarks:** 

لاحظ أن تصدير بنية المستند يزيد بشكل كبير من استهلاك الذاكرة، خاصةً للوثائق الكبيرة.

### PDF_UA_2 {#PDF-UA-2}
```
public static int PDF_UA_2
```


سيتم الامتثال لملف الإخراج لمعيار PDF/UA-2 (ISO 14289-2:2024). الغرض الأساسي من PDF/UA هو تعريف كيفية تمثيل المستندات الإلكترونية بتنسيق PDF بطريقة تسمح بأن يكون الملف قابلاً للوصول.

 **Remarks:** 

لاحظ أن تصدير بنية المستند يزيد بشكل كبير من استهلاك الذاكرة، خاصةً للوثائق الكبيرة.

### length {#length}
```
public static int length
```


### fromName(String pdfComplianceName) {#fromName-java.lang.String}
```
public static int fromName(String pdfComplianceName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfComplianceName | java.lang.String |  |

**Returns:**
int
### getName(int pdfCompliance) {#getName-int}
```
public static String getName(int pdfCompliance)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfCompliance | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfCompliance) {#toString-int}
```
public static String toString(int pdfCompliance)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfCompliance | int |  |

**Returns:**
java.lang.String
