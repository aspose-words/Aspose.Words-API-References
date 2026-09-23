---
title: "PdfTextCompression"
linktitle: "PdfTextCompression"
second_title: "Aspose.Words для Java"
description: "Указывает тип сжатия, применяемый ко всему содержимому PDF‑файла, кроме изображений, в Java."
type: docs
weight: 543
url: /ru/java/com.aspose.words/pdftextcompression/
---

**Inheritance:**
java.lang.Object
```
public class PdfTextCompression
```

Указывает тип сжатия, применяемый ко всему содержимому PDF‑файла, кроме изображений.

 **Examples:** 

Показывает, как применять сжатие текста при сохранении документа в PDF.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 for (int i = 0; i < 100; i++)
     builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
             "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "TextCompression" property to "PdfTextCompression.None" to not apply any
 // compression to text when we save the document to PDF.
 // Set the "TextCompression" property to "PdfTextCompression.Flate" to apply ZIP compression
 // to text when we save the document to PDF. The larger the document, the bigger the impact that this will have.
 options.setTextCompression(pdfTextCompression);

 doc.save(getArtifactsDir() + "PdfSaveOptions.TextCompression.pdf", options);
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [FLATE](#FLATE) | Сжатие Flate (ZIP). |
| [NONE](#NONE) | Без сжатия. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String pdfTextCompressionName)](#fromName-java.lang.String) |  |
| [getName(int pdfTextCompression)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfTextCompression)](#toString-int) |  |
### FLATE {#FLATE}
```
public static int FLATE
```


Сжатие Flate (ZIP).

### NONE {#NONE}
```
public static int NONE
```


Без сжатия.

### length {#length}
```
public static int length
```


### fromName(String pdfTextCompressionName) {#fromName-java.lang.String}
```
public static int fromName(String pdfTextCompressionName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfTextCompressionName | java.lang.String |  |

**Returns:**
int
### getName(int pdfTextCompression) {#getName-int}
```
public static String getName(int pdfTextCompression)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfTextCompression | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfTextCompression) {#toString-int}
```
public static String toString(int pdfTextCompression)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfTextCompression | int |  |

**Returns:**
java.lang.String
