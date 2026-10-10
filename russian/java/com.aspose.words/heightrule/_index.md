---
title: "HeightRule"
linktitle: "HeightRule"
second_title: "Aspose.Words для Java"
description: "Указывает правило определения высоты объекта в Java."
type: docs
weight: 373
url: /ru/java/com.aspose.words/heightrule/
---

**Inheritance:**
java.lang.Object
```
public class HeightRule
```

Указывает правило определения высоты объекта.

 **Examples:** 

Показывает, как форматировать строки с помощью DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Start a second row, and then configure its height. The builder will apply these settings to
 // its current row, as well as any new rows it creates afterwards.
 builder.endRow();

 RowFormat rowFormat = builder.getRowFormat();
 rowFormat.setHeight(100.0);
 rowFormat.setHeightRule(HeightRule.EXACTLY);

 builder.insertCell();
 builder.write("Row 2, cell 1.");
 builder.endTable();

 // The first row was unaffected by the padding reconfiguration and still holds the default values.
 Assert.assertEquals(0.0d, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());

 Assert.assertEquals(100.0d, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());

 doc.save(getArtifactsDir() + "DocumentBuilder.SetRowFormatting.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [AT_LEAST](#AT-LEAST) | Высота будет как минимум указанной высоты в пунктах. |
| [AUTO](#AUTO) | Высота будет автоматически увеличиваться, чтобы вместить весь текст внутри объекта. |
| [EXACTLY](#EXACTLY) | Высота указана точно в пунктах. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String heightRuleName)](#fromName-java.lang.String) |  |
| [getName(int heightRule)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int heightRule)](#toString-int) |  |
### AT_LEAST {#AT-LEAST}
```
public static int AT_LEAST
```


Высота будет как минимум указанной высоты в пунктах. При необходимости она будет увеличиваться, чтобы вместить весь текст внутри объекта.

### AUTO {#AUTO}
```
public static int AUTO
```


Высота будет автоматически увеличиваться, чтобы вместить весь текст внутри объекта.

### EXACTLY {#EXACTLY}
```
public static int EXACTLY
```


Высота указана точно в пунктах. Обратите внимание, что если текст не помещается в объект этой высоты, он будет обрезан.

### length {#length}
```
public static int length
```


### fromName(String heightRuleName) {#fromName-java.lang.String}
```
public static int fromName(String heightRuleName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| heightRuleName | java.lang.String |  |

**Returns:**
int
### getName(int heightRule) {#getName-int}
```
public static String getName(int heightRule)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| heightRule | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int heightRule) {#toString-int}
```
public static String toString(int heightRule)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| heightRule | int |  |

**Returns:**
java.lang.String
