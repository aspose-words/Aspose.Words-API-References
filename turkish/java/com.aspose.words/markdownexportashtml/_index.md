---
title: "MarkdownExportAsHtml"
linktitle: "MarkdownExportAsHtml"
second_title: "Aspose.Words Java için"
description: "Java'da Markdown'a ham HTML olarak dışa aktarılacak öğeleri belirtmeye izin verir."
type: docs
weight: 451
url: /tr/java/com.aspose.words/markdownexportashtml/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownExportAsHtml
```

Öğelerin Markdown'a ham HTML olarak dışa aktarılmasını belirtmeye izin verir.

 **Examples:** 

Bir tabloyu Markdown'a ham HTML olarak nasıl dışa aktaracağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Sample table:");

 // Create table.
 builder.insertCell();
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.RIGHT);
 builder.write("Cell1");
 builder.insertCell();
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write("Cell2");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setExportAsHtml(MarkdownExportAsHtml.TABLES);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ExportTableAsHtml.md", saveOptions);
 
```

Saf Markdown'ta doğru şekilde temsil edilemeyen tabloları ham HTML olarak nasıl dışa aktaracağınızı gösterir.

```

 String outputPath = getArtifactsDir() + "MarkdownSaveOptions.NonCompatibleTables.md";

 Document doc = new Document(getMyDir() + "Non compatible table.docx");

 // With the "NonCompatibleTables" option, you can export tables that have a complex structure with merged cells
 // or nested tables to raw HTML and leave simple tables in Markdown format.
 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setExportAsHtml(MarkdownExportAsHtml.NON_COMPATIBLE_TABLES);

 doc.save(outputPath, saveOptions);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [NONE](#NONE) | Tüm öğeleri ham HTML olmadan Markdown sözdizimi kullanarak dışa aktar. |
| [NON_COMPATIBLE_TABLES](#NON-COMPATIBLE-TABLES) | Saf Markdown'ta doğru şekilde temsil edilemeyen tabloları ham HTML olarak dışa aktar. |
| [TABLES](#TABLES) | Tabloları ham HTML olarak dışa aktar. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String markdownExportAsHtmlName)](#fromName-java.lang.String) |  |
| [fromNames(Set markdownExportAsHtmlNames)](#fromNames-java.util.Set) |  |
| [getName(int markdownExportAsHtml)](#getName-int) |  |
| [getNames(int markdownExportAsHtml)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownExportAsHtml)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Tüm öğeleri ham HTML olmadan Markdown sözdizimi kullanarak dışa aktar.

### NON_COMPATIBLE_TABLES {#NON-COMPATIBLE-TABLES}
```
public static int NON_COMPATIBLE_TABLES
```


Saf Markdown'ta doğru şekilde temsil edilemeyen tabloları ham HTML olarak dışa aktar.

 **Remarks:** 

Bu seçenek etkinleştirildiğinde, Aspose.Words yalnızca birleştirilmiş hücreleri veya iç içe tabloları olan tabloları ham HTML olarak dışa aktarır. Diğer tüm tablolar Markdown formatında dışa aktarılır. Ayrıca, bu seçeneğin tablonun tüm biçimlendirmesini korumadığını, yalnızca hücrelerin ilgili aralıklarını koruduğunu unutmayın.

İlgili [TABLES](../../com.aspose.words/markdownexportashtml/\#TABLES) bayrağı ayarlanmışsa, bu bayrak yoksayılacaktır.

### TABLES {#TABLES}
```
public static int TABLES
```


Tabloları ham HTML olarak dışa aktar.

 **Remarks:** 

Bu seçenek etkinleştirildiğinde, her tablo ham HTML olarak dışa aktarılacaktır. Aspose.Words bu durumda tabloların tüm biçimlendirmesini korumaya çalışacaktır.

Bu bayrak ayarlanmışsa, ilgili [NON\_COMPATIBLE\_TABLES](../../com.aspose.words/markdownexportashtml/\#NON-COMPATIBLE-TABLES) bayrağı yoksayılacaktır.

### length {#length}
```
public static int length
```


### fromName(String markdownExportAsHtmlName) {#fromName-java.lang.String}
```
public static int fromName(String markdownExportAsHtmlName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| markdownExportAsHtmlName | java.lang.String |  |

**Returns:**
int
### fromNames(Set markdownExportAsHtmlNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set markdownExportAsHtmlNames)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| markdownExportAsHtmlNames | java.util.Set |  |

**Returns:**
int
### getName(int markdownExportAsHtml) {#getName-int}
```
public static String getName(int markdownExportAsHtml)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| markdownExportAsHtml | int |  |

**Returns:**
java.lang.String
### getNames(int markdownExportAsHtml) {#getNames-int}
```
public static Set getNames(int markdownExportAsHtml)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| markdownExportAsHtml | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int markdownExportAsHtml) {#toString-int}
```
public static String toString(int markdownExportAsHtml)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| markdownExportAsHtml | int |  |

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
