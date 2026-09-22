---
title: "TextWrapping"
linktitle: "TextWrapping"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية التفاف النص حول الجدول في Java."
type: docs
weight: 679
url: /ar/java/com.aspose.words/textwrapping/
---

**Inheritance:**
java.lang.Object
```
public class TextWrapping
```

يحدد كيفية لف النص حول الجدول.

 **Examples:** 

يعرض كيفية العمل مع التفاف نص الجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 builder.getFont().setSize(16.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 // Set the "TextWrapping" property to "TextWrapping.Around" to get the table to wrap text around it,
 // and push it down into the paragraph below by setting the position.
 table.setTextWrapping(TextWrapping.AROUND);
 table.setAbsoluteHorizontalDistance(100.0);
 table.setAbsoluteVerticalDistance(20.0);

 doc.save(getArtifactsDir() + "Table.WrapText.docx");
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [AROUND](#AROUND) | يتم التفاف النص حول الجدول مشغولًا المساحة الجانبية المتاحة. |
| [DEFAULT](#DEFAULT) | القيمة الافتراضية. |
| [NONE](#NONE) | يتم عرض النص والجدول بترتيب ظهورهما في المستند. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String textWrappingName)](#fromName-java.lang.String) |  |
| [getName(int textWrapping)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textWrapping)](#toString-int) |  |
### AROUND {#AROUND}
```
public static int AROUND
```


يتم التفاف النص حول الجدول مشغولًا المساحة الجانبية المتاحة.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


القيمة الافتراضية.

### NONE {#NONE}
```
public static int NONE
```


يتم عرض النص والجدول بترتيب ظهورهما في المستند.

### length {#length}
```
public static int length
```


### fromName(String textWrappingName) {#fromName-java.lang.String}
```
public static int fromName(String textWrappingName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| textWrappingName | java.lang.String |  |

**Returns:**
int
### getName(int textWrapping) {#getName-int}
```
public static String getName(int textWrapping)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| textWrapping | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int textWrapping) {#toString-int}
```
public static String toString(int textWrapping)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| textWrapping | int |  |

**Returns:**
java.lang.String
