---
title: ListFormat
second_title: Справочник по API Aspose.Words для Java
description: Позволяет контролировать, какое форматирование списка применяется к абзацу.
type: docs
weight: 370
url: /ru/java/com.aspose.words/listformat/
---

**Наследование:**
java.lang.Object
```
public class ListFormat
```

Позволяет контролировать, какое форматирование списка применяется к абзацу.

 Чтобы узнать больше, посетите**Working with Lists** документальная статья.

Абзац в документе Microsoft Word может быть промаркирован или пронумерован. Когда абзац промаркирован или пронумерован, говорят, что к абзацу применяется форматирование списка.

 Вы не создаете объекты[ListFormat](../../com.aspose.words/listformat) класс напрямую. Вы получаете доступ[ListFormat](../../com.aspose.words/listformat) как свойство другого объекта, с которым может быть связано форматирование списка. На данный момент объекты, которые могут иметь форматирование списка:[Paragraph](../../com.aspose.words/paragraph), [Style](../../com.aspose.words/style) а также[DocumentBuilder](../../com.aspose.words/documentbuilder).

[ListFormat](../../com.aspose.words/listformat) из[Paragraph](../../com.aspose.words/paragraph)указывает, какое форматирование списка и уровень списка применяются к этому конкретному абзацу.

[ListFormat](../../com.aspose.words/listformat) из[Style](../../com.aspose.words/style) (применимо только к стилям абзаца) позволяет указать, какое форматирование списка и уровень списка применяются ко всем абзацам этого конкретного стиля.

[ListFormat](../../com.aspose.words/listformat) из[DocumentBuilder](../../com.aspose.words/documentbuilder) обеспечивает доступ к форматированию списка в текущей позиции курсора внутри[DocumentBuilder](../../com.aspose.words/documentbuilder).

 Само форматирование списка хранится внутри[List](../../com.aspose.words/list) объект, который хранится отдельно от абзацев. Объекты списка хранятся внутри[ListCollection](../../com.aspose.words/listcollection) коллекция. есть один[ListCollection](../../com.aspose.words/listcollection) сбор за[Document](../../com.aspose.words/document).

 Абзацы физически не принадлежат списку. Абзацы просто ссылаются на конкретный объект списка через[getList()](../../com.aspose.words/listformat\#getList--) / [setList(com.aspose.words.List)](../../com.aspose.words/listformat\#setList-com.aspose.words.List-) свойство и определенный уровень в списке через[getListLevelNumber()](../../com.aspose.words/listformat\#getListLevelNumber--) / [setListLevelNumber(int)](../../com.aspose.words/listformat\#setListLevelNumber-int-) имущество. Установив эти два свойства, вы определяете, какие маркеры и нумерация применяются к абзацу.
## Методы

| Метод | Описание |
| --- | --- |
| [applyBulletDefault()](#applyBulletDefault--) | Запускает новый маркированный список по умолчанию и применяет его к абзацу. |
| [applyNumberDefault()](#applyNumberDefault--) | Запускает новый нумерованный список по умолчанию и применяет его к абзацу. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getList()](#getList--) | Получает список, членом которого является этот абзац. |
| [getListLevel()](#getListLevel--) | Возвращает форматирование на уровне списка плюс любые переопределения форматирования, примененные к текущему абзацу. |
| [getListLevelNumber()](#getListLevelNumber--) | Получает номер уровня списка (от 0 до 8) для абзаца. |
| [hashCode()](#hashCode--) |  |
| [isListItem()](#isListItem--) | Истинно, если к абзацу применено маркированное или нумерованное форматирование. |
| [listIndent()](#listIndent--) | Увеличивает уровень списка текущего абзаца на один уровень. |
| [listOutdent()](#listOutdent--) | Уменьшает уровень списка текущего абзаца на один уровень. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [removeNumbers()](#removeNumbers--) | Удаляет числа или маркеры из текущего абзаца и устанавливает нулевой уровень списка. |
| [setList(List value)](#setList-com.aspose.words.List-) | Устанавливает список, членом которого является этот абзац. |
| [setListLevelNumber(int value)](#setListLevelNumber-int-) | Задает номер уровня списка (от 0 до 8) для абзаца. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### applyBulletDefault() {#applyBulletDefault--}
```
public void applyBulletDefault()
```


Запускает новый маркированный список по умолчанию и применяет его к абзацу.

Это метод быстрого доступа, который создает новый список с использованием маркированного шаблона по умолчанию, применяет его к абзацу и выбирает 1-й уровень списка.

### applyNumberDefault() {#applyNumberDefault--}
```
public void applyNumberDefault()
```


Запускает новый нумерованный список по умолчанию и применяет его к абзацу.

Это метод быстрого доступа, который создает новый список с использованием нумерованного шаблона по умолчанию, применяет его к абзацу и выбирает 1-й уровень списка.

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
### getList() {#getList--}
```
public List getList()
```


Получает список, членом которого является этот абзац.

Список, который назначается этому свойству, должен принадлежать текущему документу.

Список, назначаемый этому свойству, не должен быть определением стиля списка.

 Присвоение этому свойству значения null удаляет маркеры и нумерацию из абзаца и устанавливает номер уровня списка равным нулю. Установка для этого свойства значения null эквивалентна вызову[removeNumbers()](../../com.aspose.words/listformat\#removeNumbers--).

**Возвращает:**
[List](../../com.aspose.words/list) - Список, членом которого является этот абзац.
### getListLevel() {#getListLevel--}
```
public ListLevel getListLevel()
```


Возвращает форматирование на уровне списка плюс любые переопределения форматирования, примененные к текущему абзацу.

**Возвращает:**
[ListLevel](../../com.aspose.words/listlevel) - Форматирование на уровне списка плюс любые переопределения форматирования применяются к текущему абзацу.
### getListLevelNumber() {#getListLevelNumber--}
```
public int getListLevelNumber()
```


Получает номер уровня списка (от 0 до 8) для абзаца.

В документах Word списки могут состоять из 1 или 9 уровней, пронумерованных от 0 до 8.

 Имеет эффект только при[getList()](../../com.aspose.words/listformat\#getList--) / [setList(com.aspose.words.List)](../../com.aspose.words/listformat\#setList-com.aspose.words.List-) свойство установлено для ссылки на допустимый список.

**Возвращает:**
int — номер уровня списка (от 0 до 8) для абзаца.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isListItem() {#isListItem--}
```
public boolean isListItem()
```


Истинно, если к абзацу применено маркированное или нумерованное форматирование.

**Возвращает:**
boolean - соответствующее логическое значение.
### listIndent() {#listIndent--}
```
public void listIndent()
```


Увеличивает уровень списка текущего абзаца на один уровень.

Этот метод изменяет уровень списка и применяет свойства форматирования нового уровня.

В документах Word списки могут состоять из девяти уровней. Форматирование списка для каждого уровня указывает, какой маркер или номер используется, левый отступ, пробел между маркером и текстом и т. д.

### listOutdent() {#listOutdent--}
```
public void listOutdent()
```


Уменьшает уровень списка текущего абзаца на один уровень.

Этот метод изменяет уровень списка и применяет свойства форматирования нового уровня.

В документах Word списки могут состоять из девяти уровней. Форматирование списка для каждого уровня указывает, какой маркер или номер используется, левый отступ, пробел между маркером и текстом и т. д.

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### removeNumbers() {#removeNumbers--}
```
public void removeNumbers()
```


Удаляет числа или маркеры из текущего абзаца и устанавливает нулевой уровень списка.

Вызов этого метода эквивалентен установке[getList()](../../com.aspose.words/listformat\#getList--) / [setList(com.aspose.words.List)](../../com.aspose.words/listformat\#setList-com.aspose.words.List-) свойство в ноль.

### setList(List value) {#setList-com.aspose.words.List-}
```
public void setList(List value)
```


Устанавливает список, членом которого является этот абзац.

Список, который назначается этому свойству, должен принадлежать текущему документу.

Список, назначаемый этому свойству, не должен быть определением стиля списка.

 Присвоение этому свойству значения null удаляет маркеры и нумерацию из абзаца и устанавливает номер уровня списка равным нулю. Установка для этого свойства значения null эквивалентна вызову[removeNumbers()](../../com.aspose.words/listformat\#removeNumbers--).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [List](../../com.aspose.words/list) | Список, в который входит этот абзац. |

### setListLevelNumber(int value) {#setListLevelNumber-int-}
```
public void setListLevelNumber(int value)
```


Задает номер уровня списка (от 0 до 8) для абзаца.

В документах Word списки могут состоять из 1 или 9 уровней, пронумерованных от 0 до 8.

 Имеет эффект только при[getList()](../../com.aspose.words/listformat\#getList--) / [setList(com.aspose.words.List)](../../com.aspose.words/listformat\#setList-com.aspose.words.List-) свойство установлено для ссылки на допустимый список.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Номер уровня списка (от 0 до 8) для абзаца. |

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
