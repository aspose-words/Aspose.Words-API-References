---
title: "DataColumn"
linktitle: "DataColumn"
second_title: "Aspose.Words для Java"
description: "Представляет схему столбца в DataTable в Java."
type: docs
weight: 14
url: /ru/java/com.aspose.words.net.system.data/datacolumn/
---

**Inheritance:**
java.lang.Object
```
public class DataColumn
```

Представляет схему столбца в [DataTable](../../com.aspose.words.net.system.data/datatable/).
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [DataColumn()](#DataColumn) | Инициализирует новый экземпляр класса [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) типа string. |
| [DataColumn(String columnName)](#DataColumn-java.lang.String) | Инициализирует новый экземпляр класса [DataColumn](../../com.aspose.words.net.system.data/datacolumn/), типа string, используя указанное имя столбца. |
| [DataColumn(String name, System.Data.DataTable table)](#DataColumn-java.lang.String-com.aspose.words.net.System.Data.DataTable) | Инициализирует новый экземпляр класса @\{link DataColumn\} используя указанное имя столбца и таблицу, к которой он принадлежит. |
| [DataColumn(String columnName, Class dataType)](#DataColumn-java.lang.String-java.lang.Class) | Инициализирует новый экземпляр класса [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) используя указанное имя столбца и тип данных. |
| [DataColumn(String name, Class type, System.Data.DataTable table)](#DataColumn-java.lang.String-java.lang.Class-com.aspose.words.net.System.Data.DataTable) | Инициализирует новый экземпляр класса [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) используя указанное имя столбца, тип данных и таблицу данных, к которой он принадлежит. |
## Методы

| Метод | Описание |
| --- | --- |
| [areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet)](#areColumnSetsTheSame-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn) |  |
| [getAllowDBNull()](#getAllowDBNull) | Возвращает значение, указывающее, разрешены ли null-значения в этом столбце для строк, принадлежащих таблице. |
| [getAutoIncrement()](#getAutoIncrement) | Возвращает значение, указывающее, автоматически ли столбец увеличивает значение столбца для новых строк, добавляемых в таблицу. |
| [getAutoIncrementSeed()](#getAutoIncrementSeed) | Возвращает начальное значение для столбца, у которого свойство [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) установлено в true. |
| [getAutoIncrementStep()](#getAutoIncrementStep) | Возвращает шаг увеличения, используемый столбцом, у которого свойство [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/daticolumn/\#setAutoIncrement-boolean) установлено в true. |
| [getCaption()](#getCaption) | Возвращает подпись столбца. |
| [getColumnMapping()](#getColumnMapping) | Возвращает [MappingType](../../com.aspose.words.net.system.data/mappingtype/) столбца. |
| [getColumnName()](#getColumnName) | Возвращает имя столбца в [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [getDataType()](#getDataType) | Возвращает тип данных, хранящихся в столбце. |
| [getDefaultValue()](#getDefaultValue) | Возвращает значение по умолчанию для столбца при создании новых строк. |
| [getExpression()](#getExpression) | Возвращает выражение, используемое для фильтрации строк, вычисления значений в столбце или создания агрегатного столбца. |
| [getMaxLength()](#getMaxLength) | Возвращает максимальную длину текстового столбца. |
| [getNamespace()](#getNamespace) | Возвращает пространство имён [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| [getOrdinal()](#getOrdinal) | Возвращает позицию столбца в коллекции [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [getPrefix()](#getPrefix) | Возвращает префикс XML, который является псевдонимом пространства имён [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [getReadOnly()](#getReadOnly) | Возвращает значение, указывающее, разрешает ли столбец изменения сразу после добавления строки в таблицу. |
| [getTable()](#getTable) | Возвращает [DataTable](../../com.aspose.words.net.system.data/datatable/), к которому принадлежит столбец. |
| [getUnique()](#getUnique) | Возвращает значение, указывающее, должны ли значения в каждой строке столбца быть уникальными. |
| [isReadOnly()](#isReadOnly) |  |
| [isUnique()](#isUnique) |  |
| [setAllowDBNull(boolean value)](#setAllowDBNull-boolean) | Устанавливает значение, указывающее, разрешены ли null‑значения в этом столбце для строк, принадлежащих таблице. |
| [setAutoIncrement(boolean value)](#setAutoIncrement-boolean) | Устанавливает значение, указывающее, автоматически ли столбец увеличивает значение столбца для новых строк, добавляемых в таблицу. |
| [setAutoIncrementSeed(long value)](#setAutoIncrementSeed-long) | Устанавливает начальное значение для столбца, у которого свойство [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) установлено в true. |
| [setAutoIncrementStep(long value)](#setAutoIncrementStep-long) | Устанавливает шаг увеличения, используемый столбцом, у которого свойство [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) установлено в true. |
| [setCaption(String value)](#setCaption-java.lang.String) | Устанавливает подпись столбца. |
| [setColumnMapping(int value)](#setColumnMapping-int) | Устанавливает [MappingType](../../com.aspose.words.net.system.data/mappingtype/) столбца. |
| [setColumnName(String value)](#setColumnName-java.lang.String) | Устанавливает имя столбца в [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [setDataType(Class value)](#setDataType-java.lang.Class) | Устанавливает тип данных, хранящихся в столбце. |
| [setDefaultValue(Object value)](#setDefaultValue-java.lang.Object) | Устанавливает значение по умолчанию для столбца при создании новых строк. |
| [setMaxLength(int value)](#setMaxLength-int) | Устанавливает максимальную длину текстового столбца. |
| [setNamespace(String value)](#setNamespace-java.lang.String) | Устанавливает пространство имён для [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| [setOrdinal(int ordinal)](#setOrdinal-int) | Изменяет порядковый номер или позицию [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) на указанный порядковый номер или позицию. |
| [setPrefix(String value)](#setPrefix-java.lang.String) | Устанавливает XML‑префикс, который является псевдонимом пространства имён [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [setReadOnly(boolean value)](#setReadOnly-boolean) | Устанавливает значение, указывающее, разрешены ли изменения столбца сразу после добавления строки в таблицу. |
| [setUnique(boolean value)](#setUnique-boolean) | Устанавливает значение, указывающее, должны ли значения в каждой строке столбца быть уникальными. |
| [toString()](#toString) | Получает [getExpression()](../../com.aspose.words.net.system.data/datacolumn/\#getExpression) столбца, если он существует. |
### DataColumn() {#DataColumn}
```
public DataColumn()
```


Инициализирует новый экземпляр класса [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) типа string.

### DataColumn(String columnName) {#DataColumn-java.lang.String}
```
public DataColumn(String columnName)
```


Инициализирует новый экземпляр класса [DataColumn](../../com.aspose.words.net.system.data/datacolumn/), типа string, используя указанное имя столбца.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| columnName | java.lang.String | Строка, представляющая имя создаваемого столбца. Если установить значение null или пустую строку (\"\"), при добавлении в коллекцию столбцов будет указано имя по умолчанию. |

### DataColumn(String name, System.Data.DataTable table) {#DataColumn-java.lang.String-com.aspose.words.net.System.Data.DataTable}
```
public DataColumn(String name, System.Data.DataTable table)
```


Инициализирует новый экземпляр класса @\{link DataColumn\} используя указанное имя столбца и таблицу, к которой он принадлежит.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | имя DataColumn |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | таблица, к которой принадлежит этот столбец |

### DataColumn(String columnName, Class dataType) {#DataColumn-java.lang.String-java.lang.Class}
```
public DataColumn(String columnName, Class dataType)
```


Инициализирует новый экземпляр класса [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) используя указанное имя столбца и тип данных.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| columnName | java.lang.String | Строка, представляющая имя создаваемого столбца. Если установить значение null или пустую строку (\"\"), при добавлении в коллекцию столбцов будет указано имя по умолчанию. |
| dataType | java.lang.Class | Поддерживается [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class). |

### DataColumn(String name, Class type, System.Data.DataTable table) {#DataColumn-java.lang.String-java.lang.Class-com.aspose.words.net.System.Data.DataTable}
```
public DataColumn(String name, Class type, System.Data.DataTable table)
```


Инициализирует новый экземпляр класса [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) используя указанное имя столбца, тип данных и таблицу данных, к которой он принадлежит.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | имя DataColumn |
| тип | java.lang.Class | тип данных |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | таблица, к которой принадлежит этот столбец |

### areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet) {#areColumnSetsTheSame-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn}
```
public static boolean areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| columnSet | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) |  |
| compareSet | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) |  |

**Returns:**
boolean
### getAllowDBNull() {#getAllowDBNull}
```
public boolean getAllowDBNull()
```


Возвращает значение, указывающее, разрешены ли null-значения в этом столбце для строк, принадлежащих таблице.

**Returns:**
boolean — true, если допускаются null‑значения; иначе false. По умолчанию true.
### getAutoIncrement() {#getAutoIncrement}
```
public boolean getAutoIncrement()
```


Возвращает значение, указывающее, автоматически ли столбец увеличивает значение столбца для новых строк, добавляемых в таблицу.

**Returns:**
boolean — true, если значение столбца увеличивается автоматически; иначе false. По умолчанию false.
### getAutoIncrementSeed() {#getAutoIncrementSeed}
```
public long getAutoIncrementSeed()
```


Возвращает начальное значение для столбца, у которого свойство [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) установлено в true.

**Returns:**
long — начальное значение для функции [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean).
### getAutoIncrementStep() {#getAutoIncrementStep}
```
public long getAutoIncrementStep()
```


Возвращает шаг увеличения, используемый столбцом, у которого свойство [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/daticolumn/\#setAutoIncrement-boolean) установлено в true.

**Returns:**
long — число, на которое значение столбца автоматически увеличивается. По умолчанию 1.
### getCaption() {#getCaption}
```
public String getCaption()
```


Возвращает подпись столбца.

**Returns:**
java.lang.String — подпись столбца. Если не задано, возвращает значение [getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String).
### getColumnMapping() {#getColumnMapping}
```
public int getColumnMapping()
```


Возвращает [MappingType](../../com.aspose.words.net.system.data/mappingtype/) столбца.

**Returns:**
int — одно из значений [MappingType](../../com.aspose.words.net.system.data/mappingtype/). Возвращаемое значение является одной из констант [MappingType](../../com.aspose.words.net.system.data/mappingtype/).
### getColumnName() {#getColumnName}
```
public String getColumnName()
```


Возвращает имя столбца в [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Returns:**
java.lang.String — имя столбца.
### getDataType() {#getDataType}
```
public Class getDataType()
```


Возвращает тип данных, хранящихся в столбце.

**Returns:**
java.lang.Class — объект java.lang.Class, представляющий тип данных столбца.
### getDefaultValue() {#getDefaultValue}
```
public Object getDefaultValue()
```


Возвращает значение по умолчанию для столбца при создании новых строк.

**Returns:**
java.lang.Object — значение, соответствующее [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class) столбца.
### getExpression() {#getExpression}
```
public String getExpression()
```


Возвращает выражение, используемое для фильтрации строк, вычисления значений в столбце или создания агрегатного столбца.

**Returns:**
java.lang.String — выражение для вычисления значения столбца или создания агрегатного столбца. Тип возвращаемого значения выражения определяется [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class) столбца.
### getMaxLength() {#getMaxLength}
```
public int getMaxLength()
```


Возвращает максимальную длину текстового столбца.

**Returns:**
int — максимальная длина столбца в символах. Если у столбца нет максимальной длины, значение равно -1 (по умолчанию).
### getNamespace() {#getNamespace}
```
public String getNamespace()
```


Возвращает пространство имён [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Returns:**
java.lang.String — пространство имён [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### getOrdinal() {#getOrdinal}
```
public int getOrdinal()
```


Возвращает позицию столбца в коллекции [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Returns:**
int — позиция столбца. Возвращает -1, если столбец не является членом коллекции.
### getPrefix() {#getPrefix}
```
public String getPrefix()
```


Возвращает префикс XML, который является псевдонимом пространства имён [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
java.lang.String — XML‑префикс для пространства имён [DataTable](../../com.aspose.words.net.system.data/datatable/).
### getReadOnly() {#getReadOnly}
```
public boolean getReadOnly()
```


Возвращает значение, указывающее, разрешает ли столбец изменения сразу после добавления строки в таблицу.

**Returns:**
boolean - true, если столбец только для чтения; иначе false. По умолчанию false.
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Возвращает [DataTable](../../com.aspose.words.net.system.data/datatable/), к которому принадлежит столбец.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The [DataTable](../../com.aspose.words.net.system.data/datatable/) that the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) belongs to.
### getUnique() {#getUnique}
```
public boolean getUnique()
```


Возвращает значение, указывающее, должны ли значения в каждой строке столбца быть уникальными.

**Returns:**
boolean - true, если значение должно быть уникальным; иначе false. По умолчанию false.
### isReadOnly() {#isReadOnly}
```
public boolean isReadOnly()
```




**Returns:**
boolean
### isUnique() {#isUnique}
```
public boolean isUnique()
```




**Returns:**
boolean
### setAllowDBNull(boolean value) {#setAllowDBNull-boolean}
```
public void setAllowDBNull(boolean value)
```


Устанавливает значение, указывающее, разрешены ли null‑значения в этом столбце для строк, принадлежащих таблице.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | true, если допускаются null‑значения; иначе false. По умолчанию true. |

### setAutoIncrement(boolean value) {#setAutoIncrement-boolean}
```
public void setAutoIncrement(boolean value)
```


Устанавливает значение, указывающее, автоматически ли столбец увеличивает значение столбца для новых строк, добавляемых в таблицу.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | true, если значение столбца увеличивается автоматически; иначе false. По умолчанию false. |

### setAutoIncrementSeed(long value) {#setAutoIncrementSeed-long}
```
public void setAutoIncrementSeed(long value)
```


Устанавливает начальное значение для столбца, у которого свойство [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) установлено в true.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | long | Начальное значение для функции [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean). |

### setAutoIncrementStep(long value) {#setAutoIncrementStep-long}
```
public void setAutoIncrementStep(long value)
```


Устанавливает шаг увеличения, используемый столбцом, у которого свойство [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) установлено в true.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | long | Число, на которое значение столбца автоматически увеличивается. По умолчанию 1. |

### setCaption(String value) {#setCaption-java.lang.String}
```
public void setCaption(String value)
```


Устанавливает подпись столбца.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Подпись столбца. Если не задано, возвращается значение [getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String). |

### setColumnMapping(int value) {#setColumnMapping-int}
```
public void setColumnMapping(int value)
```


Устанавливает [MappingType](../../com.aspose.words.net.system.data/mappingtype/) столбца.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Одно из значений [MappingType](../../com.aspose.words.net.system.data/mappingtype/). Значение должно быть одной из констант [MappingType](../../com.aspose.words.net.system.data/mappingtype/). |

### setColumnName(String value) {#setColumnName-java.lang.String}
```
public void setColumnName(String value)
```


Устанавливает имя столбца в [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Имя столбца. |

### setDataType(Class value) {#setDataType-java.lang.Class}
```
public void setDataType(Class value)
```


Устанавливает тип данных, хранящихся в столбце.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.Class | Объект java.lang.Class, представляющий тип данных столбца. |

### setDefaultValue(Object value) {#setDefaultValue-java.lang.Object}
```
public void setDefaultValue(Object value)
```


Устанавливает значение по умолчанию для столбца при создании новых строк.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.Object | Значение, соответствующее [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class). |

### setMaxLength(int value) {#setMaxLength-int}
```
public void setMaxLength(int value)
```


Устанавливает максимальную длину текстового столбца.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Максимальная длина столбца в символах. Если у столбца нет максимальной длины, значение равно -1 (по умолчанию). |

### setNamespace(String value) {#setNamespace-java.lang.String}
```
public void setNamespace(String value)
```


Устанавливает пространство имён для [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Пространство имён [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |

### setOrdinal(int ordinal) {#setOrdinal-int}
```
public void setOrdinal(int ordinal)
```


Изменяет порядковый номер или позицию [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) на указанный порядковый номер или позицию.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| порядковый | int | Указанный порядковый номер. |

### setPrefix(String value) {#setPrefix-java.lang.String}
```
public void setPrefix(String value)
```


Устанавливает XML‑префикс, который является псевдонимом пространства имён [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Префикс XML для пространства имён [DataTable](../../com.aspose.words.net.system.data/datatable/). |

### setReadOnly(boolean value) {#setReadOnly-boolean}
```
public void setReadOnly(boolean value)
```


Устанавливает значение, указывающее, разрешены ли изменения столбца сразу после добавления строки в таблицу.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | true, если столбец только для чтения; иначе false. По умолчанию false. |

### setUnique(boolean value) {#setUnique-boolean}
```
public void setUnique(boolean value)
```


Устанавливает значение, указывающее, должны ли значения в каждой строке столбца быть уникальными.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | true, если значение должно быть уникальным; иначе false. По умолчанию false. |

### toString() {#toString}
```
public String toString()
```


Получает [getExpression()](../../com.aspose.words.net.system.data/datacolumn/\#getExpression) столбца, если он существует.

**Returns:**
java.lang.String - значение [getExpression()](../../com.aspose.words.net.system.data/datacolumn/\#getExpression), если свойство установлено; иначе свойство [getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String).
