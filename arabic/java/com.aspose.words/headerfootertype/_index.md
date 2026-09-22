---
title: "HeaderFooterType"
linktitle: "HeaderFooterType"
second_title: "Aspose.Words لـ Java"
description: "يحدد نوع الرأس أو التذييل الموجود في ملف Word في Java."
type: docs
weight: 372
url: /ar/java/com.aspose.words/headerfootertype/
---

**Inheritance:**
java.lang.Object
```
public class HeaderFooterType
```

يحدد نوع الرأس أو التذييل الموجود في ملف Word. هذا رأس/تذييل لكل قسم. لا تقم بإعادة الترقيم لأن القيمة هي قيمة التعداد المستخدمة كمؤشر إلى plcfhdd.

 **Examples:** 

يوضح كيفية إنشاء رؤوس وتذييلات في المستند باستخدام DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [FOOTER_EVEN](#FOOTER-EVEN) | تذييل للصفحات ذات الأرقام الزوجية. |
| [FOOTER_FIRST](#FOOTER-FIRST) | تذييل للصفحة الأولى من القسم. |
| [FOOTER_PRIMARY](#FOOTER-PRIMARY) | التذييل الأساسي، يُستخدم أيضًا للصفحات ذات الأرقام الفردية. |
| [HEADER_EVEN](#HEADER-EVEN) | رأس للصفحات ذات الأرقام الزوجية. |
| [HEADER_FIRST](#HEADER-FIRST) | رأس للصفحة الأولى من القسم. |
| [HEADER_PRIMARY](#HEADER-PRIMARY) | الرأس الأساسي، يُستخدم أيضًا للصفحات ذات الأرقام الفردية. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String headerFooterTypeName)](#fromName-java.lang.String) |  |
| [getName(int headerFooterType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int headerFooterType)](#toString-int) |  |
### FOOTER_EVEN {#FOOTER-EVEN}
```
public static int FOOTER_EVEN
```


تذييل للصفحات ذات الأرقام الزوجية.

### FOOTER_FIRST {#FOOTER-FIRST}
```
public static int FOOTER_FIRST
```


تذييل للصفحة الأولى من القسم.

### FOOTER_PRIMARY {#FOOTER-PRIMARY}
```
public static int FOOTER_PRIMARY
```


التذييل الأساسي، يُستخدم أيضًا للصفحات ذات الأرقام الفردية.

### HEADER_EVEN {#HEADER-EVEN}
```
public static int HEADER_EVEN
```


رأس للصفحات ذات الأرقام الزوجية.

### HEADER_FIRST {#HEADER-FIRST}
```
public static int HEADER_FIRST
```


رأس للصفحة الأولى من القسم.

### HEADER_PRIMARY {#HEADER-PRIMARY}
```
public static int HEADER_PRIMARY
```


الرأس الأساسي، يُستخدم أيضًا للصفحات ذات الأرقام الفردية.

### length {#length}
```
public static int length
```


### fromName(String headerFooterTypeName) {#fromName-java.lang.String}
```
public static int fromName(String headerFooterTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| headerFooterTypeName | java.lang.String |  |

**Returns:**
int
### getName(int headerFooterType) {#getName-int}
```
public static String getName(int headerFooterType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| headerFooterType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int headerFooterType) {#toString-int}
```
public static String toString(int headerFooterType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| headerFooterType | int |  |

**Returns:**
java.lang.String
