---
title: StyleCollection
second_title: Справочник по API Aspose.Words для Java
description: Коллекция объектов Style, представляющих как встроенные, так и определяемые пользователем стили в документе.
type: docs
weight: 537
url: /ru/java/com.aspose.words/stylecollection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable, java.lang.Iterable
```
public class StyleCollection implements Cloneable, Iterable
```

Коллекция объектов Style, представляющих как встроенные, так и определяемые пользователем стили в документе.

 Чтобы узнать больше, посетите**Working with Styles and Themes** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [add(int type, String name)](#add-int-java.lang.String-) |  |
| [addCopy(Style style)](#addCopy-com.aspose.words.Style-) | Копирует стиль в эту коллекцию. |
| [clearQuickStyleGallery()](#clearQuickStyleGallery--) | Удаляет все стили из панели «Галерея экспресс-стилей». |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | Получает стиль по индексу. |
| [get(String name)](#get-java.lang.String-) | Извлекает стиль из коллекции. |
| [getByStyleIdentifier(int sti)](#getByStyleIdentifier-int-) |  |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | Получает количество стилей в коллекции. |
| [getDefaultFont()](#getDefaultFont--) | Получает форматирование текста документа по умолчанию. |
| [getDefaultParagraphFormat()](#getDefaultParagraphFormat--) | Получает форматирование абзаца документа по умолчанию. |
| [getDocument()](#getDocument--) | Получает документ владельца. |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | Получает объект перечислителя, который будет перечислять стили в алфавитном порядке их имен. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(int type, String name) {#add-int-java.lang.String-}
```
public Style add(int type, String name)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| type | int |  |
| name | java.lang.String |  |

**Возвращает:**
[Style](../../com.aspose.words/style)
### addCopy(Style style) {#addCopy-com.aspose.words.Style-}
```
public Style addCopy(Style style)
```


Копирует стиль в эту коллекцию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| style | [Style](../../com.aspose.words/style) | Стиль для копирования. |

**Возвращает:**
[Style](../../com.aspose.words/style) - Скопированный стиль готов к использованию.

Копируемый стиль может принадлежать как одному, так и разным документам.

Связанный стиль копируется.

Этот метод не копирует базовые стили.

Если коллекция уже содержит стиль с таким именем, то новое имя генерируется автоматически путем добавления "\суффикс _number", начинающийся с 0, например, "Нормальный\_0", "Заголовок 1\ _1" и т. д. Используйте[Style.getName()](../../com.aspose.words/style\#getName--) / [Style.setName(java.lang.String)](../../com.aspose.words/style\#setName-java.lang.String-) setter для изменения имени импортированного стиля.
### clearQuickStyleGallery() {#clearQuickStyleGallery--}
```
public void clearQuickStyleGallery()
```


Удаляет все стили из панели «Галерея экспресс-стилей».

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
public Style get(int index)
```


Получает стиль по индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int |  |

**Возвращает:**
[Style](../../com.aspose.words/style) - Стиль по индексу.
### get(String name) {#get-java.lang.String-}
```
public Style get(String name)
```


Извлекает стиль из коллекции. Получает стиль по имени или псевдониму.

С учетом регистра, возвращает ноль, если стиль с заданным именем не найден.

Если это английское имя встроенного стиля, которого еще не существует, он создается автоматически.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String |  |

**Возвращает:**
[Style](../../com.aspose.words/style) - соответствующий[Style](../../com.aspose.words/style) ценность.
### getByStyleIdentifier(int sti) {#getByStyleIdentifier-int-}
```
public Style getByStyleIdentifier(int sti)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| sti | int |  |

**Возвращает:**
[Style](../../com.aspose.words/style)
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


Получает количество стилей в коллекции.

**Возвращает:**
int — количество стилей в коллекции.
### getDefaultFont() {#getDefaultFont--}
```
public Font getDefaultFont()
```


Получает форматирование текста документа по умолчанию.

 Обратите внимание, что значения по умолчанию для всего документа были введены в Microsoft Word 2007 и полностью поддерживаются в форматах OOXML ([LoadFormat.DOCX](../../com.aspose.words/loadformat\#DOCX)) Только. Более ранние форматы документов имеют ограниченную поддержку этой функции и могут сохранять только имена шрифтов.

**Возвращает:**
[Font](../../com.aspose.words/font) - Форматирование текста документа по умолчанию.
### getDefaultParagraphFormat() {#getDefaultParagraphFormat--}
```
public ParagraphFormat getDefaultParagraphFormat()
```


Получает форматирование абзаца документа по умолчанию.

 Обратите внимание, что значения по умолчанию для всего документа были введены в Microsoft Word 2007 и полностью поддерживаются в форматах OOXML ([LoadFormat.DOCX](../../com.aspose.words/loadformat\#DOCX)) Только. Более ранние форматы документов не поддерживают форматирование абзаца документа по умолчанию.

**Возвращает:**
[ParagraphFormat](../../com.aspose.words/paragraphformat) - Форматирование абзаца документа по умолчанию.
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


Получает документ владельца.

**Возвращает:**
[DocumentBase](../../com.aspose.words/documentbase) - Документ собственника.
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


Получает объект перечислителя, который будет перечислять стили в алфавитном порядке их имен.

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
