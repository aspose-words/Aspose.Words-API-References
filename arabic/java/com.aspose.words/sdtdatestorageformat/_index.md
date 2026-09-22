---
title: "SdtDateStorageFormat"
linktitle: "SdtDateStorageFormat"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية تخزين/استرجاع التاريخ لعنصر SDT من نوع تاريخ عندما يكون الـ SDT مرتبطًا بعقدة XML في مخزن بيانات المستندات في Java."
type: docs
weight: 601
url: /ar/java/com.aspose.words/sdtdatestorageformat/
---

**Inheritance:**
java.lang.Object
```
public class SdtDateStorageFormat
```

يحدد كيفية تخزين/استرجاع التاريخ لعنصر SDT التاريخي عندما يكون الـ SDT مرتبطًا بعقدة XML في مخزن بيانات المستند.

 **Examples:** 

يعرض كيفية مطالبة المستخدم بإدخال تاريخ باستخدام علامة مستند منسقة.

```

 Document doc = new Document();

 // Insert a structured document tag that prompts the user to enter a date.
 // In Microsoft Word, this element is known as a "Date picker content control".
 // When we click on the arrow on the right end of this tag in Microsoft Word,
 // we will see a pop up in the form of a clickable calendar.
 // We can use that popup to select a date that the tag will display.
 StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.DATE, MarkupLevel.INLINE);

 // Display the date, according to the Saudi Arabian Arabic locale.
 sdtDate.setDateDisplayLocale(1025);

 // Set the format with which to display the date.
 sdtDate.setDateDisplayFormat("dd MMMM, yyyy");
 sdtDate.setDateStorageFormat(SdtDateStorageFormat.DATE_TIME);

 // Display the date according to the Hijri calendar.
 sdtDate.setCalendarType(SdtCalendarType.HIJRI);

 // Before the user chooses a date in Microsoft Word, the tag will display the text "Click here to enter a date.".
 // According to the tag's calendar, set the "FullDate" property to get the tag to display a default date.
 Calendar cal = Calendar.getInstance();
 cal.set(1440, 10, 20);
 sdtDate.setFullDate(cal.getTime());

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(sdtDate);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.Date.docx");
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [DATE](#DATE) | يتم تخزين قيمة التاريخ لعنصر SDT من نوع تاريخ كقيمة تاريخ بصيغة تاريخ XML Schema القياسية. |
| [DATE_TIME](#DATE-TIME) | يتم تخزين قيمة التاريخ لعنصر SDT من نوع تاريخ كقيمة تاريخ بصيغة DateTime في XML Schema القياسية. |
| [DEFAULT](#DEFAULT) | الافتراضي هو [DATE\_TIME](../../com.aspose.words/sdtdatestorageformat/\#DATE-TIME) |
| [TEXT](#TEXT) | يتم تخزين قيمة التاريخ لعنصر SDT من نوع تاريخ كنص. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String sdtDateStorageFormatName)](#fromName-java.lang.String) |  |
| [getName(int sdtDateStorageFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtDateStorageFormat)](#toString-int) |  |
### DATE {#DATE}
```
public static int DATE
```


يتم تخزين قيمة التاريخ لعنصر SDT من نوع تاريخ كقيمة تاريخ بصيغة تاريخ XML Schema القياسية.

### DATE_TIME {#DATE-TIME}
```
public static int DATE_TIME
```


يتم تخزين قيمة التاريخ لعنصر SDT من نوع تاريخ كقيمة تاريخ بصيغة DateTime في XML Schema القياسية.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


الافتراضي هو [DATE\_TIME](../../com.aspose.words/sdtdatestorageformat/\#DATE-TIME)

### TEXT {#TEXT}
```
public static int TEXT
```


يتم تخزين قيمة التاريخ لعنصر SDT من نوع تاريخ كنص.

### length {#length}
```
public static int length
```


### fromName(String sdtDateStorageFormatName) {#fromName-java.lang.String}
```
public static int fromName(String sdtDateStorageFormatName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| sdtDateStorageFormatName | java.lang.String |  |

**Returns:**
int
### getName(int sdtDateStorageFormat) {#getName-int}
```
public static String getName(int sdtDateStorageFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| sdtDateStorageFormat | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int sdtDateStorageFormat) {#toString-int}
```
public static String toString(int sdtDateStorageFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| sdtDateStorageFormat | int |  |

**Returns:**
java.lang.String
