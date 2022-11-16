---
title: Footnote
second_title: Справочник по API Aspose.Words для Java
description: Представляет контейнер для текста сноски или концевой сноски.
type: docs
weight: 291
url: /ru/java/com.aspose.words/footnote/
---

**Наследование:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode), [com.aspose.words.InlineStory](../../com.aspose.words/inlinestory)
```
public class Footnote extends InlineStory
```

Представляет контейнер для текста сноски или концевой сноски.

 Чтобы узнать больше, посетите**Working with Footnote and Endnote** документальная статья.

**Footnote**класс используется для представления как сносок, так и концевых сносок в документе Word.

**Footnote** является узлом встроенного уровня и может быть только потомком**Paragraph**.

**Footnote** может содержать**Paragraph** а также**Table** дочерние узлы.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [Footnote(DocumentBase doc, int footnoteType)](#Footnote-com.aspose.words.DocumentBase-int-) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Принимает посетителя. |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node-) | Добавляет указанный узел в конец списка дочерних узлов для этого узла. |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [dd()](#dd--) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | Создает дубликат узла. |
| [ensureMinimum()](#ensureMinimum--) | Если последний дочерний элемент не является абзацем, создает и добавляет один пустой абзац. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int-) |  |
| [getAncestor(int ancestorType)](#getAncestor-int-) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class-) | Получает первого предка указанного типа объекта. |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean-) |  |
| [getChildNodes()](#getChildNodes--) | Получает все непосредственные дочерние узлы этого узла. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [getClass()](#getClass--) |  |
| [getContainer()](#getContainer--) |  |
| [getCount()](#getCount--) | Получает количество непосредственных дочерних элементов этого узла. |
| [getCurrentNode()](#getCurrentNode--) |  |
| [getCustomNodeId()](#getCustomNodeId--) | Задает идентификатор пользовательского узла. |
| [getDirectRunAttr(int fontAttr)](#getDirectRunAttr-int-) |  |
| [getDocument()](#getDocument--) | Получает документ, которому принадлежит этот узел. |
| [getDocument_IInline()](#getDocument-IInline--) |  |
| [getFirstChild()](#getFirstChild--) | Получает первый дочерний элемент узла. |
| [getFirstParagraph()](#getFirstParagraph--) | Получает первый абзац в истории. |
| [getFont()](#getFont--) | Предоставляет доступ к форматированию шрифта символа привязки этого объекта. |
| [getFootnoteType()](#getFootnoteType--) | Возвращает значение, указывающее, является ли это сноской или концевой сноской. |
| [getLastChild()](#getLastChild--) | Получает последний дочерний элемент узла. |
| [getLastParagraph()](#getLastParagraph--) | Получает последний абзац в истории. |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node-) |  |
| [getNextSibling()](#getNextSibling--) | Получает узел, следующий сразу за этим узлом. |
| [getNodeType()](#getNodeType--) |  Возвращает**NodeType.Footnote**. |
| [getParagraphs()](#getParagraphs--) | Получает коллекцию абзацев, которые являются непосредственными дочерними элементами истории. |
| [getParentNode()](#getParentNode--) | Получает непосредственного родителя этого узла. |
| [getParentParagraph()](#getParentParagraph--) |  Извлекает родителя[Paragraph](../../com.aspose.words/paragraph) этого узла. |
| [getParentParagraph_IInline()](#getParentParagraph-IInline--) |  |
| [getPreviousSibling()](#getPreviousSibling--) | Получает узел, непосредственно предшествующий этому узлу. |
| [getRange()](#getRange--) |  Возвращает**Range** объект, который представляет часть документа, содержащегося в этом узле. |
| [getReferenceMark()](#getReferenceMark--) | Получает/устанавливает пользовательскую контрольную метку, которая будет использоваться для этой сноски. |
| [getStoryType()](#getStoryType--) |  Возвращает**StoryType.Footnotes** или же**StoryType.Endnotes**. |
| [getTables()](#getTables--) | Получает коллекцию таблиц, которые являются непосредственными дочерними элементами истории. |
| [getText()](#getText--) | Получает текст этого узла и всех его дочерних элементов. |
| [hasChildNodes()](#hasChildNodes--) | Возвращает true, если у этого узла есть дочерние узлы. |
| [hashCode()](#hashCode--) |  |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node-) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node-) | Вставляет указанный узел сразу после указанного ссылочного узла. |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node-) | Вставляет указанный узел непосредственно перед указанным ссылочным узлом. |
| [isAuto()](#isAuto--) | Содержит значение, указывающее, является ли это сноской с автоматической нумерацией или сноской с определяемой пользователем пользовательской отметкой. |
| [isAuto(boolean value)](#isAuto-boolean-) | Содержит значение, указывающее, является ли это сноской с автоматической нумерацией или сноской с определяемой пользователем пользовательской отметкой. |
| [isComposite()](#isComposite--) | Возвращает true, так как этот узел может иметь дочерние узлы. |
| [isDeleteRevision()](#isDeleteRevision--) | Возвращает true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений. |
| [isInsertRevision()](#isInsertRevision--) | Возвращает true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений. |
| [isMoveFromRevision()](#isMoveFromRevision--) |  Возвращает**true** если этот объект был перемещен (удален) в Microsoft Word при включенном отслеживании изменений. |
| [isMoveToRevision()](#isMoveToRevision--) |  Возвращает**true** если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений. |
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
| [removeMoveRevisions()](#removeMoveRevisions--) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [removeSmartTags()](#removeSmartTags--) |  Удаляет все[SmartTag](../../com.aspose.words/smarttag) узлы-потомки текущего узла. |
| [selectNodes(String xpath)](#selectNodes-java.lang.String-) | Выбирает список узлов, соответствующих выражению XPath. |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String-) | Выбирает первый узел, соответствующий выражению XPath. |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | Задает идентификатор пользовательского узла. |
| [setReferenceMark(String value)](#setReferenceMark-java.lang.String-) | Получает/устанавливает пользовательскую контрольную метку, которая будет использоваться для этой сноски. |
| [setRunAttr(int fontAttr, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| [toString(int saveFormat)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### Footnote(DocumentBase doc, int footnoteType) {#Footnote-com.aspose.words.DocumentBase-int-}
```
public Footnote(DocumentBase doc, int footnoteType)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) |  |
| footnoteType | int |  |

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
boolean - Истинно, если были посещены все узлы; false, если DocumentVisitor остановил операцию перед посещением всех узлов. Вызывает DocumentVisitor.VisitFootnoteStart, затем вызывает Accept для всех дочерних узлов сноски и вызывает DocumentVisitor.VisitFootnoteEnd в конце.
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
### ensureMinimum() {#ensureMinimum--}
```
public void ensureMinimum()
```


Если последний дочерний элемент не является абзацем, создает и добавляет один пустой абзац.

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
### getFirstChild() {#getFirstChild--}
```
public Node getFirstChild()
```


Получает первый дочерний элемент узла. Если нет первого дочернего узла, возвращается нуль.

**Возвращает:**
[Node](../../com.aspose.words/node) - Первый дочерний узел.
### getFirstParagraph() {#getFirstParagraph--}
```
public Paragraph getFirstParagraph()
```


Получает первый абзац в истории.

**Возвращает:**
[Paragraph](../../com.aspose.words/paragraph) - Первый абзац рассказа.
### getFont() {#getFont--}
```
public Font getFont()
```


Предоставляет доступ к форматированию шрифта символа привязки этого объекта.

**Возвращает:**
[Font](../../com.aspose.words/font) - соответствующий[Font](../../com.aspose.words/font) ценность.
### getFootnoteType() {#getFootnoteType--}
```
public int getFootnoteType()
```


Возвращает значение, указывающее, является ли это сноской или концевой сноской.

**Возвращает:**
 int — значение, указывающее, является ли это сноской или концевой сноской. Возвращаемое значение является одним из[FootnoteType](../../com.aspose.words/footnotetype) константы.
### getLastChild() {#getLastChild--}
```
public Node getLastChild()
```


Получает последний дочерний элемент узла. Если последнего дочернего узла нет, возвращается нуль.

**Возвращает:**
[Node](../../com.aspose.words/node) - Последний дочерний узел.
### getLastParagraph() {#getLastParagraph--}
```
public Paragraph getLastParagraph()
```


Получает последний абзац в истории.

**Возвращает:**
[Paragraph](../../com.aspose.words/paragraph) - Последний абзац в рассказе.
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


 Возвращает**NodeType.Footnote**.

**Возвращает:**
 инт -**NodeType.Footnote** . Возвращаемое значение является одним из[NodeType](../../com.aspose.words/nodetype) константы.
### getParagraphs() {#getParagraphs--}
```
public ParagraphCollection getParagraphs()
```


Получает коллекцию абзацев, которые являются непосредственными дочерними элементами истории.

**Возвращает:**
[ParagraphCollection](../../com.aspose.words/paragraphcollection) - Набор абзацев, которые являются непосредственными потомками истории.
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
### getReferenceMark() {#getReferenceMark--}
```
public String getReferenceMark()
```


 Получает/устанавливает пользовательскую контрольную метку, которая будет использоваться для этой сноски. Значение по умолчанию**empty string**, что означает использование сносок с автоматической нумерацией.

 Если это свойство установлено в**empty string** или ноль, то[isAuto()](../../com.aspose.words/footnote\#isAuto--) / [isAuto(boolean)](../../com.aspose.words/footnote\#isAuto-boolean-) свойство будет автоматически установлено в true, если установлено что-либо другое, то[isAuto()](../../com.aspose.words/footnote\#isAuto--) / [isAuto(boolean)](../../com.aspose.words/footnote\#isAuto-boolean-)будет установлено значение false.

Формат RTF может хранить только 1 символ в качестве пользовательской контрольной метки, поэтому при экспорте будет записан только первый символ, остальные будут отброшены.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getStoryType() {#getStoryType--}
```
public int getStoryType()
```


 Возвращает**StoryType.Footnotes** или же**StoryType.Endnotes**.

**Возвращает:**
 инт -**StoryType.Footnotes** или же**StoryType.Endnotes** . Возвращаемое значение является одним из[StoryType](../../com.aspose.words/storytype) константы.
### getTables() {#getTables--}
```
public TableCollection getTables()
```


Получает коллекцию таблиц, которые являются непосредственными дочерними элементами истории.

**Возвращает:**
[TableCollection](../../com.aspose.words/tablecollection) - Коллекция таблиц, которые являются непосредственными дочерними элементами истории.
### getText() {#getText--}
```
public String getText()
```


Получает текст этого узла и всех его дочерних элементов.

 Возвращаемая строка включает все управляющие и специальные символы, как описано в[ControlChar](../../com.aspose.words/controlchar).

**Возвращает:**
java.lang.String
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
### isAuto() {#isAuto--}
```
public boolean isAuto()
```


 Содержит значение, указывающее, является ли это сноской с автоматической нумерацией или сноской с определяемой пользователем пользовательской отметкой.[getReferenceMark()](../../com.aspose.words/footnote\#getReferenceMark--) / [setReferenceMark(java.lang.String)](../../com.aspose.words/footnote\#setReferenceMark-java.lang.String-) инициализируется пустой строкой, если для параметра IsAuto установлено значение false.

**Возвращает:**
boolean - соответствующее логическое значение.
### isAuto(boolean value) {#isAuto-boolean-}
```
public void isAuto(boolean value)
```


 Содержит значение, указывающее, является ли это сноской с автоматической нумерацией или сноской с определяемой пользователем пользовательской отметкой.[getReferenceMark()](../../com.aspose.words/footnote\#getReferenceMark--) / [setReferenceMark(java.lang.String)](../../com.aspose.words/footnote\#setReferenceMark-java.lang.String-) инициализируется пустой строкой, если для параметра IsAuto установлено значение false.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### isComposite() {#isComposite--}
```
public boolean isComposite()
```


Возвращает true, так как этот узел может иметь дочерние узлы.

**Возвращает:**
boolean — True, так как этот узел может иметь дочерние узлы.
### isDeleteRevision() {#isDeleteRevision--}
```
public boolean isDeleteRevision()
```


Возвращает true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений.

**Возвращает:**
boolean — Истинно, если этот объект был удален в Microsoft Word при включенном отслеживании изменений.
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

### setReferenceMark(String value) {#setReferenceMark-java.lang.String-}
```
public void setReferenceMark(String value)
```


 Получает/устанавливает пользовательскую контрольную метку, которая будет использоваться для этой сноски. Значение по умолчанию**empty string**, что означает использование сносок с автоматической нумерацией.

 Если это свойство установлено в**empty string** или ноль, то[isAuto()](../../com.aspose.words/footnote\#isAuto--) / [isAuto(boolean)](../../com.aspose.words/footnote\#isAuto-boolean-) свойство будет автоматически установлено в true, если установлено что-либо другое, то[isAuto()](../../com.aspose.words/footnote\#isAuto--) / [isAuto(boolean)](../../com.aspose.words/footnote\#isAuto-boolean-)будет установлено значение false.

Формат RTF может хранить только 1 символ в качестве пользовательской контрольной метки, поэтому при экспорте будет записан только первый символ, остальные будут отброшены.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

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
