---
title: "OdsoFieldMapData"
linktitle: "OdsoFieldMapData"
second_title: "Aspose.Words для Java"
description: "Указывает, как столбец во внешнем источнике данных должен быть сопоставлен с предопределёнными полями слияния в документе на Java."
type: docs
weight: 489
url: /ru/java/com.aspose.words/odsofieldmapdata/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class OdsoFieldMapData implements Cloneable
```

Указывает, как столбец во внешнем источнике данных будет сопоставлен с предопределёнными полями слияния в документе.

Чтобы узнать больше, посетите статью документации [ Mail Merge and Reporting ][Mail Merge and Reporting].

 **Remarks:** 

Microsoft Word предоставляет некоторые предопределённые имена полей слияния, которые можно вставлять в документ как MERGEFIELD или использовать в полях ADDRESSBLOCK или GREETINGLINE. Информация, указанная в [OdsoFieldMapData](../../com.aspose.words/odsofieldmapdata/), позволяет сопоставить один столбец во внешнем источнике данных с одним предопределённым полем слияния.


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Методы

| Метод | Описание |
| --- | --- |
| [deepClone()](#deepClone) | Возвращает глубокую копию этого объекта. |
| [getColumn()](#getColumn) | Указывает нулевой индекс столбца во внешнем источнике данных, который должен быть сопоставлен с локальным именем конкретного поля MERGEFIELD. |
| [getMappedName()](#getMappedName) | Указывает предопределённое имя поля слияния, которое должно быть сопоставлено с номером столбца, указанным свойством [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) в этом сопоставлении полей. |
| [getName()](#getName) | Указывает имя столбца во внешнем источнике данных для столбца, индекс которого указан свойством [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int). |
| [getType()](#getType) | Указывает, сопоставлено ли данное поле слияния с колонкой во внешнем источнике данных. |
| [setColumn(int value)](#setColumn-int) | Указывает нулевой индекс столбца во внешнем источнике данных, который должен быть сопоставлен с локальным именем конкретного поля MERGEFIELD. |
| [setMappedName(String value)](#setMappedName-java.lang.String) | Указывает предопределённое имя поля слияния, которое должно быть сопоставлено с номером столбца, указанным свойством [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) в этом сопоставлении полей. |
| [setName(String value)](#setName-java.lang.String) | Указывает имя столбца во внешнем источнике данных для столбца, индекс которого указан свойством [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int). |
| [setType(int value)](#setType-int) | Указывает, сопоставлено ли данное поле слияния с колонкой во внешнем источнике данных. |
### deepClone() {#deepClone}
```
public OdsoFieldMapData deepClone()
```


Возвращает глубокую копию этого объекта.

**Returns:**
[OdsoFieldMapData](../../com.aspose.words/odsofieldmapdata/)
### getColumn() {#getColumn}
```
public int getColumn()
```


Указывает нулевой индекс столбца во внешнем источнике данных, который должен быть сопоставлен с локальным именем конкретного поля MERGEFIELD. Значение по умолчанию — 0.

**Returns:**
int — соответствующее значение  int .
### getMappedName() {#getMappedName}
```
public String getMappedName()
```


Указывает предопределённое имя поля слияния, которое должно быть сопоставлено с номером столбца, указанным свойством [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) в этом сопоставлении полей. Значение по умолчанию — пустая строка.

**Returns:**
java.lang.String - Соответствующее значение java.lang.String.
### getName() {#getName}
```
public String getName()
```


Указывает имя столбца во внешнем источнике данных для столбца, индекс которого указан свойством [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int). Значение по умолчанию — пустая строка.

**Returns:**
java.lang.String - Соответствующее значение java.lang.String.
### getType() {#getType}
```
public int getType()
```


Указывает, сопоставлено ли данное поле слияния с колонкой во внешнем источнике данных. Значение по умолчанию — [OdsoFieldMappingType.DEFAULT](../../com.aspose.words/odsofieldmappingtype/\#DEFAULT).

**Returns:**
int — соответствующее значение типа int. Возвращаемое значение является одним из констант [OdsoFieldMappingType](../../com.aspose.words/odsofieldmappingtype/).
### setColumn(int value) {#setColumn-int}
```
public void setColumn(int value)
```


Указывает нулевой индекс столбца во внешнем источнике данных, который должен быть сопоставлен с локальным именем конкретного поля MERGEFIELD. Значение по умолчанию — 0.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Соответствующее  int  значение. |

### setMappedName(String value) {#setMappedName-java.lang.String}
```
public void setMappedName(String value)
```


Указывает предопределённое имя поля слияния, которое должно быть сопоставлено с номером столбца, указанным свойством [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) в этом сопоставлении полей. Значение по умолчанию — пустая строка.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Соответствующее значение java.lang.String. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Указывает имя столбца во внешнем источнике данных для столбца, индекс которого указан свойством [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int). Значение по умолчанию — пустая строка.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Соответствующее значение java.lang.String. |

### setType(int value) {#setType-int}
```
public void setType(int value)
```


Указывает, сопоставлено ли данное поле слияния с колонкой во внешнем источнике данных. Значение по умолчанию — [OdsoFieldMappingType.DEFAULT](../../com.aspose.words/odsofieldmappingtype/\#DEFAULT).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее значение типа int. Значение должно быть одним из констант [OdsoFieldMappingType](../../com.aspose.words/odsofieldmappingtype/). |

