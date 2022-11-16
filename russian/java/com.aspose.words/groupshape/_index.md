---
title: GroupShape
second_title: Справочник по API Aspose.Words для Java
description: Представляет группу фигур в документе.
type: docs
weight: 314
url: /ru/java/com.aspose.words/groupshape/
---

**Наследование:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode), [com.aspose.words.ShapeBase](../../com.aspose.words/shapebase)
```
public class GroupShape extends ShapeBase
```

Представляет группу фигур в документе.

 Чтобы узнать больше, посетите**How to Add Group Shape into a Word Document** документальная статья.

 А[GroupShape](../../com.aspose.words/groupshape) является составным узлом и может иметь[Shape](../../com.aspose.words/shape) а также[GroupShape](../../com.aspose.words/groupshape) узлы как дети.

 Каждый[GroupShape](../../com.aspose.words/groupshape) определяет новую систему координат для своих дочерних фигур. Система координат определяется с помощью[ShapeBase.getCoordSize()](../../com.aspose.words/shapebase\#getCoordSize--) / [ShapeBase.setCoordSize(java.awt.Dimension)](../../com.aspose.words/shapebase\#setCoordSize-java.awt.Dimension-) а также[ShapeBase.getCoordOrigin()](../../com.aspose.words/shapebase\#getCoordOrigin--) / [ShapeBase.setCoordOrigin(java.awt.Point)](../../com.aspose.words/shapebase\#setCoordOrigin-java.awt.Point-) характеристики.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [GroupShape(DocumentBase doc)](#GroupShape-com.aspose.words.DocumentBase-) | Создает новую форму группы. |
## Методы

| Метод | Описание |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Принимает посетителя. |
| [adjustWithEffects(Rectangle2D.Float source)](#adjustWithEffects-java.awt.geom.Rectangle2D.Float-) | Добавляет к исходному прямоугольнику значения экстента эффекта и возвращает окончательный прямоугольник. |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node-) | Добавляет указанный узел в конец списка дочерних узлов для этого узла. |
| [canHaveImage()](#canHaveImage--) | Возвращает true, если тип фигуры позволяет фигуре иметь изображение. |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [dd()](#dd--) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | Создает дубликат узла. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int-) |  |
| [fetchInheritedShapeAttr(int key)](#fetchInheritedShapeAttr-int-) | Зарезервировано для системного использования. |
| [fetchShapeAttr(int key)](#fetchShapeAttr-int-) | Зарезервировано для системного использования. |
| [getAllowOverlap()](#getAllowOverlap--) | Получает значение, указывающее, может ли эта фигура перекрывать другие фигуры. |
| [getAlternativeText()](#getAlternativeText--) | Определяет альтернативный текст, который будет отображаться вместо графики. |
| [getAncestor(int ancestorType)](#getAncestor-int-) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class-) | Получает первого предка указанного типа объекта. |
| [getAnchorLocked()](#getAnchorLocked--) | Указывает, заблокирована ли привязка фигуры. |
| [getAspectRatioLocked()](#getAspectRatioLocked--) | Указывает, заблокировано ли соотношение сторон фигуры. |
| [getBehindText()](#getBehindText--) | Указывает, находится ли фигура ниже или выше текста. |
| [getBottom()](#getBottom--) | Получает положение нижнего края содержащего блока фигуры. |
| [getBounds()](#getBounds--) | Получает расположение и размер содержащего блока фигуры. |
| [getBoundsInPoints()](#getBoundsInPoints--) | Получает расположение и размер содержащего блока фигуры в пунктах относительно привязки самой верхней фигуры. |
| [getBoundsWithEffects()](#getBoundsWithEffects--) | Получает окончательную степень, которую имеет этот объект формы после применения эффектов рисования. |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean-) |  |
| [getChildNodes()](#getChildNodes--) | Получает все непосредственные дочерние узлы этого узла. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [getClass()](#getClass--) |  |
| [getContainer()](#getContainer--) |  |
| [getCoordOrigin()](#getCoordOrigin--) | Координаты в верхнем левом углу содержащего блока этой формы. |
| [getCoordSize()](#getCoordSize--) | Ширина и высота координатного пространства внутри содержащего блока этой формы. |
| [getCount()](#getCount--) | Получает количество непосредственных дочерних элементов этого узла. |
| [getCurrentNode()](#getCurrentNode--) |  |
| [getCustomNodeId()](#getCustomNodeId--) | Задает идентификатор пользовательского узла. |
| [getDirectRunAttr(int fontAttr)](#getDirectRunAttr-int-) |  |
| [getDirectShapeAttr(int key)](#getDirectShapeAttr-int-) | Зарезервировано для системного использования. |
| [getDistanceBottom()](#getDistanceBottom--) | Получает расстояние (в пунктах) между текстом документа и нижним краем фигуры. |
| [getDistanceLeft()](#getDistanceLeft--) | Получает расстояние (в пунктах) между текстом документа и левым краем фигуры. |
| [getDistanceRight()](#getDistanceRight--) | Получает расстояние (в пунктах) между текстом документа и правым краем фигуры. |
| [getDistanceTop()](#getDistanceTop--) | Получает расстояние (в пунктах) между текстом документа и верхним краем фигуры. |
| [getDocument()](#getDocument--) | Получает документ, которому принадлежит этот узел. |
| [getDocument_IInline()](#getDocument-IInline--) |  |
| [getFill()](#getFill--) | Получает форматирование заливки для фигуры. |
| [getFillType()](#getFillType--) |  |
| [getFillableBackColor()](#getFillableBackColor--) |  |
| [getFillableForeColor()](#getFillableForeColor--) |  |
| [getFillableImageBytes()](#getFillableImageBytes--) |  |
| [getFillableTransparency()](#getFillableTransparency--) |  |
| [getFillableVisible()](#getFillableVisible--) |  |
| [getFilledColor()](#getFilledColor--) |  |
| [getFirstChild()](#getFirstChild--) | Получает первый дочерний элемент узла. |
| [getFlipOrientation()](#getFlipOrientation--) | Переключает ориентацию фигуры. |
| [getFont()](#getFont--) | Предоставляет доступ к форматированию шрифта этого объекта. |
| [getGradientAngle()](#getGradientAngle--) |  |
| [getGradientStops()](#getGradientStops--) |  |
| [getGradientStyle()](#getGradientStyle--) |  |
| [getGradientVariant()](#getGradientVariant--) |  |
| [getHRef()](#getHRef--) | Получает полный адрес гиперссылки для фигуры. |
| [getHeight()](#getHeight--) | Получает высоту содержащего блока фигуры. |
| [getHorizontalAlignment()](#getHorizontalAlignment--) | Указывает, как фигура располагается по горизонтали. |
| [getLastChild()](#getLastChild--) | Получает последний дочерний элемент узла. |
| [getLeft()](#getLeft--) | Получает положение левого края содержащего блока фигуры. |
| [getMarkupLanguage()](#getMarkupLanguage--) | Получает язык разметки, используемый для этого графического объекта. |
| [getName()](#getName--) | Получает необязательное имя формы. |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node-) |  |
| [getNextSibling()](#getNextSibling--) | Получает узел, следующий сразу за этим узлом. |
| [getNodeType()](#getNodeType--) |  Возвращает[NodeType.GROUP\_SHAPE](../../com.aspose.words/nodetype\#GROUP-SHAPE). |
| [getOn()](#getOn--) |  |
| [getOpacity()](#getOpacity--) |  |
| [getParentNode()](#getParentNode--) | Получает непосредственного родителя этого узла. |
| [getParentParagraph()](#getParentParagraph--) | Возвращает ближайший родительский абзац. |
| [getParentParagraph_IInline()](#getParentParagraph-IInline--) |  |
| [getPatternType()](#getPatternType--) |  |
| [getPresetTexture()](#getPresetTexture--) |  |
| [getPreviousSibling()](#getPreviousSibling--) | Получает узел, непосредственно предшествующий этому узлу. |
| [getRange()](#getRange--) |  Возвращает**Range** объект, который представляет часть документа, содержащегося в этом узле. |
| [getRelativeHorizontalPosition()](#getRelativeHorizontalPosition--) | Указывает, относительно чего фигура расположена горизонтально. |
| [getRelativeVerticalPosition()](#getRelativeVerticalPosition--) | Указывает, относительно чего фигура расположена вертикально. |
| [getRight()](#getRight--) | Получает положение правого края содержащего блока фигуры. |
| [getRotateWithObject()](#getRotateWithObject--) |  |
| [getRotation()](#getRotation--) | Определяет угол (в градусах), на который поворачивается фигура. |
| [getScreenTip()](#getScreenTip--) | Определяет текст, отображаемый при наведении указателя мыши на фигуру. |
| [getShadowFormat()](#getShadowFormat--) | Получает теневое форматирование для фигуры. |
| [getShapeRenderer()](#getShapeRenderer--) | Создает и возвращает объект, который можно использовать для преобразования этой формы в изображение. |
| [getShapeType()](#getShapeType--) | Получает тип фигуры. |
| [getSizeInPoints()](#getSizeInPoints--) | Получает размер фигуры в точках. |
| [getTarget()](#getTarget--) | Получает целевой кадр для гиперссылки формы. |
| [getText()](#getText--) | Получает текст этого узла и всех его дочерних элементов. |
| [getTextureAlignment()](#getTextureAlignment--) |  |
| [getTitle()](#getTitle--) | Получает заголовок (заголовок) текущего объекта формы. |
| [getTop()](#getTop--) | Получает положение верхнего края содержащего блока фигуры. |
| [getVerticalAlignment()](#getVerticalAlignment--) | Указывает, как фигура расположена вертикально. |
| [getWidth()](#getWidth--) | Получает ширину содержащего блока фигуры. |
| [getWrapSide()](#getWrapSide--) | Указывает, как текст обтекает фигуру. |
| [getWrapType()](#getWrapType--) | Определяет, является ли фигура встроенной или плавающей. |
| [getZOrder()](#getZOrder--) | Определяет порядок отображения перекрывающихся фигур. |
| [getZOrder_IShape()](#getZOrder-IShape--) |  |
| [hasChildNodes()](#hasChildNodes--) | Возвращает true, если у этого узла есть дочерние узлы. |
| [hashCode()](#hashCode--) |  |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node-) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node-) | Вставляет указанный узел сразу после указанного ссылочного узла. |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node-) | Вставляет указанный узел непосредственно перед указанным ссылочным узлом. |
| [isComposite()](#isComposite--) | Возвращает true, так как этот узел может иметь дочерние узлы. |
| [isDecorative()](#isDecorative--) | Получает флаг, указывающий, является ли фигура декоративной в документе. |
| [isDecorative(boolean value)](#isDecorative-boolean-) | Устанавливает флаг, указывающий, является ли фигура декоративной в документе. |
| [isDeleteRevision()](#isDeleteRevision--) | Возвращает true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений. |
| [isGroup()](#isGroup--) | Возвращает true, если это фигура группы. |
| [isHorizontalRule()](#isHorizontalRule--) | Возвращает true, если эта фигура является горизонтальной линейкой. |
| [isImage()](#isImage--) | Возвращает true, если эта фигура является фигурой изображения. |
| [isInline()](#isInline--) | Быстрый способ определить, расположена ли эта фигура на одной линии с текстом. |
| [isInsertRevision()](#isInsertRevision--) | Возвращает true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений. |
| [isLayoutInCell()](#isLayoutInCell--) | Получает флаг, указывающий, отображается ли фигура внутри таблицы или за ее пределами. |
| [isLayoutInCell(boolean value)](#isLayoutInCell-boolean-) | Устанавливает флаг, указывающий, отображается ли фигура внутри таблицы или за ее пределами. |
| [isMoveFromRevision()](#isMoveFromRevision--) |  Возвращает**true** если этот объект был перемещен (удален) в Microsoft Word при включенном отслеживании изменений. |
| [isMoveToRevision()](#isMoveToRevision--) |  Возвращает**true** если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений. |
| [isSignatureLine()](#isSignatureLine--) | Указывает, что фигура является SignatureLine. |
| [isTopLevel()](#isTopLevel--) | Возвращает true, если эта фигура не является дочерней фигурой группы. |
| [isWordArt()](#isWordArt--) | Возвращает значение true, если эта фигура является объектом WordArt. |
| [iterator()](#iterator--) | Обеспечивает поддержку для каждой итерации стиля над дочерними узлами этого узла. |
| [localToParent(Point2D.Float value)](#localToParent-java.awt.geom.Point2D.Float-) | Преобразует значение из локального координатного пространства в координатное пространство родительской фигуры. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node-) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int-) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [oneColorGradient(int style, int variant, double degree)](#oneColorGradient-int-int-double-) |  |
| [patterned(int patternType)](#patterned-int-) |  |
| [prependChild(Node newChild)](#prependChild-com.aspose.words.Node-) | Добавляет указанный узел в начало списка дочерних узлов для этого узла. |
| [presetTextured(int presetTexture)](#presetTextured-int-) |  |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node-) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [remove()](#remove--) | Удаляет себя из родителя. |
| [removeAllChildren()](#removeAllChildren--) | Удаляет все дочерние узлы текущего узла. |
| [removeChild(Node oldChild)](#removeChild-com.aspose.words.Node-) | Удаляет указанный дочерний узел. |
| [removeMoveRevisions()](#removeMoveRevisions--) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [removeShapeAttr(int key)](#removeShapeAttr-int-) | Зарезервировано для системного использования. |
| [removeSmartTags()](#removeSmartTags--) |  Удаляет все[SmartTag](../../com.aspose.words/smarttag) узлы-потомки текущего узла. |
| [selectNodes(String xpath)](#selectNodes-java.lang.String-) | Выбирает список узлов, соответствующих выражению XPath. |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String-) | Выбирает первый узел, соответствующий выражению XPath. |
| [setAllowOverlap(boolean value)](#setAllowOverlap-boolean-) | Задает значение, указывающее, может ли эта фигура перекрывать другие фигуры. |
| [setAlternativeText(String value)](#setAlternativeText-java.lang.String-) | Определяет альтернативный текст, который будет отображаться вместо графики. |
| [setAnchorLocked(boolean value)](#setAnchorLocked-boolean-) | Указывает, заблокирована ли привязка фигуры. |
| [setAspectRatioLocked(boolean value)](#setAspectRatioLocked-boolean-) | Указывает, заблокировано ли соотношение сторон фигуры. |
| [setBehindText(boolean value)](#setBehindText-boolean-) | Указывает, находится ли фигура ниже или выше текста. |
| [setBounds(Rectangle2D.Float value)](#setBounds-java.awt.geom.Rectangle2D.Float-) | Задает положение и размер содержащего блока фигуры. |
| [setCoordOrigin(Point value)](#setCoordOrigin-java.awt.Point-) | Координаты в верхнем левом углу содержащего блока этой формы. |
| [setCoordSize(Dimension value)](#setCoordSize-java.awt.Dimension-) | Ширина и высота координатного пространства внутри содержащего блока этой формы. |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | Задает идентификатор пользовательского узла. |
| [setDistanceBottom(double value)](#setDistanceBottom-double-) | Задает расстояние (в пунктах) между текстом документа и нижним краем фигуры. |
| [setDistanceLeft(double value)](#setDistanceLeft-double-) | Задает расстояние (в пунктах) между текстом документа и левым краем фигуры. |
| [setDistanceRight(double value)](#setDistanceRight-double-) | Задает расстояние (в пунктах) между текстом документа и правым краем фигуры. |
| [setDistanceTop(double value)](#setDistanceTop-double-) | Задает расстояние (в пунктах) между текстом документа и верхним краем фигуры. |
| [setFillableBackColor(Color value)](#setFillableBackColor-java.awt.Color-) |  |
| [setFillableForeColor(Color value)](#setFillableForeColor-java.awt.Color-) |  |
| [setFillableTransparency(double value)](#setFillableTransparency-double-) |  |
| [setFillableVisible(boolean value)](#setFillableVisible-boolean-) |  |
| [setFilledColor(Color value)](#setFilledColor-java.awt.Color-) |  |
| [setFlipOrientation(int value)](#setFlipOrientation-int-) | Переключает ориентацию фигуры. |
| [setGradientAngle(double value)](#setGradientAngle-double-) |  |
| [setHRef(String value)](#setHRef-java.lang.String-) | Задает полный адрес гиперссылки для фигуры. |
| [setHeight(double value)](#setHeight-double-) | Устанавливает высоту содержащего блока фигуры. |
| [setHorizontalAlignment(int value)](#setHorizontalAlignment-int-) | Указывает, как фигура располагается по горизонтали. |
| [setImage(byte[] imageBytes)](#setImage-byte---) |  |
| [setLeft(double value)](#setLeft-double-) | Устанавливает положение левого края содержащего блока фигуры. |
| [setName(String value)](#setName-java.lang.String-) | Устанавливает необязательное имя формы. |
| [setOn(boolean value)](#setOn-boolean-) |  |
| [setOpacity(double value)](#setOpacity-double-) |  |
| [setRelativeHorizontalPosition(int value)](#setRelativeHorizontalPosition-int-) | Указывает, относительно чего фигура расположена горизонтально. |
| [setRelativeVerticalPosition(int value)](#setRelativeVerticalPosition-int-) | Указывает, относительно чего фигура расположена вертикально. |
| [setRotateWithObject(boolean value)](#setRotateWithObject-boolean-) |  |
| [setRotation(double value)](#setRotation-double-) | Определяет угол (в градусах), на который поворачивается фигура. |
| [setRunAttr(int fontAttr, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [setScreenTip(String value)](#setScreenTip-java.lang.String-) | Определяет текст, отображаемый при наведении указателя мыши на фигуру. |
| [setShapeAttr(int key, Object value)](#setShapeAttr-int-java.lang.Object-) | Зарезервировано для системного использования. |
| [setTarget(String value)](#setTarget-java.lang.String-) | Задает целевой кадр для гиперссылки формы. |
| [setTextureAlignment(int value)](#setTextureAlignment-int-) |  |
| [setTitle(String value)](#setTitle-java.lang.String-) | Задает заголовок (заголовок) текущего объекта формы. |
| [setTop(double value)](#setTop-double-) | Устанавливает положение верхнего края содержащего блока фигуры. |
| [setVerticalAlignment(int value)](#setVerticalAlignment-int-) | Указывает, как фигура расположена вертикально. |
| [setWidth(double value)](#setWidth-double-) | Задает ширину содержащего блока фигуры. |
| [setWrapSide(int value)](#setWrapSide-int-) | Указывает, как текст обтекает фигуру. |
| [setWrapType(int value)](#setWrapType-int-) | Определяет, является ли фигура встроенной или плавающей. |
| [setZOrder(int value)](#setZOrder-int-) | Определяет порядок отображения перекрывающихся фигур. |
| [setZOrder_IShape(int value)](#setZOrder-IShape-int-) |  |
| [solid()](#solid--) |  |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| [toString(int saveFormat)](#toString-int-) |  |
| [twoColorGradient(int style, int variant)](#twoColorGradient-int-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### GroupShape(DocumentBase doc) {#GroupShape-com.aspose.words.DocumentBase-}
```
public GroupShape(DocumentBase doc)
```


Создает новую форму группы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) | Документ владельца.

По умолчанию фигура является плавающей и имеет положение и размер по умолчанию.

 Вы должны указать желаемые свойства формы после того, как вы создали фигуру.|

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
 boolean - Истинно, если были посещены все узлы; false, если DocumentVisitor остановил операцию перед посещением всех узлов. Звонки[DocumentVisitor.visitGroupShapeStart(com.aspose.words.GroupShape)](../../com.aspose.words/documentvisitor\#visitGroupShapeStart-com.aspose.words.GroupShape-) , затем звонит[Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node\#accept-com.aspose.words.DocumentVisitor-) для всех дочерних форм этой групповой формы и вызовов[DocumentVisitor.visitGroupShapeEnd(com.aspose.words.GroupShape)](../../com.aspose.words/documentvisitor\#visitGroupShapeEnd-com.aspose.words.GroupShape-) в конце.
### adjustWithEffects(Rectangle2D.Float source) {#adjustWithEffects-java.awt.geom.Rectangle2D.Float-}
```
public Rectangle2D.Float adjustWithEffects(Rectangle2D.Float source)
```


Добавляет к исходному прямоугольнику значения экстента эффекта и возвращает окончательный прямоугольник.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| source | java.awt.geom.Rectangle2D.Float |  |

**Возвращает:**
java.awt.geom.Rectangle2D.Float
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
### canHaveImage() {#canHaveImage--}
```
public boolean canHaveImage()
```


Возвращает true, если тип фигуры позволяет фигуре иметь изображение.

Хотя Microsoft Word имеет специальный тип фигуры для изображений, похоже, что в документах Microsoft Word любая фигура, кроме групповой, может иметь изображение, поэтому это свойство возвращает значение true для всех фигур, кроме[GroupShape](../../com.aspose.words/groupshape).

**Возвращает:**
boolean — True, если тип фигуры позволяет фигуре иметь изображение.
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
### fetchInheritedShapeAttr(int key) {#fetchInheritedShapeAttr-int-}
```
public Object fetchInheritedShapeAttr(int key)
```


Зарезервировано для системного использования. IShapeAttrSource.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### fetchShapeAttr(int key) {#fetchShapeAttr-int-}
```
public Object fetchShapeAttr(int key)
```


Зарезервировано для системного использования. IShapeAttrSource.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### getAllowOverlap() {#getAllowOverlap--}
```
public boolean getAllowOverlap()
```


Получает значение, указывающее, может ли эта фигура перекрывать другие фигуры.

Это свойство влияет на поведение фигуры в Microsoft Word. Aspose.Words игнорирует значение этого свойства.

Это свойство применимо только к фигурам верхнего уровня.

 Значение по умолчанию**true**.

**Возвращает:**
boolean — значение, указывающее, может ли эта фигура перекрывать другие фигуры.
### getAlternativeText() {#getAlternativeText--}
```
public String getAlternativeText()
```


Определяет альтернативный текст, который будет отображаться вместо графики.

Значение по умолчанию — пустая строка.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
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
### getAnchorLocked() {#getAnchorLocked--}
```
public boolean getAnchorLocked()
```


Указывает, заблокирована ли привязка фигуры.

 Значение по умолчанию**false**.

Имеет эффект только для фигур верхнего уровня.

Это свойство влияет на поведение привязки фигуры в Microsoft Word. Если привязка не заблокирована, перемещение фигуры в Microsoft Word также может привести к перемещению привязки фигуры.

**Возвращает:**
boolean - соответствующее логическое значение.
### getAspectRatioLocked() {#getAspectRatioLocked--}
```
public boolean getAspectRatioLocked()
```


Указывает, заблокировано ли соотношение сторон фигуры.

 Значение по умолчанию зависит от[getShapeType()](../../com.aspose.words/shapebase\#getShapeType--) , для ShapeType.Image это**true** но для других типов формы это**false**.

Действует только для фигур верхнего уровня.

**Возвращает:**
boolean - соответствующее логическое значение.
### getBehindText() {#getBehindText--}
```
public boolean getBehindText()
```


Указывает, находится ли фигура ниже или выше текста.

Имеет эффект только для фигур верхнего уровня.

 Значение по умолчанию**false**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getBottom() {#getBottom--}
```
public double getBottom()
```


Получает положение нижнего края содержащего блока фигуры.

Для формы верхнего уровня значение указывается в пунктах и относительно привязки формы.

Для фигур в группе значение находится в пространстве координат и единицах родительской группы.

**Возвращает:**
double — положение нижнего края содержащего блока фигуры.
### getBounds() {#getBounds--}
```
public Rectangle2D.Float getBounds()
```


Получает расположение и размер содержащего блока фигуры. Игнорирует блокировку соотношения сторон при настройке.

Для формы верхнего уровня значение указывается в пунктах и относительно привязки формы.

Для фигур в группе значение находится в пространстве координат и единицах родительской группы.

**Возвращает:**
java.awt.geom.Rectangle2D.Float — расположение и размер содержащего блока фигуры.
### getBoundsInPoints() {#getBoundsInPoints--}
```
public Rectangle2D.Float getBoundsInPoints()
```


Получает расположение и размер содержащего блока фигуры в пунктах относительно привязки самой верхней фигуры.

**Возвращает:**
java.awt.geom.Rectangle2D.Float — расположение и размер содержащего блока фигуры в пунктах относительно привязки самой верхней фигуры.
### getBoundsWithEffects() {#getBoundsWithEffects--}
```
public Rectangle2D.Float getBoundsWithEffects()
```


Получает окончательную степень, которую имеет этот объект формы после применения эффектов рисования. Стоимость измеряется в баллах.

**Возвращает:**
java.awt.geom.Rectangle2D.Float — окончательная степень, которую имеет этот объект формы после применения эффектов рисования.
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
### getCoordOrigin() {#getCoordOrigin--}
```
public Point getCoordOrigin()
```


Координаты в верхнем левом углу содержащего блока этой формы.

Значение по умолчанию: (0,0).

**Возвращает:**
java.awt.Point — соответствующее значение java.awt.Point.
### getCoordSize() {#getCoordSize--}
```
public Dimension getCoordSize()
```


Ширина и высота координатного пространства внутри содержащего блока этой формы.

Значение по умолчанию: (1000, 1000).

**Возвращает:**
java.awt.Dimension — соответствующее значение java.awt.Dimension.
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
### getDirectShapeAttr(int key) {#getDirectShapeAttr-int-}
```
public Object getDirectShapeAttr(int key)
```


Зарезервировано для системного использования. IShapeAttrSource.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### getDistanceBottom() {#getDistanceBottom--}
```
public double getDistanceBottom()
```


Получает расстояние (в пунктах) между текстом документа и нижним краем фигуры.

Значение по умолчанию — 0.

Имеет эффект только для фигур верхнего уровня.

**Возвращает:**
double — расстояние (в пунктах) между текстом документа и нижним краем фигуры.
### getDistanceLeft() {#getDistanceLeft--}
```
public double getDistanceLeft()
```


Получает расстояние (в пунктах) между текстом документа и левым краем фигуры.

Значение по умолчанию — 1/8 дюйма.

Имеет эффект только для фигур верхнего уровня.

**Возвращает:**
double — расстояние (в пунктах) между текстом документа и левым краем фигуры.
### getDistanceRight() {#getDistanceRight--}
```
public double getDistanceRight()
```


Получает расстояние (в пунктах) между текстом документа и правым краем фигуры.

Значение по умолчанию — 1/8 дюйма.

Имеет эффект только для фигур верхнего уровня.

**Возвращает:**
double — расстояние (в пунктах) между текстом документа и правым краем фигуры.
### getDistanceTop() {#getDistanceTop--}
```
public double getDistanceTop()
```


Получает расстояние (в пунктах) между текстом документа и верхним краем фигуры.

Значение по умолчанию — 0.

Имеет эффект только для фигур верхнего уровня.

**Возвращает:**
double — расстояние (в пунктах) между текстом документа и верхним краем фигуры.
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
### getFill() {#getFill--}
```
public Fill getFill()
```


Получает форматирование заливки для фигуры.

**Возвращает:**
[Fill](../../com.aspose.words/fill) - Заполнить форматирование формы.
### getFillType() {#getFillType--}
```
public int getFillType()
```




**Возвращает:**
инт
### getFillableBackColor() {#getFillableBackColor--}
```
public Color getFillableBackColor()
```




**Возвращает:**
java.awt.Color
### getFillableForeColor() {#getFillableForeColor--}
```
public Color getFillableForeColor()
```




**Возвращает:**
java.awt.Color
### getFillableImageBytes() {#getFillableImageBytes--}
```
public byte[] getFillableImageBytes()
```




**Возвращает:**
байт[]
### getFillableTransparency() {#getFillableTransparency--}
```
public double getFillableTransparency()
```




**Возвращает:**
двойной
### getFillableVisible() {#getFillableVisible--}
```
public boolean getFillableVisible()
```




**Возвращает:**
логический
### getFilledColor() {#getFilledColor--}
```
public Color getFilledColor()
```




**Возвращает:**
java.awt.Color
### getFirstChild() {#getFirstChild--}
```
public Node getFirstChild()
```


Получает первый дочерний элемент узла. Если нет первого дочернего узла, возвращается нуль.

**Возвращает:**
[Node](../../com.aspose.words/node) - Первый дочерний узел.
### getFlipOrientation() {#getFlipOrientation--}
```
public int getFlipOrientation()
```


Переключает ориентацию фигуры.

 Значение по умолчанию[FlipOrientation.NONE](../../com.aspose.words/fliporientation\#NONE).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение представляет собой побитовую комбинацию[FlipOrientation](../../com.aspose.words/fliporientation) константы.
### getFont() {#getFont--}
```
public Font getFont()
```


Предоставляет доступ к форматированию шрифта этого объекта.

**Возвращает:**
[Font](../../com.aspose.words/font) - соответствующий[Font](../../com.aspose.words/font) ценность.
### getGradientAngle() {#getGradientAngle--}
```
public double getGradientAngle()
```




**Возвращает:**
двойной
### getGradientStops() {#getGradientStops--}
```
public GradientStopCollection getGradientStops()
```




**Возвращает:**
[GradientStopCollection](../../com.aspose.words/gradientstopcollection)
### getGradientStyle() {#getGradientStyle--}
```
public int getGradientStyle()
```




**Возвращает:**
инт
### getGradientVariant() {#getGradientVariant--}
```
public int getGradientVariant()
```




**Возвращает:**
инт
### getHRef() {#getHRef--}
```
public String getHRef()
```


Получает полный адрес гиперссылки для фигуры.

Значение по умолчанию — пустая строка.

Ниже приведены примеры допустимых значений этого свойства:

Полный URI: https://www.aspose.com/.

Полное имя файла: C:\\\\Мои документы\\\\Отчет о продажах.doc .

Относительный URI: ../../../resource.txt 

Относительное имя файла: ..\\\\Мои документы\\\\Отчет о продажах.doc .

Закладка в другом документе: https://www.aspose.com/Products/Default.aspx\#люксы 

 Закладка в этом документе:\#НазваниеЗакладки .

**Возвращает:**
java.lang.String — полный адрес гиперссылки для фигуры.
### getHeight() {#getHeight--}
```
public double getHeight()
```


Получает высоту содержащего блока фигуры.

Для формы верхнего уровня значение указывается в пунктах.

Для фигур в группе значение находится в пространстве координат и единицах родительской группы.

Значение по умолчанию — 0.

**Возвращает:**
double - высота содержащего блока формы.
### getHorizontalAlignment() {#getHorizontalAlignment--}
```
public int getHorizontalAlignment()
```


Указывает, как фигура располагается по горизонтали.

 Значение по умолчанию[HorizontalAlignment.NONE](../../com.aspose.words/horizontalalignment\#NONE).

Имеет эффект только для плавающих фигур верхнего уровня.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[HorizontalAlignment](../../com.aspose.words/horizontalalignment) константы.
### getLastChild() {#getLastChild--}
```
public Node getLastChild()
```


Получает последний дочерний элемент узла. Если последнего дочернего узла нет, возвращается нуль.

**Возвращает:**
[Node](../../com.aspose.words/node) - Последний дочерний узел.
### getLeft() {#getLeft--}
```
public double getLeft()
```


Получает положение левого края содержащего блока фигуры.

Для формы верхнего уровня значение указывается в пунктах и относительно привязки формы.

Для фигур в группе значение находится в пространстве координат и единицах родительской группы.

Значение по умолчанию — 0.

Имеет эффект только для плавающих фигур.

**Возвращает:**
double - Положение левого края содержащего блока формы.
### getMarkupLanguage() {#getMarkupLanguage--}
```
public byte getMarkupLanguage()
```


Получает язык разметки, используемый для этого графического объекта.

**Возвращает:**
 byte - язык разметки, используемый для этого графического объекта. Возвращаемое значение является одним из[ShapeMarkupLanguage](../../com.aspose.words/shapemarkuplanguage) константы.
### getName() {#getName--}
```
public String getName()
```


Получает необязательное имя формы.

По умолчанию пустая строка.

Не может быть нулевым, но может быть пустой строкой.

**Возвращает:**
java.lang.String — необязательное имя формы.
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


 Возвращает[NodeType.GROUP\_SHAPE](../../com.aspose.words/nodetype\#GROUP-SHAPE).

**Возвращает:**
 инт -\{[NodeType.GROUP\_SHAPE](../../com.aspose.words/nodetype\#GROUP-SHAPE) . Возвращаемое значение является одним из[NodeType](../../com.aspose.words/nodetype) константы.
### getOn() {#getOn--}
```
public boolean getOn()
```




**Возвращает:**
логический
### getOpacity() {#getOpacity--}
```
public double getOpacity()
```




**Возвращает:**
двойной
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


Возвращает ближайший родительский абзац. Для дочерних фигур групповой фигуры и дочерних фигур объекта Office Math всегда возвращается значение null.

**Возвращает:**
[Paragraph](../../com.aspose.words/paragraph) - Непосредственный родительский абзац.
### getParentParagraph_IInline() {#getParentParagraph-IInline--}
```
public Paragraph getParentParagraph_IInline()
```




**Возвращает:**
[Paragraph](../../com.aspose.words/paragraph)
### getPatternType() {#getPatternType--}
```
public int getPatternType()
```




**Возвращает:**
инт
### getPresetTexture() {#getPresetTexture--}
```
public int getPresetTexture()
```




**Возвращает:**
инт
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
### getRelativeHorizontalPosition() {#getRelativeHorizontalPosition--}
```
public int getRelativeHorizontalPosition()
```


Указывает, относительно чего фигура расположена горизонтально.

 Значение по умолчанию[RelativeHorizontalPosition.COLUMN](../../com.aspose.words/relativehorizontalposition\#COLUMN).

Имеет эффект только для плавающих фигур верхнего уровня.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[RelativeHorizontalPosition](../../com.aspose.words/relativehorizontalposition) константы.
### getRelativeVerticalPosition() {#getRelativeVerticalPosition--}
```
public int getRelativeVerticalPosition()
```


Указывает, относительно чего фигура расположена вертикально.

 Значение по умолчанию[RelativeVerticalPosition.PARAGRAPH](../../com.aspose.words/relativeverticalposition\#PARAGRAPH).

Имеет эффект только для плавающих фигур верхнего уровня.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[RelativeVerticalPosition](../../com.aspose.words/relativeverticalposition) константы.
### getRight() {#getRight--}
```
public double getRight()
```


Получает положение правого края содержащего блока фигуры.

Для формы верхнего уровня значение указывается в пунктах и относительно привязки формы.

Для фигур в группе значение находится в пространстве координат и единицах родительской группы.

**Возвращает:**
double - Положение правого края содержащего блока формы.
### getRotateWithObject() {#getRotateWithObject--}
```
public boolean getRotateWithObject()
```




**Возвращает:**
логический
### getRotation() {#getRotation--}
```
public double getRotation()
```


Определяет угол (в градусах), на который поворачивается фигура. Положительное значение соответствует углу поворота по часовой стрелке.

Значение по умолчанию — 0.

**Возвращает:**
double - соответствующее двойное значение.
### getScreenTip() {#getScreenTip--}
```
public String getScreenTip()
```


Определяет текст, отображаемый при наведении указателя мыши на фигуру.

Значение по умолчанию — пустая строка.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getShadowFormat() {#getShadowFormat--}
```
public ShadowFormat getShadowFormat()
```


Получает теневое форматирование для фигуры.

**Возвращает:**
[ShadowFormat](../../com.aspose.words/shadowformat) - Теневое форматирование формы.
### getShapeRenderer() {#getShapeRenderer--}
```
public ShapeRenderer getShapeRenderer()
```


Создает и возвращает объект, который можно использовать для преобразования этой формы в изображение.

 Этот метод просто вызывает[ShapeRenderer](../../com.aspose.words/shaperenderer)конструктор и передает этот объект в качестве параметра.

**Возвращает:**
[ShapeRenderer](../../com.aspose.words/shaperenderer) - Объект рендеринга для этой формы.
### getShapeType() {#getShapeType--}
```
public int getShapeType()
```


Получает тип фигуры.

**Возвращает:**
 int - Тип фигуры. Возвращаемое значение является одним из[ShapeType](../../com.aspose.words/shapetype) константы.
### getSizeInPoints() {#getSizeInPoints--}
```
public Point2D.Float getSizeInPoints()
```


Получает размер фигуры в точках. Получает размер фигуры в точках.

 Point2D.Float используется как тип возвращаемого значения, потому что здесь нам нужны значения измерения с плавающей запятой. Следует предположить, что Point2D*x == width* а также*y == height*.

**Возвращает:**
java.awt.geom.Point2D.Float — размер фигуры в пунктах.
### getTarget() {#getTarget--}
```
public String getTarget()
```


Получает целевой кадр для гиперссылки формы.

Значение по умолчанию — пустая строка.

**Возвращает:**
java.lang.String — целевой фрейм для гиперссылки формы.
### getText() {#getText--}
```
public String getText()
```


Получает текст этого узла и всех его дочерних элементов.

 Возвращаемая строка включает все управляющие и специальные символы, как описано в[ControlChar](../../com.aspose.words/controlchar).

**Возвращает:**
java.lang.String
### getTextureAlignment() {#getTextureAlignment--}
```
public int getTextureAlignment()
```




**Возвращает:**
инт
### getTitle() {#getTitle--}
```
public String getTitle()
```


Получает заголовок (заголовок) текущего объекта формы.

По умолчанию пустая строка.

Не может быть нулевым, но может быть пустой строкой.

**Возвращает:**
java.lang.String — заголовок (заголовок) текущего объекта формы.
### getTop() {#getTop--}
```
public double getTop()
```


Получает положение верхнего края содержащего блока фигуры.

Для формы верхнего уровня значение указывается в пунктах и относительно привязки формы.

Для фигур в группе значение находится в пространстве координат и единицах родительской группы.

Значение по умолчанию — 0.

Имеет эффект только для плавающих фигур.

**Возвращает:**
double — положение верхнего края содержащего блока формы.
### getVerticalAlignment() {#getVerticalAlignment--}
```
public int getVerticalAlignment()
```


Указывает, как фигура расположена вертикально.

 Значение по умолчанию[VerticalAlignment.NONE](../../com.aspose.words/verticalalignment\#NONE).

Имеет эффект только для плавающих фигур верхнего уровня.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[VerticalAlignment](../../com.aspose.words/verticalalignment) константы.
### getWidth() {#getWidth--}
```
public double getWidth()
```


Получает ширину содержащего блока фигуры.

Для формы верхнего уровня значение указывается в пунктах.

Для фигур в группе значение находится в пространстве координат и единицах родительской группы.

Значение по умолчанию — 0.

**Возвращает:**
double - Ширина содержащего блока формы.
### getWrapSide() {#getWrapSide--}
```
public int getWrapSide()
```


Указывает, как текст обтекает фигуру.

 Значение по умолчанию[WrapSide.BOTH](../../com.aspose.words/wrapside\#BOTH).

Имеет эффект только для фигур верхнего уровня.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[WrapSide](../../com.aspose.words/wrapside) константы.
### getWrapType() {#getWrapType--}
```
public int getWrapType()
```


Определяет, является ли фигура встроенной или плавающей. Для плавающих фигур определяет режим обтекания текста вокруг фигуры.

 Значение по умолчанию[WrapType.NONE](../../com.aspose.words/wraptype\#NONE).

Имеет эффект только для фигур верхнего уровня.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[WrapType](../../com.aspose.words/wraptype) константы.
### getZOrder() {#getZOrder--}
```
public int getZOrder()
```


Определяет порядок отображения перекрывающихся фигур.

Имеет эффект только для фигур верхнего уровня.

Значение по умолчанию — 0.

Число представляет приоритет стека. Фигура с более высоким номером будет отображаться так, как если бы она перекрывала (перед) фигуру с меньшим номером.

Порядок перекрывающихся фигур независим для фигур в заголовке и в основном тексте документа.

Порядок отображения дочерних фигур в фигуре группы определяется их порядком внутри фигуры группы.

**Возвращает:**
int - соответствующее значение int.
### getZOrder_IShape() {#getZOrder-IShape--}
```
public int getZOrder_IShape()
```




**Возвращает:**
инт
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
### isDecorative() {#isDecorative--}
```
public boolean isDecorative()
```


 Получает флаг, указывающий, является ли фигура декоративной в документе. Обратите внимание, что форма не пуста[getAlternativeText()](../../com.aspose.words/shapebase\#getAlternativeText--) / [setAlternativeText(java.lang.String)](../../com.aspose.words/shapebase\#setAlternativeText-java.lang.String-) не может быть декоративным.

**Возвращает:**
boolean — Флаг, указывающий, является ли фигура декоративной в документе.
### isDecorative(boolean value) {#isDecorative-boolean-}
```
public void isDecorative(boolean value)
```


 Устанавливает флаг, указывающий, является ли фигура декоративной в документе. Обратите внимание, что форма не пуста[getAlternativeText()](../../com.aspose.words/shapebase\#getAlternativeText--) / [setAlternativeText(java.lang.String)](../../com.aspose.words/shapebase\#setAlternativeText-java.lang.String-) не может быть декоративным.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Флаг, указывающий, является ли фигура декоративной в документе. |

### isDeleteRevision() {#isDeleteRevision--}
```
public boolean isDeleteRevision()
```


Возвращает true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений.

**Возвращает:**
boolean — Истинно, если этот объект был удален в Microsoft Word при включенном отслеживании изменений.
### isGroup() {#isGroup--}
```
public boolean isGroup()
```


Возвращает true, если это фигура группы.

**Возвращает:**
boolean — True, если это фигура группы.
### isHorizontalRule() {#isHorizontalRule--}
```
public boolean isHorizontalRule()
```


Возвращает true, если эта фигура является горизонтальной линейкой.

**Возвращает:**
boolean - True, если эта фигура является горизонтальной линейкой.
### isImage() {#isImage--}
```
public boolean isImage()
```


Возвращает true, если эта фигура является фигурой изображения.

**Возвращает:**
boolean — Истинно, если эта фигура является фигурой изображения.
### isInline() {#isInline--}
```
public boolean isInline()
```


Быстрый способ определить, расположена ли эта фигура на одной линии с текстом.

Имеет эффект только для фигур верхнего уровня.

**Возвращает:**
boolean - соответствующее логическое значение.
### isInsertRevision() {#isInsertRevision--}
```
public boolean isInsertRevision()
```


Возвращает true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений.

**Возвращает:**
boolean — True, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений.
### isLayoutInCell() {#isLayoutInCell--}
```
public boolean isLayoutInCell()
```


Получает флаг, указывающий, отображается ли фигура внутри таблицы или за ее пределами.

 Значение по умолчанию**true**.

Действует только для фигур верхнего уровня, свойство[getWrapType()](../../com.aspose.words/shapebase\#getWrapType--) / [setWrapType(int)](../../com.aspose.words/shapebase\#setWrapType-int-) из которых установлено значение, отличное от[Inline](../../com.aspose.words/inline).

**Возвращает:**
boolean — Флаг, указывающий, отображается ли фигура внутри таблицы или за ее пределами.
### isLayoutInCell(boolean value) {#isLayoutInCell-boolean-}
```
public void isLayoutInCell(boolean value)
```


Устанавливает флаг, указывающий, отображается ли фигура внутри таблицы или за ее пределами.

 Значение по умолчанию**true**.

Действует только для фигур верхнего уровня, свойство[getWrapType()](../../com.aspose.words/shapebase\#getWrapType--) / [setWrapType(int)](../../com.aspose.words/shapebase\#setWrapType-int-) из которых установлено значение, отличное от[Inline](../../com.aspose.words/inline).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Флаг, указывающий, отображается ли фигура внутри таблицы или за ее пределами. |

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
### isSignatureLine() {#isSignatureLine--}
```
public boolean isSignatureLine()
```


Указывает, что фигура является SignatureLine.

**Возвращает:**
boolean - соответствующее логическое значение.
### isTopLevel() {#isTopLevel--}
```
public boolean isTopLevel()
```


Возвращает true, если эта фигура не является дочерней фигурой группы.

**Возвращает:**
boolean — True, если эта фигура не является дочерней фигурой группы.
### isWordArt() {#isWordArt--}
```
public boolean isWordArt()
```


Возвращает значение true, если эта фигура является объектом WordArt. Работает до 2007 режима совместимости. В режиме совместимости 2010 и более поздних версий WordArt представляет собой просто текстовое поле с причудливыми шрифтами.

**Возвращает:**
boolean — True, если эта фигура является объектом WordArt.
### iterator() {#iterator--}
```
public Iterator iterator()
```


Обеспечивает поддержку для каждой итерации стиля над дочерними узлами этого узла.

**Возвращает:**
java.util.Iterator
### localToParent(Point2D.Float value) {#localToParent-java.awt.geom.Point2D.Float-}
```
public Point2D.Float localToParent(Point2D.Float value)
```


Преобразует значение из локального координатного пространства в координатное пространство родительской фигуры.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.geom.Point2D.Float |  |

**Возвращает:**
java.awt.geom.Point2D.Float
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




### oneColorGradient(int style, int variant, double degree) {#oneColorGradient-int-int-double-}
```
public void oneColorGradient(int style, int variant, double degree)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| style | int |  |
| variant | int |  |
| degree | double |  |

### patterned(int patternType) {#patterned-int-}
```
public void patterned(int patternType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| patternType | int |  |

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
### presetTextured(int presetTexture) {#presetTextured-int-}
```
public void presetTextured(int presetTexture)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| presetTexture | int |  |

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

### removeShapeAttr(int key) {#removeShapeAttr-int-}
```
public void removeShapeAttr(int key)
```


Зарезервировано для системного использования. IShapeAttrSource.

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
### setAllowOverlap(boolean value) {#setAllowOverlap-boolean-}
```
public void setAllowOverlap(boolean value)
```


Задает значение, указывающее, может ли эта фигура перекрывать другие фигуры.

Это свойство влияет на поведение фигуры в Microsoft Word. Aspose.Words игнорирует значение этого свойства.

Это свойство применимо только к фигурам верхнего уровня.

 Значение по умолчанию**true**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, указывающее, может ли эта фигура перекрывать другие фигуры. |

### setAlternativeText(String value) {#setAlternativeText-java.lang.String-}
```
public void setAlternativeText(String value)
```


Определяет альтернативный текст, который будет отображаться вместо графики.

Значение по умолчанию — пустая строка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setAnchorLocked(boolean value) {#setAnchorLocked-boolean-}
```
public void setAnchorLocked(boolean value)
```


Указывает, заблокирована ли привязка фигуры.

 Значение по умолчанию**false**.

Имеет эффект только для фигур верхнего уровня.

Это свойство влияет на поведение привязки фигуры в Microsoft Word. Если привязка не заблокирована, перемещение фигуры в Microsoft Word также может привести к перемещению привязки фигуры.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setAspectRatioLocked(boolean value) {#setAspectRatioLocked-boolean-}
```
public void setAspectRatioLocked(boolean value)
```


Указывает, заблокировано ли соотношение сторон фигуры.

 Значение по умолчанию зависит от[getShapeType()](../../com.aspose.words/shapebase\#getShapeType--) , для ShapeType.Image это**true** но для других типов формы это**false**.

Действует только для фигур верхнего уровня.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setBehindText(boolean value) {#setBehindText-boolean-}
```
public void setBehindText(boolean value)
```


Указывает, находится ли фигура ниже или выше текста.

Имеет эффект только для фигур верхнего уровня.

 Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setBounds(Rectangle2D.Float value) {#setBounds-java.awt.geom.Rectangle2D.Float-}
```
public void setBounds(Rectangle2D.Float value)
```


Задает положение и размер содержащего блока фигуры. Игнорирует блокировку соотношения сторон при настройке.

Для формы верхнего уровня значение указывается в пунктах и относительно привязки формы.

Для фигур в группе значение находится в пространстве координат и единицах родительской группы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.geom.Rectangle2D.Float | Расположение и размер содержащего блока фигуры. |

### setCoordOrigin(Point value) {#setCoordOrigin-java.awt.Point-}
```
public void setCoordOrigin(Point value)
```


Координаты в верхнем левом углу содержащего блока этой формы.

Значение по умолчанию: (0,0).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.Point | Соответствующее значение java.awt.Point. |

### setCoordSize(Dimension value) {#setCoordSize-java.awt.Dimension-}
```
public void setCoordSize(Dimension value)
```


Ширина и высота координатного пространства внутри содержащего блока этой формы.

Значение по умолчанию: (1000, 1000).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.Dimension | Соответствующее значение java.awt.Dimension. |

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

### setDistanceBottom(double value) {#setDistanceBottom-double-}
```
public void setDistanceBottom(double value)
```


Задает расстояние (в пунктах) между текстом документа и нижним краем фигуры.

Значение по умолчанию — 0.

Имеет эффект только для фигур верхнего уровня.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Расстояние (в пунктах) между текстом документа и нижним краем фигуры. |

### setDistanceLeft(double value) {#setDistanceLeft-double-}
```
public void setDistanceLeft(double value)
```


Задает расстояние (в пунктах) между текстом документа и левым краем фигуры.

Значение по умолчанию — 1/8 дюйма.

Имеет эффект только для фигур верхнего уровня.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Расстояние (в пунктах) между текстом документа и левым краем фигуры. |

### setDistanceRight(double value) {#setDistanceRight-double-}
```
public void setDistanceRight(double value)
```


Задает расстояние (в пунктах) между текстом документа и правым краем фигуры.

Значение по умолчанию — 1/8 дюйма.

Имеет эффект только для фигур верхнего уровня.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Расстояние (в пунктах) между текстом документа и правым краем фигуры. |

### setDistanceTop(double value) {#setDistanceTop-double-}
```
public void setDistanceTop(double value)
```


Задает расстояние (в пунктах) между текстом документа и верхним краем фигуры.

Значение по умолчанию — 0.

Имеет эффект только для фигур верхнего уровня.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Расстояние (в пунктах) между текстом документа и верхним краем фигуры. |

### setFillableBackColor(Color value) {#setFillableBackColor-java.awt.Color-}
```
public void setFillableBackColor(Color value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.Color |  |

### setFillableForeColor(Color value) {#setFillableForeColor-java.awt.Color-}
```
public void setFillableForeColor(Color value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.Color |  |

### setFillableTransparency(double value) {#setFillableTransparency-double-}
```
public void setFillableTransparency(double value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double |  |

### setFillableVisible(boolean value) {#setFillableVisible-boolean-}
```
public void setFillableVisible(boolean value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  |

### setFilledColor(Color value) {#setFilledColor-java.awt.Color-}
```
public void setFilledColor(Color value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.Color |  |

### setFlipOrientation(int value) {#setFlipOrientation-int-}
```
public void setFlipOrientation(int value)
```


Переключает ориентацию фигуры.

 Значение по умолчанию[FlipOrientation.NONE](../../com.aspose.words/fliporientation\#NONE).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть побитовой комбинацией[FlipOrientation](../../com.aspose.words/fliporientation) константы. |

### setGradientAngle(double value) {#setGradientAngle-double-}
```
public void setGradientAngle(double value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double |  |

### setHRef(String value) {#setHRef-java.lang.String-}
```
public void setHRef(String value)
```


Задает полный адрес гиперссылки для фигуры.

Значение по умолчанию — пустая строка.

Ниже приведены примеры допустимых значений этого свойства:

Полный URI: https://www.aspose.com/.

Полное имя файла: C:\\\\Мои документы\\\\Отчет о продажах.doc .

Относительный URI: ../../../resource.txt 

Относительное имя файла: ..\\\\Мои документы\\\\Отчет о продажах.doc .

Закладка в другом документе: https://www.aspose.com/Products/Default.aspx\#люксы 

 Закладка в этом документе:\#НазваниеЗакладки .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Полный адрес гиперссылки для формы. |

### setHeight(double value) {#setHeight-double-}
```
public void setHeight(double value)
```


Устанавливает высоту содержащего блока фигуры.

Для формы верхнего уровня значение указывается в пунктах.

Для фигур в группе значение находится в пространстве координат и единицах родительской группы.

Значение по умолчанию — 0.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Высота содержащего блока фигуры. |

### setHorizontalAlignment(int value) {#setHorizontalAlignment-int-}
```
public void setHorizontalAlignment(int value)
```


Указывает, как фигура располагается по горизонтали.

 Значение по умолчанию[HorizontalAlignment.NONE](../../com.aspose.words/horizontalalignment\#NONE).

Имеет эффект только для плавающих фигур верхнего уровня.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[HorizontalAlignment](../../com.aspose.words/horizontalalignment) константы. |

### setImage(byte[] imageBytes) {#setImage-byte---}
```
public void setImage(byte[] imageBytes)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| imageBytes | byte[] |  |

### setLeft(double value) {#setLeft-double-}
```
public void setLeft(double value)
```


Устанавливает положение левого края содержащего блока фигуры.

Для формы верхнего уровня значение указывается в пунктах и относительно привязки формы.

Для фигур в группе значение находится в пространстве координат и единицах родительской группы.

Значение по умолчанию — 0.

Имеет эффект только для плавающих фигур.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Положение левого края содержащего блока фигуры. |

### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


Устанавливает необязательное имя формы.

По умолчанию пустая строка.

Не может быть нулевым, но может быть пустой строкой.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Необязательное имя формы. |

### setOn(boolean value) {#setOn-boolean-}
```
public void setOn(boolean value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  |

### setOpacity(double value) {#setOpacity-double-}
```
public void setOpacity(double value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double |  |

### setRelativeHorizontalPosition(int value) {#setRelativeHorizontalPosition-int-}
```
public void setRelativeHorizontalPosition(int value)
```


Указывает, относительно чего фигура расположена горизонтально.

 Значение по умолчанию[RelativeHorizontalPosition.COLUMN](../../com.aspose.words/relativehorizontalposition\#COLUMN).

Имеет эффект только для плавающих фигур верхнего уровня.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[RelativeHorizontalPosition](../../com.aspose.words/relativehorizontalposition) константы. |

### setRelativeVerticalPosition(int value) {#setRelativeVerticalPosition-int-}
```
public void setRelativeVerticalPosition(int value)
```


Указывает, относительно чего фигура расположена вертикально.

 Значение по умолчанию[RelativeVerticalPosition.PARAGRAPH](../../com.aspose.words/relativeverticalposition\#PARAGRAPH).

Имеет эффект только для плавающих фигур верхнего уровня.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[RelativeVerticalPosition](../../com.aspose.words/relativeverticalposition) константы. |

### setRotateWithObject(boolean value) {#setRotateWithObject-boolean-}
```
public void setRotateWithObject(boolean value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  |

### setRotation(double value) {#setRotation-double-}
```
public void setRotation(double value)
```


Определяет угол (в градусах), на который поворачивается фигура. Положительное значение соответствует углу поворота по часовой стрелке.

Значение по умолчанию — 0.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Соответствующее двойное значение. |

### setRunAttr(int fontAttr, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int fontAttr, Object value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fontAttr | int |  |
| value | java.lang.Object |  |

### setScreenTip(String value) {#setScreenTip-java.lang.String-}
```
public void setScreenTip(String value)
```


Определяет текст, отображаемый при наведении указателя мыши на фигуру.

Значение по умолчанию — пустая строка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setShapeAttr(int key, Object value) {#setShapeAttr-int-java.lang.Object-}
```
public void setShapeAttr(int key, Object value)
```


Зарезервировано для системного использования. IShapeAttrSource.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setTarget(String value) {#setTarget-java.lang.String-}
```
public void setTarget(String value)
```


Задает целевой кадр для гиперссылки формы.

Значение по умолчанию — пустая строка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Целевой кадр для гиперссылки формы. |

### setTextureAlignment(int value) {#setTextureAlignment-int-}
```
public void setTextureAlignment(int value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  |

### setTitle(String value) {#setTitle-java.lang.String-}
```
public void setTitle(String value)
```


Задает заголовок (заголовок) текущего объекта формы.

По умолчанию пустая строка.

Не может быть нулевым, но может быть пустой строкой.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Заголовок (заголовок) текущего объекта формы. |

### setTop(double value) {#setTop-double-}
```
public void setTop(double value)
```


Устанавливает положение верхнего края содержащего блока фигуры.

Для формы верхнего уровня значение указывается в пунктах и относительно привязки формы.

Для фигур в группе значение находится в пространстве координат и единицах родительской группы.

Значение по умолчанию — 0.

Имеет эффект только для плавающих фигур.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Положение верхнего края содержащего блока фигуры. |

### setVerticalAlignment(int value) {#setVerticalAlignment-int-}
```
public void setVerticalAlignment(int value)
```


Указывает, как фигура расположена вертикально.

 Значение по умолчанию[VerticalAlignment.NONE](../../com.aspose.words/verticalalignment\#NONE).

Имеет эффект только для плавающих фигур верхнего уровня.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[VerticalAlignment](../../com.aspose.words/verticalalignment) константы. |

### setWidth(double value) {#setWidth-double-}
```
public void setWidth(double value)
```


Задает ширину содержащего блока фигуры.

Для формы верхнего уровня значение указывается в пунктах.

Для фигур в группе значение находится в пространстве координат и единицах родительской группы.

Значение по умолчанию — 0.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Ширина содержащего блока фигуры. |

### setWrapSide(int value) {#setWrapSide-int-}
```
public void setWrapSide(int value)
```


Указывает, как текст обтекает фигуру.

 Значение по умолчанию[WrapSide.BOTH](../../com.aspose.words/wrapside\#BOTH).

Имеет эффект только для фигур верхнего уровня.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[WrapSide](../../com.aspose.words/wrapside) константы. |

### setWrapType(int value) {#setWrapType-int-}
```
public void setWrapType(int value)
```


Определяет, является ли фигура встроенной или плавающей. Для плавающих фигур определяет режим обтекания текста вокруг фигуры.

 Значение по умолчанию[WrapType.NONE](../../com.aspose.words/wraptype\#NONE).

Имеет эффект только для фигур верхнего уровня.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[WrapType](../../com.aspose.words/wraptype) константы. |

### setZOrder(int value) {#setZOrder-int-}
```
public void setZOrder(int value)
```


Определяет порядок отображения перекрывающихся фигур.

Имеет эффект только для фигур верхнего уровня.

Значение по умолчанию — 0.

Число представляет приоритет стека. Фигура с более высоким номером будет отображаться так, как если бы она перекрывала (перед) фигуру с меньшим номером.

Порядок перекрывающихся фигур независим для фигур в заголовке и в основном тексте документа.

Порядок отображения дочерних фигур в фигуре группы определяется их порядком внутри фигуры группы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

### setZOrder_IShape(int value) {#setZOrder-IShape-int-}
```
public void setZOrder_IShape(int value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  |

### solid() {#solid--}
```
public void solid()
```




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
### twoColorGradient(int style, int variant) {#twoColorGradient-int-int-}
```
public void twoColorGradient(int style, int variant)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| style | int |  |
| variant | int |  |

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
