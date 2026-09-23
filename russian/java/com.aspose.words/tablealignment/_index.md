---
title: "TableAlignment"
linktitle: "TableAlignment"
second_title: "Aspose.Words для Java"
description: "Указывает выравнивание встроенной таблицы в Java."
type: docs
weight: 657
url: /ru/java/com.aspose.words/tablealignment/
---

**Inheritance:**
java.lang.Object
```
public class TableAlignment
```

Указывает выравнивание встроенной таблицы.

 **Examples:** 

Показывает, как применить контурную границу к таблице.

```

 Document doc = new Document(getMyDir() + "Tables.docx");
 Table table = doc.getFirstSection().getBody().getTables().get(0);

 // Align the table to the center of the page.
 table.setAlignment(TableAlignment.CENTER);

 // Clear any existing borders and shading from the table.
 table.clearBorders();
 table.clearShading();

 // Add green borders to the outline of the table.
 table.setBorder(BorderType.LEFT, LineStyle.SINGLE, 1.5, Color.GREEN, true);
 table.setBorder(BorderType.RIGHT, LineStyle.SINGLE, 1.5, Color.GREEN, true);
 table.setBorder(BorderType.TOP, LineStyle.SINGLE, 1.5, Color.GREEN, true);
 table.setBorder(BorderType.BOTTOM, LineStyle.SINGLE, 1.5, Color.GREEN, true);

 // Fill the cells with a light green solid color.
 table.setShading(TextureIndex.TEXTURE_SOLID, Color.GREEN, Color.GREEN);

 doc.save(getArtifactsDir() + "Table.SetOutlineBorders.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [CENTER](#CENTER) | Таблица центрирована. |
| [LEFT](#LEFT) | Таблица выровнена по левому краю. |
| [RIGHT](#RIGHT) | Таблица выровнена по правому краю. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String tableAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int tableAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tableAlignment)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


Таблица центрирована.

### LEFT {#LEFT}
```
public static int LEFT
```


Таблица выровнена по левому краю.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Таблица выровнена по правому краю.

### length {#length}
```
public static int length
```


### fromName(String tableAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String tableAlignmentName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| tableAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int tableAlignment) {#getName-int}
```
public static String getName(int tableAlignment)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| tableAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int tableAlignment) {#toString-int}
```
public static String toString(int tableAlignment)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| tableAlignment | int |  |

**Returns:**
java.lang.String
