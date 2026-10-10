---
title: "TableStyleOptions"
linktitle: "TableStyleOptions"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية تطبيق نمط الجدول على جدول في Java."
type: docs
weight: 661
url: /ar/java/com.aspose.words/tablestyleoptions/
---

**Inheritance:**
java.lang.Object
```
public class TableStyleOptions
```

يحدد كيفية تطبيق نمط الجدول على جدول.

 **Examples:** 

يظهر كيفية إنشاء جدول جديد أثناء تطبيق نمط.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // We must insert at least one row before setting any table formatting.
 builder.insertCell();

 // Set the table style used based on the style identifier.
 // Note that not all table styles are available when saving to .doc format.
 table.setStyleIdentifier(StyleIdentifier.MEDIUM_SHADING_1_ACCENT_1);

 // Partially apply the style to features of the table based on predicates, then build the table.
 table.setStyleOptions(TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS | TableStyleOptions.FIRST_ROW);
 table.autoFit(AutoFitBehavior.AUTO_FIT_TO_CONTENTS);

 builder.writeln("Item");
 builder.getCellFormat().setRightPadding(40.0);
 builder.insertCell();
 builder.writeln("Quantity (kg)");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Apples");
 builder.insertCell();
 builder.writeln("20");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Bananas");
 builder.insertCell();
 builder.writeln("40");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Carrots");
 builder.insertCell();
 builder.writeln("50");
 builder.endRow();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTableWithStyle.docx");
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [COLUMN_BANDS](#COLUMN-BANDS) | تطبيق تنسيق الشرط لتظليل الأعمدة. |
| [DEFAULT](#DEFAULT) | هذه هي الإعدادات الافتراضية لـ Microsoft Word. |
| [DEFAULT_2003](#DEFAULT-2003) | تم تطبيق تظليل الصفوف والأعمدة. |
| [FIRST_COLUMN](#FIRST-COLUMN) | تطبيق تنسيق الشرط للعمود الأول. |
| [FIRST_ROW](#FIRST-ROW) | تطبيق تنسيق الشرط للصف الأول. |
| [LAST_COLUMN](#LAST-COLUMN) | تطبيق تنسيق الشرط للعمود الأخير. |
| [LAST_ROW](#LAST-ROW) | تطبيق تنسيق الشرط للصف الأخير. |
| [NONE](#NONE) | لم يتم تطبيق أي تنسيق لنمط الجدول. |
| [ROW_BANDS](#ROW-BANDS) | تطبيق تنسيق الشرط لتظليل الصفوف. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String tableStyleOptionsName)](#fromName-java.lang.String) |  |
| [fromNames(Set tableStyleOptionsNames)](#fromNames-java.util.Set) |  |
| [getName(int tableStyleOptions)](#getName-int) |  |
| [getNames(int tableStyleOptions)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tableStyleOptions)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### COLUMN_BANDS {#COLUMN-BANDS}
```
public static int COLUMN_BANDS
```


تطبيق تنسيق الشرط لتظليل الأعمدة.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


هذه هي الإعدادات الافتراضية لـ Microsoft Word.

### DEFAULT_2003 {#DEFAULT-2003}
```
public static int DEFAULT_2003
```


تم تطبيق تظليل الصفوف والأعمدة. هذا هو الإعداد الافتراضي لـ Microsoft Word للأنساق القديمة مثل DOC وWML وRTF.

### FIRST_COLUMN {#FIRST-COLUMN}
```
public static int FIRST_COLUMN
```


تطبيق تنسيق الشرط للعمود الأول.

### FIRST_ROW {#FIRST-ROW}
```
public static int FIRST_ROW
```


تطبيق تنسيق الشرط للصف الأول.

### LAST_COLUMN {#LAST-COLUMN}
```
public static int LAST_COLUMN
```


تطبيق تنسيق الشرط للعمود الأخير.

### LAST_ROW {#LAST-ROW}
```
public static int LAST_ROW
```


تطبيق تنسيق الشرط للصف الأخير.

### NONE {#NONE}
```
public static int NONE
```


لم يتم تطبيق أي تنسيق لنمط الجدول.

### ROW_BANDS {#ROW-BANDS}
```
public static int ROW_BANDS
```


تطبيق تنسيق الشرط لتظليل الصفوف.

### length {#length}
```
public static int length
```


### fromName(String tableStyleOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String tableStyleOptionsName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| tableStyleOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set tableStyleOptionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set tableStyleOptionsNames)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| tableStyleOptionsNames | java.util.Set |  |

**Returns:**
int
### getName(int tableStyleOptions) {#getName-int}
```
public static String getName(int tableStyleOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| tableStyleOptions | int |  |

**Returns:**
java.lang.String
### getNames(int tableStyleOptions) {#getNames-int}
```
public static Set getNames(int tableStyleOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| tableStyleOptions | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int tableStyleOptions) {#toString-int}
```
public static String toString(int tableStyleOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| tableStyleOptions | int |  |

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
