---
title: StructuredDocumentTag
second_title: Справочник по API Aspose.Words для Java
description: Представляет тег структурированного документа SDT или элемент управления содержимым в документе.
type: docs
weight: 532
url: /ru/java/com.aspose.words/structureddocumenttag/
---

**Наследование:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode)

**Все реализованные интерфейсы:**
[com.aspose.words.IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag)
```
public class StructuredDocumentTag extends CompositeNode implements IStructuredDocumentTag
```

Представляет тег структурированного документа (SDT или элемент управления содержимым) в документе.

 Чтобы узнать больше, посетите**Structured Document Tags or Content Control** документальная статья.

Теги структурированного документа (SDT) позволяют встраивать в документ определяемую пользователем семантику, а также его поведение и внешний вид.

 В этой версии Aspose.Words предоставляет ряд общедоступных методов и свойств для управления поведением и содержимым[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) . Сопоставление узлов SDT с пользовательскими пакетами XML в документе можно выполнить с помощью[getXmlMapping()](../../com.aspose.words/structureddocumenttag\#getXmlMapping--) имущество.

[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) может встречаться в документе в следующих местах:

 *   Блочный уровень — среди абзацев и таблиц, как дочерний элемент[Body](../../com.aspose.words/body), [HeaderFooter](../../com.aspose.words/headerfooter), [Comment](../../com.aspose.words/comment), [Footnote](../../com.aspose.words/footnote) или[Shape](../../com.aspose.words/shape) узел.
 *   Уровень строки — среди строк в таблице, как дочерний элемент[Table](../../com.aspose.words/table) узел.
 *   Уровень ячейки — среди ячеек в строке таблицы, как дочерний элемент[Row](../../com.aspose.words/row) узел.
 *   Встроенный уровень — среди встроенного контента внутри, как дочерний элемент[Paragraph](../../com.aspose.words/paragraph).
 *   Вложенный в другой[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag).
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [StructuredDocumentTag(DocumentBase doc, int type, int level)](#StructuredDocumentTag-com.aspose.words.DocumentBase-int-int-) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Принимает посетителя. |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node-) | Добавляет указанный узел в конец списка дочерних узлов для этого узла. |
| [clear()](#clear--) | Очищает содержимое этого тега структурированного документа и отображает заполнитель, если он определен. |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [dd()](#dd--) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | Создает дубликат узла. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int-) |  |
| [getAncestor(int ancestorType)](#getAncestor-int-) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class-) | Получает первого предка указанного типа объекта. |
| [getAppearance()](#getAppearance--) | Получает/задает внешний вид тега структурированного документа. |
| [getBuildingBlockCategory()](#getBuildingBlockCategory--) |  Указывает категорию стандартного блока для этого**SDT** узел. |
| [getBuildingBlockGallery()](#getBuildingBlockGallery--) |  Определяет тип стандартного блока для этого**SDT**. |
| [getCalendarType()](#getCalendarType--) |  Указывает тип календаря для этого**SDT**. |
| [getChecked()](#getChecked--) |  Получает/устанавливает текущее состояние флажка**SDT**. |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean-) |  |
| [getChildNodes()](#getChildNodes--) | Получает все непосредственные дочерние узлы этого узла. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [getClass()](#getClass--) |  |
| [getColor()](#getColor--) | Получает цвет тега структурированного документа. |
| [getContainer()](#getContainer--) |  |
| [getContentsFont()](#getContentsFont--) |  Форматирование шрифта, которое будет применяться к тексту, введенному в**SDT**. |
| [getCount()](#getCount--) | Получает количество непосредственных дочерних элементов этого узла. |
| [getCurrentNode()](#getCurrentNode--) |  |
| [getCustomNodeId()](#getCustomNodeId--) | Задает идентификатор пользовательского узла. |
| [getDateDisplayFormat()](#getDateDisplayFormat--) | Строка, представляющая формат, в котором отображаются даты. |
| [getDateDisplayLocale()](#getDateDisplayLocale--) |  Позволяет установить/получить языковой формат для даты, отображаемой в этом**SDT**. |
| [getDateStorageFormat()](#getDateStorageFormat--) |  Получает/устанавливает формат, в котором дата для SDT даты сохраняется, когда**SDT** привязан к узлу XML в хранилище данных документа. |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int-) |  |
| [getDocument()](#getDocument--) | Получает документ, которому принадлежит этот узел. |
| [getEndCharacterFont()](#getEndCharacterFont--) |  Форматирование шрифта, которое будет применяться к последнему символу текста, введенного в**SDT**. |
| [getFirstChild()](#getFirstChild--) | Получает первый дочерний элемент узла. |
| [getFullDate()](#getFullDate--) |  Указывает полную дату и время последнего ввода этого**SDT**. |
| [getId()](#getId--) |  Указывает уникальный постоянный числовой идентификатор только для чтения для этого**SDT**. |
| [getLastChild()](#getLastChild--) | Получает последний дочерний элемент узла. |
| [getLevel()](#getLevel--) |  Получает уровень, на котором это**SDT** происходит в дереве документов. |
| [getLevel_IMarkupNode()](#getLevel-IMarkupNode--) |  |
| [getListItems()](#getListItems--) |  Получает[SdtListItemCollection](../../com.aspose.words/sdtlistitemcollection) связанные с этим**SDT**. |
| [getLockContentControl()](#getLockContentControl--) |  Если установлено значение true, это свойство запрещает пользователю удалять это**SDT**. |
| [getLockContents()](#getLockContents--) |  Если установлено значение true, это свойство запрещает пользователю редактировать содержимое этого**SDT**. |
| [getMultiline()](#getMultiline--) |  Указывает, является ли это**SDT** допускает несколько строк текста. |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node-) |  |
| [getNextSibling()](#getNextSibling--) | Получает узел, следующий сразу за этим узлом. |
| [getNodeType()](#getNodeType--) |  Возвращает**NodeType.StructuredDocumentTag**. |
| [getParentNode()](#getParentNode--) | Получает непосредственного родителя этого узла. |
| [getPlaceholder()](#getPlaceholder--) |  Получает[BuildingBlock](../../com.aspose.words/buildingblock)содержащий текст-заполнитель, который должен отображаться, когда содержимое этого запуска SDT пусто, связанный сопоставленный XML-элемент пуст, как указано в параметре[getXmlMapping()](../../com.aspose.words/structureddocumenttag\#getXmlMapping--) элемент или[isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttag\#isShowingPlaceholderText--) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttag\#isShowingPlaceholderText-boolean-) элемент истинный. |
| [getPlaceholderName()](#getPlaceholderName--) |  Получает или задает имя[BuildingBlock](../../com.aspose.words/buildingblock) содержащий текст-заполнитель. |
| [getPreviousSibling()](#getPreviousSibling--) | Получает узел, непосредственно предшествующий этому узлу. |
| [getRange()](#getRange--) |  Возвращает**Range** объект, который представляет часть документа, содержащегося в этом узле. |
| [getSdtType()](#getSdtType--) |  Получает тип этого**Structured document tag**. |
| [getStyle()](#getStyle--) | Получает Style тега структурированного документа. |
| [getStyleName()](#getStyleName--) | Получает имя стиля, примененного к тегу структурированного документа. |
| [getTag()](#getTag--) | Задает тег, связанный с текущим узлом SDT. |
| [getText()](#getText--) | Получает текст этого узла и всех его дочерних элементов. |
| [getTitle()](#getTitle--) |  Указывает понятное имя, связанное с этим**SDT**. |
| [getWordOpenXML()](#getWordOpenXML--) |  Получает строку, представляющую XML, содержащийся в узле в[SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC) формат. |
| [getXmlMapping()](#getXmlMapping--) | Получает объект, представляющий сопоставление этого тега структурированного документа с XML-данными в пользовательской XML-части текущего документа. |
| [hasChildNodes()](#hasChildNodes--) | Возвращает true, если у этого узла есть дочерние узлы. |
| [hashCode()](#hashCode--) |  |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node-) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node-) | Вставляет указанный узел сразу после указанного ссылочного узла. |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node-) | Вставляет указанный узел непосредственно перед указанным ссылочным узлом. |
| [isComposite()](#isComposite--) | Возвращает true, так как этот узел может иметь дочерние узлы. |
| [isRanged()](#isRanged--) |  |
| [isShowingPlaceholderText()](#isShowingPlaceholderText--) |  Указывает, является ли содержимое этого**SDT** должен интерпретироваться как содержащий текст-заполнитель (в отличие от обычного текстового содержимого в SDT). |
| [isShowingPlaceholderText(boolean value)](#isShowingPlaceholderText-boolean-) |  Указывает, является ли содержимое этого**SDT** должен интерпретироваться как содержащий текст-заполнитель (в отличие от обычного текстового содержимого в SDT). |
| [isTemporary()](#isTemporary--) |  Указывает, является ли это**SDT** должен быть удален из документа WordProcessingML при изменении его содержимого. |
| [isTemporary(boolean value)](#isTemporary-boolean-) |  Указывает, является ли это**SDT** должен быть удален из документа WordProcessingML при изменении его содержимого. |
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
| [removeSelfOnly()](#removeSelfOnly--) | Удаляет только сам этот узел SDT, но сохраняет его содержимое в дереве документа. |
| [removeSmartTags()](#removeSmartTags--) |  Удаляет все[SmartTag](../../com.aspose.words/smarttag) узлы-потомки текущего узла. |
| [selectNodes(String xpath)](#selectNodes-java.lang.String-) | Выбирает список узлов, соответствующих выражению XPath. |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String-) | Выбирает первый узел, соответствующий выражению XPath. |
| [setAppearance(int value)](#setAppearance-int-) | Получает/задает внешний вид тега структурированного документа. |
| [setBuildingBlockCategory(String value)](#setBuildingBlockCategory-java.lang.String-) |  Указывает категорию стандартного блока для этого**SDT** узел. |
| [setBuildingBlockGallery(String value)](#setBuildingBlockGallery-java.lang.String-) |  Определяет тип стандартного блока для этого**SDT**. |
| [setCalendarType(int value)](#setCalendarType-int-) |  Указывает тип календаря для этого**SDT**. |
| [setChecked(boolean value)](#setChecked-boolean-) |  Получает/устанавливает текущее состояние флажка**SDT**. |
| [setCheckedSymbol(int characterCode, String fontName)](#setCheckedSymbol-int-java.lang.String-) | Задает символ, используемый для представления отмеченного состояния элемента управления содержимым флажка. |
| [setColor(Color value)](#setColor-java.awt.Color-) | Задает цвет тега структурированного документа. |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | Задает идентификатор пользовательского узла. |
| [setDateDisplayFormat(String value)](#setDateDisplayFormat-java.lang.String-) | Строка, представляющая формат, в котором отображаются даты. |
| [setDateDisplayLocale(int value)](#setDateDisplayLocale-int-) |  Позволяет установить/получить языковой формат для даты, отображаемой в этом**SDT**. |
| [setDateStorageFormat(int value)](#setDateStorageFormat-int-) |  Получает/устанавливает формат, в котором дата для SDT даты сохраняется, когда**SDT** привязан к узлу XML в хранилище данных документа. |
| [setFullDate(Date value)](#setFullDate-java.util.Date-) |  Указывает полную дату и время последнего ввода этого**SDT**. |
| [setLockContentControl(boolean value)](#setLockContentControl-boolean-) |  Если установлено значение true, это свойство запрещает пользователю удалять это**SDT**. |
| [setLockContents(boolean value)](#setLockContents-boolean-) |  Если установлено значение true, это свойство запрещает пользователю редактировать содержимое этого**SDT**. |
| [setMultiline(boolean value)](#setMultiline-boolean-) |  Указывает, является ли это**SDT** допускает несколько строк текста. |
| [setPlaceholderName(String value)](#setPlaceholderName-java.lang.String-) |  Получает или задает имя[BuildingBlock](../../com.aspose.words/buildingblock) содержащий текст-заполнитель. |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [setStyle(Style value)](#setStyle-com.aspose.words.Style-) | Задает стиль тега структурированного документа. |
| [setStyleName(String value)](#setStyleName-java.lang.String-) | Задает имя стиля, применяемого к тегу структурированного документа. |
| [setTag(String value)](#setTag-java.lang.String-) | Задает тег, связанный с текущим узлом SDT. |
| [setTitle(String value)](#setTitle-java.lang.String-) |  Указывает понятное имя, связанное с этим**SDT**. |
| [setUncheckedSymbol(int characterCode, String fontName)](#setUncheckedSymbol-int-java.lang.String-) | Задает символ, используемый для представления неотмеченного состояния элемента управления содержимым флажка. |
| [structuredDocumentTagNode()](#structuredDocumentTagNode--) |  |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| [toString(int saveFormat)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### StructuredDocumentTag(DocumentBase doc, int type, int level) {#StructuredDocumentTag-com.aspose.words.DocumentBase-int-int-}
```
public StructuredDocumentTag(DocumentBase doc, int type, int level)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) |  |
| type | int |  |
| level | int |  |

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
 boolean - Истинно, если были посещены все узлы; false, если DocumentVisitor остановил операцию перед посещением всех узлов. Звонки[DocumentVisitor.visitStructuredDocumentTagStart(com.aspose.words.StructuredDocumentTag)](../../com.aspose.words/documentvisitor\#visitStructuredDocumentTagStart-com.aspose.words.StructuredDocumentTag-) , затем звонит[Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node\#accept-com.aspose.words.DocumentVisitor-) для всех дочерних узлов смарт-тега и вызовов[DocumentVisitor.visitStructuredDocumentTagEnd(com.aspose.words.StructuredDocumentTag)](../../com.aspose.words/documentvisitor\#visitStructuredDocumentTagEnd-com.aspose.words.StructuredDocumentTag-) в конце.
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
### clear() {#clear--}
```
public void clear()
```


Очищает содержимое этого тега структурированного документа и отображает заполнитель, если он определен.

Невозможно очистить содержимое тега структурированного документа, если он имеет редакции.

 Если этот тег структурированного документа сопоставляется с пользовательским XML (с использованием[getXmlMapping()](../../com.aspose.words/structureddocumenttag\#getXmlMapping--) свойство), указанный XML-узел очищается.

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
### getAppearance() {#getAppearance--}
```
public int getAppearance()
```


Получает/задает внешний вид тега структурированного документа.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[SdtAppearance](../../com.aspose.words/sdtappearance) константы.
### getBuildingBlockCategory() {#getBuildingBlockCategory--}
```
public String getBuildingBlockCategory()
```


 Указывает категорию стандартного блока для этого**SDT** узел. Не может быть нулевым.

 Доступ к этому свойству будет работать только для[SdtType.BUILDING\_BLOCK\_GALLERY](../../com.aspose.words/sdttype\#BUILDING-BLOCK-GALLERY) а также[SdtType.DOC\_PART\_OBJ](../../com.aspose.words/sdttype\#DOC-PART-OBJ) Типы СДТ. Он доступен только для чтения**SDT** типа части документа.

Для всех других типов SDT будет иметь место исключение.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getBuildingBlockGallery() {#getBuildingBlockGallery--}
```
public String getBuildingBlockGallery()
```


 Определяет тип стандартного блока для этого**SDT**. Не может быть нулевым.

 Доступ к этому свойству будет работать только для[SdtType.BUILDING\_BLOCK\_GALLERY](../../com.aspose.words/sdttype\#BUILDING-BLOCK-GALLERY) а также[SdtType.DOC\_PART\_OBJ](../../com.aspose.words/sdttype\#DOC-PART-OBJ) Типы СДТ. Он доступен только для чтения**SDT** типа части документа.

Для всех других типов SDT будет иметь место исключение.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getCalendarType() {#getCalendarType--}
```
public int getCalendarType()
```


 Указывает тип календаря для этого**SDT** . По умолчанию[SdtCalendarType.DEFAULT](../../com.aspose.words/sdtcalendartype\#DEFAULT)

 Доступ к этому свойству будет работать только для[SdtType.DATE](../../com.aspose.words/sdttype\#DATE)типа СДТ.

Для всех других типов SDT будет иметь место исключение.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[SdtCalendarType](../../com.aspose.words/sdtcalendartype) константы.
### getChecked() {#getChecked--}
```
public boolean getChecked()
```


 Получает/устанавливает текущее состояние флажка**SDT**. Значение по умолчанию для этого свойства — false.

 Доступ к этому свойству будет работать только для[SdtType.CHECKBOX](../../com.aspose.words/sdttype\#CHECKBOX) Типы СДТ.

Для всех других типов SDT будет иметь место исключение.

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
### getColor() {#getColor--}
```
public Color getColor()
```


Получает цвет тега структурированного документа.

**Возвращает:**
java.awt.Color — цвет тега структурированного документа.
### getContainer() {#getContainer--}
```
public CompositeNode getContainer()
```




**Возвращает:**
[CompositeNode](../../com.aspose.words/compositenode)
### getContentsFont() {#getContentsFont--}
```
public Font getContentsFont()
```


 Форматирование шрифта, которое будет применяться к тексту, введенному в**SDT**.

**Возвращает:**
[Font](../../com.aspose.words/font) - соответствующий[Font](../../com.aspose.words/font) ценность.
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
### getDateDisplayFormat() {#getDateDisplayFormat--}
```
public String getDateDisplayFormat()
```


Строка, представляющая формат, в котором отображаются даты. Не может быть нулевым. Даты для английского языка (США): «мм/дд/гггг».

 Доступ к этому свойству будет работать только для[SdtType.DATE](../../com.aspose.words/sdttype\#DATE)типа СДТ.

Для всех других типов SDT будет иметь место исключение.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getDateDisplayLocale() {#getDateDisplayLocale--}
```
public int getDateDisplayLocale()
```


 Позволяет установить/получить языковой формат для даты, отображаемой в этом**SDT**.

 Доступ к этому свойству будет работать только для[SdtType.DATE](../../com.aspose.words/sdttype\#DATE)типа СДТ.

Для всех других типов SDT будет иметь место исключение.

**Возвращает:**
int - соответствующее значение int.
### getDateStorageFormat() {#getDateStorageFormat--}
```
public int getDateStorageFormat()
```


 Получает/устанавливает формат, в котором дата для SDT даты сохраняется, когда**SDT** привязан к узлу XML в хранилище данных документа. Значение по умолчанию[SdtDateStorageFormat.DATE\_TIME](../../com.aspose.words/sdtdatestorageformat\#DATE-TIME)

 Доступ к этому свойству будет работать только для[SdtType.DATE](../../com.aspose.words/sdttype\#DATE)типа СДТ.

Для всех других типов SDT будет иметь место исключение.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[SdtDateStorageFormat](../../com.aspose.words/sdtdatestorageformat) константы.
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
### getEndCharacterFont() {#getEndCharacterFont--}
```
public Font getEndCharacterFont()
```


 Форматирование шрифта, которое будет применяться к последнему символу текста, введенного в**SDT**.

**Возвращает:**
[Font](../../com.aspose.words/font) - соответствующий[Font](../../com.aspose.words/font) ценность.
### getFirstChild() {#getFirstChild--}
```
public Node getFirstChild()
```


Получает первый дочерний элемент узла. Если нет первого дочернего узла, возвращается нуль.

**Возвращает:**
[Node](../../com.aspose.words/node) - Первый дочерний узел.
### getFullDate() {#getFullDate--}
```
public Date getFullDate()
```


 Указывает полную дату и время последнего ввода этого**SDT**.

 Доступ к этому свойству будет работать только для[SdtType.DATE](../../com.aspose.words/sdttype\#DATE)типа СДТ.

Для всех других типов SDT будет иметь место исключение.

**Возвращает:**
java.util.Date — соответствующее значение java.util.Date.
### getId() {#getId--}
```
public int getId()
```


 Указывает уникальный постоянный числовой идентификатор только для чтения для этого**SDT**.

Атрибут Id должен соответствовать следующим правилам:

 *   Документ должен сохранять идентификаторы SDT только в том случае, если весь документ клонирован.[Document.deepClone()](../../com.aspose.words/document\#deepClone--).
 *   В течение[DocumentBase.importNode(com.aspose.words.Node, boolean)](../../com.aspose.words/documentbase\#importNode-com.aspose.words.Node--boolean-) Идентификатор должен быть сохранен, если импорт не вызывает конфликтов с другими идентификаторами SDT в целевом документе.
 *  Если несколько узлов SDT задают одно и то же значение десятичного числа для атрибута Id, то первый SDT в документе должен поддерживать этот исходный идентификатор, а все последующие узлы SDT должны иметь новые идентификаторы, назначенные им при загрузке документа.
 *   Во время автономного SDT**M:Aspose.Words.Markup.StructuredDocumentTag.Clone(System.Boolean,Aspose.Words.INodeCloningListener)** операции будет создан новый уникальный идентификатор для клонированного узла SDT.
 *  Если Id не указан в исходном документе, то узлу SDT должен быть назначен новый уникальный идентификатор при загрузке документа.

**Возвращает:**
int - соответствующее значение int.
### getLastChild() {#getLastChild--}
```
public Node getLastChild()
```


Получает последний дочерний элемент узла. Если последнего дочернего узла нет, возвращается нуль.

**Возвращает:**
[Node](../../com.aspose.words/node) - Последний дочерний узел.
### getLevel() {#getLevel--}
```
public int getLevel()
```


 Получает уровень, на котором это**SDT** происходит в дереве документов.

**Возвращает:**
 int - Уровень, на котором это**SDT** происходит в дереве документов. Возвращаемое значение является одним из[MarkupLevel](../../com.aspose.words/markuplevel) константы.
### getLevel_IMarkupNode() {#getLevel-IMarkupNode--}
```
public int getLevel_IMarkupNode()
```




**Возвращает:**
инт
### getListItems() {#getListItems--}
```
public SdtListItemCollection getListItems()
```


 Получает[SdtListItemCollection](../../com.aspose.words/sdtlistitemcollection) связанные с этим**SDT**.

 Доступ к этому свойству будет работать только для[SdtType.COMBO\_BOX](../../com.aspose.words/sdttype\#COMBO-BOX) или же[SdtType.DROP\_DOWN\_LIST](../../com.aspose.words/sdttype\#DROP-DOWN-LIST) Типы СДТ.

Для всех других типов SDT будет иметь место исключение.

**Возвращает:**
[SdtListItemCollection](../../com.aspose.words/sdtlistitemcollection) -\{[SdtListItemCollection](../../com.aspose.words/sdtlistitemcollection) связанные с этим**SDT**.
### getLockContentControl() {#getLockContentControl--}
```
public boolean getLockContentControl()
```


 Если установлено значение true, это свойство запрещает пользователю удалять это**SDT**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getLockContents() {#getLockContents--}
```
public boolean getLockContents()
```


 Если установлено значение true, это свойство запрещает пользователю редактировать содержимое этого**SDT**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getMultiline() {#getMultiline--}
```
public boolean getMultiline()
```


 Указывает, является ли это**SDT** допускает несколько строк текста.

 Доступ к этому свойству будет работать только для[SdtType.RICH\_TEXT](../../com.aspose.words/sdttype\#RICH-TEXT) а также[SdtType.PLAIN\_TEXT](../../com.aspose.words/sdttype\#PLAIN-TEXT)типа СДТ.

Для всех других типов SDT будет иметь место исключение.

**Возвращает:**
boolean - соответствующее логическое значение.
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


 Возвращает**NodeType.StructuredDocumentTag**.

**Возвращает:**
 инт -**NodeType.StructuredDocumentTag** . Возвращаемое значение является одним из[NodeType](../../com.aspose.words/nodetype) константы.
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


 Получает[BuildingBlock](../../com.aspose.words/buildingblock)содержащий текст-заполнитель, который должен отображаться, когда содержимое этого запуска SDT пусто, связанный сопоставленный XML-элемент пуст, как указано в параметре[getXmlMapping()](../../com.aspose.words/structureddocumenttag\#getXmlMapping--) элемент или[isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttag\#isShowingPlaceholderText--) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttag\#isShowingPlaceholderText-boolean-) элемент истинный. Может быть нулевым, что означает, что заполнитель неприменим для этого Sdt.

**Возвращает:**
[BuildingBlock](../../com.aspose.words/buildingblock) -[BuildingBlock](../../com.aspose.words/buildingblock)содержащий текст-заполнитель, который должен отображаться, когда содержимое этого запуска SDT пусто, связанный сопоставленный XML-элемент пуст, как указано в параметре[getXmlMapping()](../../com.aspose.words/structureddocumenttag\#getXmlMapping--) элемент или[isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttag\#isShowingPlaceholderText--) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttag\#isShowingPlaceholderText-boolean-) элемент истинный.
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
### getSdtType() {#getSdtType--}
```
public int getSdtType()
```


 Получает тип этого**Structured document tag**.

**Возвращает:**
 int - Тип этого**Structured document tag** . Возвращаемое значение является одним из[SdtType](../../com.aspose.words/sdttype) константы.
### getStyle() {#getStyle--}
```
public Style getStyle()
```


 Получает Style тега структурированного документа. Только[StyleType.CHARACTER](../../com.aspose.words/styletype\#CHARACTER) стиль или[StyleType.PARAGRAPH](../../com.aspose.words/styletype\#PARAGRAPH) можно установить стиль со связанным стилем символов.

**Возвращает:**
[Style](../../com.aspose.words/style) - Стиль тега структурированного документа.
### getStyleName() {#getStyleName--}
```
public String getStyleName()
```


Получает имя стиля, примененного к тегу структурированного документа.

**Возвращает:**
java.lang.String — имя стиля, примененного к тегу структурированного документа.
### getTag() {#getTag--}
```
public String getTag()
```


Задает тег, связанный с текущим узлом SDT. Не может быть нулевым. Тег — это произвольная строка, которую приложения могут ассоциировать с SDT, чтобы идентифицировать ее, не предоставляя видимого понятного имени.

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


 Указывает понятное имя, связанное с этим**SDT**. Не может быть нулевым.

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


 Получает объект, представляющий сопоставление этого тега структурированного документа с XML-данными в пользовательской XML-части текущего документа. Вы можете использовать[XmlMapping.setMapping(com.aspose.words.CustomXmlPart, java.lang.String, java.lang.String)](../../com.aspose.words/xmlmapping\#setMapping-com.aspose.words.CustomXmlPart--java.lang.String--java.lang.String-) метод этого объекта для сопоставления тега структурированного документа с данными XML.

**Возвращает:**
[XmlMapping](../../com.aspose.words/xmlmapping) - Объект, представляющий сопоставление этого тега структурированного документа с данными XML в пользовательской части XML текущего документа.
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


 Указывает, является ли содержимое этого**SDT** должен интерпретироваться как содержащий текст-заполнитель (в отличие от обычного текстового содержимого в SDT).

если установлено значение true, это состояние должно быть возобновлено (показывая текст-заполнитель) при открытии этого документа.

**Возвращает:**
boolean - соответствующее логическое значение.
### isShowingPlaceholderText(boolean value) {#isShowingPlaceholderText-boolean-}
```
public void isShowingPlaceholderText(boolean value)
```


 Указывает, является ли содержимое этого**SDT** должен интерпретироваться как содержащий текст-заполнитель (в отличие от обычного текстового содержимого в SDT).

если установлено значение true, это состояние должно быть возобновлено (показывая текст-заполнитель) при открытии этого документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### isTemporary() {#isTemporary--}
```
public boolean isTemporary()
```


 Указывает, является ли это**SDT** должен быть удален из документа WordProcessingML при изменении его содержимого.

**Возвращает:**
boolean - соответствующее логическое значение.
### isTemporary(boolean value) {#isTemporary-boolean-}
```
public void isTemporary(boolean value)
```


 Указывает, является ли это**SDT** должен быть удален из документа WordProcessingML при изменении его содержимого.

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

### removeSelfOnly() {#removeSelfOnly--}
```
public void removeSelfOnly()
```


Удаляет только сам этот узел SDT, но сохраняет его содержимое в дереве документа.

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
### setAppearance(int value) {#setAppearance-int-}
```
public void setAppearance(int value)
```


Получает/задает внешний вид тега структурированного документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[SdtAppearance](../../com.aspose.words/sdtappearance) константы. |

### setBuildingBlockCategory(String value) {#setBuildingBlockCategory-java.lang.String-}
```
public void setBuildingBlockCategory(String value)
```


 Указывает категорию стандартного блока для этого**SDT** узел. Не может быть нулевым.

 Доступ к этому свойству будет работать только для[SdtType.BUILDING\_BLOCK\_GALLERY](../../com.aspose.words/sdttype\#BUILDING-BLOCK-GALLERY) а также[SdtType.DOC\_PART\_OBJ](../../com.aspose.words/sdttype\#DOC-PART-OBJ) Типы СДТ. Он доступен только для чтения**SDT** типа части документа.

Для всех других типов SDT будет иметь место исключение.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setBuildingBlockGallery(String value) {#setBuildingBlockGallery-java.lang.String-}
```
public void setBuildingBlockGallery(String value)
```


 Определяет тип стандартного блока для этого**SDT**. Не может быть нулевым.

 Доступ к этому свойству будет работать только для[SdtType.BUILDING\_BLOCK\_GALLERY](../../com.aspose.words/sdttype\#BUILDING-BLOCK-GALLERY) а также[SdtType.DOC\_PART\_OBJ](../../com.aspose.words/sdttype\#DOC-PART-OBJ) Типы СДТ. Он доступен только для чтения**SDT** типа части документа.

Для всех других типов SDT будет иметь место исключение.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setCalendarType(int value) {#setCalendarType-int-}
```
public void setCalendarType(int value)
```


 Указывает тип календаря для этого**SDT** . По умолчанию[SdtCalendarType.DEFAULT](../../com.aspose.words/sdtcalendartype\#DEFAULT)

 Доступ к этому свойству будет работать только для[SdtType.DATE](../../com.aspose.words/sdttype\#DATE)типа СДТ.

Для всех других типов SDT будет иметь место исключение.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[SdtCalendarType](../../com.aspose.words/sdtcalendartype) константы. |

### setChecked(boolean value) {#setChecked-boolean-}
```
public void setChecked(boolean value)
```


 Получает/устанавливает текущее состояние флажка**SDT**. Значение по умолчанию для этого свойства — false.

 Доступ к этому свойству будет работать только для[SdtType.CHECKBOX](../../com.aspose.words/sdttype\#CHECKBOX) Типы СДТ.

Для всех других типов SDT будет иметь место исключение.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setCheckedSymbol(int characterCode, String fontName) {#setCheckedSymbol-int-java.lang.String-}
```
public void setCheckedSymbol(int characterCode, String fontName)
```


Задает символ, используемый для представления отмеченного состояния элемента управления содержимым флажка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| characterCode | int | Код символа для указанного символа. |
| fontName | java.lang.String | Имя шрифта, содержащего символ.

 Доступ к этому методу будет работать только для[SdtType.CHECKBOX](../../com.aspose.words/sdttype\#CHECKBOX) Типы СДТ.

 Для всех других типов SDT будет иметь место исключение.|

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

### setDateDisplayFormat(String value) {#setDateDisplayFormat-java.lang.String-}
```
public void setDateDisplayFormat(String value)
```


Строка, представляющая формат, в котором отображаются даты. Не может быть нулевым. Даты для английского языка (США): «мм/дд/гггг».

 Доступ к этому свойству будет работать только для[SdtType.DATE](../../com.aspose.words/sdttype\#DATE)типа СДТ.

Для всех других типов SDT будет иметь место исключение.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setDateDisplayLocale(int value) {#setDateDisplayLocale-int-}
```
public void setDateDisplayLocale(int value)
```


 Позволяет установить/получить языковой формат для даты, отображаемой в этом**SDT**.

 Доступ к этому свойству будет работать только для[SdtType.DATE](../../com.aspose.words/sdttype\#DATE)типа СДТ.

Для всех других типов SDT будет иметь место исключение.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

### setDateStorageFormat(int value) {#setDateStorageFormat-int-}
```
public void setDateStorageFormat(int value)
```


 Получает/устанавливает формат, в котором дата для SDT даты сохраняется, когда**SDT** привязан к узлу XML в хранилище данных документа. Значение по умолчанию[SdtDateStorageFormat.DATE\_TIME](../../com.aspose.words/sdtdatestorageformat\#DATE-TIME)

 Доступ к этому свойству будет работать только для[SdtType.DATE](../../com.aspose.words/sdttype\#DATE)типа СДТ.

Для всех других типов SDT будет иметь место исключение.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[SdtDateStorageFormat](../../com.aspose.words/sdtdatestorageformat) константы. |

### setFullDate(Date value) {#setFullDate-java.util.Date-}
```
public void setFullDate(Date value)
```


 Указывает полную дату и время последнего ввода этого**SDT**.

 Доступ к этому свойству будет работать только для[SdtType.DATE](../../com.aspose.words/sdttype\#DATE)типа СДТ.

Для всех других типов SDT будет иметь место исключение.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.util.Date | Соответствующее значение java.util.Date. |

### setLockContentControl(boolean value) {#setLockContentControl-boolean-}
```
public void setLockContentControl(boolean value)
```


 Если установлено значение true, это свойство запрещает пользователю удалять это**SDT**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setLockContents(boolean value) {#setLockContents-boolean-}
```
public void setLockContents(boolean value)
```


 Если установлено значение true, это свойство запрещает пользователю редактировать содержимое этого**SDT**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setMultiline(boolean value) {#setMultiline-boolean-}
```
public void setMultiline(boolean value)
```


 Указывает, является ли это**SDT** допускает несколько строк текста.

 Доступ к этому свойству будет работать только для[SdtType.RICH\_TEXT](../../com.aspose.words/sdttype\#RICH-TEXT) а также[SdtType.PLAIN\_TEXT](../../com.aspose.words/sdttype\#PLAIN-TEXT)типа СДТ.

Для всех других типов SDT будет иметь место исключение.

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

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int key, Object value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setStyle(Style value) {#setStyle-com.aspose.words.Style-}
```
public void setStyle(Style value)
```


 Задает стиль тега структурированного документа. Только[StyleType.CHARACTER](../../com.aspose.words/styletype\#CHARACTER) стиль или[StyleType.PARAGRAPH](../../com.aspose.words/styletype\#PARAGRAPH) можно установить стиль со связанным стилем символов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style) | Стиль тега структурированного документа. |

### setStyleName(String value) {#setStyleName-java.lang.String-}
```
public void setStyleName(String value)
```


Задает имя стиля, применяемого к тегу структурированного документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя стиля, примененного к тегу структурированного документа. |

### setTag(String value) {#setTag-java.lang.String-}
```
public void setTag(String value)
```


Задает тег, связанный с текущим узлом SDT. Не может быть нулевым. Тег — это произвольная строка, которую приложения могут ассоциировать с SDT, чтобы идентифицировать ее, не предоставляя видимого понятного имени.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setTitle(String value) {#setTitle-java.lang.String-}
```
public void setTitle(String value)
```


 Указывает понятное имя, связанное с этим**SDT**. Не может быть нулевым.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setUncheckedSymbol(int characterCode, String fontName) {#setUncheckedSymbol-int-java.lang.String-}
```
public void setUncheckedSymbol(int characterCode, String fontName)
```


Задает символ, используемый для представления неотмеченного состояния элемента управления содержимым флажка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| characterCode | int | Код символа для указанного символа. |
| fontName | java.lang.String | Имя шрифта, содержащего символ.

 Доступ к этому методу будет работать только для[SdtType.CHECKBOX](../../com.aspose.words/sdttype\#CHECKBOX) Типы СДТ.

 Для всех других типов SDT будет иметь место исключение.|

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
