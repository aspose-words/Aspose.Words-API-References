---
title: Table
second_title: Справочник по API Aspose.Words для Java
description: Представляет таблицу в документе Word.
type: docs
weight: 548
url: /ru/java/com.aspose.words/table/
---

**Наследование:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode)
```
public class Table extends CompositeNode
```

Представляет таблицу в документе Word.

 Чтобы узнать больше, посетите**Working with Tables** документальная статья.

**Table** является узлом блочного уровня и может быть дочерним по отношению к классам, производным от**Story** или же**InlineStory**.

**Table** может содержать один или несколько**Row** узлы.

 В минимально допустимой таблице должен быть хотя бы один**Row**.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [Table(DocumentBase doc)](#Table-com.aspose.words.DocumentBase-) |  Инициализирует новый экземпляр**Table** учебный класс. |
## Методы

| Метод | Описание |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Принимает посетителя. |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node-) | Добавляет указанный узел в конец списка дочерних узлов для этого узла. |
| [autoFit(int behavior)](#autoFit-int-) |  |
| [clearBorders()](#clearBorders--) | Удаляет все границы таблиц и ячеек в этой таблице. |
| [clearShading()](#clearShading--) | Удаляет все тени на столе. |
| [convertToHorizontallyMergedCells()](#convertToHorizontallyMergedCells--) |  Преобразует ячейки, объединенные по горизонтали по ширине, в ячейки, объединенные по ширине.[CellFormat.getHorizontalMerge()](../../com.aspose.words/cellformat\#getHorizontalMerge--) / [CellFormat.setHorizontalMerge(int)](../../com.aspose.words/cellformat\#setHorizontalMerge-int-). |
| [dd()](#dd--) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | Создает дубликат узла. |
| [ensureMinimum()](#ensureMinimum--) |  Если в таблице нет строк, создает и добавляет одну**Row**. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAbsoluteHorizontalDistance()](#getAbsoluteHorizontalDistance--) | Получает абсолютную горизонтальную позицию плавающей таблицы, указанную в свойствах таблицы, в пунктах. |
| [getAbsoluteVerticalDistance()](#getAbsoluteVerticalDistance--) | Получает абсолютную вертикальную плавающую позицию таблицы, указанную в свойствах таблицы, в пунктах. |
| [getAlignment()](#getAlignment--) | Указывает, как встроенная таблица выравнивается в документе. |
| [getAllowAutoFit()](#getAllowAutoFit--) | Позволяет Microsoft Word и Aspose.Words автоматически изменять размер ячеек в таблице в соответствии с их содержимым. |
| [getAllowCellSpacing()](#getAllowCellSpacing--) | Получает параметр «Разрешить интервалы между ячейками». |
| [getAllowOverlap()](#getAllowOverlap--) | Определяет, должна ли плавающая таблица позволять другим плавающим объектам в документе перекрывать свои экстенты при отображении. |
| [getAncestor(int ancestorType)](#getAncestor-int-) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class-) | Получает первого предка указанного типа объекта. |
| [getBidi()](#getBidi--) | Получает, является ли это таблицей с письмом справа налево. |
| [getBottomPadding()](#getBottomPadding--) | Получает количество места (в пунктах), которое нужно добавить под содержимым ячеек. |
| [getCellSpacing()](#getCellSpacing--) | Получает расстояние (в пунктах) между ячейками. |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean-) |  |
| [getChildNodes()](#getChildNodes--) | Получает все непосредственные дочерние узлы этого узла. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [getClass()](#getClass--) |  |
| [getContainer()](#getContainer--) |  |
| [getCount()](#getCount--) | Получает количество непосредственных дочерних элементов этого узла. |
| [getCurrentNode()](#getCurrentNode--) |  |
| [getCustomNodeId()](#getCustomNodeId--) | Задает идентификатор пользовательского узла. |
| [getDescription()](#getDescription--) | Получает описание этой таблицы. |
| [getDistanceBottom()](#getDistanceBottom--) | Получает расстояние между нижней частью таблицы и окружающим текстом в пунктах. |
| [getDistanceLeft()](#getDistanceLeft--) | Получает расстояние между левой частью таблицы и окружающим текстом в пунктах. |
| [getDistanceRight()](#getDistanceRight--) | Получает расстояние между правой частью таблицы и окружающим текстом в пунктах. |
| [getDistanceTop()](#getDistanceTop--) | Получает расстояние между столешницей и окружающим текстом в пунктах. |
| [getDocument()](#getDocument--) | Получает документ, которому принадлежит этот узел. |
| [getFirstChild()](#getFirstChild--) | Получает первый дочерний элемент узла. |
| [getFirstRow()](#getFirstRow--) |  Возвращает первый**Row** узел в таблице. |
| [getHorizontalAnchor()](#getHorizontalAnchor--) | Получает базовый объект, из которого должно быть рассчитано горизонтальное позиционирование плавающей таблицы. |
| [getLastChild()](#getLastChild--) | Получает последний дочерний элемент узла. |
| [getLastRow()](#getLastRow--) |  Возвращает последний**Row** узел в таблице. |
| [getLeftIndent()](#getLeftIndent--) | Получает значение, представляющее левый отступ таблицы. |
| [getLeftPadding()](#getLeftPadding--) | Получает количество места (в пунктах), которое нужно добавить слева от содержимого ячеек. |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node-) |  |
| [getNextSibling()](#getNextSibling--) | Получает узел, следующий сразу за этим узлом. |
| [getNodeType()](#getNodeType--) |  Возвращает**NodeType.Table**. |
| [getParentNode()](#getParentNode--) | Получает непосредственного родителя этого узла. |
| [getPreferredWidth()](#getPreferredWidth--) | Получает предпочтительную ширину таблицы. |
| [getPreviousSibling()](#getPreviousSibling--) | Получает узел, непосредственно предшествующий этому узлу. |
| [getRange()](#getRange--) |  Возвращает**Range** объект, который представляет часть документа, содержащегося в этом узле. |
| [getRelativeHorizontalAlignment()](#getRelativeHorizontalAlignment--) | Получает относительное горизонтальное выравнивание плавающей таблицы. |
| [getRelativeVerticalAlignment()](#getRelativeVerticalAlignment--) | Получает относительное вертикальное выравнивание плавающей таблицы. |
| [getRightPadding()](#getRightPadding--) | Получает количество места (в пунктах), которое нужно добавить справа от содержимого ячеек. |
| [getRows()](#getRows--) | Предоставляет типизированный доступ к строкам таблицы. |
| [getStyle()](#getStyle--) | Получает стиль таблицы, применяемый к этой таблице. |
| [getStyleIdentifier()](#getStyleIdentifier--) | Получает независимый от языкового стандарта идентификатор стиля таблицы, примененный к этой таблице. |
| [getStyleName()](#getStyleName--) | Получает имя стиля таблицы, примененного к этой таблице. |
| [getStyleOptions()](#getStyleOptions--) | Получает битовые флаги, указывающие, как стиль таблицы применяется к этой таблице. |
| [getText()](#getText--) | Получает текст этого узла и всех его дочерних элементов. |
| [getTextWrapping()](#getTextWrapping--) |  Получает[getTextWrapping()](../../com.aspose.words/table\#getTextWrapping--) / [setTextWrapping(int)](../../com.aspose.words/table\#setTextWrapping-int-) для стола. |
| [getTitle()](#getTitle--) | Получает заголовок этой таблицы. |
| [getTopPadding()](#getTopPadding--) | Получает количество места (в пунктах), которое нужно добавить над содержимым ячеек. |
| [getVerticalAnchor()](#getVerticalAnchor--) | Получает базовый объект, из которого должно быть рассчитано вертикальное позиционирование плавающей таблицы. |
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
| [setAbsoluteHorizontalDistance(double value)](#setAbsoluteHorizontalDistance-double-) | Устанавливает абсолютную горизонтальную позицию плавающей таблицы, указанную в свойствах таблицы, в пунктах. |
| [setAbsoluteVerticalDistance(double value)](#setAbsoluteVerticalDistance-double-) | Устанавливает абсолютную вертикальную плавающую позицию таблицы, указанную в свойствах таблицы, в пунктах. |
| [setAlignment(int value)](#setAlignment-int-) | Указывает, как встроенная таблица выравнивается в документе. |
| [setAllowAutoFit(boolean value)](#setAllowAutoFit-boolean-) | Позволяет Microsoft Word и Aspose.Words автоматически изменять размер ячеек в таблице в соответствии с их содержимым. |
| [setAllowCellSpacing(boolean value)](#setAllowCellSpacing-boolean-) | Устанавливает параметр «Разрешить интервалы между ячейками». |
| [setBidi(boolean value)](#setBidi-boolean-) | Устанавливает, является ли это таблицей справа налево. |
| [setBorder(int borderType, int lineStyle, double lineWidth, Color color, boolean isOverrideCellBorders)](#setBorder-int-int-double-java.awt.Color-boolean-) |  |
| [setBorders(int lineStyle, double lineWidth, Color color)](#setBorders-int-double-java.awt.Color-) |  |
| [setBottomPadding(double value)](#setBottomPadding-double-) | Устанавливает количество места (в пунктах) для добавления под содержимым ячеек. |
| [setCellSpacing(double value)](#setCellSpacing-double-) | Устанавливает расстояние (в пунктах) между ячейками. |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | Задает идентификатор пользовательского узла. |
| [setDescription(String value)](#setDescription-java.lang.String-) | Задает описание этой таблицы. |
| [setHorizontalAnchor(int value)](#setHorizontalAnchor-int-) | Получает базовый объект, из которого должно быть рассчитано горизонтальное позиционирование плавающей таблицы. |
| [setLeftIndent(double value)](#setLeftIndent-double-) | Задает значение, представляющее левый отступ таблицы. |
| [setLeftPadding(double value)](#setLeftPadding-double-) | Устанавливает количество места (в пунктах), которое добавляется слева от содержимого ячеек. |
| [setPreferredWidth(PreferredWidth value)](#setPreferredWidth-com.aspose.words.PreferredWidth-) | Устанавливает предпочтительную ширину таблицы. |
| [setRelativeHorizontalAlignment(int value)](#setRelativeHorizontalAlignment-int-) | Устанавливает относительное горизонтальное выравнивание плавающей таблицы. |
| [setRelativeVerticalAlignment(int value)](#setRelativeVerticalAlignment-int-) | Устанавливает относительное вертикальное выравнивание плавающей таблицы. |
| [setRightPadding(double value)](#setRightPadding-double-) | Устанавливает количество места (в пунктах), которое добавляется справа от содержимого ячеек. |
| [setShading(int texture, Color foregroundColor, Color backgroundColor)](#setShading-int-java.awt.Color-java.awt.Color-) |  |
| [setStyle(Style value)](#setStyle-com.aspose.words.Style-) | Задает стиль таблицы, применяемый к этой таблице. |
| [setStyleIdentifier(int value)](#setStyleIdentifier-int-) | Задает независимый от локали идентификатор стиля таблицы, примененный к этой таблице. |
| [setStyleName(String value)](#setStyleName-java.lang.String-) | Задает имя стиля таблицы, применяемого к этой таблице. |
| [setStyleOptions(int value)](#setStyleOptions-int-) | Устанавливает битовые флаги, которые определяют, как стиль таблицы применяется к этой таблице. |
| [setTextWrapping(int value)](#setTextWrapping-int-) |  Наборы[getTextWrapping()](../../com.aspose.words/table\#getTextWrapping--) / [setTextWrapping(int)](../../com.aspose.words/table\#setTextWrapping-int-) для стола. |
| [setTitle(String value)](#setTitle-java.lang.String-) | Устанавливает заголовок этой таблицы. |
| [setTopPadding(double value)](#setTopPadding-double-) | Устанавливает количество места (в пунктах) для добавления над содержимым ячеек. |
| [setVerticalAnchor(int value)](#setVerticalAnchor-int-) | Получает базовый объект, из которого должно быть рассчитано вертикальное позиционирование плавающей таблицы. |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| [toString(int saveFormat)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### Table(DocumentBase doc) {#Table-com.aspose.words.DocumentBase-}
```
public Table(DocumentBase doc)
```


 Инициализирует новый экземпляр**Table** учебный класс.

 Когда**Table** создан, он принадлежит указанному документу, но еще не является его частью и**ParentNode** нулевой.

 Чтобы добавить**Table** к документу используйте InsertAfter или InsertBefore для истории, в которую вы хотите вставить таблицу.

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
boolean - Истинно, если были посещены все узлы; false, если DocumentVisitor остановил операцию перед посещением всех узлов. Вызывает DocumentVisitor.VisitTableStart, затем вызывает Accept для всех дочерних узлов раздела и в конце вызывает DocumentVisitor.VisitTableEnd.
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
### autoFit(int behavior) {#autoFit-int-}
```
public void autoFit(int behavior)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| behavior | int |  |

### clearBorders() {#clearBorders--}
```
public void clearBorders()
```


Удаляет все границы таблиц и ячеек в этой таблице.

### clearShading() {#clearShading--}
```
public void clearShading()
```


Удаляет все тени на столе.

### convertToHorizontallyMergedCells() {#convertToHorizontallyMergedCells--}
```
public void convertToHorizontallyMergedCells()
```


 Преобразует ячейки, объединенные по горизонтали по ширине, в ячейки, объединенные по ширине.[CellFormat.getHorizontalMerge()](../../com.aspose.words/cellformat\#getHorizontalMerge--) / [CellFormat.setHorizontalMerge(int)](../../com.aspose.words/cellformat\#setHorizontalMerge-int-).

 Ячейки таблицы могут быть объединены по горизонтали с помощью флагов слияния.[CellFormat.getHorizontalMerge()](../../com.aspose.words/cellformat\#getHorizontalMerge--) / [CellFormat.setHorizontalMerge(int)](../../com.aspose.words/cellformat\#setHorizontalMerge-int-) или используя ширину ячейки[CellFormat.getWidth()](../../com.aspose.words/cellformat\#getWidth--) / [CellFormat.setWidth(double)](../../com.aspose.words/cellformat\#setWidth-double-).

 Когда ячейка таблицы объединяется по свойству ширины[CellFormat.getHorizontalMerge()](../../com.aspose.words/cellformat\#getHorizontalMerge--) / [CellFormat.setHorizontalMerge(int)](../../com.aspose.words/cellformat\#setHorizontalMerge-int-) бессмысленно, но иногда использование флагов слияния является более удобным способом.

Используйте этот метод для преобразования ячеек таблицы, объединенных по горизонтали по ширине, в ячейки, объединенные флагами слияния.

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


 Если в таблице нет строк, создает и добавляет одну**Row**.

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
### getAbsoluteHorizontalDistance() {#getAbsoluteHorizontalDistance--}
```
public double getAbsoluteHorizontalDistance()
```


Получает абсолютную горизонтальную позицию плавающей таблицы, указанную в свойствах таблицы, в пунктах. Значение по умолчанию — 0.

**Возвращает:**
double - Абсолютная горизонтальная плавающая позиция таблицы, заданная свойствами таблицы, в пунктах.
### getAbsoluteVerticalDistance() {#getAbsoluteVerticalDistance--}
```
public double getAbsoluteVerticalDistance()
```


Получает абсолютную вертикальную плавающую позицию таблицы, указанную в свойствах таблицы, в пунктах. Значение по умолчанию — 0.

**Возвращает:**
double - Абсолютная вертикальная плавающая позиция таблицы, заданная свойствами таблицы, в пунктах.
### getAlignment() {#getAlignment--}
```
public int getAlignment()
```


Указывает, как встроенная таблица выравнивается в документе.

 Значение по умолчанию[TableAlignment.LEFT](../../com.aspose.words/tablealignment\#LEFT).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[TableAlignment](../../com.aspose.words/tablealignment) константы.
### getAllowAutoFit() {#getAllowAutoFit--}
```
public boolean getAllowAutoFit()
```


Позволяет Microsoft Word и Aspose.Words автоматически изменять размер ячеек в таблице в соответствии с их содержимым.

Значение по умолчанию верно .

**M:Aspose.Words.Tables.Table.AutoFit(Aspose.Words.Tables.AutoFitBehavior)**

**Возвращает:**
boolean - соответствующее логическое значение.
### getAllowCellSpacing() {#getAllowCellSpacing--}
```
public boolean getAllowCellSpacing()
```


Получает параметр «Разрешить интервалы между ячейками».

**Возвращает:**
boolean — опция «Разрешить интервалы между ячейками».
### getAllowOverlap() {#getAllowOverlap--}
```
public boolean getAllowOverlap()
```


Определяет, должна ли плавающая таблица позволять другим плавающим объектам в документе перекрывать свои экстенты при отображении. Значение по умолчанию — true.

**Возвращает:**
boolean - Должна ли плавающая таблица позволять другим плавающим объектам в документе перекрывать свои экстенты при отображении.
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
### getBidi() {#getBidi--}
```
public boolean getBidi()
```


Получает, является ли это таблицей с письмом справа налево.

При значении true ячейки в этой строке располагаются справа налево.

Значение по умолчанию неверно .

**Возвращает:**
boolean - Является ли это таблицей справа налево.
### getBottomPadding() {#getBottomPadding--}
```
public double getBottomPadding()
```


Получает количество места (в пунктах), которое нужно добавить под содержимым ячеек.

**Возвращает:**
double - количество места (в пунктах), которое нужно добавить под содержимым ячеек.
### getCellSpacing() {#getCellSpacing--}
```
public double getCellSpacing()
```


Получает расстояние (в пунктах) между ячейками.

**Возвращает:**
double - количество пробелов (в пунктах) между ячейками.
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


Получает описание этой таблицы. Он обеспечивает альтернативное текстовое представление информации, содержащейся в таблице.

Значение по умолчанию — пустая строка.

 Это свойство имеет значение для документов DOCX, соответствующих стандарту ISO/IEC 29500 ([OoxmlCompliance](../../com.aspose.words/ooxmlcompliance)). При сохранении в форматах, предшествующих ISO/IEC 29500, это свойство игнорируется.

**Возвращает:**
java.lang.String — Описание этой таблицы.
### getDistanceBottom() {#getDistanceBottom--}
```
public double getDistanceBottom()
```


Получает расстояние между нижней частью таблицы и окружающим текстом в пунктах.

**Возвращает:**
double - Расстояние между низом таблицы и окружающим текстом в пунктах.
### getDistanceLeft() {#getDistanceLeft--}
```
public double getDistanceLeft()
```


Получает расстояние между левой частью таблицы и окружающим текстом в пунктах.

**Возвращает:**
double - Расстояние между левой частью таблицы и окружающим текстом в пунктах.
### getDistanceRight() {#getDistanceRight--}
```
public double getDistanceRight()
```


Получает расстояние между правой частью таблицы и окружающим текстом в пунктах.

**Возвращает:**
double - Расстояние между правым столом и окружающим текстом в пунктах.
### getDistanceTop() {#getDistanceTop--}
```
public double getDistanceTop()
```


Получает расстояние между столешницей и окружающим текстом в пунктах.

**Возвращает:**
double - Расстояние между столешницей и окружающим текстом в пунктах.
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
### getFirstRow() {#getFirstRow--}
```
public Row getFirstRow()
```


 Возвращает первый**Row** узел в таблице.

**Возвращает:**
[Row](../../com.aspose.words/row) - Первый**Row** узел в таблице.
### getHorizontalAnchor() {#getHorizontalAnchor--}
```
public int getHorizontalAnchor()
```


 Получает базовый объект, из которого должно быть рассчитано горизонтальное позиционирование плавающей таблицы. Значение по умолчанию[RelativeHorizontalPosition.COLUMN](../../com.aspose.words/relativehorizontalposition\#COLUMN).

**Возвращает:**
 int - Базовый объект, из которого должно быть рассчитано горизонтальное позиционирование плавающей таблицы. Возвращаемое значение является одним из[RelativeHorizontalPosition](../../com.aspose.words/relativehorizontalposition) константы.
### getLastChild() {#getLastChild--}
```
public Node getLastChild()
```


Получает последний дочерний элемент узла. Если последнего дочернего узла нет, возвращается нуль.

**Возвращает:**
[Node](../../com.aspose.words/node) - Последний дочерний узел.
### getLastRow() {#getLastRow--}
```
public Row getLastRow()
```


 Возвращает последний**Row** узел в таблице.

**Возвращает:**
[Row](../../com.aspose.words/row) - Последний**Row** узел в таблице.
### getLeftIndent() {#getLeftIndent--}
```
public double getLeftIndent()
```


Получает значение, представляющее левый отступ таблицы.

**Возвращает:**
double — значение, представляющее левый отступ таблицы.
### getLeftPadding() {#getLeftPadding--}
```
public double getLeftPadding()
```


Получает количество места (в пунктах), которое нужно добавить слева от содержимого ячеек.

**Возвращает:**
double - Количество места (в пунктах) для добавления слева от содержимого ячеек.
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


 Возвращает**NodeType.Table**.

**Возвращает:**
 инт -**NodeType.Table** . Возвращаемое значение является одним из[NodeType](../../com.aspose.words/nodetype) константы.
### getParentNode() {#getParentNode--}
```
public CompositeNode getParentNode()
```


Получает непосредственного родителя этого узла.

Если узел был только что создан и еще не добавлен в дерево, или если он был удален из дерева, родитель имеет значение null.

**Возвращает:**
[CompositeNode](../../com.aspose.words/compositenode) - Непосредственный родитель этого узла.
### getPreferredWidth() {#getPreferredWidth--}
```
public PreferredWidth getPreferredWidth()
```


Получает предпочтительную ширину таблицы.

 Значение по умолчанию[PreferredWidth.AUTO](../../com.aspose.words/preferredwidth\#AUTO).

**Возвращает:**
[PreferredWidth](../../com.aspose.words/preferredwidth) - Предпочтительная ширина стола.
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
### getRelativeHorizontalAlignment() {#getRelativeHorizontalAlignment--}
```
public int getRelativeHorizontalAlignment()
```


Получает относительное горизонтальное выравнивание плавающей таблицы.

**Возвращает:**
 int - Относительное горизонтальное выравнивание плавающей таблицы. Возвращаемое значение является одним из[HorizontalAlignment](../../com.aspose.words/horizontalalignment) константы.
### getRelativeVerticalAlignment() {#getRelativeVerticalAlignment--}
```
public int getRelativeVerticalAlignment()
```


Получает относительное вертикальное выравнивание плавающей таблицы.

**Возвращает:**
 int - относительное вертикальное выравнивание плавающей таблицы. Возвращаемое значение является одним из[VerticalAlignment](../../com.aspose.words/verticalalignment) константы.
### getRightPadding() {#getRightPadding--}
```
public double getRightPadding()
```


Получает количество места (в пунктах), которое нужно добавить справа от содержимого ячеек.

**Возвращает:**
double - Количество места (в пунктах) для добавления справа от содержимого ячеек.
### getRows() {#getRows--}
```
public RowCollection getRows()
```


Предоставляет типизированный доступ к строкам таблицы.

**Возвращает:**
[RowCollection](../../com.aspose.words/rowcollection) - соответствующий[RowCollection](../../com.aspose.words/rowcollection) ценность.
### getStyle() {#getStyle--}
```
public Style getStyle()
```


Получает стиль таблицы, применяемый к этой таблице.

**Возвращает:**
[Style](../../com.aspose.words/style) - Стиль таблицы, примененный к этой таблице.
### getStyleIdentifier() {#getStyleIdentifier--}
```
public int getStyleIdentifier()
```


Получает независимый от языкового стандарта идентификатор стиля таблицы, примененный к этой таблице.

**Возвращает:**
 int — независимый от локали идентификатор стиля таблицы, примененный к этой таблице. Возвращаемое значение является одним из[StyleIdentifier](../../com.aspose.words/styleidentifier) константы.
### getStyleName() {#getStyleName--}
```
public String getStyleName()
```


Получает имя стиля таблицы, примененного к этой таблице.

**Возвращает:**
java.lang.String — имя стиля таблицы, примененного к этой таблице.
### getStyleOptions() {#getStyleOptions--}
```
public int getStyleOptions()
```


Получает битовые флаги, указывающие, как стиль таблицы применяется к этой таблице.

**Возвращает:**
 int — битовые флаги, указывающие, как стиль таблицы применяется к этой таблице. Возвращаемое значение представляет собой побитовую комбинацию[TableStyleOptions](../../com.aspose.words/tablestyleoptions) константы.
### getText() {#getText--}
```
public String getText()
```


Получает текст этого узла и всех его дочерних элементов.

 Возвращаемая строка включает все управляющие и специальные символы, как описано в[ControlChar](../../com.aspose.words/controlchar).

**Возвращает:**
java.lang.String
### getTextWrapping() {#getTextWrapping--}
```
public int getTextWrapping()
```


 Получает[getTextWrapping()](../../com.aspose.words/table\#getTextWrapping--) / [setTextWrapping(int)](../../com.aspose.words/table\#setTextWrapping-int-) для стола.

**Возвращает:**
 инт -\{[getTextWrapping()](../../com.aspose.words/table\#getTextWrapping--) / [setTextWrapping(int)](../../com.aspose.words/table\#setTextWrapping-int-) для стола. Возвращаемое значение является одним из[TextWrapping](../../com.aspose.words/textwrapping) константы.
### getTitle() {#getTitle--}
```
public String getTitle()
```


Получает заголовок этой таблицы. Он обеспечивает альтернативное текстовое представление информации, содержащейся в таблице.

Значение по умолчанию — пустая строка.

 Это свойство имеет значение для документов DOCX, соответствующих стандарту ISO/IEC 29500 ([OoxmlCompliance](../../com.aspose.words/ooxmlcompliance)). При сохранении в форматах, предшествующих ISO/IEC 29500, это свойство игнорируется.

**Возвращает:**
java.lang.String — Заголовок этой таблицы.
### getTopPadding() {#getTopPadding--}
```
public double getTopPadding()
```


Получает количество места (в пунктах), которое нужно добавить над содержимым ячеек.

**Возвращает:**
double - количество места (в пунктах), которое нужно добавить над содержимым ячеек.
### getVerticalAnchor() {#getVerticalAnchor--}
```
public int getVerticalAnchor()
```


 Получает базовый объект, из которого должно быть рассчитано вертикальное позиционирование плавающей таблицы. Значение по умолчанию[RelativeVerticalPosition.MARGIN](../../com.aspose.words/relativeverticalposition\#MARGIN).

**Возвращает:**
 int - Базовый объект, из которого должно быть рассчитано вертикальное позиционирование плавающей таблицы. Возвращаемое значение является одним из[RelativeVerticalPosition](../../com.aspose.words/relativeverticalposition) константы.
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
### setAbsoluteHorizontalDistance(double value) {#setAbsoluteHorizontalDistance-double-}
```
public void setAbsoluteHorizontalDistance(double value)
```


Устанавливает абсолютную горизонтальную позицию плавающей таблицы, указанную в свойствах таблицы, в пунктах. Значение по умолчанию — 0.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Абсолютное горизонтальное плавающее положение таблицы, заданное свойствами таблицы, в пунктах. |

### setAbsoluteVerticalDistance(double value) {#setAbsoluteVerticalDistance-double-}
```
public void setAbsoluteVerticalDistance(double value)
```


Устанавливает абсолютную вертикальную плавающую позицию таблицы, указанную в свойствах таблицы, в пунктах. Значение по умолчанию — 0.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Абсолютная вертикальная плавающая позиция таблицы, заданная свойствами таблицы, в пунктах. |

### setAlignment(int value) {#setAlignment-int-}
```
public void setAlignment(int value)
```


Указывает, как встроенная таблица выравнивается в документе.

 Значение по умолчанию[TableAlignment.LEFT](../../com.aspose.words/tablealignment\#LEFT).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[TableAlignment](../../com.aspose.words/tablealignment) константы. |

### setAllowAutoFit(boolean value) {#setAllowAutoFit-boolean-}
```
public void setAllowAutoFit(boolean value)
```


Позволяет Microsoft Word и Aspose.Words автоматически изменять размер ячеек в таблице в соответствии с их содержимым.

Значение по умолчанию верно .

**M:Aspose.Words.Tables.Table.AutoFit(Aspose.Words.Tables.AutoFitBehavior)**

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setAllowCellSpacing(boolean value) {#setAllowCellSpacing-boolean-}
```
public void setAllowCellSpacing(boolean value)
```


Устанавливает параметр «Разрешить интервалы между ячейками».

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Опция «Разрешить интервалы между ячейками». |

### setBidi(boolean value) {#setBidi-boolean-}
```
public void setBidi(boolean value)
```


Устанавливает, является ли это таблицей справа налево.

При значении true ячейки в этой строке располагаются справа налево.

Значение по умолчанию неверно .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Является ли это таблицей справа налево. |

### setBorder(int borderType, int lineStyle, double lineWidth, Color color, boolean isOverrideCellBorders) {#setBorder-int-int-double-java.awt.Color-boolean-}
```
public void setBorder(int borderType, int lineStyle, double lineWidth, Color color, boolean isOverrideCellBorders)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| borderType | int |  |
| lineStyle | int |  |
| lineWidth | double |  |
| color | java.awt.Color |  |
| isOverrideCellBorders | boolean |  |

### setBorders(int lineStyle, double lineWidth, Color color) {#setBorders-int-double-java.awt.Color-}
```
public void setBorders(int lineStyle, double lineWidth, Color color)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| lineStyle | int |  |
| lineWidth | double |  |
| color | java.awt.Color |  |

### setBottomPadding(double value) {#setBottomPadding-double-}
```
public void setBottomPadding(double value)
```


Устанавливает количество места (в пунктах) для добавления под содержимым ячеек.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Количество места (в пунктах), которое нужно добавить под содержимым ячеек. |

### setCellSpacing(double value) {#setCellSpacing-double-}
```
public void setCellSpacing(double value)
```


Устанавливает расстояние (в пунктах) между ячейками.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Расстояние (в пунктах) между ячейками. |

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


Задает описание этой таблицы. Он обеспечивает альтернативное текстовое представление информации, содержащейся в таблице.

Значение по умолчанию — пустая строка.

 Это свойство имеет значение для документов DOCX, соответствующих стандарту ISO/IEC 29500 ([OoxmlCompliance](../../com.aspose.words/ooxmlcompliance)). При сохранении в форматах, предшествующих ISO/IEC 29500, это свойство игнорируется.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Описание этой таблицы. |

### setHorizontalAnchor(int value) {#setHorizontalAnchor-int-}
```
public void setHorizontalAnchor(int value)
```


 Получает базовый объект, из которого должно быть рассчитано горизонтальное позиционирование плавающей таблицы. Значение по умолчанию[RelativeHorizontalPosition.COLUMN](../../com.aspose.words/relativehorizontalposition\#COLUMN).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Базовый объект, из которого должно быть рассчитано горизонтальное позиционирование плавающей таблицы. Значение должно быть одним из[RelativeHorizontalPosition](../../com.aspose.words/relativehorizontalposition) константы. |

### setLeftIndent(double value) {#setLeftIndent-double-}
```
public void setLeftIndent(double value)
```


Задает значение, представляющее левый отступ таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Значение, представляющее левый отступ таблицы. |

### setLeftPadding(double value) {#setLeftPadding-double-}
```
public void setLeftPadding(double value)
```


Устанавливает количество места (в пунктах), которое добавляется слева от содержимого ячеек.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Количество места (в пунктах) для добавления слева от содержимого ячеек. |

### setPreferredWidth(PreferredWidth value) {#setPreferredWidth-com.aspose.words.PreferredWidth-}
```
public void setPreferredWidth(PreferredWidth value)
```


Устанавливает предпочтительную ширину таблицы.

 Значение по умолчанию[PreferredWidth.AUTO](../../com.aspose.words/preferredwidth\#AUTO).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [PreferredWidth](../../com.aspose.words/preferredwidth) | Стол предпочтительной ширины. |

### setRelativeHorizontalAlignment(int value) {#setRelativeHorizontalAlignment-int-}
```
public void setRelativeHorizontalAlignment(int value)
```


Устанавливает относительное горизонтальное выравнивание плавающей таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Относительное горизонтальное выравнивание плавающей таблицы. Значение должно быть одним из[HorizontalAlignment](../../com.aspose.words/horizontalalignment) константы. |

### setRelativeVerticalAlignment(int value) {#setRelativeVerticalAlignment-int-}
```
public void setRelativeVerticalAlignment(int value)
```


Устанавливает относительное вертикальное выравнивание плавающей таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Относительное выравнивание плавающей таблицы по вертикали. Значение должно быть одним из[VerticalAlignment](../../com.aspose.words/verticalalignment) константы. |

### setRightPadding(double value) {#setRightPadding-double-}
```
public void setRightPadding(double value)
```


Устанавливает количество места (в пунктах), которое добавляется справа от содержимого ячеек.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Количество места (в пунктах), которое нужно добавить справа от содержимого ячеек. |

### setShading(int texture, Color foregroundColor, Color backgroundColor) {#setShading-int-java.awt.Color-java.awt.Color-}
```
public void setShading(int texture, Color foregroundColor, Color backgroundColor)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| texture | int |  |
| foregroundColor | java.awt.Color |  |
| backgroundColor | java.awt.Color |  |

### setStyle(Style value) {#setStyle-com.aspose.words.Style-}
```
public void setStyle(Style value)
```


Задает стиль таблицы, применяемый к этой таблице.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style) | Стиль таблицы, примененный к этой таблице. |

### setStyleIdentifier(int value) {#setStyleIdentifier-int-}
```
public void setStyleIdentifier(int value)
```


Задает независимый от локали идентификатор стиля таблицы, примененный к этой таблице.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Независимый от локали идентификатор стиля таблицы, примененный к этой таблице. Значение должно быть одним из[StyleIdentifier](../../com.aspose.words/styleidentifier) константы. |

### setStyleName(String value) {#setStyleName-java.lang.String-}
```
public void setStyleName(String value)
```


Задает имя стиля таблицы, применяемого к этой таблице.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя стиля таблицы, примененного к этой таблице. |

### setStyleOptions(int value) {#setStyleOptions-int-}
```
public void setStyleOptions(int value)
```


Устанавливает битовые флаги, которые определяют, как стиль таблицы применяется к этой таблице.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Битовые флаги, указывающие, как стиль таблицы применяется к этой таблице. Значение должно быть побитовой комбинацией[TableStyleOptions](../../com.aspose.words/tablestyleoptions) константы. |

### setTextWrapping(int value) {#setTextWrapping-int-}
```
public void setTextWrapping(int value)
```


 Наборы[getTextWrapping()](../../com.aspose.words/table\#getTextWrapping--) / [setTextWrapping(int)](../../com.aspose.words/table\#setTextWrapping-int-) для стола.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | \{[getTextWrapping()](../../com.aspose.words/table\#getTextWrapping--) / [setTextWrapping(int)](../../com.aspose.words/table\#setTextWrapping-int-) для стола. Значение должно быть одним из[TextWrapping](../../com.aspose.words/textwrapping) константы. |

### setTitle(String value) {#setTitle-java.lang.String-}
```
public void setTitle(String value)
```


Устанавливает заголовок этой таблицы. Он обеспечивает альтернативное текстовое представление информации, содержащейся в таблице.

Значение по умолчанию — пустая строка.

 Это свойство имеет значение для документов DOCX, соответствующих стандарту ISO/IEC 29500 ([OoxmlCompliance](../../com.aspose.words/ooxmlcompliance)). При сохранении в форматах, предшествующих ISO/IEC 29500, это свойство игнорируется.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Название этой таблицы. |

### setTopPadding(double value) {#setTopPadding-double-}
```
public void setTopPadding(double value)
```


Устанавливает количество места (в пунктах) для добавления над содержимым ячеек.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Количество места (в пунктах), которое нужно добавить над содержимым ячеек. |

### setVerticalAnchor(int value) {#setVerticalAnchor-int-}
```
public void setVerticalAnchor(int value)
```


 Получает базовый объект, из которого должно быть рассчитано вертикальное позиционирование плавающей таблицы. Значение по умолчанию[RelativeVerticalPosition.MARGIN](../../com.aspose.words/relativeverticalposition\#MARGIN).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Базовый объект, из которого должно быть рассчитано вертикальное позиционирование плавающего стола. Значение должно быть одним из[RelativeVerticalPosition](../../com.aspose.words/relativeverticalposition) константы. |

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
