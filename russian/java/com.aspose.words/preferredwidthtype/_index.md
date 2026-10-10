---
title: "PreferredWidthType"
linktitle: "PreferredWidthType"
second_title: "Aspose.Words для Java"
description: "Указывает единицу измерения предпочтительной ширины таблицы или ячейки в Java."
type: docs
weight: 551
url: /ru/java/com.aspose.words/preferredwidthtype/
---

**Inheritance:**
java.lang.Object
```
public class PreferredWidthType
```

Указывает единицу измерения предпочтительной ширины таблицы или ячейки.

 **Examples:** 

Показывает, как проверить тип и значение предпочтительной ширины ячейки таблицы.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 Table table = doc.getFirstSection().getBody().getTables().get(0);
 Cell firstCell = table.getFirstRow().getFirstCell();

 Assert.assertEquals(PreferredWidthType.PERCENT, firstCell.getCellFormat().getPreferredWidth().getType());
 Assert.assertEquals(11.16d, firstCell.getCellFormat().getPreferredWidth().getValue());
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [AUTO](#AUTO) | Предпочтительная ширина не указана. |
| [PERCENT](#PERCENT) | Измерьте текущую ширину элемента, используя указанный процент. |
| [POINTS](#POINTS) | Измерьте текущую ширину элемента, используя указанное количество пунктов (1/72 дюйма). |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String preferredWidthTypeName)](#fromName-java.lang.String) |  |
| [getName(int preferredWidthType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int preferredWidthType)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Предпочтительная ширина не указана. Фактическая ширина таблицы или ячейки либо задаётся явно, либо будет определена автоматически алгоритмом компоновки таблицы при отображении, в зависимости от настройки автоматической подгонки таблицы.

### PERCENT {#PERCENT}
```
public static int PERCENT
```


Измерьте текущую ширину элемента, используя указанный процент.

### POINTS {#POINTS}
```
public static int POINTS
```


Измерьте текущую ширину элемента, используя указанное количество пунктов (1/72 дюйма).

### length {#length}
```
public static int length
```


### fromName(String preferredWidthTypeName) {#fromName-java.lang.String}
```
public static int fromName(String preferredWidthTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| preferredWidthTypeName | java.lang.String |  |

**Returns:**
int
### getName(int preferredWidthType) {#getName-int}
```
public static String getName(int preferredWidthType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| preferredWidthType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int preferredWidthType) {#toString-int}
```
public static String toString(int preferredWidthType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| preferredWidthType | int |  |

**Returns:**
java.lang.String
