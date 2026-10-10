---
title: "HtmlElementSizeOutputMode"
linktitle: "HtmlElementSizeOutputMode"
second_title: "Aspose.Words Java için"
description: "Aspose.Words'in Java'da öğe genişliklerini ve yüksekliklerini HTML, MHTML ve EPUB formatına nasıl dışa aktardığını belirtir."
type: docs
weight: 378
url: /tr/java/com.aspose.words/htmlelementsizeoutputmode/
---

**Inheritance:**
java.lang.Object
```
public class HtmlElementSizeOutputMode
```

Aspose.Words'ün öğe genişliklerini ve yüksekliklerini HTML, MHTML ve EPUB'a nasıl dışa aktardığını belirtir.

 **Examples:** 

Çıktı .html dosyasında negatif girintileri nasıl koruyacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a table with a negative indent, which will push it to the left past the left page boundary.
 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, Cell 1");
 builder.insertCell();
 builder.write("Row 1, Cell 2");
 builder.endTable();
 table.setLeftIndent(-36);
 table.setPreferredWidth(PreferredWidth.fromPoints(144.0));

 builder.insertBreak(BreakType.PARAGRAPH_BREAK);

 // Insert a table with a positive indent, which will push the table to the right.
 table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, Cell 1");
 builder.insertCell();
 builder.write("Row 1, Cell 2");
 builder.endTable();
 table.setLeftIndent(36.0);
 table.setPreferredWidth(PreferredWidth.fromPoints(144.0));

 // When we save a document to HTML, Aspose.Words will only preserve negative indents
 // such as the one we have applied to the first table if we set the "AllowNegativeIndent" flag
 // in a SaveOptions object that we will pass to "true".
 HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.HTML);
 {
     options.setAllowNegativeIndent(allowNegativeIndent);
     options.setTableWidthOutputMode(HtmlElementSizeOutputMode.RELATIVE_ONLY);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.NegativeIndent.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.NegativeIndent.html"), StandardCharsets.UTF_8);

 if (allowNegativeIndent) {
     Assert.assertTrue(outDocContents.contains(
             " "));
     Assert.assertTrue(outDocContents.contains(
             " "));
 }
 else
 {
     Assert.assertTrue(outDocContents.contains(
             " "));
     Assert.assertTrue(outDocContents.contains(
             " "));
 }
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [ALL](#ALL) | Belgede belirtilen, mutlak ve göreceli birimlerdeki tüm öğe boyutları dışa aktarılır. |
| [NONE](#NONE) | Öğe boyutları dışa aktarılmaz. |
| [RELATIVE_ONLY](#RELATIVE-ONLY) | Öğe boyutları yalnızca belgede göreceli birimlerde belirtilmişse dışa aktarılır. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String htmlElementSizeOutputModeName)](#fromName-java.lang.String) |  |
| [getName(int htmlElementSizeOutputMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int htmlElementSizeOutputMode)](#toString-int) |  |
### ALL {#ALL}
```
public static int ALL
```


Belgede belirtilen, mutlak ve göreceli birimlerdeki tüm öğe boyutları dışa aktarılır.

### NONE {#NONE}
```
public static int NONE
```


Eleman boyutları dışa aktarılmaz. Görsel ajanlar, elemanlar arasındaki ilişkiye göre düzeni otomatik olarak oluşturur.

### RELATIVE_ONLY {#RELATIVE-ONLY}
```
public static int RELATIVE_ONLY
```


Eleman boyutları yalnızca belgede göreceli birimlerle belirtilmişse dışa aktarılır. Sabit boyutlar bu modda dışa aktarılmaz. Görsel ajanlar, belge düzenini daha doğal hâle getirmek için eksik boyutları hesaplayacaktır.

### length {#length}
```
public static int length
```


### fromName(String htmlElementSizeOutputModeName) {#fromName-java.lang.String}
```
public static int fromName(String htmlElementSizeOutputModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| htmlElementSizeOutputModeName | java.lang.String |  |

**Returns:**
int
### getName(int htmlElementSizeOutputMode) {#getName-int}
```
public static String getName(int htmlElementSizeOutputMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| htmlElementSizeOutputMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int htmlElementSizeOutputMode) {#toString-int}
```
public static String toString(int htmlElementSizeOutputMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| htmlElementSizeOutputMode | int |  |

**Returns:**
java.lang.String
