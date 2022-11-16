---
title: HtmlInsertOptions
second_title: Справочник по API Aspose.Words для Java
description: Задает параметры для метода MAspose.Words.DocumentBuilder.InsertHtmlSystem.StringAspose.Words.HtmlInsertOptions.
type: docs
weight: 327
url: /ru/java/com.aspose.words/htmlinsertoptions/
---

**Наследование:**
java.lang.Object
```
public class HtmlInsertOptions
```

 Задает параметры для**M:Aspose.Words.DocumentBuilder.InsertHtml(System.String,Aspose.Words.HtmlInsertOptions)** метод.
## Поля

| Поле | Описание |
| --- | --- |
| [NONE](#NONE) | Используйте параметры по умолчанию при вставке HTML. |
| [PRESERVE_BLOCKS](#PRESERVE-BLOCKS) | Сохранять свойства элементов блочного уровня. |
| [REMOVE_LAST_EMPTY_PARAGRAPH](#REMOVE-LAST-EMPTY-PARAGRAPH) | Удалите пустой абзац, который обычно вставляется после HTML, заканчивающегося элементом уровня блока. |
| [USE_BUILDER_FORMATTING](#USE-BUILDER-FORMATTING) |  Используйте форматирование шрифта и абзаца, указанное в[DocumentBuilder](../../com.aspose.words/documentbuilder) в качестве базового форматирования для текста, вставленного из HTML. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String htmlInsertOptionsName)](#fromName-java.lang.String-) |  |
| [fromNames(Set htmlInsertOptionsNames)](#fromNames-java.util.Set-) |  |
| [getClass()](#getClass--) |  |
| [getName(int htmlInsertOptions)](#getName-int-) |  |
| [getNames(int htmlInsertOptions)](#getNames-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int htmlInsertOptions)](#toString-int-) |  |
| [toStringSet(int attr)](#toStringSet-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### NONE {#NONE}
```
public static int NONE
```


Используйте параметры по умолчанию при вставке HTML.

### PRESERVE_BLOCKS {#PRESERVE-BLOCKS}
```
public static int PRESERVE_BLOCKS
```


Сохранять свойства элементов блочного уровня.

По умолчанию свойства родительских блоков объединяются и сохраняются в их дочерних элементах (например, в абзацах или таблицах). Если указана эта опция, свойства каждого блока хранятся отдельно в специальной логической структуре. В результате этот параметр позволяет лучше сохранить отдельные границы и поля, видимые в HTML-документе, и получить лучшие результаты преобразования. Недостатком является то, что результирующий документ становится сложнее модифицировать, так как границы и поля, хранящиеся в логической структуре, недоступны для редактирования.

Сохраняются только поля и границы HTML-элементов body, div и blockquote. Свойства каждого элемента HTML хранятся отдельно.

Если указан этот параметр, Aspose.Words имитирует поведение MS Word в отношении импорта свойств блока.

### REMOVE_LAST_EMPTY_PARAGRAPH {#REMOVE-LAST-EMPTY-PARAGRAPH}
```
public static int REMOVE_LAST_EMPTY_PARAGRAPH
```


 Удалите пустой абзац, который обычно вставляется после HTML, заканчивающегося элементом уровня блока. По умолчанию,[DocumentBuilder](../../com.aspose.words/documentbuilder)гарантирует, что последний элемент уровня блока, импортированный из HTML, будет закрыт после импорта, и вставит разрыв абзаца после элемента. Этот разрыв абзаца отделяет содержимое, импортированное из HTML, от содержимого шаблона документа. Однако, если фрагмент HTML вставлен в пустой абзац, этот разрыв абзаца создаст дополнительный пустой абзац. Если такое поведение нежелательно, укажите этот параметр.

### USE_BUILDER_FORMATTING {#USE-BUILDER-FORMATTING}
```
public static int USE_BUILDER_FORMATTING
```


 Используйте форматирование шрифта и абзаца, указанное в[DocumentBuilder](../../com.aspose.words/documentbuilder) в качестве базового форматирования для текста, вставленного из HTML.

 Если этот параметр не указан, форматирование[DocumentBuilder](../../com.aspose.words/documentbuilder) игнорируется, и текст вставляется с форматированием HTML по умолчанию. В результате текст выглядит так, как он отображается в браузерах.

 Если указан этот параметр, форматирование вставляемого текста основано на форматировании, указанном в[DocumentBuilder](../../com.aspose.words/documentbuilder) , и текст выглядит так, как будто он был вставлен с помощью[DocumentBuilder.write(java.lang.String)](../../com.aspose.words/documentbuilder\#write-java.lang.String-).

### length {#length}
```
public static int length
```


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
### fromName(String htmlInsertOptionsName) {#fromName-java.lang.String-}
```
public static int fromName(String htmlInsertOptionsName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| htmlInsertOptionsName | java.lang.String |  |

**Возвращает:**
инт
### fromNames(Set htmlInsertOptionsNames) {#fromNames-java.util.Set-}
```
public static int fromNames(Set htmlInsertOptionsNames)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| htmlInsertOptionsNames | java.util.Set |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int htmlInsertOptions) {#getName-int-}
```
public static String getName(int htmlInsertOptions)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| htmlInsertOptions | int |  |

**Возвращает:**
java.lang.String
### getNames(int htmlInsertOptions) {#getNames-int-}
```
public static Set getNames(int htmlInsertOptions)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| htmlInsertOptions | int |  |

**Возвращает:**
java.util.Set
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Возвращает:**
инт[]
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




### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### toString(int htmlInsertOptions) {#toString-int-}
```
public static String toString(int htmlInsertOptions)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| htmlInsertOptions | int |  |

**Возвращает:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int-}
```
public static String toStringSet(int attr)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| attr | int |  |

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
