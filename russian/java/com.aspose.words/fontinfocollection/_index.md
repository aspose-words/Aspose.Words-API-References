---
title: FontInfoCollection
second_title: Справочник по API Aspose.Words для Java
description: Представляет набор шрифтов, используемых в документе.
type: docs
weight: 281
url: /ru/java/com.aspose.words/fontinfocollection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Iterable
```
public class FontInfoCollection implements Iterable
```

Представляет набор шрифтов, используемых в документе.

 Чтобы узнать больше, посетите**Working with Fonts** документальная статья.

 Предметы[FontInfo](../../com.aspose.words/fontinfo) объекты.

Вы не создаете экземпляры этого класса напрямую. Использовать[DocumentBase.getFontInfos()](../../com.aspose.words/documentbase\#getFontInfos--) свойство для доступа к коллекции шрифтов, определенных в документе.
## Методы

| Метод | Описание |
| --- | --- |
| [contains(String name)](#contains-java.lang.String-) | Определяет, содержит ли коллекция шрифт с заданным именем. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | Получает шрифт по указанному индексу. |
| [get(String name)](#get-java.lang.String-) | Предоставляет доступ к элементам коллекции. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | Получает количество элементов, содержащихся в коллекции. |
| [getEmbedSystemFonts()](#getEmbedSystemFonts--) | Указывает, следует ли внедрять системные шрифты в документ. |
| [getEmbedTrueTypeFonts()](#getEmbedTrueTypeFonts--) | Указывает, следует ли встраивать шрифты TrueType в документ при его сохранении. |
| [getSaveSubsetFonts()](#getSaveSubsetFonts--) | Указывает, следует ли сохранять вместе с документом подмножество встроенных шрифтов TrueType. |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | Возвращает объект итератора, который можно использовать для перебора всех элементов коллекции. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setEmbedSystemFonts(boolean value)](#setEmbedSystemFonts-boolean-) | Указывает, следует ли внедрять системные шрифты в документ. |
| [setEmbedTrueTypeFonts(boolean value)](#setEmbedTrueTypeFonts-boolean-) | Указывает, следует ли встраивать шрифты TrueType в документ при его сохранении. |
| [setSaveSubsetFonts(boolean value)](#setSaveSubsetFonts-boolean-) | Указывает, следует ли сохранять вместе с документом подмножество встроенных шрифтов TrueType. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### contains(String name) {#contains-java.lang.String-}
```
public boolean contains(String name)
```


Определяет, содержит ли коллекция шрифт с заданным именем.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Нечувствительное к регистру имя шрифта для поиска. |

**Возвращает:**
boolean — Истинно, если элемент найден в коллекции; в противном случае ложно.
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
### get(int index) {#get-int-}
```
public FontInfo get(int index)
```


Получает шрифт по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Отсчитываемый от нуля индекс шрифта. |

**Возвращает:**
[FontInfo](../../com.aspose.words/fontinfo) - Шрифт по указанному индексу.
### get(String name) {#get-java.lang.String-}
```
public FontInfo get(String name)
```


Предоставляет доступ к элементам коллекции. Получает шрифт с указанным именем.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Нечувствительное к регистру имя шрифта для поиска. |

**Возвращает:**
[FontInfo](../../com.aspose.words/fontinfo) - соответствующий[FontInfo](../../com.aspose.words/fontinfo) ценность.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getCount() {#getCount--}
```
public int getCount()
```


Получает количество элементов, содержащихся в коллекции.

**Возвращает:**
int - количество элементов, содержащихся в коллекции.
### getEmbedSystemFonts() {#getEmbedSystemFonts--}
```
public boolean getEmbedSystemFonts()
```


 Указывает, следует ли внедрять системные шрифты в документ. Значение по умолчанию для этого свойства**false**.

 Этот вариант работает только тогда, когда[getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrueTypeFonts--) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrueTypeFonts-boolean-) опция установлена на**true**.

Установка этого свойства в значение True полезна, если пользователь работает в восточноазиатской системе и хочет создать документ, который смогут прочитать другие пользователи, у которых нет шрифтов для этого языка в их системе. Например, пользователь японской системы может выбрать встраивание шрифтов в документ, чтобы японский документ можно было прочитать во всех системах.

Эта опция работает только для форматов DOC, DOCX и RTF.

**Возвращает:**
boolean - соответствующее логическое значение.
### getEmbedTrueTypeFonts() {#getEmbedTrueTypeFonts--}
```
public boolean getEmbedTrueTypeFonts()
```


Указывает, следует ли встраивать шрифты TrueType в документ при его сохранении. Значение по умолчанию для этого свойства**false**.

Внедрение шрифтов TrueType позволяет другим пользователям просматривать документ с теми же шрифтами, которые использовались при его создании, но может существенно увеличить размер документа.

Эта опция работает только для форматов DOC, DOCX и RTF.

**Возвращает:**
boolean - соответствующее логическое значение.
### getSaveSubsetFonts() {#getSaveSubsetFonts--}
```
public boolean getSaveSubsetFonts()
```


 Указывает, следует ли сохранять вместе с документом подмножество встроенных шрифтов TrueType. Значение по умолчанию для этого свойства**false**.

 Этот вариант работает только тогда, когда[getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrueTypeFonts--) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrueTypeFonts-boolean-) свойство установлено на**true**.

Эта опция работает только для форматов DOC, DOCX и RTF.

**Возвращает:**
boolean - соответствующее логическое значение.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### iterator() {#iterator--}
```
public Iterator iterator()
```


Возвращает объект итератора, который можно использовать для перебора всех элементов коллекции.

**Возвращает:**
java.util.Iterator
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setEmbedSystemFonts(boolean value) {#setEmbedSystemFonts-boolean-}
```
public void setEmbedSystemFonts(boolean value)
```


 Указывает, следует ли внедрять системные шрифты в документ. Значение по умолчанию для этого свойства**false**.

 Этот вариант работает только тогда, когда[getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrueTypeFonts--) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrueTypeFonts-boolean-) опция установлена на**true**.

Установка этого свойства в значение True полезна, если пользователь работает в восточноазиатской системе и хочет создать документ, который смогут прочитать другие пользователи, у которых нет шрифтов для этого языка в их системе. Например, пользователь японской системы может выбрать встраивание шрифтов в документ, чтобы японский документ можно было прочитать во всех системах.

Эта опция работает только для форматов DOC, DOCX и RTF.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setEmbedTrueTypeFonts(boolean value) {#setEmbedTrueTypeFonts-boolean-}
```
public void setEmbedTrueTypeFonts(boolean value)
```


Указывает, следует ли встраивать шрифты TrueType в документ при его сохранении. Значение по умолчанию для этого свойства**false**.

Внедрение шрифтов TrueType позволяет другим пользователям просматривать документ с теми же шрифтами, которые использовались при его создании, но может существенно увеличить размер документа.

Эта опция работает только для форматов DOC, DOCX и RTF.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setSaveSubsetFonts(boolean value) {#setSaveSubsetFonts-boolean-}
```
public void setSaveSubsetFonts(boolean value)
```


 Указывает, следует ли сохранять вместе с документом подмножество встроенных шрифтов TrueType. Значение по умолчанию для этого свойства**false**.

 Этот вариант работает только тогда, когда[getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrueTypeFonts--) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrueTypeFonts-boolean-) свойство установлено на**true**.

Эта опция работает только для форматов DOC, DOCX и RTF.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

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
