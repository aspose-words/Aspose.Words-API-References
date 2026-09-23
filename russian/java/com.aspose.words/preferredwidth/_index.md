---
title: "PreferredWidth"
linktitle: "PreferredWidth"
second_title: "Aspose.Words для Java"
description: "Представляет значение и его единицу измерения, используемые для указания предпочтительной ширины таблицы или ячейки в Java."
type: docs
weight: 550
url: /ru/java/com.aspose.words/preferredwidth/
---

**Inheritance:**
java.lang.Object
```
public class PreferredWidth
```

Представляет значение и его единицу измерения, используемые для указания предпочтительной ширины таблицы или ячейки.

Чтобы узнать больше, посетите статью документации [ Working with Tables ][Working with Tables].

 **Remarks:** 

Предпочтительная ширина может быть указана в процентах, количестве пунктов или специальным значением "none/auto".

Экземпляры этого класса неизменяемы.

 **Examples:** 

Показывает, как установить автоматическое подгонку таблицы до 50% ширины страницы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell #1");
 builder.insertCell();
 builder.write("Cell #2");
 builder.insertCell();
 builder.write("Cell #3");

 table.setPreferredWidth(PreferredWidth.fromPercent(50.0));

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
 
```

Показывает, как задать предпочтительную ширину для ячеек таблицы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```


[Working with Tables]: https://docs.aspose.com/words/java/working-with-tables/
## Поля

| Поле | Описание |
| --- | --- |
| [AUTO](#AUTO) | Возвращает экземпляр, представляющий значение "preferred width is not specified". |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(PreferredWidth other)](#equals-com.aspose.words.PreferredWidth) | Определяет, равен ли указанный [PreferredWidth](../../com.aspose.words/preferredwidth/) по значению текущему [PreferredWidth](../../com.aspose.words/preferredwidth/). |
| [equals(Object obj)](#equals-java.lang.Object) | Определяет, равен ли указанный объект по значению текущему объекту. |
| [fromPercent(double percent)](#fromPercent-double) | Метод создания, возвращающий новый экземпляр, представляющий предпочтительную ширину, указанную в процентах. |
| [fromPoints(double points)](#fromPoints-double) | Метод создания, возвращающий новый экземпляр, представляющий предпочтительную ширину, указанную в пунктах. |
| [getType()](#getType) | Получает единицу измерения, используемую для этого предпочтительного значения ширины. |
| [getValue()](#getValue) | Получает предпочтительное значение ширины. |
| [hashCode()](#hashCode) |  |
| [toString()](#toString) | Возвращает удобочитаемую строку, отображающую значение этого объекта. |
### AUTO {#AUTO}
```
public static PreferredWidth AUTO
```


Возвращает экземпляр, представляющий значение "preferred width is not specified".

 **Examples:** 

Показывает, как задать предпочтительную ширину для ячеек таблицы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```

### equals(PreferredWidth other) {#equals-com.aspose.words.PreferredWidth}
```
public boolean equals(PreferredWidth other)
```


Определяет, равен ли указанный [PreferredWidth](../../com.aspose.words/preferredwidth/) по значению текущему [PreferredWidth](../../com.aspose.words/preferredwidth/).

 **Examples:** 

Показывает, как задать предпочтительную ширину для ячеек таблицы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| other | [PreferredWidth](../../com.aspose.words/preferredwidth/) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Определяет, равен ли указанный объект по значению текущему объекту.

 **Examples:** 

Показывает, как задать предпочтительную ширину для ячеек таблицы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### fromPercent(double percent) {#fromPercent-double}
```
public static PreferredWidth fromPercent(double percent)
```


Метод создания, возвращающий новый экземпляр, представляющий предпочтительную ширину, указанную в процентах.

 **Examples:** 

Показывает, как установить автоматическое подгонку таблицы до 50% ширины страницы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell #1");
 builder.insertCell();
 builder.write("Cell #2");
 builder.insertCell();
 builder.write("Cell #3");

 table.setPreferredWidth(PreferredWidth.fromPercent(50.0));

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
 
```

Показывает, как задать предпочтительную ширину для ячеек таблицы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| процент | double | Значение должно быть от 0 до 100. |

**Returns:**
[PreferredWidth](../../com.aspose.words/preferredwidth/)
### fromPoints(double points) {#fromPoints-double}
```
public static PreferredWidth fromPoints(double points)
```


Метод создания, возвращающий новый экземпляр, представляющий предпочтительную ширину, указанную в пунктах.

 **Examples:** 

Показывает, как задать предпочтительную ширину для ячеек таблицы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```

Показывает, как использовать инструменты конвертации единиц при указании предпочтительной ширины ячейки.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(ConvertUtil.inchToPoint(3.0)));
 builder.insertCell();

 Assert.assertEquals(216.0d, table.getFirstRow().getFirstCell().getCellFormat().getPreferredWidth().getValue());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| пункты | double | Значение должно быть от 0 до 22 дюймов (22 \* 72 пункта). |

**Returns:**
[PreferredWidth](../../com.aspose.words/preferredwidth/)
### getType() {#getType}
```
public int getType()
```


Получает единицу измерения, используемую для этого предпочтительного значения ширины.

 **Examples:** 

Показывает, как проверить тип и значение предпочтительной ширины ячейки таблицы.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 Table table = doc.getFirstSection().getBody().getTables().get(0);
 Cell firstCell = table.getFirstRow().getFirstCell();

 Assert.assertEquals(PreferredWidthType.PERCENT, firstCell.getCellFormat().getPreferredWidth().getType());
 Assert.assertEquals(11.16d, firstCell.getCellFormat().getPreferredWidth().getValue());
 
```

**Returns:**
int - Единица измерения, используемая для этого предпочтительного значения ширины. Возвращаемое значение является одной из констант [PreferredWidthType](../../com.aspose.words/preferredwidthtype/).
### getValue() {#getValue}
```
public double getValue()
```


Получает предпочтительное значение ширины. Единица измерения указывается в свойстве [getType()](../../com.aspose.words/preferredwidth/\#getType).

 **Examples:** 

Показывает, как проверить тип и значение предпочтительной ширины ячейки таблицы.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 Table table = doc.getFirstSection().getBody().getTables().get(0);
 Cell firstCell = table.getFirstRow().getFirstCell();

 Assert.assertEquals(PreferredWidthType.PERCENT, firstCell.getCellFormat().getPreferredWidth().getType());
 Assert.assertEquals(11.16d, firstCell.getCellFormat().getPreferredWidth().getValue());
 
```

**Returns:**
double - Предпочтительное значение ширины.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### toString() {#toString}
```
public String toString()
```


Возвращает удобочитаемую строку, отображающую значение этого объекта.

 **Examples:** 

Показывает, как задать предпочтительную ширину для ячеек таблицы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```

**Returns:**
java.lang.String
