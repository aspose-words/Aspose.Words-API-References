---
title: DocumentBase
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет абстрактный базовый класс для основного документа и глоссария документа Word.
type: docs
weight: 121
url: /ru/java/com.aspose.words/documentbase/
---

**Наследование:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode)
```
public abstract class DocumentBase extends CompositeNode
```

Предоставляет абстрактный базовый класс для основного документа и глоссария документа Word.

 Чтобы узнать больше, посетите**Aspose.Words Document Object Model (DOM)** документальная статья.

 Aspose.Words представляет документ Word в виде дерева узлов.[DocumentBase](../../com.aspose.words/documentbase) является корневым узлом дерева, содержащего все остальные узлы документа.

[DocumentBase](../../com.aspose.words/documentbase) также хранит информацию о документе, такую как[getStyles()](../../com.aspose.words/documentbase\#getStyles--) а также[getLists()](../../com.aspose.words/documentbase\#getLists--) на которые могут ссылаться узлы дерева.
## Методы

| Метод | Описание |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Принимает посетителя. |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node-) | Добавляет указанный узел в конец списка дочерних узлов для этого узла. |
| [dd()](#dd--) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | Создает дубликат узла. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAncestor(int ancestorType)](#getAncestor-int-) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class-) | Получает первого предка указанного типа объекта. |
| [getBackgroundShape()](#getBackgroundShape--) | Получает форму фона документа. |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean-) |  |
| [getChildNodes()](#getChildNodes--) | Получает все непосредственные дочерние узлы этого узла. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [getClass()](#getClass--) |  |
| [getContainer()](#getContainer--) |  |
| [getCount()](#getCount--) | Получает количество непосредственных дочерних элементов этого узла. |
| [getCurrentNode()](#getCurrentNode--) |  |
| [getCustomNodeId()](#getCustomNodeId--) | Задает идентификатор пользовательского узла. |
| [getDocument()](#getDocument--) |  |
| [getFirstChild()](#getFirstChild--) | Получает первый дочерний элемент узла. |
| [getFontInfos()](#getFontInfos--) | Предоставляет доступ к свойствам шрифтов, используемых в этом документе. |
| [getLastChild()](#getLastChild--) | Получает последний дочерний элемент узла. |
| [getLists()](#getLists--) | Предоставляет доступ к форматированию списка, используемому в документе. |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node-) |  |
| [getNextSibling()](#getNextSibling--) | Получает узел, следующий сразу за этим узлом. |
| [getNodeChangingCallback()](#getNodeChangingCallback--) | Вызывается при вставке или удалении узла в документе. |
| [getNodeType()](#getNodeType--) | Получает тип этого узла. |
| [getPageColor()](#getPageColor--) | Получает цвет страницы документа. |
| [getParentNode()](#getParentNode--) | Получает непосредственного родителя этого узла. |
| [getPreviousSibling()](#getPreviousSibling--) | Получает узел, непосредственно предшествующий этому узлу. |
| [getRange()](#getRange--) |  Возвращает**Range** объект, который представляет часть документа, содержащегося в этом узле. |
| [getResourceLoadingCallback()](#getResourceLoadingCallback--) | Позволяет контролировать загрузку внешних ресурсов. |
| [getStyles()](#getStyles--) | Возвращает набор стилей, определенных в документе. |
| [getText()](#getText--) | Получает текст этого узла и всех его дочерних элементов. |
| [getWarningCallback()](#getWarningCallback--) | Вызывается во время различных процедур обработки документов при обнаружении проблемы, которая может привести к потере точности данных или форматирования. |
| [hasChildNodes()](#hasChildNodes--) | Возвращает true, если у этого узла есть дочерние узлы. |
| [hashCode()](#hashCode--) |  |
| [importNode(Node srcNode, boolean isImportChildren)](#importNode-com.aspose.words.Node-boolean-) | Импортирует узел из другого документа в текущий документ. |
| [importNode(Node srcNode, boolean isImportChildren, int importFormatMode)](#importNode-com.aspose.words.Node-boolean-int-) |  |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node-) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node-) | Вставляет указанный узел сразу после указанного ссылочного узла. |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node-) | Вставляет указанный узел непосредственно перед указанным ссылочным узлом. |
| [isComposite()](#isComposite--) | Возвращает true, так как этот узел может иметь дочерние узлы. |
| [iterator()](#iterator--) | Обеспечивает поддержку для каждой итерации стиля над дочерними узлами этого узла. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node-) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int-) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [prependChild(Node newChild)](#prependChild-com.aspose.words.Node-) | Добавляет указанный узел в начало списка дочерних узлов для этого узла. |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node-) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [remove()](#remove--) | Удаляет себя из родителя. |
| [removeAllChildren()](#removeAllChildren--) | Удаляет все дочерние узлы текущего узла. |
| [removeChild(Node oldChild)](#removeChild-com.aspose.words.Node-) | Удаляет указанный дочерний узел. |
| [removeSmartTags()](#removeSmartTags--) |  Удаляет все[SmartTag](../../com.aspose.words/smarttag) узлы-потомки текущего узла. |
| [selectNodes(String xpath)](#selectNodes-java.lang.String-) | Выбирает список узлов, соответствующих выражению XPath. |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String-) | Выбирает первый узел, соответствующий выражению XPath. |
| [setBackgroundShape(Shape value)](#setBackgroundShape-com.aspose.words.Shape-) | Устанавливает форму фона документа. |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | Задает идентификатор пользовательского узла. |
| [setNodeChangingCallback(INodeChangingCallback value)](#setNodeChangingCallback-com.aspose.words.INodeChangingCallback-) | Вызывается при вставке или удалении узла в документе. |
| [setPageColor(Color value)](#setPageColor-java.awt.Color-) | Устанавливает цвет страницы документа. |
| [setResourceLoadingCallback(IResourceLoadingCallback value)](#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback-) | Позволяет контролировать загрузку внешних ресурсов. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback-) | Вызывается во время различных процедур обработки документов при обнаружении проблемы, которая может привести к потере точности данных или форматирования. |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| [toString(int saveFormat)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
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
### appendChild(Node newChild) {#appendChild-com.aspose.words.Node-}
```
public Node appendChild(Node newChild)
```


Добавляет указанный узел в конец списка дочерних узлов для этого узла.

Если новый дочерний элемент уже находится в дереве, он сначала удаляется.

 Если вставляемый узел был создан из другого документа, следует использовать**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** чтобы импортировать узел в текущий документ. Затем импортированный узел можно вставить в текущий документ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | Добавляемый узел. |

**Возвращает:**
[Node](../../com.aspose.words/node) - Добавлен узел.
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
### getBackgroundShape() {#getBackgroundShape--}
```
public Shape getBackgroundShape()
```


Получает форму фона документа. Может быть нулевым.

Microsoft Word допускает только ту форму, которая имеет свою[ShapeBase.getShapeType()](../../com.aspose.words/shapebase\#getShapeType--) свойство, равное[ShapeType.RECTANGLE](../../com.aspose.words/shapetype\#RECTANGLE) для использования в качестве фоновой формы для документа.

Microsoft Word поддерживает только свойства заливки фоновой фигуры. Все остальные свойства игнорируются.

 Установка для этого свойства ненулевого значения также установит[ViewOptions.getDisplayBackgroundShape()](../../com.aspose.words/viewoptions\#getDisplayBackgroundShape--) / [ViewOptions.setDisplayBackgroundShape(boolean)](../../com.aspose.words/viewoptions\#setDisplayBackgroundShape-boolean-) к истине.

**Возвращает:**
[Shape](../../com.aspose.words/shape) - Форма фона документа.
### getChild(int nodeType, int index, boolean isDeep) {#getChild-int-int-boolean-}
```
public Node getChild(int nodeType, int index, boolean isDeep)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| nodeType | int |  |
| index | int |  |
| isDeep | boolean |  |

**Возвращает:**
[Node](../../com.aspose.words/node)
### getChildNodes() {#getChildNodes--}
```
public NodeCollection getChildNodes()
```


Получает все непосредственные дочерние узлы этого узла.

 Примечание,[getChildNodes()](../../com.aspose.words/compositenode\#getChildNodes--) эквивалентно вызову GetChildNodes(NodeType.Any, false) и создает и возвращает новую коллекцию при каждом доступе к ней.

Если дочерних узлов нет, это свойство возвращает пустую коллекцию.

**Возвращает:**
[NodeCollection](../../com.aspose.words/nodecollection) - Все непосредственные дочерние узлы этого узла.
### getChildNodes(int nodeType, boolean isDeep) {#getChildNodes-int-boolean-}
```
public NodeCollection getChildNodes(int nodeType, boolean isDeep)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| nodeType | int |  |
| isDeep | boolean |  |

**Возвращает:**
[NodeCollection](../../com.aspose.words/nodecollection)
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getContainer() {#getContainer--}
```
public CompositeNode getContainer()
```




**Возвращает:**
[CompositeNode](../../com.aspose.words/compositenode)
### getCount() {#getCount--}
```
public int getCount()
```


Получает количество непосредственных дочерних элементов этого узла.

**Возвращает:**
int - количество непосредственных дочерних элементов этого узла.
### getCurrentNode() {#getCurrentNode--}
```
public Node getCurrentNode()
```




**Возвращает:**
[Node](../../com.aspose.words/node)
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
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


Получает документ, которому принадлежит этот узел.

Узел всегда принадлежит документу, даже если он только что создан и еще не добавлен в дерево или удален из дерева.

**Возвращает:**
[DocumentBase](../../com.aspose.words/documentbase)
### getFirstChild() {#getFirstChild--}
```
public Node getFirstChild()
```


Получает первый дочерний элемент узла. Если нет первого дочернего узла, возвращается нуль.

**Возвращает:**
[Node](../../com.aspose.words/node) - Первый дочерний узел.
### getFontInfos() {#getFontInfos--}
```
public FontInfoCollection getFontInfos()
```


Предоставляет доступ к свойствам шрифтов, используемых в этом документе.

Эта коллекция определений шрифтов загружается как есть из документа. Определения шрифтов могут быть необязательными, отсутствовать или быть неполными в некоторых документах.

Не полагайтесь на эту коллекцию, чтобы убедиться, что в документе используется определенный шрифт. Вы должны использовать эту коллекцию только для получения информации о шрифтах, которые могут использоваться в документе.

**Возвращает:**
[FontInfoCollection](../../com.aspose.words/fontinfocollection) - соответствующий[FontInfoCollection](../../com.aspose.words/fontinfocollection) ценность.
### getLastChild() {#getLastChild--}
```
public Node getLastChild()
```


Получает последний дочерний элемент узла. Если последнего дочернего узла нет, возвращается нуль.

**Возвращает:**
[Node](../../com.aspose.words/node) - Последний дочерний узел.
### getLists() {#getLists--}
```
public ListCollection getLists()
```


Предоставляет доступ к форматированию списка, используемому в документе.

 Для получения дополнительной информации см. описание[ListCollection](../../com.aspose.words/listcollection) учебный класс.

**Возвращает:**
[ListCollection](../../com.aspose.words/listcollection) - соответствующий[ListCollection](../../com.aspose.words/listcollection) ценность.
### getNextMatchingNode(Node curNode) {#getNextMatchingNode-com.aspose.words.Node-}
```
public Node getNextMatchingNode(Node curNode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node) |  |

**Возвращает:**
[Node](../../com.aspose.words/node)
### getNextSibling() {#getNextSibling--}
```
public Node getNextSibling()
```


Получает узел, следующий сразу за этим узлом. Если следующего узла нет, возвращается нуль.

**Возвращает:**
[Node](../../com.aspose.words/node) - Узел, непосредственно следующий за этим узлом.
### getNodeChangingCallback() {#getNodeChangingCallback--}
```
public INodeChangingCallback getNodeChangingCallback()
```


Вызывается при вставке или удалении узла в документе.

**Возвращает:**
[INodeChangingCallback](../../com.aspose.words/inodechangingcallback) - соответствующий[INodeChangingCallback](../../com.aspose.words/inodechangingcallback) ценность.
### getNodeType() {#getNodeType--}
```
public abstract int getNodeType()
```


Получает тип этого узла.

**Возвращает:**
 int - Тип этого узла. Возвращаемое значение является одним из[NodeType](../../com.aspose.words/nodetype) константы.
### getPageColor() {#getPageColor--}
```
public Color getPageColor()
```


 Получает цвет страницы документа. Это свойство является упрощенной версией[getBackgroundShape()](../../com.aspose.words/documentbase\#getBackgroundShape--) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase\#setBackgroundShape-com.aspose.words.Shape-).

 Это свойство предоставляет простой способ указать сплошной цвет страницы для документа. Установка этого свойства создает и устанавливает соответствующий[getBackgroundShape()](../../com.aspose.words/documentbase\#getBackgroundShape--) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase\#setBackgroundShape-com.aspose.words.Shape-).

Если цвет страницы не задан (например, в документе нет формы фона), возвращает нулевой цвет.

**Возвращает:**
java.awt.Color — цвет страницы документа.
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
### getResourceLoadingCallback() {#getResourceLoadingCallback--}
```
public IResourceLoadingCallback getResourceLoadingCallback()
```


Позволяет контролировать загрузку внешних ресурсов.

**Возвращает:**
[IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) - соответствующий[IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) ценность.
### getStyles() {#getStyles--}
```
public StyleCollection getStyles()
```


Возвращает набор стилей, определенных в документе.

 Для получения дополнительной информации см. описание[StyleCollection](../../com.aspose.words/stylecollection) учебный класс.

**Возвращает:**
[StyleCollection](../../com.aspose.words/stylecollection) - Набор стилей, определенных в документе.
### getText() {#getText--}
```
public String getText()
```


Получает текст этого узла и всех его дочерних элементов.

 Возвращаемая строка включает все управляющие и специальные символы, как описано в[ControlChar](../../com.aspose.words/controlchar).

**Возвращает:**
java.lang.String
### getWarningCallback() {#getWarningCallback--}
```
public IWarningCallback getWarningCallback()
```


 Вызывается во время различных процедур обработки документов при обнаружении проблемы, которая может привести к потере точности данных или форматирования. Документ может генерировать предупреждения на любом этапе своего существования, поэтому важно настроить обратный вызов предупреждения как можно раньше, чтобы избежать потери предупреждений. Например, такие свойства, как[Document.getPageCount()](../../com.aspose.words/document\#getPageCount--) на самом деле создать макет документа, который позже используется для рендеринга, и предупреждения макета могут быть потеряны, если обратный вызов предупреждения указан только для вызовов рендеринга позже.

**Возвращает:**
[IWarningCallback](../../com.aspose.words/iwarningcallback) - соответствующий[IWarningCallback](../../com.aspose.words/iwarningcallback) ценность.
### hasChildNodes() {#hasChildNodes--}
```
public boolean hasChildNodes()
```


Возвращает true, если у этого узла есть дочерние узлы.

**Возвращает:**
boolean — Истинно, если у этого узла есть дочерние узлы.
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


Импортирует узел из другого документа в текущий документ.

Импортирует узел из другого документа в текущий документ.

 Этот метод использует[ImportFormatMode.USE\_DESTINATION\_STYLES](../../com.aspose.words/importformatmode\#USE-DESTINATION-STYLES) возможность разрешить форматирование.

При импорте узла создается копия исходного узла, принадлежащего импортируемому документу. Возвращенный узел не имеет родителя. Исходный узел не изменяется и не удаляется из исходного документа.

 Прежде чем узел из другого документа можно будет вставить в этот документ, его необходимо импортировать. Во время импорта свойства документа, такие как ссылки на стили и списки, переводятся из оригинала в импортируемый документ. После того, как узел был импортирован, его можно вставить в соответствующее место документа с помощью[CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertBefore-com.aspose.words.Node--com.aspose.words.Node-) или же[CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertAfter-com.aspose.words.Node--com.aspose.words.Node-).

Если исходный узел уже принадлежит целевому документу, то создается просто глубокий клон исходного узла.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcNode | [Node](../../com.aspose.words/node) | Импортируемый узел. |
| isImportChildren | boolean | Значение true для рекурсивного импорта всех дочерних узлов; в противном случае ложно. |

**Возвращает:**
[Node](../../com.aspose.words/node) Клонированный узел, принадлежащий текущему документу.
### importNode(Node srcNode, boolean isImportChildren, int importFormatMode) {#importNode-com.aspose.words.Node-boolean-int-}
```
public Node importNode(Node srcNode, boolean isImportChildren, int importFormatMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcNode | [Node](../../com.aspose.words/node) |  |
| isImportChildren | boolean |  |
| importFormatMode | int |  |

**Возвращает:**
[Node](../../com.aspose.words/node)
### indexOf(Node child) {#indexOf-com.aspose.words.Node-}
```
public int indexOf(Node child)
```


Возвращает индекс указанного дочернего узла в массиве дочерних узлов. Возвращает -1, если узел не найден среди дочерних узлов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| child | [Node](../../com.aspose.words/node) |  |

**Возвращает:**
инт
### insertAfter(Node newChild, Node refChild) {#insertAfter-com.aspose.words.Node-com.aspose.words.Node-}
```
public Node insertAfter(Node newChild, Node refChild)
```


Вставляет указанный узел сразу после указанного ссылочного узла.

Если refChild имеет значение null, вставляет newChild в начало списка дочерних узлов.

Если новый дочерний элемент уже находится в дереве, он сначала удаляется.

 Если вставляемый узел был создан из другого документа, следует использовать**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** чтобы импортировать узел в текущий документ. Затем импортированный узел можно вставить в текущий документ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | Узел для вставки. |
| refChild | [Node](../../com.aspose.words/node) | Узел, который является эталонным узлом. newNode размещается после refNode. |

**Возвращает:**
[Node](../../com.aspose.words/node) - Вставленный узел.
### insertBefore(Node newChild, Node refChild) {#insertBefore-com.aspose.words.Node-com.aspose.words.Node-}
```
public Node insertBefore(Node newChild, Node refChild)
```


Вставляет указанный узел непосредственно перед указанным ссылочным узлом.

Если refChild имеет значение null, вставляет newChild в конец списка дочерних узлов.

Если новый дочерний элемент уже находится в дереве, он сначала удаляется.

 Если вставляемый узел был создан из другого документа, следует использовать**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** чтобы импортировать узел в текущий документ. Затем импортированный узел можно вставить в текущий документ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | Узел для вставки. |
| refChild | [Node](../../com.aspose.words/node) | Узел, который является эталонным узлом. Новый дочерний элемент помещается перед этим узлом. |

**Возвращает:**
[Node](../../com.aspose.words/node) - Вставленный узел.
### isComposite() {#isComposite--}
```
public boolean isComposite()
```


Возвращает true, так как этот узел может иметь дочерние узлы.

**Возвращает:**
boolean — True, так как этот узел может иметь дочерние узлы.
### iterator() {#iterator--}
```
public Iterator iterator()
```


Обеспечивает поддержку для каждой итерации стиля над дочерними узлами этого узла.

**Возвращает:**
java.util.Iterator
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




### prependChild(Node newChild) {#prependChild-com.aspose.words.Node-}
```
public Node prependChild(Node newChild)
```


Добавляет указанный узел в начало списка дочерних узлов для этого узла.

Если новый дочерний элемент уже находится в дереве, он сначала удаляется.

 Если вставляемый узел был создан из другого документа, следует использовать**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** чтобы импортировать узел в текущий документ. Затем импортированный узел можно вставить в текущий документ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | Добавляемый узел. |

**Возвращает:**
[Node](../../com.aspose.words/node) - Добавлен узел.
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

### removeAllChildren() {#removeAllChildren--}
```
public void removeAllChildren()
```


Удаляет все дочерние узлы текущего узла.

### removeChild(Node oldChild) {#removeChild-com.aspose.words.Node-}
```
public Node removeChild(Node oldChild)
```


Удаляет указанный дочерний узел.

Родительский элемент oldChild устанавливается равным нулю после удаления узла.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| oldChild | [Node](../../com.aspose.words/node) | Узел для удаления. |

**Возвращает:**
[Node](../../com.aspose.words/node) - Удаленный узел.
### removeSmartTags() {#removeSmartTags--}
```
public void removeSmartTags()
```


 Удаляет все[SmartTag](../../com.aspose.words/smarttag) узлы-потомки текущего узла. Этот метод не удаляет содержимое смарт-тегов.

### selectNodes(String xpath) {#selectNodes-java.lang.String-}
```
public NodeList selectNodes(String xpath)
```


Выбирает список узлов, соответствующих выражению XPath.

На данный момент поддерживаются только выражения с именами элементов. Выражения, использующие имена атрибутов, не поддерживаются.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| xpath | java.lang.String | Выражение XPath. |

**Возвращает:**
[NodeList](../../com.aspose.words/nodelist) - Список узлов, соответствующих запросу XPath.
### selectSingleNode(String xpath) {#selectSingleNode-java.lang.String-}
```
public Node selectSingleNode(String xpath)
```


Выбирает первый узел, соответствующий выражению XPath.

На данный момент поддерживаются только выражения с именами элементов. Выражения, использующие имена атрибутов, не поддерживаются.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| xpath | java.lang.String | Выражение XPath. |

**Возвращает:**
[Node](../../com.aspose.words/node) - Первый узел, соответствующий запросу XPath, или нуль, если соответствующий узел не найден.
### setBackgroundShape(Shape value) {#setBackgroundShape-com.aspose.words.Shape-}
```
public void setBackgroundShape(Shape value)
```


Устанавливает форму фона документа. Может быть нулевым.

Microsoft Word допускает только ту форму, которая имеет свою[ShapeBase.getShapeType()](../../com.aspose.words/shapebase\#getShapeType--) свойство, равное[ShapeType.RECTANGLE](../../com.aspose.words/shapetype\#RECTANGLE) для использования в качестве фоновой формы для документа.

Microsoft Word поддерживает только свойства заливки фоновой фигуры. Все остальные свойства игнорируются.

 Установка для этого свойства ненулевого значения также установит[ViewOptions.getDisplayBackgroundShape()](../../com.aspose.words/viewoptions\#getDisplayBackgroundShape--) / [ViewOptions.setDisplayBackgroundShape(boolean)](../../com.aspose.words/viewoptions\#setDisplayBackgroundShape-boolean-) к истине.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [Shape](../../com.aspose.words/shape) | Форма фона документа. |

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

### setNodeChangingCallback(INodeChangingCallback value) {#setNodeChangingCallback-com.aspose.words.INodeChangingCallback-}
```
public void setNodeChangingCallback(INodeChangingCallback value)
```


Вызывается при вставке или удалении узла в документе.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [INodeChangingCallback](../../com.aspose.words/inodechangingcallback) |  Соответствующий[INodeChangingCallback](../../com.aspose.words/inodechangingcallback) ценность. |

### setPageColor(Color value) {#setPageColor-java.awt.Color-}
```
public void setPageColor(Color value)
```


 Устанавливает цвет страницы документа. Это свойство является упрощенной версией[getBackgroundShape()](../../com.aspose.words/documentbase\#getBackgroundShape--) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase\#setBackgroundShape-com.aspose.words.Shape-).

 Это свойство предоставляет простой способ указать сплошной цвет страницы для документа. Установка этого свойства создает и устанавливает соответствующий[getBackgroundShape()](../../com.aspose.words/documentbase\#getBackgroundShape--) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase\#setBackgroundShape-com.aspose.words.Shape-).

Если цвет страницы не задан (например, в документе нет формы фона), возвращает нулевой цвет.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.Color | Цвет страницы документа. |

### setResourceLoadingCallback(IResourceLoadingCallback value) {#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback-}
```
public void setResourceLoadingCallback(IResourceLoadingCallback value)
```


Позволяет контролировать загрузку внешних ресурсов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) |  Соответствующий[IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) ценность. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback-}
```
public void setWarningCallback(IWarningCallback value)
```


 Вызывается во время различных процедур обработки документов при обнаружении проблемы, которая может привести к потере точности данных или форматирования. Документ может генерировать предупреждения на любом этапе своего существования, поэтому важно настроить обратный вызов предупреждения как можно раньше, чтобы избежать потери предупреждений. Например, такие свойства, как[Document.getPageCount()](../../com.aspose.words/document\#getPageCount--) на самом деле создать макет документа, который позже используется для рендеринга, и предупреждения макета могут быть потеряны, если обратный вызов предупреждения указан только для вызовов рендеринга позже.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback) |  Соответствующий[IWarningCallback](../../com.aspose.words/iwarningcallback) ценность. |

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
