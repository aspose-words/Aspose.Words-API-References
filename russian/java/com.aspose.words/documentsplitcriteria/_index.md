---
title: DocumentSplitCriteria
second_title: Справочник по API Aspose.Words для Java
description: Указывает, как документ разбивается на части при сохранении или форматировании.
type: docs
weight: 131
url: /ru/java/com.aspose.words/documentsplitcriteria/
---

**Наследование:**
java.lang.Object
```
public class DocumentSplitCriteria
```

 Указывает, как документ разбивается на части при сохранении в[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB) или же[SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3) формат.

[DocumentSplitCriteria](../../com.aspose.words/documentsplitcriteria) представляет собой набор флагов, которые можно комбинировать. Например, вы можете разделить документ на разрывы страниц и абзацы заголовков в одной и той же операции экспорта.

 Различные критерии могут частично совпадать. Например,**Heading 1** стиль часто дается[ParagraphFormat.getPageBreakBefore()](../../com.aspose.words/paragraphformat\#getPageBreakBefore--) / [ParagraphFormat.setPageBreakBefore(boolean)](../../com.aspose.words/paragraphformat\#setPageBreakBefore-boolean-) свойство, поэтому оно подпадает под два критерия:[PAGE\_BREAK](../../com.aspose.words/documentsplitcriteria\#PAGE-BREAK) а также[HEADING\_PARAGRAPH](../../com.aspose.words/documentsplitcriteria\#HEADING-PARAGRAPH). Некоторые разрывы разделов могут привести к разрывам страниц и так далее. В типичных случаях наиболее практичным вариантом является указание только одного флага.
## Поля

| Поле | Описание |
| --- | --- |
| [COLUMN_BREAK](#COLUMN-BREAK) | Документ разбивается на части по разрывам столбцов. |
| [HEADING_PARAGRAPH](#HEADING-PARAGRAPH) |  Документ разбит на части по абзацу, отформатированному с использованием стиля заголовка.**Heading 1**, **Heading 2** и т.п. |
| [NONE](#NONE) | Документ не разделен. |
| [PAGE_BREAK](#PAGE-BREAK) | Документ разбит на части по явным разрывам страниц. |
| [SECTION_BREAK](#SECTION-BREAK) | Документ разбивается на части при разрыве раздела любого типа. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String documentSplitCriteriaName)](#fromName-java.lang.String-) |  |
| [fromNames(Set documentSplitCriteriaNames)](#fromNames-java.util.Set-) |  |
| [getClass()](#getClass--) |  |
| [getName(int documentSplitCriteria)](#getName-int-) |  |
| [getNames(int documentSplitCriteria)](#getNames-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int documentSplitCriteria)](#toString-int-) |  |
| [toStringSet(int attr)](#toStringSet-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### COLUMN_BREAK {#COLUMN-BREAK}
```
public static int COLUMN_BREAK
```


 Документ разбивается на части по разрывам столбцов. Разрыв столбца может быть указан с помощью[ControlChar.COLUMN\_BREAK](../../com.aspose.words/controlchar\#COLUMN-BREAK) символ или разрыв раздела, указывающий начало нового раздела в новом столбце.

### HEADING_PARAGRAPH {#HEADING-PARAGRAPH}
```
public static int HEADING_PARAGRAPH
```


 Документ разбит на части по абзацу, отформатированному с использованием стиля заголовка.**Heading 1**, **Heading 2** и т.д. Используйте вместе с[HtmlSaveOptions.getDocumentSplitHeadingLevel()](../../com.aspose.words/htmlsaveoptions\#getDocumentSplitHeadingLevel--) / [HtmlSaveOptions.setDocumentSplitHeadingLevel(int)](../../com.aspose.words/htmlsaveoptions\#setDocumentSplitHeadingLevel-int-) чтобы указать уровни заголовков (от 1 до указанного уровня), на которых следует разделить.

### NONE {#NONE}
```
public static int NONE
```


Документ не разделен.

### PAGE_BREAK {#PAGE-BREAK}
```
public static int PAGE_BREAK
```


 Документ разбит на части по явным разрывам страниц. Разрыв страницы может быть указан с помощью[ControlChar.PAGE\_BREAK](../../com.aspose.words/controlchar\#PAGE-BREAK) символ разрыва раздела, указывающий начало нового раздела на новой странице, или абзац, который имеет свой[ParagraphFormat.getPageBreakBefore()](../../com.aspose.words/paragraphformat\#getPageBreakBefore--) / [ParagraphFormat.setPageBreakBefore(boolean)](../../com.aspose.words/paragraphformat\#setPageBreakBefore-boolean-) свойство установлено в true .

### SECTION_BREAK {#SECTION-BREAK}
```
public static int SECTION_BREAK
```


Документ разбивается на части при разрыве раздела любого типа.

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
### fromName(String documentSplitCriteriaName) {#fromName-java.lang.String-}
```
public static int fromName(String documentSplitCriteriaName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| documentSplitCriteriaName | java.lang.String |  |

**Возвращает:**
инт
### fromNames(Set documentSplitCriteriaNames) {#fromNames-java.util.Set-}
```
public static int fromNames(Set documentSplitCriteriaNames)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| documentSplitCriteriaNames | java.util.Set |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int documentSplitCriteria) {#getName-int-}
```
public static String getName(int documentSplitCriteria)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| documentSplitCriteria | int |  |

**Возвращает:**
java.lang.String
### getNames(int documentSplitCriteria) {#getNames-int-}
```
public static Set getNames(int documentSplitCriteria)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| documentSplitCriteria | int |  |

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
### toString(int documentSplitCriteria) {#toString-int-}
```
public static String toString(int documentSplitCriteria)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| documentSplitCriteria | int |  |

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
