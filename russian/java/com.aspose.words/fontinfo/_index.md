---
title: FontInfo
second_title: Справочник по API Aspose.Words для Java
description: Задает информацию о шрифте, используемом в документе.
type: docs
weight: 280
url: /ru/java/com.aspose.words/fontinfo/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class FontInfo implements Cloneable
```

Задает информацию о шрифте, используемом в документе.

 Чтобы узнать больше, посетите**Working with Fonts** документальная статья.

Вы не создаете экземпляры этого класса напрямую. Использовать[DocumentBase.getFontInfos()](../../com.aspose.words/documentbase\#getFontInfos--) для доступа к коллекции шрифтов, определенных в документе.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAltName()](#getAltName--) | Получает альтернативное имя шрифта. |
| [getCharset()](#getCharset--) | Получает набор символов для шрифта. |
| [getClass()](#getClass--) |  |
| [getEmbeddedFont(int format, int style)](#getEmbeddedFont-int-int-) |  |
| [getEmbeddedFontAsOpenType(int style)](#getEmbeddedFontAsOpenType-int-) |  |
| [getFamily()](#getFamily--) | Получает семейство шрифтов, к которому принадлежит этот шрифт. |
| [getName()](#getName--) | Получает имя шрифта. |
| [getPanose()](#getPanose--) | Получает классификационный номер шрифта PANOSE. |
| [getPitch()](#getPitch--) | Шаг указывает, является ли шрифт фиксированным шагом, пропорционально расположенным или зависит от настройки по умолчанию. |
| [hashCode()](#hashCode--) |  |
| [isTrueType()](#isTrueType--) | Указывает, что этот шрифт является шрифтом TrueType или OpenType, а не растровым или векторным шрифтом. |
| [isTrueType(boolean value)](#isTrueType-boolean-) | Указывает, что этот шрифт является шрифтом TrueType или OpenType, а не растровым или векторным шрифтом. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAltName(String value)](#setAltName-java.lang.String-) | Устанавливает альтернативное имя для шрифта. |
| [setCharset(int value)](#setCharset-int-) | Устанавливает набор символов для шрифта. |
| [setFamily(int value)](#setFamily-int-) | Устанавливает семейство шрифтов, к которому принадлежит этот шрифт. |
| [setPanose(byte[] value)](#setPanose-byte---) | Устанавливает классификационный номер шрифта PANOSE. |
| [setPitch(int value)](#setPitch-int-) | Шаг указывает, является ли шрифт фиксированным шагом, пропорционально расположенным или зависит от настройки по умолчанию. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
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
### getAltName() {#getAltName--}
```
public String getAltName()
```


Получает альтернативное имя шрифта.

Не может быть нулевым. Может быть пустой строкой.

**Возвращает:**
java.lang.String — альтернативное имя шрифта.
### getCharset() {#getCharset--}
```
public int getCharset()
```


Получает набор символов для шрифта.

**Возвращает:**
int — набор символов для шрифта.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getEmbeddedFont(int format, int style) {#getEmbeddedFont-int-int-}
```
public byte[] getEmbeddedFont(int format, int style)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| format | int |  |
| style | int |  |

**Возвращает:**
байт[]
### getEmbeddedFontAsOpenType(int style) {#getEmbeddedFontAsOpenType-int-}
```
public byte[] getEmbeddedFontAsOpenType(int style)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| style | int |  |

**Возвращает:**
байт[]
### getFamily() {#getFamily--}
```
public int getFamily()
```


Получает семейство шрифтов, к которому принадлежит этот шрифт.

**Возвращает:**
 int — семейство шрифтов, к которому принадлежит этот шрифт. Возвращаемое значение является одним из[FontFamily](../../com.aspose.words/fontfamily) константы.
### getName() {#getName--}
```
public String getName()
```


Получает имя шрифта.

Не может быть нулевым. Может быть пустой строкой.

**Возвращает:**
java.lang.String — Имя шрифта.
### getPanose() {#getPanose--}
```
public byte[] getPanose()
```


Получает классификационный номер шрифта PANOSE.

PANOSE — это компактное 10-байтовое описание важнейших визуальных характеристик шрифта, таких как контрастность, насыщенность и стиль с засечками. Цифры обозначают вид семейства, стиль засечек, толщину, пропорцию, контраст, вариацию штриха, стиль руки, форму буквы, среднюю линию и высоту по оси X.

Может быть нулевым.

**Возвращает:**
байт[] - Классификационный номер шрифта PANOSE.
### getPitch() {#getPitch--}
```
public int getPitch()
```


Шаг указывает, является ли шрифт фиксированным шагом, пропорционально расположенным или зависит от настройки по умолчанию.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[FontPitch](../../com.aspose.words/fontpitch) константы.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isTrueType() {#isTrueType--}
```
public boolean isTrueType()
```


Указывает, что этот шрифт является шрифтом TrueType или OpenType, а не растровым или векторным шрифтом. Значение по умолчанию верно.

**Возвращает:**
boolean - соответствующее логическое значение.
### isTrueType(boolean value) {#isTrueType-boolean-}
```
public void isTrueType(boolean value)
```


Указывает, что этот шрифт является шрифтом TrueType или OpenType, а не растровым или векторным шрифтом. Значение по умолчанию верно.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setAltName(String value) {#setAltName-java.lang.String-}
```
public void setAltName(String value)
```


Устанавливает альтернативное имя для шрифта.

Не может быть нулевым. Может быть пустой строкой.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Альтернативное имя шрифта. |

### setCharset(int value) {#setCharset-int-}
```
public void setCharset(int value)
```


Устанавливает набор символов для шрифта.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Набор символов для шрифта. |

### setFamily(int value) {#setFamily-int-}
```
public void setFamily(int value)
```


Устанавливает семейство шрифтов, к которому принадлежит этот шрифт.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Семейство шрифтов, к которому принадлежит этот шрифт. Значение должно быть одним из[FontFamily](../../com.aspose.words/fontfamily) константы. |

### setPanose(byte[] value) {#setPanose-byte---}
```
public void setPanose(byte[] value)
```


Устанавливает классификационный номер шрифта PANOSE.

PANOSE — это компактное 10-байтовое описание важнейших визуальных характеристик шрифта, таких как контрастность, насыщенность и стиль с засечками. Цифры обозначают вид семейства, стиль засечек, толщину, пропорцию, контраст, вариацию штриха, стиль руки, форму буквы, среднюю линию и высоту по оси X.

Может быть нулевым.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | byte[] | Классификационный номер шрифта PANOSE. |

### setPitch(int value) {#setPitch-int-}
```
public void setPitch(int value)
```


Шаг указывает, является ли шрифт фиксированным шагом, пропорционально расположенным или зависит от настройки по умолчанию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[FontPitch](../../com.aspose.words/fontpitch) константы. |

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
