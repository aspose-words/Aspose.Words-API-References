---
title: Comment
second_title: Справочник по API Aspose.Words для Java
description: Представляет контейнер для текста комментария.
type: docs
weight: 76
url: /ru/java/com.aspose.words/comment/
---

**Наследование:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode), [com.aspose.words.InlineStory](../../com.aspose.words/inlinestory)
```
public class Comment extends InlineStory
```

Представляет контейнер для текста комментария.

 Чтобы узнать больше, посетите**Working with Comments** документальная статья.

Комментарий — это аннотация, привязанная к области текста или позиции в тексте. Комментарий может содержать произвольное количество контента блочного уровня.

 Если[Comment](../../com.aspose.words/comment) объект возникает сам по себе, комментарий привязывается к позиции[Comment](../../com.aspose.words/comment) объект.

 Для привязки комментария к области текста требуются три объекта:[Comment](../../com.aspose.words/comment), [CommentRangeStart](../../com.aspose.words/commentrangestart) а также[CommentRangeEnd](../../com.aspose.words/commentrangeend) . Все три объекта должны иметь одинаковый[getId()](../../com.aspose.words/comment\#getId--) ценность.

[Comment](../../com.aspose.words/comment) является узлом встроенного уровня и может быть только потомком[Paragraph](../../com.aspose.words/paragraph).

[Comment](../../com.aspose.words/comment) может содержать[Paragraph](../../com.aspose.words/paragraph) а также[Table](../../com.aspose.words/table) дочерние узлы.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [Comment(DocumentBase doc)](#Comment-com.aspose.words.DocumentBase-) |  Инициализирует новый экземпляр**Comment** учебный класс. |
| [Comment(DocumentBase doc, String author, String initial, Date dateTime)](#Comment-com.aspose.words.DocumentBase-java.lang.String-java.lang.String-java.util.Date-) |  Инициализирует новый экземпляр**Comment** учебный класс. |
## Методы

| Метод | Описание |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Принимает посетителя. |
| [addReply(String author, String initial, Date dateTime, String text)](#addReply-java.lang.String-java.lang.String-java.util.Date-java.lang.String-) | Добавляет ответ на этот комментарий. |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node-) | Добавляет указанный узел в конец списка дочерних узлов для этого узла. |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [dd()](#dd--) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | Создает дубликат узла. |
| [ensureMinimum()](#ensureMinimum--) | Если последний дочерний элемент не является абзацем, создает и добавляет один пустой абзац. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int-) |  |
| [getAncestor()](#getAncestor--) | Возвращает родительский объект Comment. |
| [getAncestor(int ancestorType)](#getAncestor-int-) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class-) | Получает первого предка указанного типа объекта. |
| [getAuthor()](#getAuthor--) | Получает имя автора комментария. |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean-) |  |
| [getChildNodes()](#getChildNodes--) | Получает все непосредственные дочерние узлы этого узла. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [getClass()](#getClass--) |  |
| [getContainer()](#getContainer--) |  |
| [getCount()](#getCount--) | Получает количество непосредственных дочерних элементов этого узла. |
| [getCurrentNode()](#getCurrentNode--) |  |
| [getCustomNodeId()](#getCustomNodeId--) | Задает идентификатор пользовательского узла. |
| [getDateTime()](#getDateTime--) | Получает дату и время создания комментария. |
| [getDirectRunAttr(int fontAttr)](#getDirectRunAttr-int-) |  |
| [getDocument()](#getDocument--) | Получает документ, которому принадлежит этот узел. |
| [getDocument_IInline()](#getDocument-IInline--) |  |
| [getDone()](#getDone--) | Получает флаг, указывающий, что комментарий помечен как выполненный. |
| [getFirstChild()](#getFirstChild--) | Получает первый дочерний элемент узла. |
| [getFirstParagraph()](#getFirstParagraph--) | Получает первый абзац в истории. |
| [getFont()](#getFont--) | Предоставляет доступ к форматированию шрифта символа привязки этого объекта. |
| [getId()](#getId--) | Получает идентификатор комментария. |
| [getIdInternal()](#getIdInternal--) |  |
| [getInitial()](#getInitial--) | Получает инициалы пользователя, связанного с конкретным комментарием. |
| [getLastChild()](#getLastChild--) | Получает последний дочерний элемент узла. |
| [getLastParagraph()](#getLastParagraph--) | Получает последний абзац в истории. |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node-) |  |
| [getNextSibling()](#getNextSibling--) | Получает узел, следующий сразу за этим узлом. |
| [getNodeType()](#getNodeType--) |  Возвращает**NodeType.Comment**. |
| [getParagraphs()](#getParagraphs--) | Получает коллекцию абзацев, которые являются непосредственными дочерними элементами истории. |
| [getParentIdInternal()](#getParentIdInternal--) |  |
| [getParentNode()](#getParentNode--) | Получает непосредственного родителя этого узла. |
| [getParentParagraph()](#getParentParagraph--) |  Извлекает родителя[Paragraph](../../com.aspose.words/paragraph) этого узла. |
| [getParentParagraph_IInline()](#getParentParagraph-IInline--) |  |
| [getPreviousSibling()](#getPreviousSibling--) | Получает узел, непосредственно предшествующий этому узлу. |
| [getRange()](#getRange--) |  Возвращает**Range** объект, который представляет часть документа, содержащегося в этом узле. |
| [getReplies()](#getReplies--) |  Возвращает коллекцию[Comment](../../com.aspose.words/comment) объекты, которые являются непосредственными дочерними элементами указанного комментария. |
| [getStoryType()](#getStoryType--) |  Возвращает**StoryType.Comments**. |
| [getTables()](#getTables--) | Получает коллекцию таблиц, которые являются непосредственными дочерними элементами истории. |
| [getText()](#getText--) | Получает текст этого узла и всех его дочерних элементов. |
| [hasChildNodes()](#hasChildNodes--) | Возвращает true, если у этого узла есть дочерние узлы. |
| [hashCode()](#hashCode--) |  |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node-) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node-) | Вставляет указанный узел сразу после указанного ссылочного узла. |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node-) | Вставляет указанный узел непосредственно перед указанным ссылочным узлом. |
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
| [removeAllReplies()](#removeAllReplies--) | Удаляет все ответы на этот комментарий. |
| [removeChild(Node oldChild)](#removeChild-com.aspose.words.Node-) | Удаляет указанный дочерний узел. |
| [removeMoveRevisions()](#removeMoveRevisions--) |  |
| [removeReply(Comment reply)](#removeReply-com.aspose.words.Comment-) | Удаляет указанный ответ на этот комментарий. |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [removeSmartTags()](#removeSmartTags--) |  Удаляет все[SmartTag](../../com.aspose.words/smarttag) узлы-потомки текущего узла. |
| [selectNodes(String xpath)](#selectNodes-java.lang.String-) | Выбирает список узлов, соответствующих выражению XPath. |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String-) | Выбирает первый узел, соответствующий выражению XPath. |
| [setAuthor(String value)](#setAuthor-java.lang.String-) | Устанавливает имя автора комментария. |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | Задает идентификатор пользовательского узла. |
| [setDateTime(Date value)](#setDateTime-java.util.Date-) | Получает дату и время создания комментария. |
| [setDone(boolean value)](#setDone-boolean-) | Устанавливает флаг, указывающий, что комментарий помечен как выполненный. |
| [setIdInternal(int value)](#setIdInternal-int-) |  |
| [setInitial(String value)](#setInitial-java.lang.String-) | Устанавливает инициалы пользователя, связанные с конкретным комментарием. |
| [setParentIdInternal(int value)](#setParentIdInternal-int-) |  |
| [setRunAttr(int fontAttr, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [setText(String text)](#setText-java.lang.String-) | Это удобный метод, позволяющий легко задать текст комментария. |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| [toString(int saveFormat)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### Comment(DocumentBase doc) {#Comment-com.aspose.words.DocumentBase-}
```
public Comment(DocumentBase doc)
```


 Инициализирует новый экземпляр**Comment** учебный класс.

 Когда**Comment** создан, он принадлежит указанному документу, но еще не является его частью и**ParentNode** нулевой.

 Чтобы добавить**Comment** к документу используйте InsertAfter или InsertBefore для абзаца, в который вы хотите вставить комментарий.

 После создания комментария не забудьте установить его[getAuthor()](../../com.aspose.words/comment\#getAuthor--) / [setAuthor(java.lang.String)](../../com.aspose.words/comment\#setAuthor-java.lang.String-), [getInitial()](../../com.aspose.words/comment\#getInitial--) / [setInitial(java.lang.String)](../../com.aspose.words/comment\#setInitial-java.lang.String-) а также[getDateTime()](../../com.aspose.words/comment\#getDateTime--) / [setDateTime(java.util.Date)](../../com.aspose.words/comment\#setDateTime-java.util.Date-) характеристики.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) | Документ владельца. |

### Comment(DocumentBase doc, String author, String initial, Date dateTime) {#Comment-com.aspose.words.DocumentBase-java.lang.String-java.lang.String-java.util.Date-}
```
public Comment(DocumentBase doc, String author, String initial, Date dateTime)
```


 Инициализирует новый экземпляр**Comment** учебный класс.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) | Документ владельца. |
| author | java.lang.String | Имя автора комментария. Не может быть нулевым. |
| initial | java.lang.String | Инициалы автора комментария. Не может быть нулевым. |
| dateTime | java.util.Date | Дата и время комментария. |

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
 boolean - Истинно, если были посещены все узлы; false, если DocumentVisitor остановил операцию перед посещением всех узлов. Звонки[DocumentVisitor.visitCommentStart(com.aspose.words.Comment)](../../com.aspose.words/documentvisitor\#visitCommentStart-com.aspose.words.Comment-) , затем звонит[Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node\#accept-com.aspose.words.DocumentVisitor-) для всех дочерних узлов комментария и вызовов[DocumentVisitor.visitCommentEnd(com.aspose.words.Comment)](../../com.aspose.words/documentvisitor\#visitCommentEnd-com.aspose.words.Comment-) в конце.
### addReply(String author, String initial, Date dateTime, String text) {#addReply-java.lang.String-java.lang.String-java.util.Date-java.lang.String-}
```
public Comment addReply(String author, String initial, Date dateTime, String text)
```


Добавляет ответ на этот комментарий.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| author | java.lang.String | Имя автора ответа. |
| initial | java.lang.String | Автор инициалов для ответа. |
| dateTime | java.util.Date | Дата и время ответа. |
| text | java.lang.String | Текст ответа. |

**Возвращает:**
[Comment](../../com.aspose.words/comment) Созданный[Comment](../../com.aspose.words/comment) узел для ответа. Из-за существующих ограничений MS Office в документе допускается только 1 уровень ответов. Исключение типа java.lang.IllegalStateException будет вызвано, если этот метод вызывается для существующего комментария Reply.
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
### getAncestor() {#getAncestor--}
```
public Comment getAncestor()
```


Возвращает родительский объект Comment. Возвращает null для комментариев верхнего уровня.

**Возвращает:**
[Comment](../../com.aspose.words/comment) - Родительский объект комментария.
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
### getAuthor() {#getAuthor--}
```
public String getAuthor()
```


Получает имя автора комментария.

Не может быть нулевым.

По умолчанию пустая строка.

**Возвращает:**
java.lang.String — имя автора комментария.
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
### getDateTime() {#getDateTime--}
```
public Date getDateTime()
```


Получает дату и время создания комментария.

По умолчанию 03.01.0001.

**Возвращает:**
java.util.Date — дата и время создания комментария.
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
### getDone() {#getDone--}
```
public boolean getDone()
```


Получает флаг, указывающий, что комментарий помечен как выполненный.

**Возвращает:**
boolean — Флаг, указывающий, что комментарий помечен как выполненный.
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
### getId() {#getId--}
```
public int getId()
```


Получает идентификатор комментария.

 Идентификатор комментария позволяет привязать комментарий к области текста в документе. Область должна быть разграничена с помощью[CommentRangeStart](../../com.aspose.words/commentrangestart) а также[CommentRangeEnd](../../com.aspose.words/commentrangeend) объект, использующий то же значение идентификатора, что и[Comment](../../com.aspose.words/comment) объект.

 Вы бы использовали это значение при поиске[CommentRangeStart](../../com.aspose.words/commentrangestart) а также[CommentRangeEnd](../../com.aspose.words/commentrangeend) узлы, которые связаны с этим комментарием.

Идентификаторы комментариев должны быть уникальными для всего документа, и Aspose.Words автоматически поддерживает идентификаторы комментариев при загрузке, сохранении и объединении документов.

**Возвращает:**
int - идентификатор комментария.
### getIdInternal() {#getIdInternal--}
```
public int getIdInternal()
```




**Возвращает:**
инт
### getInitial() {#getInitial--}
```
public String getInitial()
```


Получает инициалы пользователя, связанного с конкретным комментарием.

Не может быть нулевым.

По умолчанию пустая строка.

**Возвращает:**
java.lang.String — Инициалы пользователя, связанные с конкретным комментарием.
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


 Возвращает**NodeType.Comment**.

**Возвращает:**
 инт -**NodeType.Comment** . Возвращаемое значение является одним из[NodeType](../../com.aspose.words/nodetype) константы.
### getParagraphs() {#getParagraphs--}
```
public ParagraphCollection getParagraphs()
```


Получает коллекцию абзацев, которые являются непосредственными дочерними элементами истории.

**Возвращает:**
[ParagraphCollection](../../com.aspose.words/paragraphcollection) - Набор абзацев, которые являются непосредственными потомками истории.
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
### getReplies() {#getReplies--}
```
public CommentCollection getReplies()
```


 Возвращает коллекцию[Comment](../../com.aspose.words/comment) объекты, которые являются непосредственными дочерними элементами указанного комментария.

**Возвращает:**
[CommentCollection](../../com.aspose.words/commentcollection) - Коллекция[Comment](../../com.aspose.words/comment) объекты, которые являются непосредственными дочерними элементами указанного комментария.
### getStoryType() {#getStoryType--}
```
public int getStoryType()
```


 Возвращает**StoryType.Comments**.

**Возвращает:**
 инт -**StoryType.Comments** . Возвращаемое значение является одним из[StoryType](../../com.aspose.words/storytype) константы.
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

### removeAllReplies() {#removeAllReplies--}
```
public void removeAllReplies()
```


Удаляет все ответы на этот комментарий. Все составляющие узлы ответов будут удалены из документа.

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




### removeReply(Comment reply) {#removeReply-com.aspose.words.Comment-}
```
public void removeReply(Comment reply)
```


Удаляет указанный ответ на этот комментарий. Все составляющие узлы ответа будут удалены из документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| reply | [Comment](../../com.aspose.words/comment) | Узел комментария удаляющего ответа. |

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
### setAuthor(String value) {#setAuthor-java.lang.String-}
```
public void setAuthor(String value)
```


Устанавливает имя автора комментария.

Не может быть нулевым.

По умолчанию пустая строка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя автора комментария. |

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

### setDateTime(Date value) {#setDateTime-java.util.Date-}
```
public void setDateTime(Date value)
```


Получает дату и время создания комментария.

По умолчанию 03.01.0001.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.util.Date | Дата и время, когда был сделан комментарий. |

### setDone(boolean value) {#setDone-boolean-}
```
public void setDone(boolean value)
```


Устанавливает флаг, указывающий, что комментарий помечен как выполненный.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Флаг, указывающий, что комментарий помечен как выполненный. |

### setIdInternal(int value) {#setIdInternal-int-}
```
public void setIdInternal(int value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  |

### setInitial(String value) {#setInitial-java.lang.String-}
```
public void setInitial(String value)
```


Устанавливает инициалы пользователя, связанные с конкретным комментарием.

Не может быть нулевым.

По умолчанию пустая строка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Инициалы пользователя, связанные с конкретным комментарием. |

### setParentIdInternal(int value) {#setParentIdInternal-int-}
```
public void setParentIdInternal(int value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  |

### setRunAttr(int fontAttr, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int fontAttr, Object value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fontAttr | int |  |
| value | java.lang.Object |  |

### setText(String text) {#setText-java.lang.String-}
```
public void setText(String text)
```


Это удобный метод, позволяющий легко задать текст комментария.

Этот метод позволяет быстро задать текст комментария из строки. Строка может содержать разрывы абзацев, это соответственно создаст абзацы текста в комментарии. Если вы хотите вставить в комментарий более сложные элементы, например, закладки или таблицы, или применить расширенное форматирование, то вам нужно использовать соответствующие классы узлов для построения текста комментария.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| text | java.lang.String | Новый текст комментария. |

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
