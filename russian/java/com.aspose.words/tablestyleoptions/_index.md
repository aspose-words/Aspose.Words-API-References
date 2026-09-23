---
title: "TableStyleOptions"
linktitle: "TableStyleOptions"
second_title: "Aspose.Words для Java"
description: "Указывает, как стиль таблицы применяется к таблице в Java."
type: docs
weight: 661
url: /ru/java/com.aspose.words/tablestyleoptions/
---

**Inheritance:**
java.lang.Object
```
public class TableStyleOptions
```

Указывает, как стиль таблицы применяется к таблице.

 **Examples:** 

Показывает, как создать новую таблицу, применяя стиль.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // We must insert at least one row before setting any table formatting.
 builder.insertCell();

 // Set the table style used based on the style identifier.
 // Note that not all table styles are available when saving to .doc format.
 table.setStyleIdentifier(StyleIdentifier.MEDIUM_SHADING_1_ACCENT_1);

 // Partially apply the style to features of the table based on predicates, then build the table.
 table.setStyleOptions(TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS | TableStyleOptions.FIRST_ROW);
 table.autoFit(AutoFitBehavior.AUTO_FIT_TO_CONTENTS);

 builder.writeln("Item");
 builder.getCellFormat().setRightPadding(40.0);
 builder.insertCell();
 builder.writeln("Quantity (kg)");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Apples");
 builder.insertCell();
 builder.writeln("20");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Bananas");
 builder.insertCell();
 builder.writeln("40");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Carrots");
 builder.insertCell();
 builder.writeln("50");
 builder.endRow();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTableWithStyle.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [COLUMN_BANDS](#COLUMN-BANDS) | Применить условное форматирование полосы столбцов. |
| [DEFAULT](#DEFAULT) | Это настройки по умолчанию Microsoft Word. |
| [DEFAULT_2003](#DEFAULT-2003) | Применено полосатое форматирование строк и столбцов. |
| [FIRST_COLUMN](#FIRST-COLUMN) | Применить условное форматирование первого столбца. |
| [FIRST_ROW](#FIRST-ROW) | Применить условное форматирование первой строки. |
| [LAST_COLUMN](#LAST-COLUMN) | Применить условное форматирование последнего столбца. |
| [LAST_ROW](#LAST-ROW) | Применить условное форматирование последней строки. |
| [NONE](#NONE) | Стиль таблицы не применяется. |
| [ROW_BANDS](#ROW-BANDS) | Применить условное форматирование полосы строк. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String tableStyleOptionsName)](#fromName-java.lang.String) |  |
| [fromNames(Set tableStyleOptionsNames)](#fromNames-java.util.Set) |  |
| [getName(int tableStyleOptions)](#getName-int) |  |
| [getNames(int tableStyleOptions)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tableStyleOptions)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### COLUMN_BANDS {#COLUMN-BANDS}
```
public static int COLUMN_BANDS
```


Применить условное форматирование полосы столбцов.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Это настройки по умолчанию Microsoft Word.

### DEFAULT_2003 {#DEFAULT-2003}
```
public static int DEFAULT_2003
```


Применено полосатое форматирование строк и столбцов. Это значение по умолчанию Microsoft Word для старых форматов, таких как DOC, WML и RTF.

### FIRST_COLUMN {#FIRST-COLUMN}
```
public static int FIRST_COLUMN
```


Применить условное форматирование первого столбца.

### FIRST_ROW {#FIRST-ROW}
```
public static int FIRST_ROW
```


Применить условное форматирование первой строки.

### LAST_COLUMN {#LAST-COLUMN}
```
public static int LAST_COLUMN
```


Применить условное форматирование последнего столбца.

### LAST_ROW {#LAST-ROW}
```
public static int LAST_ROW
```


Применить условное форматирование последней строки.

### NONE {#NONE}
```
public static int NONE
```


Стиль таблицы не применяется.

### ROW_BANDS {#ROW-BANDS}
```
public static int ROW_BANDS
```


Применить условное форматирование полосы строк.

### length {#length}
```
public static int length
```


### fromName(String tableStyleOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String tableStyleOptionsName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| tableStyleOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set tableStyleOptionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set tableStyleOptionsNames)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| tableStyleOptionsNames | java.util.Set |  |

**Returns:**
int
### getName(int tableStyleOptions) {#getName-int}
```
public static String getName(int tableStyleOptions)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| tableStyleOptions | int |  |

**Returns:**
java.lang.String
### getNames(int tableStyleOptions) {#getNames-int}
```
public static Set getNames(int tableStyleOptions)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| tableStyleOptions | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int tableStyleOptions) {#toString-int}
```
public static String toString(int tableStyleOptions)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| tableStyleOptions | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
