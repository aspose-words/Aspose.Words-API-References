---
title: Paragraph
second_title: Справочник по API Aspose.Words для Java
description: Представляет абзац текста.
type: docs
weight: 443
url: /ru/java/com.aspose.words/paragraph/
---

**Наследование:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode)
```
public class Paragraph extends CompositeNode
```

Представляет абзац текста.

 Чтобы узнать больше, посетите**Working with Paragraphs** документальная статья.

[Paragraph](../../com.aspose.words/paragraph) является узлом блочного уровня и может быть дочерним по отношению к классам, производным от[Story](../../com.aspose.words/story) или же[InlineStory](../../com.aspose.words/inlinestory).

[Paragraph](../../com.aspose.words/paragraph) может содержать любое количество встроенных узлов и закладок.

 Полный список дочерних узлов, которые могут находиться внутри абзаца, состоит из[BookmarkStart](../../com.aspose.words/bookmarkstart), [BookmarkEnd](../../com.aspose.words/bookmarkend), [FieldStart](../../com.aspose.words/fieldstart), [FieldSeparator](../../com.aspose.words/fieldseparator), [FieldEnd](../../com.aspose.words/fieldend), [FormField](../../com.aspose.words/formfield), [Comment](../../com.aspose.words/comment), [Footnote](../../com.aspose.words/footnote), [Run](../../com.aspose.words/run), [SpecialChar](../../com.aspose.words/specialchar), [Shape](../../com.aspose.words/shape), [GroupShape](../../com.aspose.words/groupshape), [SmartTag](../../com.aspose.words/smarttag).

Действительный абзац в Microsoft Word всегда заканчивается символом разрыва абзаца, а минимальный допустимый абзац состоит только из разрыва абзаца.**Paragraph** class автоматически добавляет соответствующий символ разрыва абзаца в конце, и этот символ не является частью дочерних узлов класса.**Paragraph** , поэтому**Paragraph** может быть пустым.

 Не включать конец абзаца[ControlChar.PARAGRAPH\_BREAK](../../com.aspose.words/controlchar\#PARAGRAPH-BREAK) или конец ячейки[ControlChar.CELL](../../com.aspose.words/controlchar\#CELL) символов внутри текста абзаца, так как это может сделать абзац недействительным при открытии документа в Microsoft Word.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [Paragraph(DocumentBase doc)](#Paragraph-com.aspose.words.DocumentBase-) |  Инициализирует новый экземпляр**Paragraph** учебный класс. |
## Методы

| Метод | Описание |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Принимает посетителя. |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node-) | Добавляет указанный узел в конец списка дочерних узлов для этого узла. |
| [appendField(int fieldType, boolean updateField)](#appendField-int-boolean-) |  |
| [appendField(String fieldCode)](#appendField-java.lang.String-) | Добавляет поле Word к этому абзацу. |
| [appendField(String fieldCode, String fieldValue)](#appendField-java.lang.String-java.lang.String-) | Добавляет поле Word к этому абзацу. |
| [clearParaAttrs()](#clearParaAttrs--) |  |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [dd()](#dd--) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | Создает дубликат узла. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedParaAttr(int key)](#fetchInheritedParaAttr-int-) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int-) |  |
| [fetchParaAttr(int key)](#fetchParaAttr-int-) |  |
| [getAncestor(int ancestorType)](#getAncestor-int-) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class-) | Получает первого предка указанного типа объекта. |
| [getBreakIsStyleSeparator()](#getBreakIsStyleSeparator--) | Истинно, если этот разрыв абзаца является разделителем стилей. |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean-) |  |
| [getChildNodes()](#getChildNodes--) | Получает все непосредственные дочерние узлы этого узла. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [getClass()](#getClass--) |  |
| [getContainer()](#getContainer--) |  |
| [getCount()](#getCount--) | Получает количество непосредственных дочерних элементов этого узла. |
| [getCurrentNode()](#getCurrentNode--) |  |
| [getCustomNodeId()](#getCustomNodeId--) | Задает идентификатор пользовательского узла. |
| [getDirectParaAttr(int key)](#getDirectParaAttr-int-) |  |
| [getDirectParaAttr(int key, int revisionsView)](#getDirectParaAttr-int-int-) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int-) |  |
| [getDocument()](#getDocument--) | Получает документ, которому принадлежит этот узел. |
| [getEffectiveTabStops()](#getEffectiveTabStops--) | Возвращает массив всех позиций табуляции, примененных к этому абзацу, в том числе примененных косвенно с помощью стилей или списков. |
| [getFirstChild()](#getFirstChild--) | Получает первый дочерний элемент узла. |
| [getFrameFormat()](#getFrameFormat--) | Предоставляет доступ к свойствам форматирования абзаца. |
| [getLastChild()](#getLastChild--) | Получает последний дочерний элемент узла. |
| [getListFormat()](#getListFormat--) | Предоставляет доступ к свойствам форматирования списка абзаца. |
| [getListLabel()](#getListLabel--) | Получает[getListLabel()](../../com.aspose.words/paragraph\#getListLabel--) объект, предоставляющий доступ к нумерации списка и форматированию этого абзаца. |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node-) |  |
| [getNextSibling()](#getNextSibling--) | Получает узел, следующий сразу за этим узлом. |
| [getNodeType()](#getNodeType--) |  Возвращает**NodeType.Paragraph**. |
| [getParagraphBreakFont()](#getParagraphBreakFont--) | Предоставляет доступ к форматированию шрифта символа разрыва абзаца. |
| [getParagraphFormat()](#getParagraphFormat--) | Предоставляет доступ к свойствам форматирования абзаца. |
| [getParentNode()](#getParentNode--) | Получает непосредственного родителя этого узла. |
| [getParentSection()](#getParentSection--) |  Извлекает родителя[Section](../../com.aspose.words/section) параграфа. |
| [getParentStory()](#getParentStory--) |  Извлекает историю на уровне родительского раздела, которую можно[Body](../../com.aspose.words/body) или же[HeaderFooter](../../com.aspose.words/headerfooter). |
| [getPreviousSibling()](#getPreviousSibling--) | Получает узел, непосредственно предшествующий этому узлу. |
| [getRange()](#getRange--) |  Возвращает**Range** объект, который представляет часть документа, содержащегося в этом узле. |
| [getRuns()](#getRuns--) | Предоставляет доступ к типизированной коллекции фрагментов текста внутри абзаца. |
| [getText()](#getText--) | Получает текст этого абзаца, включая символ конца абзаца. |
| [hasChildNodes()](#hasChildNodes--) | Возвращает true, если у этого узла есть дочерние узлы. |
| [hashCode()](#hashCode--) |  |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node-) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node-) | Вставляет указанный узел сразу после указанного ссылочного узла. |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node-) | Вставляет указанный узел непосредственно перед указанным ссылочным узлом. |
| [insertField(int fieldType, boolean updateField, Node refNode, boolean isAfter)](#insertField-int-boolean-com.aspose.words.Node-boolean-) |  |
| [insertField(String fieldCode, Node refNode, boolean isAfter)](#insertField-java.lang.String-com.aspose.words.Node-boolean-) | Вставляет поле Word в этот абзац. |
| [insertField(String fieldCode, String fieldValue, Node refNode, boolean isAfter)](#insertField-java.lang.String-java.lang.String-com.aspose.words.Node-boolean-) | Вставляет поле Word в этот абзац. |
| [isComposite()](#isComposite--) | Возвращает true, так как этот узел может иметь дочерние узлы. |
| [isDeleteRevision()](#isDeleteRevision--) | Возвращает true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений. |
| [isEndOfCell()](#isEndOfCell--) |  Истинно, если этот абзац является последним абзацем в[Cell](../../com.aspose.words/cell); ложно в противном случае. |
| [isEndOfDocument()](#isEndOfDocument--) | Истинно, если этот абзац является последним абзацем в последнем разделе документа. |
| [isEndOfHeaderFooter()](#isEndOfHeaderFooter--) |  Истинно, если этот абзац является последним абзацем в**HeaderFooter** (рассказ основного текста)**Section**; ложно в противном случае. |
| [isEndOfSection()](#isEndOfSection--) |  Истинно, если этот абзац является последним абзацем в**Body** (рассказ основного текста)**Section**; ложно в противном случае. |
| [isFormatRevision()](#isFormatRevision--) | Возвращает true, если форматирование объекта было изменено в Microsoft Word при включенном отслеживании изменений. |
| [isInCell()](#isInCell--) |  Истинно, если этот абзац является непосредственным потомком[Cell](../../com.aspose.words/cell); ложно в противном случае. |
| [isInsertRevision()](#isInsertRevision--) | Возвращает true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений. |
| [isListItem()](#isListItem--) | Истинно, если абзац является элементом маркированного или нумерованного списка в исходной редакции. |
| [isMoveFromRevision()](#isMoveFromRevision--) |  Возвращает**true** если этот объект был перемещен (удален) в Microsoft Word при включенном отслеживании изменений. |
| [isMoveToRevision()](#isMoveToRevision--) |  Возвращает**true** если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений. |
| [iterator()](#iterator--) | Обеспечивает поддержку для каждой итерации стиля над дочерними узлами этого узла. |
| [joinRunsWithSameFormatting()](#joinRunsWithSameFormatting--) | Соединения выполняются с тем же форматированием, что и абзац. |
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
| [removeParaAttr(int key)](#removeParaAttr-int-) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [removeSmartTags()](#removeSmartTags--) |  Удаляет все[SmartTag](../../com.aspose.words/smarttag) узлы-потомки текущего узла. |
| [selectNodes(String xpath)](#selectNodes-java.lang.String-) | Выбирает список узлов, соответствующих выражению XPath. |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String-) | Выбирает первый узел, соответствующий выражению XPath. |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | Задает идентификатор пользовательского узла. |
| [setParaAttr(int key, Object value)](#setParaAttr-int-java.lang.Object-) |  |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| [toString(int saveFormat)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### Paragraph(DocumentBase doc) {#Paragraph-com.aspose.words.DocumentBase-}
```
public Paragraph(DocumentBase doc)
```


 Инициализирует новый экземпляр**Paragraph** учебный класс.

 Когда**Paragraph** создан, он принадлежит указанному документу, но еще не является его частью и**ParentNode** нулевой.

 Чтобы добавить**Paragraph** к документу используйте InsertAfter или InsertBefore для статьи, в которую вы хотите вставить абзац.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) | Документ владельца. |

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
boolean - Истинно, если были посещены все узлы; false, если DocumentVisitor остановил операцию перед посещением всех узлов. Вызывает DocumentVisitor.VisitParagraphStart, затем вызывает Accept для всех дочерних узлов абзаца и вызывает DocumentVisitor.VisitParagraphEnd в конце.
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
### appendField(int fieldType, boolean updateField) {#appendField-int-boolean-}
```
public Field appendField(int fieldType, boolean updateField)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldType | int |  |
| updateField | boolean |  |

**Возвращает:**
[Field](../../com.aspose.words/field)
### appendField(String fieldCode) {#appendField-java.lang.String-}
```
public Field appendField(String fieldCode)
```


Добавляет поле Word к этому абзацу. Добавляет поле к этому абзацу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldCode | java.lang.String | Код поля для добавления (без фигурных скобок). |

**Возвращает:**
[Field](../../com.aspose.words/field) - А[Field](../../com.aspose.words/field) объект, который представляет добавленное поле.
### appendField(String fieldCode, String fieldValue) {#appendField-java.lang.String-java.lang.String-}
```
public Field appendField(String fieldCode, String fieldValue)
```


Добавляет поле Word к этому абзацу. Добавляет поле к этому абзацу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldCode | java.lang.String | Код поля для добавления (без фигурных скобок). |
| fieldValue | java.lang.String | Значение поля для добавления. Передайте null для полей, которые не имеют значения. |

**Возвращает:**
[Field](../../com.aspose.words/field) - А[Field](../../com.aspose.words/field) объект, который представляет добавленное поле.
### clearParaAttrs() {#clearParaAttrs--}
```
public void clearParaAttrs()
```




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
### fetchInheritedParaAttr(int key) {#fetchInheritedParaAttr-int-}
```
public Object fetchInheritedParaAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### fetchInheritedRunAttr(int key) {#fetchInheritedRunAttr-int-}
```
public Object fetchInheritedRunAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### fetchParaAttr(int key) {#fetchParaAttr-int-}
```
public Object fetchParaAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

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
### getBreakIsStyleSeparator() {#getBreakIsStyleSeparator--}
```
public boolean getBreakIsStyleSeparator()
```


Истинно, если этот разрыв абзаца является разделителем стилей. Разделитель стилей позволяет одному абзацу состоять из частей с разными стилями абзаца.

**Возвращает:**
boolean - соответствующее логическое значение.
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
### getDirectParaAttr(int key) {#getDirectParaAttr-int-}
```
public Object getDirectParaAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### getDirectParaAttr(int key, int revisionsView) {#getDirectParaAttr-int-int-}
```
public Object getDirectParaAttr(int key, int revisionsView)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Возвращает:**
java.lang.Объект
### getDirectRunAttr(int key) {#getDirectRunAttr-int-}
```
public Object getDirectRunAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

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
### getEffectiveTabStops() {#getEffectiveTabStops--}
```
public TabStop[] getEffectiveTabStops()
```


Возвращает массив всех позиций табуляции, примененных к этому абзацу, в том числе примененных косвенно с помощью стилей или списков.

**Возвращает:**
com.aspose.words.TabStop[]
### getFirstChild() {#getFirstChild--}
```
public Node getFirstChild()
```


Получает первый дочерний элемент узла. Если нет первого дочернего узла, возвращается нуль.

**Возвращает:**
[Node](../../com.aspose.words/node) - Первый дочерний узел.
### getFrameFormat() {#getFrameFormat--}
```
public FrameFormat getFrameFormat()
```


Предоставляет доступ к свойствам форматирования абзаца.

**Возвращает:**
[FrameFormat](../../com.aspose.words/frameformat) - соответствующий[FrameFormat](../../com.aspose.words/frameformat) ценность.
### getLastChild() {#getLastChild--}
```
public Node getLastChild()
```


Получает последний дочерний элемент узла. Если последнего дочернего узла нет, возвращается нуль.

**Возвращает:**
[Node](../../com.aspose.words/node) - Последний дочерний узел.
### getListFormat() {#getListFormat--}
```
public ListFormat getListFormat()
```


Предоставляет доступ к свойствам форматирования списка абзаца.

**Возвращает:**
[ListFormat](../../com.aspose.words/listformat) - соответствующий[ListFormat](../../com.aspose.words/listformat) ценность.
### getListLabel() {#getListLabel--}
```
public ListLabel getListLabel()
```


Получает[getListLabel()](../../com.aspose.words/paragraph\#getListLabel--) объект, предоставляющий доступ к нумерации списка и форматированию этого абзаца.

**Возвращает:**
[ListLabel](../../com.aspose.words/listlabel) - А[getListLabel()](../../com.aspose.words/paragraph\#getListLabel--) объект, предоставляющий доступ к нумерации списка и форматированию этого абзаца.
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


 Возвращает**NodeType.Paragraph**.

**Возвращает:**
 инт -**NodeType.Paragraph** . Возвращаемое значение является одним из[NodeType](../../com.aspose.words/nodetype) константы.
### getParagraphBreakFont() {#getParagraphBreakFont--}
```
public Font getParagraphBreakFont()
```


Предоставляет доступ к форматированию шрифта символа разрыва абзаца.

**Возвращает:**
[Font](../../com.aspose.words/font) - соответствующий[Font](../../com.aspose.words/font) ценность.
### getParagraphFormat() {#getParagraphFormat--}
```
public ParagraphFormat getParagraphFormat()
```


Предоставляет доступ к свойствам форматирования абзаца.

**Возвращает:**
[ParagraphFormat](../../com.aspose.words/paragraphformat) - соответствующий[ParagraphFormat](../../com.aspose.words/paragraphformat) ценность.
### getParentNode() {#getParentNode--}
```
public CompositeNode getParentNode()
```


Получает непосредственного родителя этого узла.

Если узел был только что создан и еще не добавлен в дерево, или если он был удален из дерева, родитель имеет значение null.

**Возвращает:**
[CompositeNode](../../com.aspose.words/compositenode) - Непосредственный родитель этого узла.
### getParentSection() {#getParentSection--}
```
public Section getParentSection()
```


 Извлекает родителя[Section](../../com.aspose.words/section) параграфа.

**Возвращает:**
[Section](../../com.aspose.words/section) - соответствующий[Section](../../com.aspose.words/section) ценность.
### getParentStory() {#getParentStory--}
```
public Story getParentStory()
```


 Извлекает историю на уровне родительского раздела, которую можно[Body](../../com.aspose.words/body) или же[HeaderFooter](../../com.aspose.words/headerfooter).

**Возвращает:**
[Story](../../com.aspose.words/story) - соответствующий[Story](../../com.aspose.words/story) ценность.
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
### getRuns() {#getRuns--}
```
public RunCollection getRuns()
```


Предоставляет доступ к типизированной коллекции фрагментов текста внутри абзаца.

**Возвращает:**
[RunCollection](../../com.aspose.words/runcollection) - соответствующий[RunCollection](../../com.aspose.words/runcollection) ценность.
### getText() {#getText--}
```
public String getText()
```


Получает текст этого абзаца, включая символ конца абзаца.

Текст всех дочерних узлов объединяется, а символ конца абзаца добавляется следующим образом:

 *   Если абзац является последним абзацем[Body](../../com.aspose.words/body) , тогда[ControlChar.SECTION\_BREAK](../../com.aspose.words/controlchar\#SECTION-BREAK) (\\x000c) добавляется.
 *   Если абзац является последним абзацем[Cell](../../com.aspose.words/cell) , тогда[ControlChar.CELL](../../com.aspose.words/controlchar\#CELL) (\\x0007) добавляется.
 *   Для всех остальных абзацев[ControlChar.PARAGRAPH\_BREAK](../../com.aspose.words/controlchar\#PARAGRAPH-BREAK) (\\r) добавляется.

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
### insertField(int fieldType, boolean updateField, Node refNode, boolean isAfter) {#insertField-int-boolean-com.aspose.words.Node-boolean-}
```
public Field insertField(int fieldType, boolean updateField, Node refNode, boolean isAfter)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldType | int |  |
| updateField | boolean |  |
| refNode | [Node](../../com.aspose.words/node) |  |
| isAfter | boolean |  |

**Возвращает:**
[Field](../../com.aspose.words/field)
### insertField(String fieldCode, Node refNode, boolean isAfter) {#insertField-java.lang.String-com.aspose.words.Node-boolean-}
```
public Field insertField(String fieldCode, Node refNode, boolean isAfter)
```


Вставляет поле Word в этот абзац. Вставляет поле в этот абзац.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldCode | java.lang.String | Код поля для вставки (без фигурных скобок). |
| refNode | [Node](../../com.aspose.words/node) | Узел ссылки внутри этого абзаца (если refNode имеет значение null, то добавляется в конец абзаца). |
| isAfter | boolean | Следует ли вставлять поле после или перед ссылочным узлом. |

**Возвращает:**
[Field](../../com.aspose.words/field) - А[Field](../../com.aspose.words/field) объект, представляющий вставленное поле.
### insertField(String fieldCode, String fieldValue, Node refNode, boolean isAfter) {#insertField-java.lang.String-java.lang.String-com.aspose.words.Node-boolean-}
```
public Field insertField(String fieldCode, String fieldValue, Node refNode, boolean isAfter)
```


Вставляет поле Word в этот абзац. Вставляет поле в этот абзац.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldCode | java.lang.String | Код поля для вставки (без фигурных скобок). |
| fieldValue | java.lang.String | Значение поля для вставки. Передайте null для полей, которые не имеют значения. |
| refNode | [Node](../../com.aspose.words/node) | Узел ссылки внутри этого абзаца (если refNode имеет значение null, то добавляется в конец абзаца). |
| isAfter | boolean | Следует ли вставлять поле после или перед ссылочным узлом. |

**Возвращает:**
[Field](../../com.aspose.words/field) - А[Field](../../com.aspose.words/field) объект, представляющий вставленное поле.
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
### isEndOfCell() {#isEndOfCell--}
```
public boolean isEndOfCell()
```


 Истинно, если этот абзац является последним абзацем в[Cell](../../com.aspose.words/cell); ложно в противном случае.

**Возвращает:**
boolean - соответствующее логическое значение.
### isEndOfDocument() {#isEndOfDocument--}
```
public boolean isEndOfDocument()
```


Истинно, если этот абзац является последним абзацем в последнем разделе документа.

**Возвращает:**
boolean - соответствующее логическое значение.
### isEndOfHeaderFooter() {#isEndOfHeaderFooter--}
```
public boolean isEndOfHeaderFooter()
```


 Истинно, если этот абзац является последним абзацем в**HeaderFooter** (рассказ основного текста)**Section**; ложно в противном случае.

**Возвращает:**
boolean - соответствующее логическое значение.
### isEndOfSection() {#isEndOfSection--}
```
public boolean isEndOfSection()
```


 Истинно, если этот абзац является последним абзацем в**Body** (рассказ основного текста)**Section**; ложно в противном случае.

**Возвращает:**
boolean - соответствующее логическое значение.
### isFormatRevision() {#isFormatRevision--}
```
public boolean isFormatRevision()
```


Возвращает true, если форматирование объекта было изменено в Microsoft Word при включенном отслеживании изменений.

**Возвращает:**
boolean — Истинно, если форматирование объекта было изменено в Microsoft Word при включенном отслеживании изменений.
### isInCell() {#isInCell--}
```
public boolean isInCell()
```


 Истинно, если этот абзац является непосредственным потомком[Cell](../../com.aspose.words/cell); ложно в противном случае.

**Возвращает:**
boolean - соответствующее логическое значение.
### isInsertRevision() {#isInsertRevision--}
```
public boolean isInsertRevision()
```


Возвращает true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений.

**Возвращает:**
boolean — True, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений.
### isListItem() {#isListItem--}
```
public boolean isListItem()
```


Истинно, если абзац является элементом маркированного или нумерованного списка в исходной редакции.

**Возвращает:**
boolean - соответствующее логическое значение.
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
### joinRunsWithSameFormatting() {#joinRunsWithSameFormatting--}
```
public int joinRunsWithSameFormatting()
```


Соединения выполняются с тем же форматированием, что и абзац.

**Возвращает:**
 int — количество выполненных объединений. Когда**N** соединяются соседние прогоны, они считаются**N - 1** присоединяется.
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




### removeParaAttr(int key) {#removeParaAttr-int-}
```
public void removeParaAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

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

### setParaAttr(int key, Object value) {#setParaAttr-int-java.lang.Object-}
```
public void setParaAttr(int key, Object value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int key, Object value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |
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
