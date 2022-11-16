---
title: List
second_title: Справочник по API Aspose.Words для Java
description: Представляет форматирование списка.
type: docs
weight: 368
url: /ru/java/com.aspose.words/list/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable, java.lang.Comparable
```
public class List implements Cloneable, Comparable
```

Представляет форматирование списка.

 Чтобы узнать больше, посетите**Working with Lists** документальная статья.

Список в документе Microsoft Word представляет собой набор свойств форматирования списка. Каждый список может иметь до 9 уровней, а свойства форматирования, такие как стиль чисел, начальное значение, отступ, позиция табуляции и т. д., определяются отдельно для каждого уровня.

 А[List](../../com.aspose.words/list) объект всегда принадлежит[ListCollection](../../com.aspose.words/listcollection) коллекция.

 Чтобы создать новый список, используйте методы Add класса[ListCollection](../../com.aspose.words/listcollection) коллекция.

 Чтобы изменить форматирование списка, используйте[ListLevel](../../com.aspose.words/listlevel) предметы, найденные в[getListLevels()](../../com.aspose.words/list\#getListLevels--) коллекция.

 Чтобы применить или удалить форматирование списка из абзаца, используйте[ListFormat](../../com.aspose.words/listformat).
## Методы

| Метод | Описание |
| --- | --- |
| [compareTo(List other)](#compareTo-com.aspose.words.List-) | Сравнивает указанный список с текущим списком. |
| [equals(List list)](#equals-com.aspose.words.List-) | Сравнивается с указанным списком. |
| [equals(Object obj)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDocument()](#getDocument--) | Получает документ владельца. |
| [getListId()](#getListId--) | Получает уникальный идентификатор списка. |
| [getListLevels()](#getListLevels--) | Получает коллекцию уровней списка для этого списка. |
| [getStyle()](#getStyle--) | Получает стиль списка, на который ссылается или который определяет этот список. |
| [hasSameTemplate(List other)](#hasSameTemplate-com.aspose.words.List-) | Возвращает true, если текущий список и данный список созданы из одного и того же шаблона. |
| [hashCode()](#hashCode--) |  |
| [isListStyleDefinition()](#isListStyleDefinition--) | Возвращает true, если этот список является определением стиля списка. |
| [isListStyleReference()](#isListStyleReference--) | Возвращает true, если этот список является ссылкой на стиль списка. |
| [isMultiLevel()](#isMultiLevel--) | Возвращает true, если список содержит 9 уровней; false при 1 уровне. |
| [isRestartAtEachSection()](#isRestartAtEachSection--) | Указывает, следует ли перезапускать список в каждом разделе. |
| [isRestartAtEachSection(boolean value)](#isRestartAtEachSection-boolean-) | Указывает, следует ли перезапускать список в каждом разделе. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### compareTo(List other) {#compareTo-com.aspose.words.List-}
```
public int compareTo(List other)
```


Сравнивает указанный список с текущим списком.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| other | [List](../../com.aspose.words/list) |  |

**Возвращает:**
инт
### equals(List list) {#equals-com.aspose.words.List-}
```
public boolean equals(List list)
```


Сравнивается с указанным списком.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| list | [List](../../com.aspose.words/list) |  |

**Возвращает:**
логический
### equals(Object obj) {#equals-java.lang.Object-}
```
public boolean equals(Object obj)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Возвращает:**
логический
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


Получает документ владельца.

Список всегда имеет родительский документ и действителен только в контексте этого документа.

**Возвращает:**
[DocumentBase](../../com.aspose.words/documentbase) - Документ собственника.
### getListId() {#getListId--}
```
public int getListId()
```


Получает уникальный идентификатор списка.

 Обычно вам не нужно использовать это свойство. Но если вы используете его, вы обычно делаете это в сочетании с[ListCollection.getListByListId(int)](../../com.aspose.words/listcollection\#getListByListId-int-) метод поиска списка по его идентификатору.

**Возвращает:**
int — уникальный идентификатор списка.
### getListLevels() {#getListLevels--}
```
public ListLevelCollection getListLevels()
```


Получает коллекцию уровней списка для этого списка.

Используйте это свойство для доступа и изменения форматирования для каждого уровня списка.

**Возвращает:**
[ListLevelCollection](../../com.aspose.words/listlevelcollection) - Коллекция уровней списка для этого списка.
### getStyle() {#getStyle--}
```
public Style getStyle()
```


Получает стиль списка, на который ссылается или который определяет этот список.

Если этот список не связан со стилем списка, свойство вернет значение null.

 Список может быть ссылкой на стиль списка, в этом случае[isListStyleReference()](../../com.aspose.words/list\#isListStyleReference--) будет правдой.

 Список может быть определением стиля списка, в этом случае[isListStyleDefinition()](../../com.aspose.words/list\#isListStyleDefinition--) будет правдой. Такой список нельзя применить к абзацам документа напрямую.

**Возвращает:**
[Style](../../com.aspose.words/style) - Стиль списка, на который ссылается или который определяет этот список.
### hasSameTemplate(List other) {#hasSameTemplate-com.aspose.words.List-}
```
public boolean hasSameTemplate(List other)
```


Возвращает true, если текущий список и данный список созданы из одного и того же шаблона.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| other | [List](../../com.aspose.words/list) |  |

**Возвращает:**
логический
### hashCode() {#hashCode--}
```
public int hashCode()
```




**Возвращает:**
инт
### isListStyleDefinition() {#isListStyleDefinition--}
```
public boolean isListStyleDefinition()
```


Возвращает true, если этот список является определением стиля списка.

Когда это свойство истинно,[getStyle()](../../com.aspose.words/list\#getStyle--) свойство возвращает стиль списка, который определяет этот список.

Изменяя свойства списка, определяющего стиль списка, вы изменяете свойства стиля списка.

Список, являющийся определением стиля списка, нельзя применить непосредственно к абзацам, чтобы сделать их нумерованными.

**Возвращает:**
boolean — Истинно, если этот список является определением стиля списка.
### isListStyleReference() {#isListStyleReference--}
```
public boolean isListStyleReference()
```


Возвращает true, если этот список является ссылкой на стиль списка.

Обратите внимание, что изменение свойств списка, который является ссылкой на стиль списка, не имеет никакого эффекта. Форматирование списка, указанное в самом стиле списка, всегда имеет приоритет.

**Возвращает:**
boolean — Истинно, если этот список является ссылкой на стиль списка.
### isMultiLevel() {#isMultiLevel--}
```
public boolean isMultiLevel()
```


Возвращает true, если список содержит 9 уровней; false при 1 уровне.

Списки, которые вы создаете с помощью Aspose.Words, всегда являются многоуровневыми списками и содержат 9 уровней.

Microsoft Word 2003 и более поздние версии всегда создают многоуровневые списки с 9 уровнями. Но в некоторых документах, созданных с помощью более ранних версий Microsoft Word, вы можете встретить списки, имеющие только 1 уровень.

**Возвращает:**
boolean - True, если список содержит 9 уровней; false при 1 уровне.
### isRestartAtEachSection() {#isRestartAtEachSection--}
```
public boolean isRestartAtEachSection()
```


Указывает, следует ли перезапускать список в каждом разделе. Значение по умолчанию**false**.

Эта опция поддерживается только в форматах документов RTF, DOC и DOCX.

 Эта опция будет записана в DOCX, только если[OoxmlCompliance](../../com.aspose.words/ooxmlcompliance) выше, чем[OoxmlCompliance.ECMA\_376\_2006](../../com.aspose.words/ooxmlcompliance\#ECMA-376-2006).

**Возвращает:**
boolean - соответствующее логическое значение.
### isRestartAtEachSection(boolean value) {#isRestartAtEachSection-boolean-}
```
public void isRestartAtEachSection(boolean value)
```


Указывает, следует ли перезапускать список в каждом разделе. Значение по умолчанию**false**.

Эта опция поддерживается только в форматах документов RTF, DOC и DOCX.

 Эта опция будет записана в DOCX, только если[OoxmlCompliance](../../com.aspose.words/ooxmlcompliance) выше, чем[OoxmlCompliance.ECMA\_376\_2006](../../com.aspose.words/ooxmlcompliance\#ECMA-376-2006).

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
