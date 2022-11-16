---
title: LayoutCollector
second_title: Справочник по API Aspose.Words для Java
description: Этот класс позволяет вычислять номера страниц узлов документа.
type: docs
weight: 358
url: /ru/java/com.aspose.words/layoutcollector/
---

**Наследование:**
java.lang.Object
```
public class LayoutCollector
```

Этот класс позволяет вычислять номера страниц узлов документа.

 Чтобы узнать больше, посетите**Converting to Fixed-page Format** документальная статья.

 Когда вы создаете[LayoutCollector](../../com.aspose.words/layoutcollector) и указать[Document](../../com.aspose.words/document) объект документа для присоединения, коллектор запишет сопоставление узлов документа с объектами макета, когда документ отформатирован в страницы.

 Вы сможете узнать, на какой странице находится тот или иной узел документа (например, прогон, абзац или ячейка таблицы), воспользовавшись кнопкой[getStartPageIndex(com.aspose.words.Node)](../../com.aspose.words/layoutcollector\#getStartPageIndex-com.aspose.words.Node-), [getEndPageIndex(com.aspose.words.Node)](../../com.aspose.words/layoutcollector\#getEndPageIndex-com.aspose.words.Node-) а также[getNumPagesSpanned(com.aspose.words.Node)](../../com.aspose.words/layoutcollector\#getNumPagesSpanned-com.aspose.words.Node-) методы. Эти методы автоматически создают модель макета страницы документа и при необходимости обновляют поля.

 Когда вам больше не нужно собирать информацию о макете, лучше всего установить[getDocument()](../../com.aspose.words/layoutcollector\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/layoutcollector\#setDocument-com.aspose.words.Document-) значение null, чтобы избежать ненужного сбора дополнительных сопоставлений макета.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [LayoutCollector(Document doc)](#LayoutCollector-com.aspose.words.Document-) | Инициализирует экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [clear()](#clear--) | Очищает все собранные данные макета. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDocument()](#getDocument--) | Получает документ, к которому присоединен этот экземпляр сборщика. |
| [getEndPageIndex(Node node)](#getEndPageIndex-com.aspose.words.Node-) | Получает отсчитываемый от 1 индекс страницы, на которой заканчивается узел. |
| [getEntity(Node node)](#getEntity-com.aspose.words.Node-) |  Возвращает непрозрачную позицию[LayoutEnumerator](../../com.aspose.words/layoutenumerator) что соответствует указанному узлу. |
| [getNumPagesSpanned(Node node)](#getNumPagesSpanned-com.aspose.words.Node-) | Получает количество страниц, которые охватывает указанный узел. |
| [getStartPageIndex(Node node)](#getStartPageIndex-com.aspose.words.Node-) | Получает отсчитываемый от 1 индекс страницы, с которой начинается узел. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setDocument(Document value)](#setDocument-com.aspose.words.Document-) | Задает документ, к которому прикреплен этот экземпляр сборщика. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### LayoutCollector(Document doc) {#LayoutCollector-com.aspose.words.Document-}
```
public LayoutCollector(Document doc)
```


Инициализирует экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document) | Документ, к которому будет прикреплен этот экземпляр коллектора. |

### clear() {#clear--}
```
public void clear()
```


Очищает все собранные данные макета. Вызовите этот метод после обновления документа вручную или перестроения макета.

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
### getDocument() {#getDocument--}
```
public Document getDocument()
```


Получает документ, к которому присоединен этот экземпляр сборщика. Если вам нужно получить доступ к индексам страниц узлов документа, вам нужно установить это свойство так, чтобы оно указывало на экземпляр документа, прежде чем будет построен макет страницы документа. Лучше всего впоследствии установить для этого свойства значение null, иначе сборщик продолжит накапливать информацию из последующих перестроений макета страницы документа.

**Возвращает:**
[Document](../../com.aspose.words/document) - Документ, к которому прикреплен этот экземпляр коллектора.
### getEndPageIndex(Node node) {#getEndPageIndex-com.aspose.words.Node-}
```
public int getEndPageIndex(Node node)
```


Получает отсчитываемый от 1 индекс страницы, на которой заканчивается узел. Возвращает 0, если узел не может быть сопоставлен со страницей.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) |  |

**Возвращает:**
инт
### getEntity(Node node) {#getEntity-com.aspose.words.Node-}
```
public Object getEntity(Node node)
```


 Возвращает непрозрачную позицию[LayoutEnumerator](../../com.aspose.words/layoutenumerator) что соответствует указанному узлу. Вы можете использовать возвращаемое значение в качестве аргумента для[LayoutEnumerator.getCurrent()](../../com.aspose.words/layoutenumerator\#getCurrent--) / [LayoutEnumerator.setCurrent(java.lang.Object)](../../com.aspose.words/layoutenumerator\#setCurrent-java.lang.Object-)учитывая, что перечисляемый документ и документ узла совпадают.

 Этот метод работает только для[Paragraph](../../com.aspose.words/paragraph) узлы, а также неделимые встроенные узлы, например[BookmarkStart](../../com.aspose.words/bookmarkstart) или же[Shape](../../com.aspose.words/shape) . Это не работает для[Run](../../com.aspose.words/run), [Cell](../../com.aspose.words/cell) [Row](../../com.aspose.words/row) или же[Table](../../com.aspose.words/table) узлы и узлы в верхнем/нижнем колонтитуле.

 Обратите внимание, что объект вернулся для[Paragraph](../../com.aspose.words/paragraph) узел является диапазоном разрыва абзаца. Используйте соответствующий метод, чтобы подняться на родительскую линию

 Если вам нужно перейти к[Run](../../com.aspose.words/run) текста, вы можете вставить закладку прямо перед ней, а затем вместо этого перейти к закладке.

 Если вам нужно перейти к[Cell](../../com.aspose.words/cell) node, затем вы можете перейти к[Paragraph](../../com.aspose.words/paragraph) узла в этой ячейке, а затем подняться к родительскому объекту. Тот же подход можно использовать для[Row](../../com.aspose.words/row) а также[Table](../../com.aspose.words/table) узлы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) |  |

**Возвращает:**
java.lang.Объект
### getNumPagesSpanned(Node node) {#getNumPagesSpanned-com.aspose.words.Node-}
```
public int getNumPagesSpanned(Node node)
```


 Получает количество страниц, которые охватывает указанный узел. 0, если узел находится на одной странице. Это то же самое, что[getEndPageIndex(com.aspose.words.Node)](../../com.aspose.words/layoutcollector\#getEndPageIndex-com.aspose.words.Node-) -[getStartPageIndex(com.aspose.words.Node)](../../com.aspose.words/layoutcollector\#getStartPageIndex-com.aspose.words.Node-).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) |  |

**Возвращает:**
инт
### getStartPageIndex(Node node) {#getStartPageIndex-com.aspose.words.Node-}
```
public int getStartPageIndex(Node node)
```


Получает отсчитываемый от 1 индекс страницы, с которой начинается узел. Возвращает 0, если узел не может быть сопоставлен со страницей.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) |  |

**Возвращает:**
инт
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




### setDocument(Document value) {#setDocument-com.aspose.words.Document-}
```
public void setDocument(Document value)
```


Задает документ, к которому прикреплен этот экземпляр сборщика. Если вам нужно получить доступ к индексам страниц узлов документа, вам нужно установить это свойство так, чтобы оно указывало на экземпляр документа, прежде чем будет построен макет страницы документа. Лучше всего впоследствии установить для этого свойства значение null, иначе сборщик продолжит накапливать информацию из последующих перестроений макета страницы документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [Document](../../com.aspose.words/document) | Документ, к которому прикреплен этот экземпляр сборщика. |

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
