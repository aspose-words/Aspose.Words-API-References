---
title: OdsoFieldMapData
second_title: Справочник по API Aspose.Words для Java
description: Указывает, как столбец во внешнем источнике данных должен быть сопоставлен с предопределенными полями слияния в документе.
type: docs
weight: 413
url: /ru/java/com.aspose.words/odsofieldmapdata/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class OdsoFieldMapData implements Cloneable
```

Указывает, как столбец во внешнем источнике данных должен быть сопоставлен с предопределенными полями слияния в документе.

 Чтобы узнать больше, посетите**Mail Merge and Reporting** документальная статья.

 Microsoft Word предоставляет некоторые предопределенные имена полей слияния, которые он позволяет вставлять в документ как MERGEFIELD или использовать в полях ADDRESSBLOCK или GREETINGLINE. Информация, указанная в[OdsoFieldMapData](../../com.aspose.words/odsofieldmapdata)позволяет сопоставить один столбец внешнего источника данных с одним предопределенным полем слияния.
## Методы

| Метод | Описание |
| --- | --- |
| [deepClone()](#deepClone--) | Возвращает глубокий клон этого объекта. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getColumn()](#getColumn--) | Задает отсчитываемый от нуля индекс столбца во внешнем источнике данных, который должен быть сопоставлен с локальным именем определенного поля MERGEFIELD. |
| [getMappedName()](#getMappedName--) |  Указывает предопределенное имя поля слияния, которое должно быть сопоставлено с номером столбца, указанным[getColumn()](../../com.aspose.words/odsofieldmapdata\#getColumn--) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata\#setColumn-int-) свойство в этом сопоставлении полей. |
| [getName()](#getName--) |  Задает имя столбца во внешнем источнике данных для столбца, индекс которого указан параметром[getColumn()](../../com.aspose.words/odsofieldmapdata\#getColumn--) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata\#setColumn-int-) имущество. |
| [getType()](#getType--) | Указывает, сопоставлено ли данное поле слияния со столбцом в данном внешнем источнике данных или нет. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setColumn(int value)](#setColumn-int-) | Задает отсчитываемый от нуля индекс столбца во внешнем источнике данных, который должен быть сопоставлен с локальным именем определенного поля MERGEFIELD. |
| [setMappedName(String value)](#setMappedName-java.lang.String-) |  Указывает предопределенное имя поля слияния, которое должно быть сопоставлено с номером столбца, указанным[getColumn()](../../com.aspose.words/odsofieldmapdata\#getColumn--) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata\#setColumn-int-) свойство в этом сопоставлении полей. |
| [setName(String value)](#setName-java.lang.String-) |  Задает имя столбца во внешнем источнике данных для столбца, индекс которого указан параметром[getColumn()](../../com.aspose.words/odsofieldmapdata\#getColumn--) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata\#setColumn-int-) имущество. |
| [setType(int value)](#setType-int-) | Указывает, сопоставлено ли данное поле слияния со столбцом в данном внешнем источнике данных или нет. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### deepClone() {#deepClone--}
```
public OdsoFieldMapData deepClone()
```


Возвращает глубокий клон этого объекта.

**Возвращает:**
[OdsoFieldMapData](../../com.aspose.words/odsofieldmapdata)
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getColumn() {#getColumn--}
```
public int getColumn()
```


Задает отсчитываемый от нуля индекс столбца во внешнем источнике данных, который должен быть сопоставлен с локальным именем определенного поля MERGEFIELD. Значение по умолчанию — 0.

**Возвращает:**
int - соответствующее значение int.
### getMappedName() {#getMappedName--}
```
public String getMappedName()
```


 Указывает предопределенное имя поля слияния, которое должно быть сопоставлено с номером столбца, указанным[getColumn()](../../com.aspose.words/odsofieldmapdata\#getColumn--) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata\#setColumn-int-) свойство в этом сопоставлении полей. Значение по умолчанию — пустая строка.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getName() {#getName--}
```
public String getName()
```


 Задает имя столбца во внешнем источнике данных для столбца, индекс которого указан параметром[getColumn()](../../com.aspose.words/odsofieldmapdata\#getColumn--) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata\#setColumn-int-) имущество. Значение по умолчанию — пустая строка.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getType() {#getType--}
```
public int getType()
```


Указывает, сопоставлено ли данное поле слияния со столбцом в данном внешнем источнике данных или нет. Значение по умолчанию[OdsoFieldMappingType.DEFAULT](../../com.aspose.words/odsofieldmappingtype\#DEFAULT).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[OdsoFieldMappingType](../../com.aspose.words/odsofieldmappingtype) константы.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setColumn(int value) {#setColumn-int-}
```
public void setColumn(int value)
```


Задает отсчитываемый от нуля индекс столбца во внешнем источнике данных, который должен быть сопоставлен с локальным именем определенного поля MERGEFIELD. Значение по умолчанию — 0.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

### setMappedName(String value) {#setMappedName-java.lang.String-}
```
public void setMappedName(String value)
```


 Указывает предопределенное имя поля слияния, которое должно быть сопоставлено с номером столбца, указанным[getColumn()](../../com.aspose.words/odsofieldmapdata\#getColumn--) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata\#setColumn-int-) свойство в этом сопоставлении полей. Значение по умолчанию — пустая строка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


 Задает имя столбца во внешнем источнике данных для столбца, индекс которого указан параметром[getColumn()](../../com.aspose.words/odsofieldmapdata\#getColumn--) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata\#setColumn-int-) имущество. Значение по умолчанию — пустая строка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setType(int value) {#setType-int-}
```
public void setType(int value)
```


Указывает, сопоставлено ли данное поле слияния со столбцом в данном внешнем источнике данных или нет. Значение по умолчанию[OdsoFieldMappingType.DEFAULT](../../com.aspose.words/odsofieldmappingtype\#DEFAULT).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[OdsoFieldMappingType](../../com.aspose.words/odsofieldmappingtype) константы. |

### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
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
