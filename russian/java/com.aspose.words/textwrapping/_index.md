---
title: "TextWrapping"
linktitle: "TextWrapping"
second_title: "Aspose.Words для Java"
description: "Указывает, как текст обтекает таблицу в Java."
type: docs
weight: 679
url: /ru/java/com.aspose.words/textwrapping/
---

**Inheritance:**
java.lang.Object
```
public class TextWrapping
```

Указывает, как текст обтекает таблицу.

 **Examples:** 

Показывает, как работать с обтеканием текста таблицы.

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
## Поля

| Поле | Описание |
| --- | --- |
| [AROUND](#AROUND) | Текст обтекает таблицу, занимая доступное боковое пространство. |
| [DEFAULT](#DEFAULT) | Значение по умолчанию. |
| [NONE](#NONE) | Текст и таблица отображаются в порядке их появления в документе. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String textWrappingName)](#fromName-java.lang.String) |  |
| [getName(int textWrapping)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textWrapping)](#toString-int) |  |
### AROUND {#AROUND}
```
public static int AROUND
```


Текст обтекает таблицу, занимая доступное боковое пространство.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Значение по умолчанию.

### NONE {#NONE}
```
public static int NONE
```


Текст и таблица отображаются в порядке их появления в документе.

### length {#length}
```
public static int length
```


### fromName(String textWrappingName) {#fromName-java.lang.String}
```
public static int fromName(String textWrappingName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| textWrappingName | java.lang.String |  |

**Returns:**
int
### getName(int textWrapping) {#getName-int}
```
public static String getName(int textWrapping)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| textWrapping | int |  |

**Returns:**
java.lang.String
