---
title: "TableStyleOptions"
linktitle: "TableStyleOptions"
second_title: "Aspose.Words Java için"
description: "Java'da bir tabloya tablo stilinin nasıl uygulandığını belirtir."
type: docs
weight: 661
url: /tr/java/com.aspose.words/tablestyleoptions/
---

**Inheritance:**
java.lang.Object
```
public class TableStyleOptions
```

Tablo stilinin bir tabloya nasıl uygulandığını belirtir.

 **Examples:** 

Bir stil uygularken yeni bir tablo nasıl oluşturulacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [COLUMN_BANDS](#COLUMN-BANDS) | Sütun bantlamalı koşullu biçimlendirmeyi uygula. |
| [DEFAULT](#DEFAULT) | Bu, Microsoft Word varsayılanlarıdır. |
| [DEFAULT_2003](#DEFAULT-2003) | Satır ve sütun bantlaması uygulanır. |
| [FIRST_COLUMN](#FIRST-COLUMN) | İlk sütun için koşullu biçimlendirme uygula. |
| [FIRST_ROW](#FIRST-ROW) | İlk satır için koşullu biçimlendirme uygula. |
| [LAST_COLUMN](#LAST-COLUMN) | Son sütun için koşullu biçimlendirme uygula. |
| [LAST_ROW](#LAST-ROW) | Son satır için koşullu biçimlendirme uygula. |
| [NONE](#NONE) | Tablo stili biçimlendirmesi uygulanmaz. |
| [ROW_BANDS](#ROW-BANDS) | Satır bantlamalı koşullu biçimlendirme uygula. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
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


Sütun bantlamalı koşullu biçimlendirmeyi uygula.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Bu, Microsoft Word varsayılanlarıdır.

### DEFAULT_2003 {#DEFAULT-2003}
```
public static int DEFAULT_2003
```


Satır ve sütun bantlaması uygulanır. Bu, DOC, WML ve RTF gibi eski formatlar için Microsoft Word varsayılanıdır.

### FIRST_COLUMN {#FIRST-COLUMN}
```
public static int FIRST_COLUMN
```


İlk sütun için koşullu biçimlendirme uygula.

### FIRST_ROW {#FIRST-ROW}
```
public static int FIRST_ROW
```


İlk satır için koşullu biçimlendirme uygula.

### LAST_COLUMN {#LAST-COLUMN}
```
public static int LAST_COLUMN
```


Son sütun için koşullu biçimlendirme uygula.

### LAST_ROW {#LAST-ROW}
```
public static int LAST_ROW
```


Son satır için koşullu biçimlendirme uygula.

### NONE {#NONE}
```
public static int NONE
```


Tablo stili biçimlendirmesi uygulanmaz.

### ROW_BANDS {#ROW-BANDS}
```
public static int ROW_BANDS
```


Satır bantlamalı koşullu biçimlendirme uygula.

### length {#length}
```
public static int length
```


### fromName(String tableStyleOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String tableStyleOptionsName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tableStyleOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set tableStyleOptionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set tableStyleOptionsNames)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tableStyleOptionsNames | java.util.Set |  |

**Returns:**
int
### getName(int tableStyleOptions) {#getName-int}
```
public static String getName(int tableStyleOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tableStyleOptions | int |  |

**Returns:**
java.lang.String
### getNames(int tableStyleOptions) {#getNames-int}
```
public static Set getNames(int tableStyleOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tableStyleOptions | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
