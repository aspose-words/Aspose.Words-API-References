---
title: Inline
second_title: Справочник по API Aspose.Words для Java
description: Базовый класс для узлов встроенного уровня, которые могут иметь связанное с ними форматирование символов, но не могут иметь собственных дочерних узлов.
type: docs
weight: 349
url: /ru/java/com.aspose.words/inline/
---

**Наследование:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node)
```
public abstract class Inline extends Node
```

Базовый класс для узлов встроенного уровня, которые могут иметь связанное с ними форматирование символов, но не могут иметь собственных дочерних узлов.

 Чтобы узнать больше, посетите**Logical Levels of Nodes in a Document** документальная статья.

 Класс, производный от**Inline** может быть ребенком**Paragraph**.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [Inline()](#Inline--) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Принимает посетителя. |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [dd()](#dd--) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | Создает дубликат узла. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int-) |  |
| [getAncestor(int ancestorType)](#getAncestor-int-) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class-) | Получает первого предка указанного типа объекта. |
| [getClass()](#getClass--) |  |
| [getCustomNodeId()](#getCustomNodeId--) | Задает идентификатор пользовательского узла. |
| [getDirectRunAttr(int fontAttr)](#getDirectRunAttr-int-) |  |
| [getDocument()](#getDocument--) | Получает документ, которому принадлежит этот узел. |
| [getDocument_IInline()](#getDocument-IInline--) |  |
| [getFont()](#getFont--) | Предоставляет доступ к форматированию шрифта этого объекта. |
| [getNextSibling()](#getNextSibling--) | Получает узел, следующий сразу за этим узлом. |
| [getNodeType()](#getNodeType--) | Получает тип этого узла. |
| [getParentNode()](#getParentNode--) | Получает непосредственного родителя этого узла. |
| [getParentParagraph()](#getParentParagraph--) |  Извлекает родителя[Paragraph](../../com.aspose.words/paragraph) этого узла. |
| [getParentParagraph_IInline()](#getParentParagraph-IInline--) |  |
| [getPreviousSibling()](#getPreviousSibling--) | Получает узел, непосредственно предшествующий этому узлу. |
| [getRange()](#getRange--) |  Возвращает**Range** объект, который представляет часть документа, содержащегося в этом узле. |
| [getText()](#getText--) | Получает текст этого узла и всех его дочерних элементов. |
| [hashCode()](#hashCode--) |  |
| [isComposite()](#isComposite--) | Возвращает true, если этот узел может содержать другие узлы. |
| [isDeleteRevision()](#isDeleteRevision--) | Возвращает true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений. |
| [isFormatRevision()](#isFormatRevision--) | Возвращает true, если форматирование объекта было изменено в Microsoft Word при включенном отслеживании изменений. |
| [isInsertRevision()](#isInsertRevision--) | Возвращает true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений. |
| [isMoveFromRevision()](#isMoveFromRevision--) |  Возвращает**true** если этот объект был перемещен (удален) в Microsoft Word при включенном отслеживании изменений. |
| [isMoveToRevision()](#isMoveToRevision--) |  Возвращает**true** если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node-) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int-) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node-) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [remove()](#remove--) | Удаляет себя из родителя. |
| [removeMoveRevisions()](#removeMoveRevisions--) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | Задает идентификатор пользовательского узла. |
| [setRunAttr(int fontAttr, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| [toString(int saveFormat)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### Inline() {#Inline--}
```
public Inline()
```


### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public abstract boolean accept(DocumentVisitor visitor)
```


Принимает посетителя.

Перечисляет этот узел и все его дочерние элементы. Каждый узел вызывает соответствующий метод в DocumentVisitor.

Дополнительные сведения см. в шаблоне проектирования «Посетитель».

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | Посетитель, который будет посещать узлы. |

**Возвращает:**
boolean - Истинно, если были посещены все узлы; false, если DocumentVisitor остановил операцию перед посещением всех узлов.
### clearRunAttrs() {#clearRunAttrs--}
```
public void clearRunAttrs()
```




### dd() {#dd--}
```
public void dd()
```




### deepClone(boolean isCloneChildren) {#deepClone-boolean-}
```
public Node deepClone(boolean isCloneChildren)
```


Создает дубликат узла.

Этот метод служит конструктором копирования для узлов. Клонированный узел не имеет родителя, но принадлежит к тому же документу, что и исходный узел.

 Этот метод всегда выполняет глубокую копию узла.*isCloneChildren* Параметр указывает, следует ли также выполнять копирование всех дочерних узлов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| isCloneChildren | boolean | Значение true, чтобы рекурсивно клонировать поддерево в указанном узле; false, чтобы клонировать только сам узел. |

**Возвращает:**
[Node](../../com.aspose.words/node) - Клонированный узел.
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
### fetchInheritedRunAttr(int fontAttr) {#fetchInheritedRunAttr-int-}
```
public Object fetchInheritedRunAttr(int fontAttr)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fontAttr | int |  |

**Возвращает:**
java.lang.Объект
### getAncestor(int ancestorType) {#getAncestor-int-}
```
public CompositeNode getAncestor(int ancestorType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| ancestorType | int |  |

**Возвращает:**
[CompositeNode](../../com.aspose.words/compositenode)
### getAncestor(Class ancestorType) {#getAncestor-java.lang.Class-}
```
public CompositeNode getAncestor(Class ancestorType)
```


Получает первого предка указанного типа объекта.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| ancestorType | java.lang.Class | Тип объекта-предка для извлечения. |

**Возвращает:**
[CompositeNode](../../com.aspose.words/compositenode) - предок указанного типа или ноль, если предок этого типа не найден.

Тип предка совпадает, если он равен ancestorType или является производным от ancestorType.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getCustomNodeId() {#getCustomNodeId--}
```
public int getCustomNodeId()
```


Задает идентификатор пользовательского узла.

По умолчанию ноль.

Этот идентификатор можно установить и использовать произвольно. Например, как ключ для получения внешних данных.

Важное примечание: указанное значение не сохраняется в выходной файл и существует только в течение срока службы узла.

**Возвращает:**
int - соответствующее значение int.
### getDirectRunAttr(int fontAttr) {#getDirectRunAttr-int-}
```
public Object getDirectRunAttr(int fontAttr)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fontAttr | int |  |

**Возвращает:**
java.lang.Объект
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


Получает документ, которому принадлежит этот узел.

Узел всегда принадлежит документу, даже если он только что создан и еще не добавлен в дерево или удален из дерева.

**Возвращает:**
[DocumentBase](../../com.aspose.words/documentbase) - Документ, которому принадлежит этот узел.
### getDocument_IInline() {#getDocument-IInline--}
```
public DocumentBase getDocument_IInline()
```




**Возвращает:**
[DocumentBase](../../com.aspose.words/documentbase)
### getFont() {#getFont--}
```
public Font getFont()
```


Предоставляет доступ к форматированию шрифта этого объекта.

**Возвращает:**
[Font](../../com.aspose.words/font) - соответствующий[Font](../../com.aspose.words/font) ценность.
### getNextSibling() {#getNextSibling--}
```
public Node getNextSibling()
```


Получает узел, следующий сразу за этим узлом. Если следующего узла нет, возвращается нуль.

**Возвращает:**
[Node](../../com.aspose.words/node) - Узел, непосредственно следующий за этим узлом.
### getNodeType() {#getNodeType--}
```
public abstract int getNodeType()
```


Получает тип этого узла.

**Возвращает:**
 int - Тип этого узла. Возвращаемое значение является одним из[NodeType](../../com.aspose.words/nodetype) константы.
### getParentNode() {#getParentNode--}
```
public CompositeNode getParentNode()
```


Получает непосредственного родителя этого узла.

Если узел был только что создан и еще не добавлен в дерево, или если он был удален из дерева, родитель имеет значение null.

**Возвращает:**
[CompositeNode](../../com.aspose.words/compositenode) - Непосредственный родитель этого узла.
### getParentParagraph() {#getParentParagraph--}
```
public Paragraph getParentParagraph()
```


 Извлекает родителя[Paragraph](../../com.aspose.words/paragraph) этого узла.

**Возвращает:**
[Paragraph](../../com.aspose.words/paragraph) - соответствующий[Paragraph](../../com.aspose.words/paragraph) ценность.
### getParentParagraph_IInline() {#getParentParagraph-IInline--}
```
public Paragraph getParentParagraph_IInline()
```




**Возвращает:**
[Paragraph](../../com.aspose.words/paragraph)
### getPreviousSibling() {#getPreviousSibling--}
```
public Node getPreviousSibling()
```


Получает узел, непосредственно предшествующий этому узлу. Если предыдущего узла нет, возвращается нуль.

**Возвращает:**
[Node](../../com.aspose.words/node) - Узел, непосредственно предшествующий этому узлу.
### getRange() {#getRange--}
```
public Range getRange()
```


 Возвращает**Range** объект, который представляет часть документа, содержащегося в этом узле.

**Возвращает:**
[Range](../../com.aspose.words/range) - А**Range** объект, который представляет часть документа, содержащегося в этом узле.
### getText() {#getText--}
```
public String getText()
```


Получает текст этого узла и всех его дочерних элементов.

 Возвращаемая строка включает все управляющие и специальные символы, как описано в[ControlChar](../../com.aspose.words/controlchar).

**Возвращает:**
java.lang.String
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isComposite() {#isComposite--}
```
public boolean isComposite()
```


Возвращает true, если этот узел может содержать другие узлы. (31110,6)

**Возвращает:**
boolean — Истинно, если этот узел может содержать другие узлы.
### isDeleteRevision() {#isDeleteRevision--}
```
public boolean isDeleteRevision()
```


Возвращает true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений.

**Возвращает:**
boolean — Истинно, если этот объект был удален в Microsoft Word при включенном отслеживании изменений.
### isFormatRevision() {#isFormatRevision--}
```
public boolean isFormatRevision()
```


Возвращает true, если форматирование объекта было изменено в Microsoft Word при включенном отслеживании изменений.

**Возвращает:**
boolean — Истинно, если форматирование объекта было изменено в Microsoft Word при включенном отслеживании изменений.
### isInsertRevision() {#isInsertRevision--}
```
public boolean isInsertRevision()
```


Возвращает true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений.

**Возвращает:**
boolean — True, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений.
### isMoveFromRevision() {#isMoveFromRevision--}
```
public boolean isMoveFromRevision()
```


 Возвращает**true** если этот объект был перемещен (удален) в Microsoft Word при включенном отслеживании изменений.

**Возвращает:**
 логический -**true** если этот объект был перемещен (удален) в Microsoft Word при включенном отслеживании изменений.
### isMoveToRevision() {#isMoveToRevision--}
```
public boolean isMoveToRevision()
```


 Возвращает**true** если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений.

**Возвращает:**
 логический -**true** если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений.
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node-}
```
public Node nextPreOrder(Node rootNode)
```


Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | Верхний узел (предел) обхода. |

**Возвращает:**
[Node](../../com.aspose.words/node) - Следующий узел в порядке предварительного заказа. Null, если достигнут rootNode.
### nodeTypeToString(int nodeType) {#nodeTypeToString-int-}
```
public static String nodeTypeToString(int nodeType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| nodeType | int |  |

**Возвращает:**
java.lang.String
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node-}
```
public Node previousPreOrder(Node rootNode)
```


Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | Верхний узел (предел) обхода. |

**Возвращает:**
[Node](../../com.aspose.words/node) - Предыдущий узел в порядке предварительного заказа. Null, если достигнут rootNode.
### remove() {#remove--}
```
public void remove()
```


Удаляет себя из родителя.

### removeMoveRevisions() {#removeMoveRevisions--}
```
public void removeMoveRevisions()
```




### removeRunAttr(int key) {#removeRunAttr-int-}
```
public void removeRunAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

### setCustomNodeId(int value) {#setCustomNodeId-int-}
```
public void setCustomNodeId(int value)
```


Задает идентификатор пользовательского узла.

По умолчанию ноль.

Этот идентификатор можно установить и использовать произвольно. Например, как ключ для получения внешних данных.

Важное примечание: указанное значение не сохраняется в выходной файл и существует только в течение срока службы узла.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

### setRunAttr(int fontAttr, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int fontAttr, Object value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fontAttr | int |  |
| value | java.lang.Object |  |

### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### toString(SaveOptions saveOptions) {#toString-com.aspose.words.SaveOptions-}
```
public String toString(SaveOptions saveOptions)
```


Экспортирует содержимое узла в строку, используя указанные параметры сохранения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions) | Указывает параметры, управляющие способом сохранения узла. |

**Возвращает:**
java.lang.String — содержимое узла в указанном формате.
### toString(int saveFormat) {#toString-int-}
```
public String toString(int saveFormat)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| saveFormat | int |  |

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
