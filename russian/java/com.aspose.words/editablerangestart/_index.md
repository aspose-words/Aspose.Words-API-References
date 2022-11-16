---
title: EditableRangeStart
second_title: Справочник по API Aspose.Words для Java
description: Представляет начало редактируемого диапазона в документе Word.
type: docs
weight: 138
url: /ru/java/com.aspose.words/editablerangestart/
---

**Наследование:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node)
```
public class EditableRangeStart extends Node
```

Представляет начало редактируемого диапазона в документе Word.

 Чтобы узнать больше, посетите**Aspose.Words Document Object Model (DOM)** документальная статья.

 Полный редактируемый диапазон в документе Word состоит из[EditableRangeStart](../../com.aspose.words/editablerangestart) и соответствие[EditableRangeEnd](../../com.aspose.words/editablerangeend) с тем же идентификатором.

[EditableRangeStart](../../com.aspose.words/editablerangestart) а также[EditableRangeEnd](../../com.aspose.words/editablerangeend) являются просто маркерами внутри документа, которые указывают, где начинается и заканчивается редактируемый диапазон.

 Использовать[getEditableRange()](../../com.aspose.words/editablerangestart\#getEditableRange--) class как «фасад» для работы с редактируемым диапазоном как с единым объектом.

 В настоящее время редактируемые диапазоны поддерживаются только на встроенном уровне, то есть внутри[Paragraph](../../com.aspose.words/paragraph), но начало редактируемого диапазона и конец редактируемого диапазона могут находиться в разных абзацах.
## Методы

| Метод | Описание |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Принимает посетителя. |
| [dd()](#dd--) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | Создает дубликат узла. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAncestor(int ancestorType)](#getAncestor-int-) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class-) | Получает первого предка указанного типа объекта. |
| [getClass()](#getClass--) |  |
| [getCustomNodeId()](#getCustomNodeId--) | Задает идентификатор пользовательского узла. |
| [getDisplacedByCustomXml()](#getDisplacedByCustomXml--) |  |
| [getDocument()](#getDocument--) | Получает документ, которому принадлежит этот узел. |
| [getEditableRange()](#getEditableRange--) | Получает объект фасада, который инкапсулирует начало и конец редактируемого диапазона. |
| [getId()](#getId--) | Задает идентификатор редактируемого диапазона. |
| [getIdInternal()](#getIdInternal--) |  |
| [getNextSibling()](#getNextSibling--) | Получает узел, следующий сразу за этим узлом. |
| [getNodeType()](#getNodeType--) |  Возвращает[NodeType.EDITABLE\_RANGE\_START](../../com.aspose.words/nodetype\#EDITABLE-RANGE-START). |
| [getParentIdInternal()](#getParentIdInternal--) |  |
| [getParentNode()](#getParentNode--) | Получает непосредственного родителя этого узла. |
| [getPreviousSibling()](#getPreviousSibling--) | Получает узел, непосредственно предшествующий этому узлу. |
| [getRange()](#getRange--) |  Возвращает**Range** объект, который представляет часть документа, содержащегося в этом узле. |
| [getText()](#getText--) | Получает текст этого узла и всех его дочерних элементов. |
| [hashCode()](#hashCode--) |  |
| [isComposite()](#isComposite--) | Возвращает true, если этот узел может содержать другие узлы. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node-) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int-) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node-) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [remove()](#remove--) | Удаляет себя из родителя. |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | Задает идентификатор пользовательского узла. |
| [setDisplacedByCustomXml(int value)](#setDisplacedByCustomXml-int-) |  |
| [setId(int value)](#setId-int-) | Задает идентификатор редактируемого диапазона. |
| [setIdInternal(int value)](#setIdInternal-int-) |  |
| [setParentIdInternal(int value)](#setParentIdInternal-int-) |  |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| [toString(int saveFormat)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public boolean accept(DocumentVisitor visitor)
```


Принимает посетителя.

 Звонки[DocumentVisitor.visitEditableRangeStart(com.aspose.words.EditableRangeStart)](../../com.aspose.words/documentvisitor\#visitEditableRangeStart-com.aspose.words.EditableRangeStart-).

Дополнительные сведения см. в шаблоне проектирования «Посетитель».

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | Посетитель, который посетит узел. |

**Возвращает:**
boolean — False, если посетитель запросил остановку перечисления.
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
### getDisplacedByCustomXml() {#getDisplacedByCustomXml--}
```
public int getDisplacedByCustomXml()
```




**Возвращает:**
инт
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


Получает документ, которому принадлежит этот узел.

Узел всегда принадлежит документу, даже если он только что создан и еще не добавлен в дерево или удален из дерева.

**Возвращает:**
[DocumentBase](../../com.aspose.words/documentbase) - Документ, которому принадлежит этот узел.
### getEditableRange() {#getEditableRange--}
```
public EditableRange getEditableRange()
```


Получает объект фасада, который инкапсулирует начало и конец редактируемого диапазона.

**Возвращает:**
[EditableRange](../../com.aspose.words/editablerange) - Объект фасада, который инкапсулирует начало и конец этого редактируемого диапазона.
### getId() {#getId--}
```
public int getId()
```


Задает идентификатор редактируемого диапазона.

**Возвращает:**
int - соответствующее значение int.
### getIdInternal() {#getIdInternal--}
```
public int getIdInternal()
```




**Возвращает:**
инт
### getNextSibling() {#getNextSibling--}
```
public Node getNextSibling()
```


Получает узел, следующий сразу за этим узлом. Если следующего узла нет, возвращается нуль.

**Возвращает:**
[Node](../../com.aspose.words/node) - Узел, непосредственно следующий за этим узлом.
### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


 Возвращает[NodeType.EDITABLE\_RANGE\_START](../../com.aspose.words/nodetype\#EDITABLE-RANGE-START).

**Возвращает:**
 инт -\{[NodeType.EDITABLE\_RANGE\_START](../../com.aspose.words/nodetype\#EDITABLE-RANGE-START) . Возвращаемое значение является одним из[NodeType](../../com.aspose.words/nodetype) константы.
### getParentIdInternal() {#getParentIdInternal--}
```
public int getParentIdInternal()
```




**Возвращает:**
инт
### getParentNode() {#getParentNode--}
```
public CompositeNode getParentNode()
```


Получает непосредственного родителя этого узла.

Если узел был только что создан и еще не добавлен в дерево, или если он был удален из дерева, родитель имеет значение null.

**Возвращает:**
[CompositeNode](../../com.aspose.words/compositenode) - Непосредственный родитель этого узла.
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

### setDisplacedByCustomXml(int value) {#setDisplacedByCustomXml-int-}
```
public void setDisplacedByCustomXml(int value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  |

### setId(int value) {#setId-int-}
```
public void setId(int value)
```


Задает идентификатор редактируемого диапазона.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

### setIdInternal(int value) {#setIdInternal-int-}
```
public void setIdInternal(int value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  |

### setParentIdInternal(int value) {#setParentIdInternal-int-}
```
public void setParentIdInternal(int value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  |

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
