---
title: BuildingBlock
second_title: Справочник по API Aspose.Words для Java
description: Представляет запись документа глоссария, такую как автотекст стандартного блока или запись автозамены.
type: docs
weight: 41
url: /ru/java/com.aspose.words/buildingblock/
---

**Наследование:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode)
```
public class BuildingBlock extends CompositeNode
```

Представляет запись документа глоссария, такую как стандартный блок, автотекст или запись автозамены.

 Чтобы узнать больше, посетите**Aspose.Words Document Object Model (DOM)** документальная статья.

[BuildingBlock](../../com.aspose.words/buildingblock) может содержать только[Section](../../com.aspose.words/section) узлы.

[BuildingBlock](../../com.aspose.words/buildingblock) может быть только ребенком[GlossaryDocument](../../com.aspose.words/glossarydocument).

Вы можете создавать новые стандартные блоки и вставлять их в глоссарий. Вы можете изменить или удалить существующие стандартные блоки. Вы можете копировать или перемещать стандартные блоки между документами. Вы можете вставить содержимое стандартного блока в документ.

 Соответствует**docPart**, **docPartPr** а также**docPartBody** элементы в OOXML.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [BuildingBlock(GlossaryDocument glossaryDoc)](#BuildingBlock-com.aspose.words.GlossaryDocument-) | Инициализирует новый экземпляр этого класса. |
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
| [getBehavior()](#getBehavior--) | Определяет поведение, которое должно применяться, когда содержимое стандартного блока вставляется в основной документ. |
| [getCategory()](#getCategory--) | Указывает категоризацию второго уровня для стандартного блока. |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean-) |  |
| [getChildNodes()](#getChildNodes--) | Получает все непосредственные дочерние узлы этого узла. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [getClass()](#getClass--) |  |
| [getContainer()](#getContainer--) |  |
| [getCount()](#getCount--) | Получает количество непосредственных дочерних элементов этого узла. |
| [getCurrentNode()](#getCurrentNode--) |  |
| [getCustomNodeId()](#getCustomNodeId--) | Задает идентификатор пользовательского узла. |
| [getDescription()](#getDescription--) | Получает описание, связанное с этим стандартным блоком. |
| [getDocument()](#getDocument--) | Получает документ, которому принадлежит этот узел. |
| [getFirstChild()](#getFirstChild--) | Получает первый дочерний элемент узла. |
| [getFirstSection()](#getFirstSection--) | Получает первый раздел в стандартном блоке. |
| [getGallery()](#getGallery--) | Задает категоризацию первого уровня для стандартного блока в целях классификации или сортировки пользовательского интерфейса. |
| [getGuid()](#getGuid--) | Получает идентификатор (128-разрядный GUID), однозначно идентифицирующий этот стандартный блок. |
| [getLastChild()](#getLastChild--) | Получает последний дочерний элемент узла. |
| [getLastSection()](#getLastSection--) | Получает последний раздел в стандартном блоке. |
| [getName()](#getName--) | Получает имя этого стандартного блока. |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node-) |  |
| [getNextSibling()](#getNextSibling--) | Получает узел, следующий сразу за этим узлом. |
| [getNodeType()](#getNodeType--) |  Возвращает[NodeType.BUILDING\_BLOCK](../../com.aspose.words/nodetype\#BUILDING-BLOCK) ценность. |
| [getParentNode()](#getParentNode--) | Получает непосредственного родителя этого узла. |
| [getPreviousSibling()](#getPreviousSibling--) | Получает узел, непосредственно предшествующий этому узлу. |
| [getRange()](#getRange--) |  Возвращает**Range** объект, который представляет часть документа, содержащегося в этом узле. |
| [getSections()](#getSections--) | Возвращает коллекцию, представляющую все разделы стандартного блока. |
| [getText()](#getText--) | Получает текст этого узла и всех его дочерних элементов. |
| [getType()](#getType--) | Задает тип стандартного блока. |
| [hasChildNodes()](#hasChildNodes--) | Возвращает true, если у этого узла есть дочерние узлы. |
| [hashCode()](#hashCode--) |  |
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
| [setBehavior(int value)](#setBehavior-int-) | Определяет поведение, которое должно применяться, когда содержимое стандартного блока вставляется в основной документ. |
| [setCategory(String value)](#setCategory-java.lang.String-) | Указывает категоризацию второго уровня для стандартного блока. |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | Задает идентификатор пользовательского узла. |
| [setDescription(String value)](#setDescription-java.lang.String-) | Задает описание, связанное с этим стандартным блоком. |
| [setGallery(int value)](#setGallery-int-) | Задает категоризацию первого уровня для стандартного блока в целях классификации или сортировки пользовательского интерфейса. |
| [setGuid(UUID value)](#setGuid-java.util.UUID-) | Задает идентификатор (128-разрядный GUID), однозначно идентифицирующий этот стандартный блок. |
| [setName(String value)](#setName-java.lang.String-) | Задает имя этого стандартного блока. |
| [setType(int value)](#setType-int-) | Задает тип стандартного блока. |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| [toString(int saveFormat)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### BuildingBlock(GlossaryDocument glossaryDoc) {#BuildingBlock-com.aspose.words.GlossaryDocument-}
```
public BuildingBlock(GlossaryDocument glossaryDoc)
```


Инициализирует новый экземпляр этого класса.

 Когда[BuildingBlock](../../com.aspose.words/buildingblock) создан, он принадлежит указанному документу глоссария, но еще не является частью документа глоссария и[Node.getParentNode()](../../com.aspose.words/node\#getParentNode--) нулевой .

 Чтобы добавить[BuildingBlock](../../com.aspose.words/buildingblock) к[GlossaryDocument](../../com.aspose.words/glossarydocument) использовать[CompositeNode.appendChild(com.aspose.words.Node)](../../com.aspose.words/compositenode\#appendChild-com.aspose.words.Node-).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| glossaryDoc | [GlossaryDocument](../../com.aspose.words/glossarydocument) | Документ владельца. |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public boolean accept(DocumentVisitor visitor)
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

 Звонки[DocumentVisitor.visitBuildingBlockStart(com.aspose.words.BuildingBlock)](../../com.aspose.words/documentvisitor\#visitBuildingBlockStart-com.aspose.words.BuildingBlock-) , затем звонит[Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node\#accept-com.aspose.words.DocumentVisitor-) для всех дочерних узлов этого строительного блока, затем вызывает[DocumentVisitor.visitBuildingBlockEnd(com.aspose.words.BuildingBlock)](../../com.aspose.words/documentvisitor\#visitBuildingBlockEnd-com.aspose.words.BuildingBlock-).

Примечание. Узел стандартного блока и его дочерние элементы не посещаются, когда вы выполняете посетителя над узлом.[Document](../../com.aspose.words/document) . Если вы хотите выполнить посетителя над строительным блоком, вам нужно выполнить посетителя над[GlossaryDocument](../../com.aspose.words/glossarydocument) или позвоните по телефону[accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/buildingblock\#accept-com.aspose.words.DocumentVisitor-).
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
### getBehavior() {#getBehavior--}
```
public int getBehavior()
```


Определяет поведение, которое должно применяться, когда содержимое стандартного блока вставляется в основной документ.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[BuildingBlockBehavior](../../com.aspose.words/buildingblockbehavior) константы.
### getCategory() {#getCategory--}
```
public String getCategory()
```


Указывает категоризацию второго уровня для стандартного блока.

 Стандартные блоки в пользовательском интерфейсе Microsoft Word объединены в галереи. Каждый[getGallery()](../../com.aspose.words/buildingblock\#getGallery--) / [setGallery(int)](../../com.aspose.words/buildingblock\#setGallery-int-) может иметь несколько категорий. Каждый блок внутри[getCategory()](../../com.aspose.words/buildingblock\#getCategory--) / [setCategory(java.lang.String)](../../com.aspose.words/buildingblock\#setCategory-java.lang.String-) имеет[getName()](../../com.aspose.words/buildingblock\#getName--) / [setName(java.lang.String)](../../com.aspose.words/buildingblock\#setName-java.lang.String-).

Не может быть нулевым и не может быть пустой строкой.

 Соответствует**docPartPr.category.name** элемент в OOXML.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
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
### getDescription() {#getDescription--}
```
public String getDescription()
```


Получает описание, связанное с этим стандартным блоком.

Описание может содержать любое строковое содержимое, обычно дополнительную информацию.

Не может быть null , но может быть пустой строкой.

 Соответствует**docPartPr.description** элемент в OOXML.

**Возвращает:**
java.lang.String — описание, связанное с этим строительным блоком.
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


Получает документ, которому принадлежит этот узел.

Узел всегда принадлежит документу, даже если он только что создан и еще не добавлен в дерево или удален из дерева.

**Возвращает:**
[DocumentBase](../../com.aspose.words/documentbase) - Документ, которому принадлежит этот узел.
### getFirstChild() {#getFirstChild--}
```
public Node getFirstChild()
```


Получает первый дочерний элемент узла. Если нет первого дочернего узла, возвращается нуль.

**Возвращает:**
[Node](../../com.aspose.words/node) - Первый дочерний узел.
### getFirstSection() {#getFirstSection--}
```
public Section getFirstSection()
```


Получает первый раздел в стандартном блоке. Возвращает null, если разделов нет.

**Возвращает:**
[Section](../../com.aspose.words/section) - Первая секция в строительном блоке.
### getGallery() {#getGallery--}
```
public int getGallery()
```


Задает категоризацию первого уровня для стандартного блока в целях классификации или сортировки пользовательского интерфейса.

 Стандартные блоки в пользовательском интерфейсе Microsoft Word объединены в галереи. Каждый[getGallery()](../../com.aspose.words/buildingblock\#getGallery--) / [setGallery(int)](../../com.aspose.words/buildingblock\#setGallery-int-) может иметь несколько категорий. Каждый блок внутри[getCategory()](../../com.aspose.words/buildingblock\#getCategory--) / [setCategory(java.lang.String)](../../com.aspose.words/buildingblock\#setCategory-java.lang.String-) имеет[getName()](../../com.aspose.words/buildingblock\#getName--) / [setName(java.lang.String)](../../com.aspose.words/buildingblock\#setName-java.lang.String-).

 Соответствует**docPartPr.category.gallery** элемент в OOXML.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[BuildingBlockGallery](../../com.aspose.words/buildingblockgallery) константы.
### getGuid() {#getGuid--}
```
public UUID getGuid()
```


Получает идентификатор (128-разрядный GUID), однозначно идентифицирующий этот стандартный блок.

Может использоваться приложением для уникальной ссылки на строительный блок независимо от другого имени из-за локализации.

 Соответствует**docPartPr.guid** элемент в OOXML.

**Возвращает:**
java.util.UUID — идентификатор (128-битный GUID), однозначно идентифицирующий этот строительный блок.
### getLastChild() {#getLastChild--}
```
public Node getLastChild()
```


Получает последний дочерний элемент узла. Если последнего дочернего узла нет, возвращается нуль.

**Возвращает:**
[Node](../../com.aspose.words/node) - Последний дочерний узел.
### getLastSection() {#getLastSection--}
```
public Section getLastSection()
```


Получает последний раздел в стандартном блоке. Возвращает null, если разделов нет.

**Возвращает:**
[Section](../../com.aspose.words/section) - Последний раздел в строительном блоке.
### getName() {#getName--}
```
public String getName()
```


Получает имя этого стандартного блока.

Имя может содержать любое строковое содержимое, обычно дружественный идентификатор. Несколько строительных блоков могут иметь одно и то же имя.

Не может быть нулевым и не может быть пустой строкой.

 Соответствует**docPartPr.name** элемент в OOXML.

**Возвращает:**
java.lang.String — имя этого стандартного блока.
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
### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


 Возвращает[NodeType.BUILDING\_BLOCK](../../com.aspose.words/nodetype\#BUILDING-BLOCK) ценность.

**Возвращает:**
 интервал -[NodeType.BUILDING\_BLOCK](../../com.aspose.words/nodetype\#BUILDING-BLOCK) ценность. Возвращаемое значение является одним из[NodeType](../../com.aspose.words/nodetype) константы.
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
### getSections() {#getSections--}
```
public SectionCollection getSections()
```


Возвращает коллекцию, представляющую все разделы стандартного блока.

**Возвращает:**
[SectionCollection](../../com.aspose.words/sectioncollection) - Коллекция, представляющая все разделы в строительном блоке.
### getText() {#getText--}
```
public String getText()
```


Получает текст этого узла и всех его дочерних элементов.

 Возвращаемая строка включает все управляющие и специальные символы, как описано в[ControlChar](../../com.aspose.words/controlchar).

**Возвращает:**
java.lang.String
### getType() {#getType--}
```
public int getType()
```


Задает тип стандартного блока.

Тип стандартного блока может влиять на видимость и поведение стандартного блока в Microsoft Word.

 Соответствует**docPartPr.types** элемент в OOXML.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[BuildingBlockType](../../com.aspose.words/buildingblocktype) константы.
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
### setBehavior(int value) {#setBehavior-int-}
```
public void setBehavior(int value)
```


Определяет поведение, которое должно применяться, когда содержимое стандартного блока вставляется в основной документ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[BuildingBlockBehavior](../../com.aspose.words/buildingblockbehavior) константы. |

### setCategory(String value) {#setCategory-java.lang.String-}
```
public void setCategory(String value)
```


Указывает категоризацию второго уровня для стандартного блока.

 Стандартные блоки в пользовательском интерфейсе Microsoft Word объединены в галереи. Каждый[getGallery()](../../com.aspose.words/buildingblock\#getGallery--) / [setGallery(int)](../../com.aspose.words/buildingblock\#setGallery-int-) может иметь несколько категорий. Каждый блок внутри[getCategory()](../../com.aspose.words/buildingblock\#getCategory--) / [setCategory(java.lang.String)](../../com.aspose.words/buildingblock\#setCategory-java.lang.String-) имеет[getName()](../../com.aspose.words/buildingblock\#getName--) / [setName(java.lang.String)](../../com.aspose.words/buildingblock\#setName-java.lang.String-).

Не может быть нулевым и не может быть пустой строкой.

 Соответствует**docPartPr.category.name** элемент в OOXML.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

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

### setDescription(String value) {#setDescription-java.lang.String-}
```
public void setDescription(String value)
```


Задает описание, связанное с этим стандартным блоком.

Описание может содержать любое строковое содержимое, обычно дополнительную информацию.

Не может быть null , но может быть пустой строкой.

 Соответствует**docPartPr.description** элемент в OOXML.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Описание, связанное с этим стандартным блоком. |

### setGallery(int value) {#setGallery-int-}
```
public void setGallery(int value)
```


Задает категоризацию первого уровня для стандартного блока в целях классификации или сортировки пользовательского интерфейса.

 Стандартные блоки в пользовательском интерфейсе Microsoft Word объединены в галереи. Каждый[getGallery()](../../com.aspose.words/buildingblock\#getGallery--) / [setGallery(int)](../../com.aspose.words/buildingblock\#setGallery-int-) может иметь несколько категорий. Каждый блок внутри[getCategory()](../../com.aspose.words/buildingblock\#getCategory--) / [setCategory(java.lang.String)](../../com.aspose.words/buildingblock\#setCategory-java.lang.String-) имеет[getName()](../../com.aspose.words/buildingblock\#getName--) / [setName(java.lang.String)](../../com.aspose.words/buildingblock\#setName-java.lang.String-).

 Соответствует**docPartPr.category.gallery** элемент в OOXML.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[BuildingBlockGallery](../../com.aspose.words/buildingblockgallery) константы. |

### setGuid(UUID value) {#setGuid-java.util.UUID-}
```
public void setGuid(UUID value)
```


Задает идентификатор (128-разрядный GUID), однозначно идентифицирующий этот стандартный блок.

Может использоваться приложением для уникальной ссылки на строительный блок независимо от другого имени из-за локализации.

 Соответствует**docPartPr.guid** элемент в OOXML.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.util.UUID | Идентификатор (128-разрядный GUID), однозначно идентифицирующий этот стандартный блок. |

### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


Задает имя этого стандартного блока.

Имя может содержать любое строковое содержимое, обычно дружественный идентификатор. Несколько строительных блоков могут иметь одно и то же имя.

Не может быть нулевым и не может быть пустой строкой.

 Соответствует**docPartPr.name** элемент в OOXML.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя этого строительного блока. |

### setType(int value) {#setType-int-}
```
public void setType(int value)
```


Задает тип стандартного блока.

Тип стандартного блока может влиять на видимость и поведение стандартного блока в Microsoft Word.

 Соответствует**docPartPr.types** элемент в OOXML.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[BuildingBlockType](../../com.aspose.words/buildingblocktype) константы. |

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
