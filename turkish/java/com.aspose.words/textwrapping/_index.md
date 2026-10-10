---
title: "TextWrapping"
linktitle: "TextWrapping"
second_title: "Aspose.Words Java için"
description: "Metnin Java'da tablo etrafında nasıl kaydırıldığını belirtir."
type: docs
weight: 679
url: /tr/java/com.aspose.words/textwrapping/
---

**Inheritance:**
java.lang.Object
```
public class TextWrapping
```

Metnin tablo etrafında nasıl sarıldığını belirtir.

 **Examples:** 

Tablo metin kaydırmasıyla nasıl çalışılacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [AROUND](#AROUND) | Metin, mevcut yan boşluğu kaplayarak tablo etrafında kaydırılır. |
| [DEFAULT](#DEFAULT) | Varsayılan değer. |
| [NONE](#NONE) | Metin ve tablo, belgede göründükleri sırayla görüntülenir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String textWrappingName)](#fromName-java.lang.String) |  |
| [getName(int textWrapping)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textWrapping)](#toString-int) |  |
### AROUND {#AROUND}
```
public static int AROUND
```


Metin, mevcut yan boşluğu kaplayarak tablo etrafında kaydırılır.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Varsayılan değer.

### NONE {#NONE}
```
public static int NONE
```


Metin ve tablo, belgede göründükleri sırayla görüntülenir.

### length {#length}
```
public static int length
```


### fromName(String textWrappingName) {#fromName-java.lang.String}
```
public static int fromName(String textWrappingName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| textWrappingName | java.lang.String |  |

**Returns:**
int
### getName(int textWrapping) {#getName-int}
```
public static String getName(int textWrapping)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| textWrapping | int |  |

**Returns:**
java.lang.String
