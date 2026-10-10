---
title: "CompressionLevel"
linktitle: "CompressionLevel"
second_title: "Aspose.Words для Java"
description: "Уровень сжатия для файлов OOXML и XPS в Java."
type: docs
weight: 122
url: /ru/java/com.aspose.words/compressionlevel/
---

**Inheritance:**
java.lang.Object
```
public class CompressionLevel
```

Уровень сжатия для файлов OOXML и XPS.

(Файлы DOCX, DOTX и XPS внутренно являются ZIP-архивом, это свойство управляет уровнем сжатия архива.

Обратите внимание, что файл FlatOpc не является ZIP-архивом, поэтому это свойство не влияет на файлы FlatOpc.)

 **Examples:** 

Показывает, как указать уровень сжатия, используемый при сохранении документа OOXML.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 // When we save the document to an OOXML format, we can create an OoxmlSaveOptions object
 // and then pass it to the document's saving method to modify how we save the document.
 // Set the "CompressionLevel" property to "CompressionLevel.Maximum" to apply the strongest and slowest compression.
 // Set the "CompressionLevel" property to "CompressionLevel.Normal" to apply
 // the default compression that Aspose.Words uses while saving OOXML documents.
 // Set the "CompressionLevel" property to "CompressionLevel.Fast" to apply a faster and weaker compression.
 // Set the "CompressionLevel" property to "CompressionLevel.SuperFast" to apply
 // the default compression that Microsoft Word uses.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.DOCX);
 saveOptions.setCompressionLevel(compressionLevel);

 StopWatch st = new StopWatch();
 st.start();
 doc.save(getArtifactsDir() + "OoxmlSaveOptions.DocumentCompression.docx", saveOptions);
 st.stop();

 File fileInfo = new File(getArtifactsDir() + "OoxmlSaveOptions.DocumentCompression.docx");

 System.out.println(MessageFormat.format("Saving operation done using the \"{0}\" compression level:", compressionLevel));
 System.out.println(MessageFormat.format("\tDuration:\t{0}", st.getTime()));
 System.out.println(MessageFormat.format("\tFile Size:\t{0} bytes", fileInfo.length()));
 
```

Показывает, как управлять уровнем сжатия при сохранении документа в формате XPS.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Sample document for XPS compression test.");

 // Create an XpsSaveOptions object and set the compression level.
 XpsSaveOptions options = new XpsSaveOptions();
 options.setCompressionLevel(CompressionLevel.MAXIMUM);

 doc.save(getArtifactsDir() + "XpsSaveOptions.CompressionLevelXps.xps", options);
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [FAST](#FAST) | Быстрый уровень сжатия. |
| [MAXIMUM](#MAXIMUM) | Максимальный уровень сжатия. |
| [NORMAL](#NORMAL) | Обычный уровень сжатия. |
| [SUPER_FAST](#SUPER-FAST) | Сверхбыстрый уровень сжатия. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String compressionLevelName)](#fromName-java.lang.String) |  |
| [getName(int compressionLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int compressionLevel)](#toString-int) |  |
### FAST {#FAST}
```
public static int FAST
```


Быстрый уровень сжатия.

### MAXIMUM {#MAXIMUM}
```
public static int MAXIMUM
```


Максимальный уровень сжатия.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Обычный уровень сжатия. Уровень сжатия по умолчанию, используемый в Aspose.Words.

### SUPER_FAST {#SUPER-FAST}
```
public static int SUPER_FAST
```


Сверхбыстрый уровень сжатия. Microsoft Word использует этот уровень сжатия.

### length {#length}
```
public static int length
```


### fromName(String compressionLevelName) {#fromName-java.lang.String}
```
public static int fromName(String compressionLevelName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| compressionLevelName | java.lang.String |  |

**Returns:**
int
### getName(int compressionLevel) {#getName-int}
```
public static String getName(int compressionLevel)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| compressionLevel | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int compressionLevel) {#toString-int}
```
public static String toString(int compressionLevel)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| compressionLevel | int |  |

**Returns:**
java.lang.String
