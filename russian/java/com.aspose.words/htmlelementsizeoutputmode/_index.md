---
title: "HtmlElementSizeOutputMode"
linktitle: "HtmlElementSizeOutputMode"
second_title: "Aspose.Words для Java"
description: "Указывает, как Aspose.Words экспортирует ширину и высоту элементов в HTML, MHTML и EPUB в Java."
type: docs
weight: 378
url: /ru/java/com.aspose.words/htmlelementsizeoutputmode/
---

**Inheritance:**
java.lang.Object
```
public class HtmlElementSizeOutputMode
```

Указывает, как Aspose.Words экспортирует ширину и высоту элементов в HTML, MHTML и EPUB.

 **Examples:** 

Показывает, как сохранить отрицательные отступы в выходном .html.

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
## Поля

| Поле | Описание |
| --- | --- |
| [ALL](#ALL) | Все размеры элементов, как в абсолютных, так и в относительных единицах, указанные в документе, экспортируются. |
| [NONE](#NONE) | Размеры элементов не экспортируются. |
| [RELATIVE_ONLY](#RELATIVE-ONLY) | Размеры элементов экспортируются только в том случае, если они указаны в документе в относительных единицах. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String htmlElementSizeOutputModeName)](#fromName-java.lang.String) |  |
| [getName(int htmlElementSizeOutputMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int htmlElementSizeOutputMode)](#toString-int) |  |
### ALL {#ALL}
```
public static int ALL
```


Все размеры элементов, как в абсолютных, так и в относительных единицах, указанные в документе, экспортируются.

### NONE {#NONE}
```
public static int NONE
```


Размеры элементов не экспортируются. Визуальные агенты автоматически построят макет в соответствии с взаимосвязью между элементами.

### RELATIVE_ONLY {#RELATIVE-ONLY}
```
public static int RELATIVE_ONLY
```


Размеры элементов экспортируются только в том случае, если они указаны в относительных единицах в документе. Фиксированные размеры в этом режиме не экспортируются. Визуальные агенты вычислят недостающие размеры, чтобы сделать макет документа более естественным.

### length {#length}
```
public static int length
```


### fromName(String htmlElementSizeOutputModeName) {#fromName-java.lang.String}
```
public static int fromName(String htmlElementSizeOutputModeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| htmlElementSizeOutputModeName | java.lang.String |  |

**Returns:**
int
### getName(int htmlElementSizeOutputMode) {#getName-int}
```
public static String getName(int htmlElementSizeOutputMode)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| htmlElementSizeOutputMode | int |  |

**Returns:**
java.lang.String
