---
title: DataColumn
second_title: Справочник по API Aspose.Words для Java
description: Представляет схему столбца в .
type: docs
weight: 14
url: /ru/java/com.aspose.words.net.system.data/datacolumn/
---

**Наследование:**
java.lang.Object
```
public class DataColumn
```

 Представляет схему столбца в[DataTable](../../com.aspose.words.net.system.data/datatable).
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [DataColumn()](#DataColumn--) |  Инициализирует новый экземпляр[DataColumn](../../com.aspose.words.net.system.data/datacolumn) класс как тип строки. |
| [DataColumn(String columnName)](#DataColumn-java.lang.String-) |  Инициализирует новый экземпляр[DataColumn](../../com.aspose.words.net.system.data/datacolumn) class, как тип строки, используя указанное имя столбца. |
| [DataColumn(String name, System.Data.DataTable table)](#DataColumn-java.lang.String-com.aspose.words.net.System.Data.DataTable-) | Инициализирует новый экземпляр @\{ссылка на столбец данных\} класс, используя указанное имя столбца и таблицу, которой он принадлежит. |
| [DataColumn(String columnName, Class dataType)](#DataColumn-java.lang.String-java.lang.Class-) |  Инициализирует новый экземпляр[DataColumn](../../com.aspose.words.net.system.data/datacolumn) класс, используя указанное имя столбца и тип данных. |
| [DataColumn(String name, Class type, System.Data.DataTable table)](#DataColumn-java.lang.String-java.lang.Class-com.aspose.words.net.System.Data.DataTable-) |  Инициализирует новый экземпляр[DataColumn](../../com.aspose.words.net.system.data/datacolumn) класс, используя указанное имя столбца, тип данных и таблицу данных, к которой он принадлежит. |
## Методы

| Метод | Описание |
| --- | --- |
| [areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet)](#areColumnSetsTheSame-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn---) |  |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAllowDBNull()](#getAllowDBNull--) | Получает значение, указывающее, разрешены ли пустые значения в этом столбце для строк, принадлежащих таблице. |
| [getAutoIncrement()](#getAutoIncrement--) | Получает значение, указывающее, увеличивает ли столбец автоматически значение столбца для новых строк, добавленных в таблицу. |
| [getAutoIncrementSeed()](#getAutoIncrementSeed--) |  Получает начальное значение для столбца, имеющего[getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn\#getAutoIncrement--) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn\#setAutoIncrement-boolean-)свойство установлено в true. |
| [getAutoIncrementStep()](#getAutoIncrementStep--) |  Получает приращение, используемое столбцом с его[getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn\#getAutoIncrement--) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn\#setAutoIncrement-boolean-)свойство установлено в true. |
| [getCaption()](#getCaption--) | Получает заголовок столбца. |
| [getClass()](#getClass--) |  |
| [getColumnMapping()](#getColumnMapping--) |  Получает[MappingType](../../com.aspose.words.net.system.data/mappingtype) колонны. |
| [getColumnName()](#getColumnName--) |  Получает имя столбца в[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection). |
| [getDataType()](#getDataType--) | Получает тип данных, хранящихся в столбце. |
| [getDefaultValue()](#getDefaultValue--) | Получает значение по умолчанию для столбца при создании новых строк. |
| [getExpression()](#getExpression--) | Получает выражение, используемое для фильтрации строк, вычисления значений в столбце или создания статистического столбца. |
| [getMaxLength()](#getMaxLength--) | Получает максимальную длину текстового столбца. |
| [getNamespace()](#getNamespace--) |  Получает пространство имен[DataColumn](../../com.aspose.words.net.system.data/datacolumn). |
| [getOrdinal()](#getOrdinal--) |  Получает позицию столбца в[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection) коллекция. |
| [getPrefix()](#getPrefix--) |  Получает префикс XML, который является псевдонимом пространства имен[DataTable](../../com.aspose.words.net.system.data/datatable). |
| [getReadOnly()](#getReadOnly--) | Получает значение, указывающее, разрешены ли изменения в столбце после добавления строки в таблицу. |
| [getTable()](#getTable--) |  Получает[DataTable](../../com.aspose.words.net.system.data/datatable) которому принадлежит столбец. |
| [getUnique()](#getUnique--) | Получает значение, указывающее, должны ли значения в каждой строке столбца быть уникальными. |
| [hashCode()](#hashCode--) |  |
| [isReadOnly()](#isReadOnly--) |  |
| [isUnique()](#isUnique--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAllowDBNull(boolean value)](#setAllowDBNull-boolean-) | Задает значение, указывающее, разрешены ли нулевые значения в этом столбце для строк, принадлежащих таблице. |
| [setAutoIncrement(boolean value)](#setAutoIncrement-boolean-) | Задает значение, указывающее, увеличивает ли столбец автоматически значение столбца для новых строк, добавляемых в таблицу. |
| [setAutoIncrementSeed(long value)](#setAutoIncrementSeed-long-) |  Задает начальное значение для столбца, имеющего[getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn\#getAutoIncrement--) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn\#setAutoIncrement-boolean-)свойство установлено в true. |
| [setAutoIncrementStep(long value)](#setAutoIncrementStep-long-) |  Устанавливает приращение, используемое столбцом с его[getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn\#getAutoIncrement--) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn\#setAutoIncrement-boolean-)свойство установлено в true. |
| [setCaption(String value)](#setCaption-java.lang.String-) | Устанавливает заголовок для столбца. |
| [setColumnMapping(int value)](#setColumnMapping-int-) |  Устанавливает[MappingType](../../com.aspose.words.net.system.data/mappingtype) колонны. |
| [setColumnName(String value)](#setColumnName-java.lang.String-) |  Задает имя столбца в[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection). |
| [setDataType(Class value)](#setDataType-java.lang.Class-) | Задает тип данных, хранящихся в столбце. |
| [setDefaultValue(Object value)](#setDefaultValue-java.lang.Object-) | Задает значение по умолчанию для столбца при создании новых строк. |
| [setMaxLength(int value)](#setMaxLength-int-) | Устанавливает максимальную длину текстового столбца. |
| [setNamespace(String value)](#setNamespace-java.lang.String-) |  Задает пространство имен[DataColumn](../../com.aspose.words.net.system.data/datacolumn). |
| [setOrdinal(int ordinal)](#setOrdinal-int-) |  Изменяет порядковый номер или позицию[DataColumn](../../com.aspose.words.net.system.data/datacolumn) к указанному порядковому номеру или позиции. |
| [setPrefix(String value)](#setPrefix-java.lang.String-) |  Задает префикс XML, который является псевдонимом пространства имен[DataTable](../../com.aspose.words.net.system.data/datatable). |
| [setReadOnly(boolean value)](#setReadOnly-boolean-) | Задает значение, указывающее, разрешены ли изменения в столбце после добавления строки в таблицу. |
| [setUnique(boolean value)](#setUnique-boolean-) | Задает значение, указывающее, должны ли значения в каждой строке столбца быть уникальными. |
| [toString()](#toString--) |  Получает[getExpression()](../../com.aspose.words.net.system.data/datacolumn\#getExpression--) столбца, если он существует. |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DataColumn() {#DataColumn--}
```
public DataColumn()
```


 Инициализирует новый экземпляр[DataColumn](../../com.aspose.words.net.system.data/datacolumn) класс как тип строки.

### DataColumn(String columnName) {#DataColumn-java.lang.String-}
```
public DataColumn(String columnName)
```


 Инициализирует новый экземпляр[DataColumn](../../com.aspose.words.net.system.data/datacolumn) class, как тип строки, используя указанное имя столбца.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| columnName | java.lang.String | Строка, представляющая имя создаваемого столбца. Если задано значение null или пустая строка (""), при добавлении в коллекцию столбцов будет указано имя по умолчанию. |

### DataColumn(String name, System.Data.DataTable table) {#DataColumn-java.lang.String-com.aspose.words.net.System.Data.DataTable-}
```
public DataColumn(String name, System.Data.DataTable table)
```


Инициализирует новый экземпляр @\{ссылка на столбец данных\} класс, используя указанное имя столбца и таблицу, которой он принадлежит.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | имя столбца данных |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable) | таблица, которой принадлежит этот столбец |

### DataColumn(String columnName, Class dataType) {#DataColumn-java.lang.String-java.lang.Class-}
```
public DataColumn(String columnName, Class dataType)
```


 Инициализирует новый экземпляр[DataColumn](../../com.aspose.words.net.system.data/datacolumn) класс, используя указанное имя столбца и тип данных.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| columnName | java.lang.String | Строка, представляющая имя создаваемого столбца. Если задано значение null или пустая строка (""), при добавлении в коллекцию столбцов будет указано имя по умолчанию. |
| dataType | java.lang.Class |  Поддерживается[getDataType()](../../com.aspose.words.net.system.data/datacolumn\#getDataType--) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn\#setDataType-java.lang.Class-). |

### DataColumn(String name, Class type, System.Data.DataTable table) {#DataColumn-java.lang.String-java.lang.Class-com.aspose.words.net.System.Data.DataTable-}
```
public DataColumn(String name, Class type, System.Data.DataTable table)
```


 Инициализирует новый экземпляр[DataColumn](../../com.aspose.words.net.system.data/datacolumn) класс, используя указанное имя столбца, тип данных и таблицу данных, к которой он принадлежит.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | имя столбца данных |
| type | java.lang.Class | тип данных |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable) | таблица, которой принадлежит этот столбец |

### areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet) {#areColumnSetsTheSame-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn---}
```
public static boolean areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| columnSet | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn) |  |
| compareSet | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn) |  |

**Возвращает:**
логический
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Возвращает:**
логический
### getAllowDBNull() {#getAllowDBNull--}
```
public boolean getAllowDBNull()
```


Получает значение, указывающее, разрешены ли пустые значения в этом столбце для строк, принадлежащих таблице.

**Возвращает:**
boolean - true, если разрешены нулевые значения; в противном случае ложно. Значение по умолчанию верно.
### getAutoIncrement() {#getAutoIncrement--}
```
public boolean getAutoIncrement()
```


Получает значение, указывающее, увеличивает ли столбец автоматически значение столбца для новых строк, добавленных в таблицу.

**Возвращает:**
boolean - true, если значение столбца увеличивается автоматически; в противном случае ложно. Значение по умолчанию — ложь.
### getAutoIncrementSeed() {#getAutoIncrementSeed--}
```
public long getAutoIncrementSeed()
```


 Получает начальное значение для столбца, имеющего[getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn\#getAutoIncrement--) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn\#setAutoIncrement-boolean-)свойство установлено в true.

**Возвращает:**
 long - начальное значение для[getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn\#getAutoIncrement--) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn\#setAutoIncrement-boolean-) особенность.
### getAutoIncrementStep() {#getAutoIncrementStep--}
```
public long getAutoIncrementStep()
```


 Получает приращение, используемое столбцом с его[getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn\#getAutoIncrement--) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn\#setAutoIncrement-boolean-)свойство установлено в true.

**Возвращает:**
long — число, на которое автоматически увеличивается значение столбца. По умолчанию 1.
### getCaption() {#getCaption--}
```
public String getCaption()
```


Получает заголовок столбца.

**Возвращает:**
 java.lang.String — заголовок столбца. Если не установлено, возвращает[getColumnName()](../../com.aspose.words.net.system.data/datacolumn\#getColumnName--) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn\#setColumnName-java.lang.String-) ценность.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getColumnMapping() {#getColumnMapping--}
```
public int getColumnMapping()
```


 Получает[MappingType](../../com.aspose.words.net.system.data/mappingtype) колонны.

**Возвращает:**
 инт - один из[MappingType](../../com.aspose.words.net.system.data/mappingtype) ценности. Возвращаемое значение является одним из[MappingType](../../com.aspose.words.net.system.data/mappingtype) константы.
### getColumnName() {#getColumnName--}
```
public String getColumnName()
```


 Получает имя столбца в[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection).

**Возвращает:**
java.lang.String — имя столбца.
### getDataType() {#getDataType--}
```
public Class getDataType()
```


Получает тип данных, хранящихся в столбце.

**Возвращает:**
java.lang.Class — объект java.lang.Class, представляющий тип данных столбца.
### getDefaultValue() {#getDefaultValue--}
```
public Object getDefaultValue()
```


Получает значение по умолчанию для столбца при создании новых строк.

**Возвращает:**
 java.lang.Object — значение, соответствующее столбцу[getDataType()](../../com.aspose.words.net.system.data/datacolumn\#getDataType--) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn\#setDataType-java.lang.Class-).
### getExpression() {#getExpression--}
```
public String getExpression()
```


Получает выражение, используемое для фильтрации строк, вычисления значений в столбце или создания статистического столбца.

**Возвращает:**
java.lang.String — выражение для вычисления значения столбца или создания сводного столбца. Тип возвращаемого значения выражения определяется[getDataType()](../../com.aspose.words.net.system.data/datacolumn\#getDataType--) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn\#setDataType-java.lang.Class-) колонны.
### getMaxLength() {#getMaxLength--}
```
public int getMaxLength()
```


Получает максимальную длину текстового столбца.

**Возвращает:**
int — максимальная длина столбца в символах. Если столбец не имеет максимальной длины, значение равно -1 (по умолчанию).
### getNamespace() {#getNamespace--}
```
public String getNamespace()
```


 Получает пространство имен[DataColumn](../../com.aspose.words.net.system.data/datacolumn).

**Возвращает:**
 java.lang.String — пространство имен[DataColumn](../../com.aspose.words.net.system.data/datacolumn).
### getOrdinal() {#getOrdinal--}
```
public int getOrdinal()
```


 Получает позицию столбца в[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection) коллекция.

**Возвращает:**
int - Позиция столбца. Получает -1, если столбец не является членом коллекции.
### getPrefix() {#getPrefix--}
```
public String getPrefix()
```


 Получает префикс XML, который является псевдонимом пространства имен[DataTable](../../com.aspose.words.net.system.data/datatable).

**Возвращает:**
 java.lang.String — префикс XML для[DataTable](../../com.aspose.words.net.system.data/datatable) пространство имен.
### getReadOnly() {#getReadOnly--}
```
public boolean getReadOnly()
```


Получает значение, указывающее, разрешены ли изменения в столбце после добавления строки в таблицу.

**Возвращает:**
boolean - true, если столбец доступен только для чтения; в противном случае ложно. Значение по умолчанию — ложь.
### getTable() {#getTable--}
```
public System.Data.DataTable getTable()
```


 Получает[DataTable](../../com.aspose.words.net.system.data/datatable) которому принадлежит столбец.

**Возвращает:**
[DataTable](../../com.aspose.words.net.system.data/datatable) -[DataTable](../../com.aspose.words.net.system.data/datatable) что[DataColumn](../../com.aspose.words.net.system.data/datacolumn) принадлежит.
### getUnique() {#getUnique--}
```
public boolean getUnique()
```


Получает значение, указывающее, должны ли значения в каждой строке столбца быть уникальными.

**Возвращает:**
boolean - true, если значение должно быть уникальным; в противном случае ложно. Значение по умолчанию — ложь.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isReadOnly() {#isReadOnly--}
```
public boolean isReadOnly()
```




**Возвращает:**
логический
### isUnique() {#isUnique--}
```
public boolean isUnique()
```




**Возвращает:**
логический
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setAllowDBNull(boolean value) {#setAllowDBNull-boolean-}
```
public void setAllowDBNull(boolean value)
```


Задает значение, указывающее, разрешены ли нулевые значения в этом столбце для строк, принадлежащих таблице.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | true, если разрешены нулевые значения; в противном случае ложно. Значение по умолчанию верно. |

### setAutoIncrement(boolean value) {#setAutoIncrement-boolean-}
```
public void setAutoIncrement(boolean value)
```


Задает значение, указывающее, увеличивает ли столбец автоматически значение столбца для новых строк, добавляемых в таблицу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение true, если значение столбца увеличивается автоматически; в противном случае ложно. Значение по умолчанию — ложь. |

### setAutoIncrementSeed(long value) {#setAutoIncrementSeed-long-}
```
public void setAutoIncrementSeed(long value)
```


 Задает начальное значение для столбца, имеющего[getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn\#getAutoIncrement--) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn\#setAutoIncrement-boolean-)свойство установлено в true.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | long |  Начальное значение для[getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn\#getAutoIncrement--) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn\#setAutoIncrement-boolean-) особенность. |

### setAutoIncrementStep(long value) {#setAutoIncrementStep-long-}
```
public void setAutoIncrementStep(long value)
```


 Устанавливает приращение, используемое столбцом с его[getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn\#getAutoIncrement--) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn\#setAutoIncrement-boolean-)свойство установлено в true.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | long | Число, на которое автоматически увеличивается значение столбца. По умолчанию 1. |

### setCaption(String value) {#setCaption-java.lang.String-}
```
public void setCaption(String value)
```


Устанавливает заголовок для столбца.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Заголовок столбца. Если не установлено, возвращает[getColumnName()](../../com.aspose.words.net.system.data/datacolumn\#getColumnName--) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn\#setColumnName-java.lang.String-) ценность. |

### setColumnMapping(int value) {#setColumnMapping-int-}
```
public void setColumnMapping(int value)
```


 Устанавливает[MappingType](../../com.aspose.words.net.system.data/mappingtype) колонны.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Один из[MappingType](../../com.aspose.words.net.system.data/mappingtype) ценности. Значение должно быть одним из[MappingType](../../com.aspose.words.net.system.data/mappingtype) константы. |

### setColumnName(String value) {#setColumnName-java.lang.String-}
```
public void setColumnName(String value)
```


 Задает имя столбца в[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя столбца. |

### setDataType(Class value) {#setDataType-java.lang.Class-}
```
public void setDataType(Class value)
```


Задает тип данных, хранящихся в столбце.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.Class | Объект java.lang.Class, представляющий тип данных столбца. |

### setDefaultValue(Object value) {#setDefaultValue-java.lang.Object-}
```
public void setDefaultValue(Object value)
```


Задает значение по умолчанию для столбца при создании новых строк.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.Object |  Значение, соответствующее столбцу[getDataType()](../../com.aspose.words.net.system.data/datacolumn\#getDataType--) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn\#setDataType-java.lang.Class-). |

### setMaxLength(int value) {#setMaxLength-int-}
```
public void setMaxLength(int value)
```


Устанавливает максимальную длину текстового столбца.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Максимальная длина столбца в символах. Если столбец не имеет максимальной длины, значение равно -1 (по умолчанию). |

### setNamespace(String value) {#setNamespace-java.lang.String-}
```
public void setNamespace(String value)
```


 Задает пространство имен[DataColumn](../../com.aspose.words.net.system.data/datacolumn).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String |  Пространство имен[DataColumn](../../com.aspose.words.net.system.data/datacolumn). |

### setOrdinal(int ordinal) {#setOrdinal-int-}
```
public void setOrdinal(int ordinal)
```


 Изменяет порядковый номер или позицию[DataColumn](../../com.aspose.words.net.system.data/datacolumn) к указанному порядковому номеру или позиции.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| ordinal | int | Указанный порядковый номер. |

### setPrefix(String value) {#setPrefix-java.lang.String-}
```
public void setPrefix(String value)
```


 Задает префикс XML, который является псевдонимом пространства имен[DataTable](../../com.aspose.words.net.system.data/datatable).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String |  Префикс XML для[DataTable](../../com.aspose.words.net.system.data/datatable) пространство имен. |

### setReadOnly(boolean value) {#setReadOnly-boolean-}
```
public void setReadOnly(boolean value)
```


Задает значение, указывающее, разрешены ли изменения в столбце после добавления строки в таблицу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | true, если столбец доступен только для чтения; в противном случае ложно. Значение по умолчанию — ложь. |

### setUnique(boolean value) {#setUnique-boolean-}
```
public void setUnique(boolean value)
```


Задает значение, указывающее, должны ли значения в каждой строке столбца быть уникальными.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | true, если значение должно быть уникальным; в противном случае ложно. Значение по умолчанию — ложь. |

### toString() {#toString--}
```
public String toString()
```


 Получает[getExpression()](../../com.aspose.words.net.system.data/datacolumn\#getExpression--) столбца, если он существует.

**Возвращает:**
 java.lang.String —[getExpression()](../../com.aspose.words.net.system.data/datacolumn\#getExpression--) значение, если свойство установлено; в противном случае[getColumnName()](../../com.aspose.words.net.system.data/datacolumn\#getColumnName--) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn\#setColumnName-java.lang.String-) имущество.
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
