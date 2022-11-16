---
title: NodeImporter
second_title: Справочник по API Aspose.Words для Java
description: Позволяет эффективно выполнять повторный импорт узлов из одного документа в другой.
type: docs
weight: 405
url: /ru/java/com.aspose.words/nodeimporter/
---

**Наследование:**
java.lang.Object
```
public class NodeImporter
```

Позволяет эффективно выполнять повторный импорт узлов из одного документа в другой.

 Чтобы узнать больше, посетите**Aspose.Words Document Object Model (DOM)** документальная статья.

Aspose.Words предоставляет функциональные возможности для простого копирования и перемещения фрагментов между документами Microsoft Word. Это известно как «импорт узлов». Прежде чем вы сможете вставить фрагмент из одного документа в другой, его необходимо «импортировать». При импорте создается глубокий клон исходного узла, готовый к вставке в целевой документ.

 Самый простой способ импортировать узел — использовать[DocumentBase.importNode(com.aspose.words.Node, boolean)](../../com.aspose.words/documentbase\#importNode-com.aspose.words.Node--boolean-) метод, предоставляемый[DocumentBase](../../com.aspose.words/documentbase) объект.

 Однако, когда вам нужно несколько раз импортировать узлы из одного документа в другой, лучше использовать[NodeImporter](../../com.aspose.words/nodeimporter) учебный класс.[NodeImporter](../../com.aspose.words/nodeimporter) class позволяет свести к минимуму количество стилей и списков, созданных в целевом документе.

Копирование или перемещение фрагментов из одного документа Microsoft Word в другой представляет ряд технических проблем для Aspose.Words. В документе Word стили и форматирование списка хранятся централизованно, отдельно от текста документа. Абзацы и фрагменты текста просто ссылаются на стили по внутренним уникальным идентификаторам.

Проблемы возникают из-за того, что стили и списки различаются в разных документах. Например, чтобы скопировать абзац, отформатированный в стиле «Заголовок 1», из одного документа в другой, необходимо принять во внимание ряд факторов: решить, копировать ли стиль «Заголовок 1» из исходного документа в целевой документ, клонировать абзац, обновите клонированный абзац, чтобы он ссылался на правильный стиль Заголовка 1 в целевом документе. Если стиль должен быть скопирован, все стили, на которые он ссылается (на основе стиля и стиля следующего абзаца), должны быть проанализированы и, возможно, скопированы, и так далее. Аналогичные проблемы возникают при копировании маркированных или пронумерованных абзацев, поскольку Microsoft Word хранит определения списков отдельно от текста.

[NodeImporter](../../com.aspose.words/nodeimporter) class похож на контекст, который содержит «таблицы перевода» во время импорта. Он правильно переводит стили и списки в исходном и целевом документах.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode)](#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int-) | Инициализирует новый экземпляр этого класса. |
| [NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions)](#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int-com.aspose.words.ImportFormatOptions-) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [hashCode()](#hashCode--) |  |
| [importNode(Node srcNode, boolean isImportChildren)](#importNode-com.aspose.words.Node-boolean-) | Импортирует узел из одного документа в другой. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode) {#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int-}
```
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcDoc | [DocumentBase](../../com.aspose.words/documentbase) |  |
| dstDoc | [DocumentBase](../../com.aspose.words/documentbase) |  |
| importFormatMode | int |  |

### NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions) {#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int-com.aspose.words.ImportFormatOptions-}
```
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcDoc | [DocumentBase](../../com.aspose.words/documentbase) |  |
| dstDoc | [DocumentBase](../../com.aspose.words/documentbase) |  |
| importFormatMode | int |  |
| importFormatOptions | [ImportFormatOptions](../../com.aspose.words/importformatoptions) |  |

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
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### importNode(Node srcNode, boolean isImportChildren) {#importNode-com.aspose.words.Node-boolean-}
```
public Node importNode(Node srcNode, boolean isImportChildren)
```


Импортирует узел из одного документа в другой.

При импорте узла создается копия исходного узла, принадлежащего импортируемому документу. Возвращенный узел не имеет родителя. Исходный узел не изменяется и не удаляется из исходного документа.

 Прежде чем узел из другого документа можно будет вставить в этот документ, его необходимо импортировать. Во время импорта свойства документа, такие как ссылки на стили и списки, переводятся из оригинала в импортируемый документ. После того, как узел был импортирован, его можно вставить в соответствующее место документа с помощью[CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertBefore-com.aspose.words.Node--com.aspose.words.Node-) или же[CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertAfter-com.aspose.words.Node--com.aspose.words.Node-).

Если исходный узел уже принадлежит целевому документу, то создается просто глубокий клон исходного узла.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcNode | [Node](../../com.aspose.words/node) | Узел для импорта. |
| isImportChildren | boolean | Значение true для рекурсивного импорта всех дочерних узлов; в противном случае ложно. |

**Возвращает:**
[Node](../../com.aspose.words/node) Клонированный, импортированный узел. Узел принадлежит целевому документу, но не имеет родителя.
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
