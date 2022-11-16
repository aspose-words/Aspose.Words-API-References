---
title: StructuredDocumentTagRangeStart
second_title: Справочник по API Aspose.Words для Java
description: Представляет начало тега ранжированного структурированного документа, который принимает содержимое, состоящее из нескольких разделов.
type: docs
weight: 535
url: /ru/java/com.aspose.words/structureddocumenttagrangestart/
---

**Наследование:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node)

**Все реализованные интерфейсы:**
[com.aspose.words.IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag), java.lang.Итерабельный
```
public class StructuredDocumentTagRangeStart extends Node implements IStructuredDocumentTag, Iterable
```

 Представляет собой начало**ranged** тег структурированного документа, который принимает содержимое из нескольких разделов. Смотрите также[StructuredDocumentTagRangeEnd](../../com.aspose.words/structureddocumenttagrangeend).

 Чтобы узнать больше, посетите**Structured Document Tags or Content Control** документальная статья.

 Может быть непосредственным потомком[Body](../../com.aspose.words/body) узел**only**.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [StructuredDocumentTagRangeStart(DocumentBase doc, int type)](#StructuredDocumentTagRangeStart-com.aspose.words.DocumentBase-int-) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) |  |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node-) | Добавляет указанный узел в конец диапазона stdContent. |
| [dd()](#dd--) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | Создает дубликат узла. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAncestor(int ancestorType)](#getAncestor-int-) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class-) | Получает первого предка указанного типа объекта. |
| [getChildNodes()](#getChildNodes--) | Получает все узлы между этим начальным узлом диапазона и конечным узлом диапазона. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [getClass()](#getClass--) |  |
| [getColor()](#getColor--) | Получает цвет тега структурированного документа. |
| [getCustomNodeId()](#getCustomNodeId--) | Задает идентификатор пользовательского узла. |
| [getDocument()](#getDocument--) | Получает документ, которому принадлежит этот узел. |
| [getId()](#getId--) | Указывает уникальный постоянный числовой идентификатор только для чтения для этого тега структурированного документа. |
| [getLastChild()](#getLastChild--) | Получает последний дочерний элемент в диапазоне stdContent. |
| [getLevel()](#getLevel--) | Получает уровень, на котором этот диапазон тегов структурированного документа начинается в дереве документа. |
| [getLockContentControl()](#getLockContentControl--) | Если установлено значение true, это свойство запрещает пользователю удалять этот структурированный тег документа. |
| [getLockContents()](#getLockContents--) | Если установлено значение true, это свойство запрещает пользователю редактировать содержимое этого тега структурированного документа. |
| [getNextSibling()](#getNextSibling--) | Получает узел, следующий сразу за этим узлом. |
| [getNodeType()](#getNodeType--) |  |
| [getParentNode()](#getParentNode--) | Получает непосредственного родителя этого узла. |
| [getPlaceholder()](#getPlaceholder--) |  Получает[BuildingBlock](../../com.aspose.words/buildingblock) содержащий текст-заполнитель, который должен отображаться, когда содержимое этого тега структурированного документа пусто, связанный сопоставленный XML-элемент пуст, как указано в параметре[getXmlMapping()](../../com.aspose.words/structureddocumenttagrangestart\#getXmlMapping--) элемент или[isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttagrangestart\#isShowingPlaceholderText--) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttagrangestart\#isShowingPlaceholderText-boolean-) элемент истинный. |
| [getPlaceholderName()](#getPlaceholderName--) |  Получает или задает имя[BuildingBlock](../../com.aspose.words/buildingblock) содержащий текст-заполнитель. |
| [getPreviousSibling()](#getPreviousSibling--) | Получает узел, непосредственно предшествующий этому узлу. |
| [getRange()](#getRange--) |  Возвращает**Range** объект, который представляет часть документа, содержащегося в этом узле. |
| [getRangeEnd()](#getRangeEnd--) | Указывает конец диапазона, если StructuredDocumentTag является ранжированным тегом структурированного документа. |
| [getSdtType()](#getSdtType--) | Получает тип этого тега структурированного документа. |
| [getTag()](#getTag--) | Указывает тег, связанный с текущим узлом тега структурированного документа. |
| [getText()](#getText--) | Получает текст этого узла и всех его дочерних элементов. |
| [getTitle()](#getTitle--) | Задает понятное имя, связанное с этим тегом структурированного документа. |
| [getWordOpenXML()](#getWordOpenXML--) |  Получает строку, представляющую XML, содержащийся в узле в[SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC) формат. |
| [getXmlMapping()](#getXmlMapping--) | Получает объект, представляющий сопоставление этого диапазона тегов структурированного документа с XML-данными в пользовательской XML-части текущего документа. |
| [hashCode()](#hashCode--) |  |
| [isComposite()](#isComposite--) | Возвращает true, если этот узел может содержать другие узлы. |
| [isRanged()](#isRanged--) |  |
| [isShowingPlaceholderText()](#isShowingPlaceholderText--) | Указывает, должно ли содержимое этого тега структурированного документа интерпретироваться как текст-заполнитель (в отличие от обычного текстового содержимого в теге структурированного документа). |
| [isShowingPlaceholderText(boolean value)](#isShowingPlaceholderText-boolean-) | Указывает, должно ли содержимое этого тега структурированного документа интерпретироваться как текст-заполнитель (в отличие от обычного текстового содержимого в теге структурированного документа). |
| [iterator()](#iterator--) | Обеспечивает поддержку для каждой итерации стиля над дочерними узлами этого узла. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node-) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int-) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node-) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [remove()](#remove--) | Удаляет себя из родителя. |
| [removeAllChildren()](#removeAllChildren--) | Удаляет все узлы между этим начальным узлом диапазона и конечным узлом диапазона. |
| [removeSelfOnly()](#removeSelfOnly--) | Удаляет это начало диапазона и соответствующие конечные узлы диапазона тега структурированного документа, но сохраняет его содержимое в дереве документа. |
| [setColor(Color value)](#setColor-java.awt.Color-) | Задает цвет тега структурированного документа. |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | Задает идентификатор пользовательского узла. |
| [setLockContentControl(boolean value)](#setLockContentControl-boolean-) | Если установлено значение true, это свойство запрещает пользователю удалять этот структурированный тег документа. |
| [setLockContents(boolean value)](#setLockContents-boolean-) | Если установлено значение true, это свойство запрещает пользователю редактировать содержимое этого тега структурированного документа. |
| [setPlaceholderName(String value)](#setPlaceholderName-java.lang.String-) |  Получает или задает имя[BuildingBlock](../../com.aspose.words/buildingblock) содержащий текст-заполнитель. |
| [setTag(String value)](#setTag-java.lang.String-) | Указывает тег, связанный с текущим узлом тега структурированного документа. |
| [setTitle(String value)](#setTitle-java.lang.String-) | Задает понятное имя, связанное с этим тегом структурированного документа. |
| [structuredDocumentTagNode()](#structuredDocumentTagNode--) |  |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| [toString(int saveFormat)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### StructuredDocumentTagRangeStart(DocumentBase doc, int type) {#StructuredDocumentTagRangeStart-com.aspose.words.DocumentBase-int-}
```
public StructuredDocumentTagRangeStart(DocumentBase doc, int type)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) |  |
| type | int |  |

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
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) |  |

**Возвращает:**
логический
### appendChild(Node newChild) {#appendChild-com.aspose.words.Node-}
```
public Node appendChild(Node newChild)
```


Добавляет указанный узел в конец диапазона stdContent.

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
### getChildNodes() {#getChildNodes--}
```
public NodeCollection getChildNodes()
```


Получает все узлы между этим начальным узлом диапазона и конечным узлом диапазона.

**Возвращает:**
[NodeCollection](../../com.aspose.words/nodecollection) - Все узлы между этим начальным узлом диапазона и конечным узлом диапазона.
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
### getColor() {#getColor--}
```
public Color getColor()
```


Получает цвет тега структурированного документа.

**Возвращает:**
java.awt.Color — цвет тега структурированного документа.
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
[DocumentBase](../../com.aspose.words/documentbase) - Документ, которому принадлежит этот узел.
### getId() {#getId--}
```
public int getId()
```


Указывает уникальный постоянный числовой идентификатор только для чтения для этого тега структурированного документа.

Атрибут Id должен соответствовать следующим правилам:

 *   Документ должен сохранять идентификаторы тегов структурированного документа, только если клонируется весь документ.[Document.deepClone()](../../com.aspose.words/document\#deepClone--).
 *   В течение[DocumentBase.importNode(com.aspose.words.Node, boolean)](../../com.aspose.words/documentbase\#importNode-com.aspose.words.Node--boolean-) Идентификатор должен быть сохранен, если импорт не вызывает конфликтов с другими идентификаторами тегов структурированного документа в целевом документе.
 *  Если несколько узлов тегов структурированного документа задают одно и то же значение десятичного числа для атрибута Id, то первый тег структурированного документа в документе должен поддерживать этот исходный идентификатор, а все последующие узлы тегов структурированного документа должны иметь новые идентификаторы, назначенные им при создании документа. загружен.
 *   Во время тега автономного структурированного документа**M:Aspose.Words.Markup.StructuredDocumentTag.Clone(System.Boolean,Aspose.Words.INodeCloningListener)** операции будет создан новый уникальный идентификатор для клонированного узла тега структурированного документа.
 *  Если Id не указан в исходном документе, то узел тега структурированного документа должен иметь новый уникальный идентификатор, назначенный ему при загрузке документа.

**Возвращает:**
int - соответствующее значение int.
### getLastChild() {#getLastChild--}
```
public Node getLastChild()
```


Получает последний дочерний элемент в диапазоне stdContent. Если последнего дочернего узла нет, возвращается нуль.

**Возвращает:**
[Node](../../com.aspose.words/node) - Последний дочерний элемент в диапазоне stdContent.
### getLevel() {#getLevel--}
```
public int getLevel()
```


Получает уровень, на котором этот диапазон тегов структурированного документа начинается в дереве документа.

**Возвращает:**
 int — уровень, на котором этот диапазон тегов структурированного документа начинается в дереве документа. Возвращаемое значение является одним из[MarkupLevel](../../com.aspose.words/markuplevel) константы.
### getLockContentControl() {#getLockContentControl--}
```
public boolean getLockContentControl()
```


Если установлено значение true, это свойство запрещает пользователю удалять этот структурированный тег документа.

**Возвращает:**
boolean - соответствующее логическое значение.
### getLockContents() {#getLockContents--}
```
public boolean getLockContents()
```


Если установлено значение true, это свойство запрещает пользователю редактировать содержимое этого тега структурированного документа.

**Возвращает:**
boolean - соответствующее логическое значение.
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


Получает тип этого узла.

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
### getPlaceholder() {#getPlaceholder--}
```
public BuildingBlock getPlaceholder()
```


 Получает[BuildingBlock](../../com.aspose.words/buildingblock) содержащий текст-заполнитель, который должен отображаться, когда содержимое этого тега структурированного документа пусто, связанный сопоставленный XML-элемент пуст, как указано в параметре[getXmlMapping()](../../com.aspose.words/structureddocumenttagrangestart\#getXmlMapping--) элемент или[isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttagrangestart\#isShowingPlaceholderText--) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttagrangestart\#isShowingPlaceholderText-boolean-)элемент истинный. Может быть нулевым, что означает, что заполнитель неприменим для этого тега структурированного документа.

**Возвращает:**
[BuildingBlock](../../com.aspose.words/buildingblock) -[BuildingBlock](../../com.aspose.words/buildingblock) содержащий текст-заполнитель, который должен отображаться, когда содержимое этого тега структурированного документа пусто, связанный сопоставленный XML-элемент пуст, как указано в параметре[getXmlMapping()](../../com.aspose.words/structureddocumenttagrangestart\#getXmlMapping--) элемент или[isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttagrangestart\#isShowingPlaceholderText--) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttagrangestart\#isShowingPlaceholderText-boolean-) элемент истинный.
### getPlaceholderName() {#getPlaceholderName--}
```
public String getPlaceholderName()
```


 Получает или задает имя[BuildingBlock](../../com.aspose.words/buildingblock) содержащий текст-заполнитель.

 BuildingBlock с этим названием[BuildingBlock.getName()](../../com.aspose.words/buildingblock\#getName--) / [BuildingBlock.setName(java.lang.String)](../../com.aspose.words/buildingblock\#setName-java.lang.String-) должен присутствовать в[Document.getGlossaryDocument()](../../com.aspose.words/document\#getGlossaryDocument--) / [Document.setGlossaryDocument(com.aspose.words.GlossaryDocument)](../../com.aspose.words/document\#setGlossaryDocument-com.aspose.words.GlossaryDocument-) в противном случае возникнет исключение java.lang.IllegalStateException.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
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
### getRangeEnd() {#getRangeEnd--}
```
public StructuredDocumentTagRangeEnd getRangeEnd()
```


Указывает конец диапазона, если StructuredDocumentTag является ранжированным тегом структурированного документа. В противном случае возвращает ноль.

**Возвращает:**
[StructuredDocumentTagRangeEnd](../../com.aspose.words/structureddocumenttagrangeend) - соответствующий[StructuredDocumentTagRangeEnd](../../com.aspose.words/structureddocumenttagrangeend) ценность.
### getSdtType() {#getSdtType--}
```
public int getSdtType()
```


Получает тип этого тега структурированного документа.

**Возвращает:**
 int - Тип этого тега структурированного документа. Возвращаемое значение является одним из[SdtType](../../com.aspose.words/sdttype) константы.
### getTag() {#getTag--}
```
public String getTag()
```


Указывает тег, связанный с текущим узлом тега структурированного документа. Не может быть нулевым. Тег — это произвольная строка, которую приложения могут ассоциировать со структурированным тегом документа, чтобы идентифицировать его, не предоставляя понятное имя.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getText() {#getText--}
```
public String getText()
```


Получает текст этого узла и всех его дочерних элементов.

 Возвращаемая строка включает все управляющие и специальные символы, как описано в[ControlChar](../../com.aspose.words/controlchar).

**Возвращает:**
java.lang.String
### getTitle() {#getTitle--}
```
public String getTitle()
```


Задает понятное имя, связанное с этим тегом структурированного документа. Не может быть нулевым.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getWordOpenXML() {#getWordOpenXML--}
```
public String getWordOpenXML()
```


 Получает строку, представляющую XML, содержащийся в узле в[SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC) формат.

**Возвращает:**
 java.lang.String — строка, представляющая XML, содержащийся в узле в[SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC) формат.
### getXmlMapping() {#getXmlMapping--}
```
public XmlMapping getXmlMapping()
```


 Получает объект, представляющий сопоставление этого диапазона тегов структурированного документа с XML-данными в пользовательской XML-части текущего документа. Вы можете использовать[XmlMapping.setMapping(com.aspose.words.CustomXmlPart, java.lang.String, java.lang.String)](../../com.aspose.words/xmlmapping\#setMapping-com.aspose.words.CustomXmlPart--java.lang.String--java.lang.String-) метод этого объекта для сопоставления диапазона тегов структурированного документа с данными XML.

**Возвращает:**
[XmlMapping](../../com.aspose.words/xmlmapping) Объект, представляющий сопоставление этого диапазона тегов структурированного документа с данными XML в пользовательской части XML текущего документа.
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
### isRanged() {#isRanged--}
```
public boolean isRanged()
```


Возвращает true, если этот экземпляр является ранжированным структурированным тегом документа.

**Возвращает:**
логический
### isShowingPlaceholderText() {#isShowingPlaceholderText--}
```
public boolean isShowingPlaceholderText()
```


Указывает, должно ли содержимое этого тега структурированного документа интерпретироваться как текст-заполнитель (в отличие от обычного текстового содержимого в теге структурированного документа).

если установлено значение true, это состояние должно быть возобновлено (показывая текст-заполнитель) при открытии этого документа.

**Возвращает:**
boolean - соответствующее логическое значение.
### isShowingPlaceholderText(boolean value) {#isShowingPlaceholderText-boolean-}
```
public void isShowingPlaceholderText(boolean value)
```


Указывает, должно ли содержимое этого тега структурированного документа интерпретироваться как текст-заполнитель (в отличие от обычного текстового содержимого в теге структурированного документа).

если установлено значение true, это состояние должно быть возобновлено (показывая текст-заполнитель) при открытии этого документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

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


Удаляет все узлы между этим начальным узлом диапазона и конечным узлом диапазона.

### removeSelfOnly() {#removeSelfOnly--}
```
public void removeSelfOnly()
```


Удаляет это начало диапазона и соответствующие конечные узлы диапазона тега структурированного документа, но сохраняет его содержимое в дереве документа.

### setColor(Color value) {#setColor-java.awt.Color-}
```
public void setColor(Color value)
```


Задает цвет тега структурированного документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.Color | Цвет тега структурированного документа. |

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

### setLockContentControl(boolean value) {#setLockContentControl-boolean-}
```
public void setLockContentControl(boolean value)
```


Если установлено значение true, это свойство запрещает пользователю удалять этот структурированный тег документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setLockContents(boolean value) {#setLockContents-boolean-}
```
public void setLockContents(boolean value)
```


Если установлено значение true, это свойство запрещает пользователю редактировать содержимое этого тега структурированного документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setPlaceholderName(String value) {#setPlaceholderName-java.lang.String-}
```
public void setPlaceholderName(String value)
```


 Получает или задает имя[BuildingBlock](../../com.aspose.words/buildingblock) содержащий текст-заполнитель.

 BuildingBlock с этим названием[BuildingBlock.getName()](../../com.aspose.words/buildingblock\#getName--) / [BuildingBlock.setName(java.lang.String)](../../com.aspose.words/buildingblock\#setName-java.lang.String-) должен присутствовать в[Document.getGlossaryDocument()](../../com.aspose.words/document\#getGlossaryDocument--) / [Document.setGlossaryDocument(com.aspose.words.GlossaryDocument)](../../com.aspose.words/document\#setGlossaryDocument-com.aspose.words.GlossaryDocument-) в противном случае возникнет исключение java.lang.IllegalStateException.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setTag(String value) {#setTag-java.lang.String-}
```
public void setTag(String value)
```


Указывает тег, связанный с текущим узлом тега структурированного документа. Не может быть нулевым. Тег — это произвольная строка, которую приложения могут ассоциировать со структурированным тегом документа, чтобы идентифицировать его, не предоставляя понятное имя.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setTitle(String value) {#setTitle-java.lang.String-}
```
public void setTitle(String value)
```


Задает понятное имя, связанное с этим тегом структурированного документа. Не может быть нулевым.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### structuredDocumentTagNode() {#structuredDocumentTagNode--}
```
public Node structuredDocumentTagNode()
```


Возвращает объект Node, реализующий этот интерфейс.

**Возвращает:**
[Node](../../com.aspose.words/node)
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
