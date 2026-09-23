---
title: "TextColumnCollection"
linktitle: "TextColumnCollection"
second_title: "Aspose.Words для Java"
description: "Коллекция объектов TextColumn, представляющих все столбцы текста в разделе документа в Java."
type: docs
weight: 671
url: /ru/java/com.aspose.words/textcolumncollection/
---

**Inheritance:**
java.lang.Object
```
public class TextColumnCollection
```

Коллекция объектов [TextColumn](../../com.aspose.words/textcolumn/), представляющих все столбцы текста в разделе документа.

Чтобы узнать больше, посетите статью документации [ Working with Sections ][Working with Sections].

 **Remarks:** 

Используйте [setCount(int)](../../com.aspose.words/textcolumncollection/\#setCount-int) чтобы задать количество текстовых колонок.

Чтобы сделать все колонки одинаковой ширины и равномерно распределёнными, установите [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) в  true  и укажите величину промежутка между колонками в [getSpacing()](../../com.aspose.words/textcolumncollection/\#getSpacing) / [setSpacing(double)](../../com.aspose.words/textcolumncollection/\#setSpacing-double). MS Word автоматически вычислит ширину колонок.

Если у вас [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) установлен в  false , вам необходимо указать ширину и промежуток для каждой колонки отдельно. Используйте индексатор для доступа к отдельным объектам [TextColumn](../../com.aspose.words/textcolumn/).

При использовании пользовательских ширин колонок убедитесь, что сумма всех ширин колонок и промежутков между ними равна ширине страницы за вычетом левых и правых полей страницы.

 **Examples:** 

Показывает, как создать несколько колонок с равномерным расстоянием в разделе.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```


[Working with Sections]: https://docs.aspose.com/words/java/working-with-sections/
## Методы

| Метод | Описание |
| --- | --- |
| [get(int index)](#get-int) | Возвращает текстовую колонку по указанному индексу. |
| [getCount()](#getCount) | Получает количество колонок в разделе документа. |
| [getEvenlySpaced()](#getEvenlySpaced) | True, если текстовые колонки имеют одинаковую ширину и равномерно распределены. |
| [getLineBetween()](#getLineBetween) | Когда  true , добавляет вертикальную линию между колонками. |
| [getSpacing()](#getSpacing) | Когда колонки равномерно распределены, получает или задает величину промежутка между каждой колонкой в пунктах. |
| [getWidth()](#getWidth) | Когда колонки равномерно распределены, получает ширину колонок. |
| [setCount(int newCount)](#setCount-int) | Размещает текст в указанном количестве текстовых колонок. |
| [setEvenlySpaced(boolean value)](#setEvenlySpaced-boolean) | True, если текстовые колонки имеют одинаковую ширину и равномерно распределены. |
| [setLineBetween(boolean value)](#setLineBetween-boolean) | Когда  true , добавляет вертикальную линию между колонками. |
| [setSpacing(double value)](#setSpacing-double) | Когда колонки равномерно распределены, получает или задает величину промежутка между каждой колонкой в пунктах. |
### get(int index) {#get-int}
```
public TextColumn get(int index)
```


Возвращает текстовую колонку по указанному индексу.

 **Examples:** 

Показывает, как создать колонки с неравномерным расстоянием.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 PageSetup pageSetup = builder.getPageSetup();

 TextColumnCollection columns = pageSetup.getTextColumns();
 columns.setEvenlySpaced(false);
 columns.setCount(2);

 // Determine the amount of room that we have available for arranging columns.
 double contentWidth = pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin();

 Assert.assertEquals(468.0d, contentWidth, 0.01d);

 // Set the first column to be narrow.
 TextColumn column = columns.get(0);
 column.setWidth(100.0);
 column.setSpaceAfter(20.0);

 // Set the second column to take the rest of the space available within the margins of the page.
 column = columns.get(1);
 column.setWidth(contentWidth - column.getWidth() - column.getSpaceAfter());

 builder.writeln("Narrow column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Wide column 2.");

 doc.save(getArtifactsDir() + "PageSetup.CustomColumnWidth.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int |  |

**Returns:**
[TextColumn](../../com.aspose.words/textcolumn/) - A text column at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Получает количество колонок в разделе документа.

 **Examples:** 

Показывает, как создать несколько колонок с равномерным расстоянием в разделе.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Returns:**
int — количество колонок в разделе документа.
### getEvenlySpaced() {#getEvenlySpaced}
```
public boolean getEvenlySpaced()
```


True, если текстовые колонки имеют одинаковую ширину и равномерно распределены.

 **Examples:** 

Показывает, как создать колонки с неравномерным расстоянием.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 PageSetup pageSetup = builder.getPageSetup();

 TextColumnCollection columns = pageSetup.getTextColumns();
 columns.setEvenlySpaced(false);
 columns.setCount(2);

 // Determine the amount of room that we have available for arranging columns.
 double contentWidth = pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin();

 Assert.assertEquals(468.0d, contentWidth, 0.01d);

 // Set the first column to be narrow.
 TextColumn column = columns.get(0);
 column.setWidth(100.0);
 column.setSpaceAfter(20.0);

 // Set the second column to take the rest of the space available within the margins of the page.
 column = columns.get(1);
 column.setWidth(contentWidth - column.getWidth() - column.getSpaceAfter());

 builder.writeln("Narrow column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Wide column 2.");

 doc.save(getArtifactsDir() + "PageSetup.CustomColumnWidth.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getLineBetween() {#getLineBetween}
```
public boolean getLineBetween()
```


Когда  true , добавляет вертикальную линию между колонками.

 **Examples:** 

Показывает, как разделить колонки вертикальной линией.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Configure the current section's PageSetup object to divide the text into several columns.
 // Set the "LineBetween" property to "true" to put a dividing line between columns.
 // Set the "LineBetween" property to "false" to leave the space between columns blank.
 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setLineBetween(lineBetween);
 columns.setCount(3);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 3.");

 doc.save(getArtifactsDir() + "PageSetup.VerticalLineBetweenColumns.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getSpacing() {#getSpacing}
```
public double getSpacing()
```


Когда колонки равномерно распределены, получает или задает величину промежутка между каждой колонкой в пунктах.

 **Remarks:** 

Имеет эффект только когда [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) установлен в  true .

 **Examples:** 

Показывает, как создать несколько колонок с равномерным расстоянием в разделе.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Returns:**
double - Соответствующее  double  значение.
### getWidth() {#getWidth}
```
public double getWidth()
```


Когда колонки равномерно распределены, получает ширину колонок.

 **Remarks:** 

Имеет эффект только когда [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) установлен в  true .

 **Examples:** 

Показывает, как создать несколько колонок с равномерным расстоянием в разделе.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Returns:**
double - Соответствующее  double  значение.
### setCount(int newCount) {#setCount-int}
```
public void setCount(int newCount)
```


Размещает текст в указанном количестве текстовых колонок.

 **Remarks:** 

Когда [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) имеет значение  false  и вы увеличиваете количество колонок, новые объекты [TextColumn](../../com.aspose.words/textcolumn/) создаются с нулевой шириной и промежутком. Необходимо задать ширину и промежуток для новых колонок.

 **Examples:** 

Показывает, как создать несколько колонок с равномерным расстоянием в разделе.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| newCount | int | Количество колонок, в которые будет размещён текст. |

### setEvenlySpaced(boolean value) {#setEvenlySpaced-boolean}
```
public void setEvenlySpaced(boolean value)
```


True, если текстовые колонки имеют одинаковую ширину и равномерно распределены.

 **Examples:** 

Показывает, как создать колонки с неравномерным расстоянием.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 PageSetup pageSetup = builder.getPageSetup();

 TextColumnCollection columns = pageSetup.getTextColumns();
 columns.setEvenlySpaced(false);
 columns.setCount(2);

 // Determine the amount of room that we have available for arranging columns.
 double contentWidth = pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin();

 Assert.assertEquals(468.0d, contentWidth, 0.01d);

 // Set the first column to be narrow.
 TextColumn column = columns.get(0);
 column.setWidth(100.0);
 column.setSpaceAfter(20.0);

 // Set the second column to take the rest of the space available within the margins of the page.
 column = columns.get(1);
 column.setWidth(contentWidth - column.getWidth() - column.getSpaceAfter());

 builder.writeln("Narrow column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Wide column 2.");

 doc.save(getArtifactsDir() + "PageSetup.CustomColumnWidth.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setLineBetween(boolean value) {#setLineBetween-boolean}
```
public void setLineBetween(boolean value)
```


Когда  true , добавляет вертикальную линию между колонками.

 **Examples:** 

Показывает, как разделить колонки вертикальной линией.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Configure the current section's PageSetup object to divide the text into several columns.
 // Set the "LineBetween" property to "true" to put a dividing line between columns.
 // Set the "LineBetween" property to "false" to leave the space between columns blank.
 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setLineBetween(lineBetween);
 columns.setCount(3);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 3.");

 doc.save(getArtifactsDir() + "PageSetup.VerticalLineBetweenColumns.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setSpacing(double value) {#setSpacing-double}
```
public void setSpacing(double value)
```


Когда колонки равномерно распределены, получает или задает величину промежутка между каждой колонкой в пунктах.

 **Remarks:** 

Имеет эффект только когда [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) установлен в  true .

 **Examples:** 

Показывает, как создать несколько колонок с равномерным расстоянием в разделе.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Соответствующее  double  значение. |

