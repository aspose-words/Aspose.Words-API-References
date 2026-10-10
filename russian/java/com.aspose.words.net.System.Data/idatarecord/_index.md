---
title: "IDataRecord"
linktitle: "IDataRecord"
second_title: "Aspose.Words для Java"
description: "Обеспечивает доступ к значениям столбцов в каждой строке для DataReader и реализуется поставщиками данных .NET Framework, которые работают с реляционными базами данных в Java."
type: docs
weight: 35
url: /ru/java/com.aspose.words.net.system.data/idatarecord/
---
```
public interface IDataRecord
```

Обеспечивает доступ к значениям столбцов в каждой строке DataReader и реализуется поставщиками данных .NET Framework, работающими с реляционными базами данных.
## Методы

| Метод | Описание |
| --- | --- |
| [get(int i)](#get-int) | Получает столбец, расположенный по указанному индексу. |
| [getFieldCount()](#getFieldCount) | Получает количество столбцов в текущей строке. |
| [getFieldType(int i)](#getFieldType-int) | Получает информацию java.lang.Class, соответствующую типу java.lang.Object, который будет возвращён из [getValue(int)](../../com.aspose.words.net.system.data/idatarecord/\#getValue-int). |
| [getName(int i)](#getName-int) | Получает имя поля для поиска. |
| [getValue(int i)](#getValue-int) | Возвращает значение указанного поля. |
### get(int i) {#get-int}
```
public abstract Object get(int i)
```


Получает столбец, расположенный по указанному индексу.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| i | int | Нулевой (начиная с нуля) индекс столбца для получения. |

**Returns:**
java.lang.Object — Столбец, расположенный по указанному индексу, в виде java.lang.Object.
### getFieldCount() {#getFieldCount}
```
public abstract int getFieldCount()
```


Получает количество столбцов в текущей строке.

**Returns:**
int — Когда не находится в действительном наборе записей, 0; в противном случае — количество столбцов в текущей записи. По умолчанию — -1.
### getFieldType(int i) {#getFieldType-int}
```
public abstract Class getFieldType(int i)
```


Получает информацию java.lang.Class, соответствующую типу java.lang.Object, который будет возвращён из [getValue(int)](../../com.aspose.words.net.system.data/idatarecord/\#getValue-int).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| i | int | Индекс поля для поиска. |

**Returns:**
java.lang.Class — Информация java.lang.Class, соответствующая типу java.lang.Object, который будет возвращён из [getValue(int)](../../com.aspose.words.net.system.data/idatarecord/\#getValue-int).
### getName(int i) {#getName-int}
```
public abstract String getName(int i)
```


Получает имя поля для поиска.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| i | int | Индекс поля для поиска. |

**Returns:**
java.lang.String — Имя поля или пустая строка (""), если нет значения для возврата.
### getValue(int i) {#getValue-int}
```
public abstract Object getValue(int i)
```


Возвращает значение указанного поля.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| i | int | Индекс поля для поиска. |

**Returns:**
java.lang.Object — Объект java.lang.Object, который будет содержать значение поля при возврате.
