---
title: "SectionLayoutMode"
linktitle: "SectionLayoutMode"
second_title: "Aspose.Words для Java"
description: "Указывает режим компоновки для раздела, позволяющий определить поведение сетки документа в Java."
type: docs
weight: 607
url: /ru/java/com.aspose.words/sectionlayoutmode/
---

**Inheritance:**
java.lang.Object
```
public class SectionLayoutMode
```

Указывает режим компоновки раздела, позволяющий задавать поведение сетки документа.

 **Examples:** 

Показывает, как задать ограничение для количества символов, которое может содержать каждая строка.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of characters per line in this section.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.GRID);
 builder.getPageSetup().setCharactersPerLine(10);

 // The number of characters also depends on the size of the font.
 doc.getStyles().get("Normal").getFont().setSize(20.0);

 Assert.assertEquals(8, doc.getFirstSection().getPageSetup().getCharactersPerLine());

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "PageSetup.CharactersPerLine.docx");
 
```

Показывает, как задать ограничение количества строк, которое может быть на каждой странице.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of lines per page in this section.
 // A large enough font size will push some lines down onto the next page to avoid overlapping characters.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.LINE_GRID);
 builder.getPageSetup().setLinesPerPage(15);

 builder.getParagraphFormat().setSnapToGrid(true);

 for (int i = 0; i < 30; i++)
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

 doc.save(getArtifactsDir() + "PageSetup.LinesPerPage.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [DEFAULT](#DEFAULT) | Указывает, что к содержимому соответствующего раздела в документе не будет применяться сетка документа. |
| [GRID](#GRID) | Указывает, что соответствующий раздел будет иметь как дополнительный межстрочный интервал, так и межсимвольный интервал, добавленные к каждой строке и каждому символу внутри него, чтобы поддерживать определённое количество строк на страницу и символов в строке. |
| [LINE_GRID](#LINE-GRID) | Указывает, что к каждой строке соответствующего раздела будет добавлен дополнительный межстрочный интервал, чтобы поддерживать указанное количество строк на страницу. |
| [SNAP_TO_CHARS](#SNAP-TO-CHARS) | Указывает, что соответствующий раздел будет иметь как дополнительный межстрочный интервал, так и межсимвольный интервал, добавленные к каждой строке и каждому символу внутри него, чтобы поддерживать определённое количество строк на страницу и символов в строке. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String sectionLayoutModeName)](#fromName-java.lang.String) |  |
| [getName(int sectionLayoutMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sectionLayoutMode)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Указывает, что к содержимому соответствующего раздела в документе не будет применяться сетка документа.

### GRID {#GRID}
```
public static int GRID
```


Указывает, что соответствующий раздел будет иметь как дополнительный межстрочный интервал, так и межсимвольный интервал, добавленные к каждой строке и каждому символу внутри него, чтобы поддерживать определённое количество строк на страницу и символов в строке. Символы не будут автоматически выравниваться по линиям сетки при вводе.

### LINE_GRID {#LINE-GRID}
```
public static int LINE_GRID
```


Указывает, что к каждой строке соответствующего раздела будет добавлен дополнительный межстрочный интервал, чтобы поддерживать указанное количество строк на страницу.

### SNAP_TO_CHARS {#SNAP-TO-CHARS}
```
public static int SNAP_TO_CHARS
```


Указывает, что соответствующий раздел будет иметь как дополнительный межстрочный интервал, так и межсимвольный интервал, добавленные к каждой строке и каждому символу внутри него, чтобы поддерживать определённое количество строк на страницу и символов в строке. Символы будут автоматически выравниваться по линиям сетки при вводе.

### length {#length}
```
public static int length
```


### fromName(String sectionLayoutModeName) {#fromName-java.lang.String}
```
public static int fromName(String sectionLayoutModeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| sectionLayoutModeName | java.lang.String |  |

**Returns:**
int
### getName(int sectionLayoutMode) {#getName-int}
```
public static String getName(int sectionLayoutMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| sectionLayoutMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int sectionLayoutMode) {#toString-int}
```
public static String toString(int sectionLayoutMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| sectionLayoutMode | int |  |

**Returns:**
java.lang.String
