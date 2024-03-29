---
title: Shape
second_title: Aspose.Words for Java API 参考
description: 表示绘图层中的对象，例如自选图形文本框自由格式 OLE 对象 ActiveX 控件或图片。
type: docs
weight: 516
url: /zh/java/com.aspose.words/shape/
---

**遗产：**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode), [com.aspose.words.ShapeBase](../../com.aspose.words/shapebase)
```
public class Shape extends ShapeBase
```

表示绘图层中的对象，例如自选图形、文本框、自由格式、OLE 对象、ActiveX 控件或图片。

要了解更多信息，请访问**Working with Shapes**文档文章。

使用[Shape](../../com.aspose.words/shape)类，您可以在 Microsoft Word 文档中创建或修改形状。

形状的一个重要属性是它的[ShapeBase.getShapeType()](../../com.aspose.words/shapebase\#getShapeType--).不同类型的形状在 Word 文档中可以具有不同的功能。例如，只有图像和 OLE 形状可以在其中包含图像。大多数形状都可以有文本，但不是全部。

可以有文本的形状，可以包含[Paragraph](../../com.aspose.words/paragraph)和[Table](../../com.aspose.words/table)节点作为孩子。
## 构造器

| 构造函数 | 描述 |
| --- | --- |
| [Shape(DocumentBase doc, int shapeType)](#Shape-com.aspose.words.DocumentBase-int-) | 初始化此类的新实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | 接待来访者。 |
| [adjustWithEffects(Rectangle2D.Float source)](#adjustWithEffects-java.awt.geom.Rectangle2D.Float-) | 添加到效果范围的源矩形值并返回最终矩形。 |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node-) | 将指定节点添加到此节点的子节点列表的末尾。 |
| [canHaveImage()](#canHaveImage--) | 如果形状类型允许形状具有图像，则返回 true。 |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [dd()](#dd--) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | 创建节点的副本。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int-) |  |
| [fetchInheritedShapeAttr(int key)](#fetchInheritedShapeAttr-int-) | 保留供系统使用。 |
| [fetchShapeAttr(int key)](#fetchShapeAttr-int-) | 保留供系统使用。 |
| [getAllowOverlap()](#getAllowOverlap--) | 获取一个值，该值指定此形状是否可以与其他形状重叠。 |
| [getAlternativeText()](#getAlternativeText--) | 定义要显示的替代文本而不是图形。 |
| [getAncestor(int ancestorType)](#getAncestor-int-) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class-) | 获取指定对象类型的第一个祖先。 |
| [getAnchorLocked()](#getAnchorLocked--) | 指定形状的锚点是否被锁定。 |
| [getAspectRatioLocked()](#getAspectRatioLocked--) | 指定形状的纵横比是否被锁定。 |
| [getBehindText()](#getBehindText--) | 指定形状是低于还是高于文本。 |
| [getBottom()](#getBottom--) | 获取形状包含块的底部边缘的位置。 |
| [getBounds()](#getBounds--) | 获取形状包含块的位置和大小。 |
| [getBoundsInPoints()](#getBoundsInPoints--) | 获取形状包含块的位置和大小，以点为单位，相对于最顶部形状的锚点。 |
| [getBoundsWithEffects()](#getBoundsWithEffects--) | 获取此形状对象在应用绘图效果后的最终范围。 |
| [getChart()](#getChart--) | 如果此形状具有图表，则提供对图表属性的访问。 |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean-) |  |
| [getChildNodes()](#getChildNodes--) | 获取此节点的所有直接子节点。 |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [getClass()](#getClass--) |  |
| [getContainer()](#getContainer--) |  |
| [getCoordOrigin()](#getCoordOrigin--) | 此形状的包含块左上角的坐标。 |
| [getCoordSize()](#getCoordSize--) | 此形状的包含块内的坐标空间的宽度和高度。 |
| [getCount()](#getCount--) | 获取此节点的直接子节点数。 |
| [getCurrentNode()](#getCurrentNode--) |  |
| [getCustomNodeId()](#getCustomNodeId--) | 指定自定义节点标识符。 |
| [getDashStyle()](#getDashStyle--) |  |
| [getDirectRunAttr(int fontAttr)](#getDirectRunAttr-int-) |  |
| [getDirectShapeAttr(int key)](#getDirectShapeAttr-int-) | 保留供系统使用。 |
| [getDistanceBottom()](#getDistanceBottom--) | 获取文档文本与形状底部边缘之间的距离（以磅为单位）。 |
| [getDistanceLeft()](#getDistanceLeft--) | 获取文档文本与形状左边缘之间的距离（以磅为单位）。 |
| [getDistanceRight()](#getDistanceRight--) | 获取文档文本与形状右边缘之间的距离（以磅为单位）。 |
| [getDistanceTop()](#getDistanceTop--) | 获取文档文本与形状上边缘之间的距离（以磅为单位）。 |
| [getDocument()](#getDocument--) | 获取此节点所属的文档。 |
| [getDocument_IInline()](#getDocument-IInline--) |  |
| [getEndArrowLength()](#getEndArrowLength--) |  |
| [getEndArrowType()](#getEndArrowType--) |  |
| [getEndArrowWidth()](#getEndArrowWidth--) |  |
| [getEndCap()](#getEndCap--) |  |
| [getExtrusionEnabled()](#getExtrusionEnabled--) | 如果启用了挤压效果，则返回 true。 |
| [getFill()](#getFill--) | 获取形状的填充格式。 |
| [getFillColor()](#getFillColor--) | 定义填充形状闭合路径的画笔颜色。 |
| [getFillType()](#getFillType--) |  |
| [getFillableBackColor()](#getFillableBackColor--) |  |
| [getFillableForeColor()](#getFillableForeColor--) |  |
| [getFillableImageBytes()](#getFillableImageBytes--) |  |
| [getFillableTransparency()](#getFillableTransparency--) |  |
| [getFillableVisible()](#getFillableVisible--) |  |
| [getFilled()](#getFilled--) | 确定是否填充形状的闭合路径。 |
| [getFilledColor()](#getFilledColor--) |  |
| [getFirstChild()](#getFirstChild--) | 获取节点的第一个子节点。 |
| [getFirstParagraph()](#getFirstParagraph--) | 获取形状中的第一段。 |
| [getFlipOrientation()](#getFlipOrientation--) | 切换形状的方向。 |
| [getFont()](#getFont--) | 提供对此对象的字体格式的访问。 |
| [getGradientAngle()](#getGradientAngle--) |  |
| [getGradientStops()](#getGradientStops--) |  |
| [getGradientStyle()](#getGradientStyle--) |  |
| [getGradientVariant()](#getGradientVariant--) |  |
| [getHRef()](#getHRef--) | 获取形状的完整超链接地址。 |
| [getHeight()](#getHeight--) | 获取形状包含块的高度。 |
| [getHorizontalAlignment()](#getHorizontalAlignment--) | 指定形状如何水平放置。 |
| [getHorizontalMargins_ITextBox()](#getHorizontalMargins-ITextBox--) |  |
| [getHorizontalRuleFormat()](#getHorizontalRuleFormat--) | 提供对水平规则形状属性的访问。 |
| [getImageData()](#getImageData--) | 提供对形状图像的访问。 |
| [getJoinStyle()](#getJoinStyle--) |  |
| [getLastChild()](#getLastChild--) | 获取节点的最后一个子节点。 |
| [getLastParagraph()](#getLastParagraph--) | 获取形状中的最后一段。 |
| [getLeft()](#getLeft--) | 获取形状包含块左边缘的位置。 |
| [getLineFillType()](#getLineFillType--) |  |
| [getLineStyle()](#getLineStyle--) |  |
| [getMarkupLanguage()](#getMarkupLanguage--) | 获取用于此图形对象的 MarkupLanguage。 |
| [getMarkupLanguage_ITextBox()](#getMarkupLanguage-ITextBox--) |  |
| [getName()](#getName--) | 获取可选的形状名称。 |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node-) |  |
| [getNextSibling()](#getNextSibling--) | 获取紧跟在该节点之后的节点。 |
| [getNodeType()](#getNodeType--) | 退货[NodeType.SHAPE](../../com.aspose.words/nodetype\#SHAPE). |
| [getOleFormat()](#getOleFormat--) | 提供对形状的 OLE 数据的访问。 |
| [getOn()](#getOn--) |  |
| [getOpacity()](#getOpacity--) |  |
| [getParentNode()](#getParentNode--) | 获取此节点的直接父级。 |
| [getParentParagraph()](#getParentParagraph--) | 返回直接父段落。 |
| [getParentParagraph_IInline()](#getParentParagraph-IInline--) |  |
| [getPatternType()](#getPatternType--) |  |
| [getPresetTexture()](#getPresetTexture--) |  |
| [getPreviousSibling()](#getPreviousSibling--) | 获取紧接在该节点之前的节点。 |
| [getRange()](#getRange--) | 返回一个**Range**表示包含在该节点中的文档部分的对象。 |
| [getRelativeHorizontalPosition()](#getRelativeHorizontalPosition--) | 指定相对于形状的水平位置。 |
| [getRelativeVerticalPosition()](#getRelativeVerticalPosition--) | 指定相对于垂直放置的形状。 |
| [getRight()](#getRight--) | 获取形状包含块右边缘的位置。 |
| [getRotateWithObject()](#getRotateWithObject--) |  |
| [getRotation()](#getRotation--) | 定义形状旋转的角度（以度为单位）。 |
| [getScreenTip()](#getScreenTip--) | 定义当鼠标指针移到形状上时显示的文本。 |
| [getShadowEnabled()](#getShadowEnabled--) | 如果启用了阴影效果，则返回 true。 |
| [getShadowFormat()](#getShadowFormat--) | 获取形状的阴影格式。 |
| [getShapeRenderer()](#getShapeRenderer--) | 创建并返回可用于将此形状渲染成图像的对象。 |
| [getShapeType()](#getShapeType--) | 获取形状类型。 |
| [getSignatureLine()](#getSignatureLine--) | 得到[getSignatureLine()](../../com.aspose.words/shape\#getSignatureLine--)如果形状是签名行，则对象。 |
| [getSizeInPoints()](#getSizeInPoints--) | 获取形状的大小（以磅为单位）。 |
| [getStartArrowLength()](#getStartArrowLength--) |  |
| [getStartArrowType()](#getStartArrowType--) |  |
| [getStartArrowWidth()](#getStartArrowWidth--) |  |
| [getStoryType()](#getStoryType--) | 退货[StoryType.TEXTBOX](../../com.aspose.words/storytype\#TEXTBOX). |
| [getStroke()](#getStroke--) | 定义形状的描边。 |
| [getStrokeColor()](#getStrokeColor--) | 定义描边的颜色。 |
| [getStrokeImageBytes()](#getStrokeImageBytes--) |  |
| [getStrokeTransparency()](#getStrokeTransparency--) |  |
| [getStrokeVisible()](#getStrokeVisible--) |  |
| [getStrokeWeight()](#getStrokeWeight--) | 以点为单位定义描边形状路径的画笔厚度。 |
| [getStroked()](#getStroked--) | 定义是否将描边路径。 |
| [getTarget()](#getTarget--) | 获取形状超链接的目标框架。 |
| [getText()](#getText--) | 获取此节点及其所有子节点的文本。 |
| [getTextBox()](#getTextBox--) | 定义指定文本如何在形状中显示的属性。 |
| [getTextBoxWrapMode_ITextBox()](#getTextBoxWrapMode-ITextBox--) |  |
| [getTextPath()](#getTextPath--) | 定义文本路径的文本（艺术字对象的）。 |
| [getTextboxLayoutFlow_ITextBox()](#getTextboxLayoutFlow-ITextBox--) |  |
| [getTextureAlignment()](#getTextureAlignment--) |  |
| [getTitle()](#getTitle--) | 获取当前形状对象的标题（标题）。 |
| [getTop()](#getTop--) | 获取形状包含块的上边缘位置。 |
| [getVerticalAlignment()](#getVerticalAlignment--) | 指定形状的垂直放置方式。 |
| [getWeight()](#getWeight--) |  |
| [getWidth()](#getWidth--) | 获取形状包含块的宽度。 |
| [getWrapSide()](#getWrapSide--) | 指定文本环绕形状的方式。 |
| [getWrapType()](#getWrapType--) | 定义形状是内嵌的还是浮动的。 |
| [getZOrder()](#getZOrder--) | 确定重叠形状的显示顺序。 |
| [getZOrder_IShape()](#getZOrder-IShape--) |  |
| [hasChart()](#hasChart--) | 如果此 Shape 有一个[getChart()](../../com.aspose.words/shape\#getChart--). |
| [hasChildNodes()](#hasChildNodes--) | 如果此节点有任何子节点，则返回 true。 |
| [hasImage()](#hasImage--) | 如果形状有图像字节或链接图像，则返回 true。 |
| [hasSmartArt()](#hasSmartArt--) | 如果此 Shape 具有 SmartArt 对象，则返回 true。 |
| [hasVerticalTextFlow_ITextBox()](#hasVerticalTextFlow-ITextBox--) |  |
| [hashCode()](#hashCode--) |  |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node-) | 返回子节点数组中指定子节点的索引。 |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node-) | 在指定的引用节点之后立即插入指定的节点。 |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node-) | 将指定节点插入到紧靠指定引用节点之前。 |
| [isComposite()](#isComposite--) | 返回 true，因为此节点可以有子节点。 |
| [isDecorative()](#isDecorative--) | 获取指定形状在文档中是否为装饰性的标志。 |
| [isDecorative(boolean value)](#isDecorative-boolean-) | 设置指定形状在文档中是否具有装饰性的标志。 |
| [isDeleteRevision()](#isDeleteRevision--) | 如果启用更改跟踪时此对象在 Microsoft Word 中被删除，则返回 true。 |
| [isGroup()](#isGroup--) | 如果这是一个组形状，则返回 true。 |
| [isHorizontalRule()](#isHorizontalRule--) | 如果此形状是水平规则，则返回 true。 |
| [isImage()](#isImage--) | 如果此形状是图像形状，则返回 true。 |
| [isInline()](#isInline--) | 一种快速确定此形状是否与文本内联的方法。 |
| [isInsertRevision()](#isInsertRevision--) | 如果在启用更改跟踪时将此对象插入 Microsoft Word，则返回 true。 |
| [isLayoutInCell()](#isLayoutInCell--) | 获取一个标志，该标志指示形状是显示在表格内部还是表格外部。 |
| [isLayoutInCell(boolean value)](#isLayoutInCell-boolean-) | 设置一个标志，指示形状是显示在表格内部还是表格外部。 |
| [isMoveFromRevision()](#isMoveFromRevision--) | 退货**true**如果启用更改跟踪时此对象在 Microsoft Word 中被移动（删除）。 |
| [isMoveToRevision()](#isMoveToRevision--) | 退货**true**如果启用更改跟踪时在 Microsoft Word 中移动（插入）此对象。 |
| [isSignatureLine()](#isSignatureLine--) | 指示该形状是 SignatureLine。 |
| [isTopLevel()](#isTopLevel--) | 如果此形状不是组形状的子形状，则返回 true。 |
| [isWordArt()](#isWordArt--) | 如果此形状是艺术字对象，则返回 true。 |
| [iterator()](#iterator--) | 为该节点的子节点上的每个样式迭代提供支持。 |
| [localToParent(Point2D.Float value)](#localToParent-java.awt.geom.Point2D.Float-) | 将本地坐标空间中的值转换为父形状的坐标空间。 |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node-) | 根据前序树遍历算法获取下一个节点。 |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int-) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [oneColorGradient(int style, int variant, double degree)](#oneColorGradient-int-int-double-) |  |
| [patterned(int patternType)](#patterned-int-) |  |
| [prependChild(Node newChild)](#prependChild-com.aspose.words.Node-) | 将指定节点添加到此节点的子节点列表的开头。 |
| [presetTextured(int presetTexture)](#presetTextured-int-) |  |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node-) | 根据前序树遍历算法获取上一个节点。 |
| [remove()](#remove--) | 从父级中移除自身。 |
| [removeAllChildren()](#removeAllChildren--) | 移除当前节点的所有子节点。 |
| [removeChild(Node oldChild)](#removeChild-com.aspose.words.Node-) | 删除指定的子节点。 |
| [removeMoveRevisions()](#removeMoveRevisions--) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [removeShapeAttr(int key)](#removeShapeAttr-int-) | 保留供系统使用。 |
| [removeSmartTags()](#removeSmartTags--) | 删除所有[SmartTag](../../com.aspose.words/smarttag)当前节点的后代节点。 |
| [selectNodes(String xpath)](#selectNodes-java.lang.String-) | 选择与 XPath 表达式匹配的节点列表。 |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String-) | 选择与 XPath 表达式匹配的第一个节点。 |
| [setAllowOverlap(boolean value)](#setAllowOverlap-boolean-) | 设置一个值，该值指定此形状是否可以与其他形状重叠。 |
| [setAlternativeText(String value)](#setAlternativeText-java.lang.String-) | 定义要显示的替代文本而不是图形。 |
| [setAnchorLocked(boolean value)](#setAnchorLocked-boolean-) | 指定形状的锚点是否被锁定。 |
| [setAspectRatioLocked(boolean value)](#setAspectRatioLocked-boolean-) | 指定形状的纵横比是否被锁定。 |
| [setBehindText(boolean value)](#setBehindText-boolean-) | 指定形状是低于还是高于文本。 |
| [setBounds(Rectangle2D.Float value)](#setBounds-java.awt.geom.Rectangle2D.Float-) | 设置形状包含块的位置和大小。 |
| [setCoordOrigin(Point value)](#setCoordOrigin-java.awt.Point-) | 此形状的包含块左上角的坐标。 |
| [setCoordSize(Dimension value)](#setCoordSize-java.awt.Dimension-) | 此形状的包含块内的坐标空间的宽度和高度。 |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | 指定自定义节点标识符。 |
| [setDashStyle(int value)](#setDashStyle-int-) |  |
| [setDistanceBottom(double value)](#setDistanceBottom-double-) | 设置文档文本和形状底部边缘之间的距离（以磅为单位）。 |
| [setDistanceLeft(double value)](#setDistanceLeft-double-) | 设置文档文本和形状左边缘之间的距离（以磅为单位）。 |
| [setDistanceRight(double value)](#setDistanceRight-double-) | 设置文档文本和形状右边缘之间的距离（以磅为单位）。 |
| [setDistanceTop(double value)](#setDistanceTop-double-) | 设置文档文本和形状上边缘之间的距离（以磅为单位）。 |
| [setEndArrowLength(int value)](#setEndArrowLength-int-) |  |
| [setEndArrowType(int value)](#setEndArrowType-int-) |  |
| [setEndArrowWidth(int value)](#setEndArrowWidth-int-) |  |
| [setEndCap(int value)](#setEndCap-int-) |  |
| [setFillColor(Color value)](#setFillColor-java.awt.Color-) | 定义填充形状闭合路径的画笔颜色。 |
| [setFillableBackColor(Color value)](#setFillableBackColor-java.awt.Color-) |  |
| [setFillableForeColor(Color value)](#setFillableForeColor-java.awt.Color-) |  |
| [setFillableTransparency(double value)](#setFillableTransparency-double-) |  |
| [setFillableVisible(boolean value)](#setFillableVisible-boolean-) |  |
| [setFilled(boolean value)](#setFilled-boolean-) | 确定是否填充形状的闭合路径。 |
| [setFilledColor(Color value)](#setFilledColor-java.awt.Color-) |  |
| [setFlipOrientation(int value)](#setFlipOrientation-int-) | 切换形状的方向。 |
| [setGradientAngle(double value)](#setGradientAngle-double-) |  |
| [setHRef(String value)](#setHRef-java.lang.String-) | 设置形状的完整超链接地址。 |
| [setHeight(double value)](#setHeight-double-) | 设置形状包含块的高度。 |
| [setHorizontalAlignment(int value)](#setHorizontalAlignment-int-) | 指定形状如何水平放置。 |
| [setImage(byte[] imageBytes)](#setImage-byte---) |  |
| [setJoinStyle(int value)](#setJoinStyle-int-) |  |
| [setLeft(double value)](#setLeft-double-) | 设置形状包含块左边缘的位置。 |
| [setLineFillType(int value)](#setLineFillType-int-) |  |
| [setLineStyle(int value)](#setLineStyle-int-) |  |
| [setName(String value)](#setName-java.lang.String-) | 设置可选的形状名称。 |
| [setOn(boolean value)](#setOn-boolean-) |  |
| [setOpacity(double value)](#setOpacity-double-) |  |
| [setRelativeHorizontalPosition(int value)](#setRelativeHorizontalPosition-int-) | 指定相对于形状的水平位置。 |
| [setRelativeVerticalPosition(int value)](#setRelativeVerticalPosition-int-) | 指定相对于垂直放置的形状。 |
| [setRotateWithObject(boolean value)](#setRotateWithObject-boolean-) |  |
| [setRotation(double value)](#setRotation-double-) | 定义形状旋转的角度（以度为单位）。 |
| [setRunAttr(int fontAttr, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [setScreenTip(String value)](#setScreenTip-java.lang.String-) | 定义当鼠标指针移到形状上时显示的文本。 |
| [setShapeAttr(int key, Object value)](#setShapeAttr-int-java.lang.Object-) | 保留供系统使用。 |
| [setStartArrowLength(int value)](#setStartArrowLength-int-) |  |
| [setStartArrowType(int value)](#setStartArrowType-int-) |  |
| [setStartArrowWidth(int value)](#setStartArrowWidth-int-) |  |
| [setStrokeColor(Color value)](#setStrokeColor-java.awt.Color-) | 定义描边的颜色。 |
| [setStrokeTransparency(double value)](#setStrokeTransparency-double-) |  |
| [setStrokeVisible(boolean value)](#setStrokeVisible-boolean-) |  |
| [setStrokeWeight(double value)](#setStrokeWeight-double-) | 以点为单位定义描边形状路径的画笔厚度。 |
| [setStroked(boolean value)](#setStroked-boolean-) | 定义是否将描边路径。 |
| [setTarget(String value)](#setTarget-java.lang.String-) | 设置形状超链接的目标框架。 |
| [setTextureAlignment(int value)](#setTextureAlignment-int-) |  |
| [setTitle(String value)](#setTitle-java.lang.String-) | 设置当前形状对象的标题（标题）。 |
| [setTop(double value)](#setTop-double-) | 设置形状包含块的上边缘位置。 |
| [setVerticalAlignment(int value)](#setVerticalAlignment-int-) | 指定形状的垂直放置方式。 |
| [setWeight(double value)](#setWeight-double-) |  |
| [setWidth(double value)](#setWidth-double-) | 设置形状包含块的宽度。 |
| [setWrapSide(int value)](#setWrapSide-int-) | 指定文本环绕形状的方式。 |
| [setWrapType(int value)](#setWrapType-int-) | 定义形状是内嵌的还是浮动的。 |
| [setZOrder(int value)](#setZOrder-int-) | 确定重叠形状的显示顺序。 |
| [setZOrder_IShape(int value)](#setZOrder-IShape-int-) |  |
| [solid()](#solid--) |  |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | 使用指定的保存选项将节点的内容导出为字符串。 |
| [toString(int saveFormat)](#toString-int-) |  |
| [twoColorGradient(int style, int variant)](#twoColorGradient-int-int-) |  |
| [updateSmartArtDrawing()](#updateSmartArtDrawing--) | 使用 Aspose.Words 的 SmartArt 冷渲染引擎更新 SmartArt 预渲染绘图。 |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### Shape(DocumentBase doc, int shapeType) {#Shape-com.aspose.words.DocumentBase-int-}
```
public Shape(DocumentBase doc, int shapeType)
```


初始化此类的新实例。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) |  |
| shapeType | int |  |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public boolean accept(DocumentVisitor visitor)
```


接待来访者。

枚举此节点及其所有子节点。每个节点调用 DocumentVisitor 上的相应方法。

有关更多信息，请参阅访问者设计模式。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | 将访问节点的访问者。 |

**退货：**
 boolean - 如果所有节点都被访问，则为真；如果 DocumentVisitor 在访问所有节点之前停止操作，则返回 false。来电[DocumentVisitor.visitShapeStart(com.aspose.words.Shape)](../../com.aspose.words/documentvisitor\#visitShapeStart-com.aspose.words.Shape-) , 然后调用[Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node\#accept-com.aspose.words.DocumentVisitor-)对于形状和调用的所有子节点[DocumentVisitor.visitShapeEnd(com.aspose.words.Shape)](../../com.aspose.words/documentvisitor\#visitShapeEnd-com.aspose.words.Shape-)在最后。
### adjustWithEffects(Rectangle2D.Float source) {#adjustWithEffects-java.awt.geom.Rectangle2D.Float-}
```
public Rectangle2D.Float adjustWithEffects(Rectangle2D.Float source)
```


添加到效果范围的源矩形值并返回最终矩形。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| source | java.awt.geom.Rectangle2D.Float |  |

**退货：**
java.awt.geom.Rectangle2D.Float
### appendChild(Node newChild) {#appendChild-com.aspose.words.Node-}
```
public Node appendChild(Node newChild)
```


将指定节点添加到此节点的子节点列表的末尾。

如果 newChild 已经在树中，则首先将其删除。

如果被插入的节点是从另一个文档创建的，你应该使用**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**将节点导入当前文档。然后可以将导入的节点插入到当前文档中。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | 要添加的节点。 |

**退货：**
[Node](../../com.aspose.words/node) - 添加的节点。
### canHaveImage() {#canHaveImage--}
```
public boolean canHaveImage()
```


如果形状类型允许形状具有图像，则返回 true。

尽管 Microsoft Word 有一种特殊的图像形状类型，但似乎在 Microsoft Word 文档中，除了组形状之外的任何形状都可以有图像，因此对于所有形状，除了[GroupShape](../../com.aspose.words/groupshape).

**退货：**
boolean - 如果形状类型允许形状具有图像，则为真。
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


创建节点的副本。

此方法用作节点的复制构造函数。克隆的节点没有父节点，但与原始节点属于同一个文档。

此方法始终执行节点的深层复制。这*isCloneChildren*参数指定是否也执行复制所有子节点。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| isCloneChildren | boolean | True 递归克隆指定节点下的子树； false 仅克隆节点本身。 |

**退货：**
[Node](../../com.aspose.words/node) - 克隆节点。
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货：**
布尔值
### fetchInheritedRunAttr(int fontAttr) {#fetchInheritedRunAttr-int-}
```
public Object fetchInheritedRunAttr(int fontAttr)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontAttr | int |  |

**退货：**
java.lang.Object
### fetchInheritedShapeAttr(int key) {#fetchInheritedShapeAttr-int-}
```
public Object fetchInheritedShapeAttr(int key)
```


保留供系统使用。 IShapeAttrSource。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货：**
java.lang.Object
### fetchShapeAttr(int key) {#fetchShapeAttr-int-}
```
public Object fetchShapeAttr(int key)
```


保留供系统使用。 IShapeAttrSource。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货：**
java.lang.Object
### getAllowOverlap() {#getAllowOverlap--}
```
public boolean getAllowOverlap()
```


获取一个值，该值指定此形状是否可以与其他形状重叠。

此属性会影响 Microsoft Word 中形状的行为。 Aspose.Words 忽略此属性的值。

此属性仅适用于顶级形状。

默认值为**true**.

**退货：**
boolean - 指定此形状是否可以与其他形状重叠的值。
### getAlternativeText() {#getAlternativeText--}
```
public String getAlternativeText()
```


定义要显示的替代文本而不是图形。

默认值为空字符串。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getAncestor(int ancestorType) {#getAncestor-int-}
```
public CompositeNode getAncestor(int ancestorType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| ancestorType | int |  |

**退货：**
[CompositeNode](../../com.aspose.words/compositenode)
### getAncestor(Class ancestorType) {#getAncestor-java.lang.Class-}
```
public CompositeNode getAncestor(Class ancestorType)
```


获取指定对象类型的第一个祖先。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| ancestorType | java.lang.Class | 要检索的祖先的对象类型。 |

**退货：**
[CompositeNode](../../com.aspose.words/compositenode) - 指定类型的祖先，如果未找到此类型的祖先，则为 null。

如果祖先类型等于 ancestorType 或派生自 ancestorType，则祖先类型匹配。
### getAnchorLocked() {#getAnchorLocked--}
```
public boolean getAnchorLocked()
```


指定形状的锚点是否被锁定。

默认值为**false**.

仅对顶级形状有效。

此属性会影响 Microsoft Word 中形状锚点的行为。当锚点未锁定时，在 Microsoft Word 中移动形状也可以移动形状的锚点。

**退货：**
boolean - 相应的布尔值。
### getAspectRatioLocked() {#getAspectRatioLocked--}
```
public boolean getAspectRatioLocked()
```


指定形状的纵横比是否被锁定。

默认值取决于[getShapeType()](../../com.aspose.words/shapebase\#getShapeType--) 对于 ShapeType.Image 它是**true**但对于其他形状类型，它是**false**.

仅对顶级形状有效。

**退货：**
boolean - 相应的布尔值。
### getBehindText() {#getBehindText--}
```
public boolean getBehindText()
```


指定形状是低于还是高于文本。

仅对顶级形状有效。

默认值为**false**.

**退货：**
boolean - 相应的布尔值。
### getBottom() {#getBottom--}
```
public double getBottom()
```


获取形状包含块的底部边缘的位置。

对于顶级形状，该值以点为单位并且相对于形状锚点。

对于组中的形状，该值位于父组的坐标空间和单位中。

**退货：**
double - 形状包含块的底部边缘的位置。
### getBounds() {#getBounds--}
```
public Rectangle2D.Float getBounds()
```


获取形状包含块的位置和大小。设置时忽略纵横比锁定。

对于顶级形状，该值以点为单位并且相对于形状锚点。

对于组中的形状，该值位于父组的坐标空间和单位中。

**退货：**
java.awt.geom.Rectangle2D.Float - 形状包含块的位置和大小。
### getBoundsInPoints() {#getBoundsInPoints--}
```
public Rectangle2D.Float getBoundsInPoints()
```


获取形状包含块的位置和大小，以点为单位，相对于最顶部形状的锚点。

**退货：**
java.awt.geom.Rectangle2D.Float - 形状包含块的位置和大小，以点为单位，相对于最顶部形状的锚点。
### getBoundsWithEffects() {#getBoundsWithEffects--}
```
public Rectangle2D.Float getBoundsWithEffects()
```


获取此形状对象在应用绘图效果后的最终范围。价值以点为单位。

**退货：**
java.awt.geom.Rectangle2D.Float - 此形状对象在应用绘图效果后的最终范围。
### getChart() {#getChart--}
```
public Chart getChart()
```


如果此形状具有图表，则提供对图表属性的访问。该属性将返回[getChart()](../../com.aspose.words/shape\#getChart--)只有当[hasChart()](../../com.aspose.words/shape\#hasChart--)此 Shape 属性为真，否则将抛出异常。

**退货：**
[Chart](../../com.aspose.words/chart) - 相应的[Chart](../../com.aspose.words/chart)价值。
### getChild(int nodeType, int index, boolean isDeep) {#getChild-int-int-boolean-}
```
public Node getChild(int nodeType, int index, boolean isDeep)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| nodeType | int |  |
| index | int |  |
| isDeep | boolean |  |

**退货：**
[Node](../../com.aspose.words/node)
### getChildNodes() {#getChildNodes--}
```
public NodeCollection getChildNodes()
```


获取此节点的所有直接子节点。

笔记，[getChildNodes()](../../com.aspose.words/compositenode\#getChildNodes--)相当于调用 GetChildNodes(NodeType.Any, false) 并在每次访问时创建并返回一个新集合。

如果没有子节点，则此属性返回一个空集合。

**退货：**
[NodeCollection](../../com.aspose.words/nodecollection) - 该节点的所有直接子节点。
### getChildNodes(int nodeType, boolean isDeep) {#getChildNodes-int-boolean-}
```
public NodeCollection getChildNodes(int nodeType, boolean isDeep)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| nodeType | int |  |
| isDeep | boolean |  |

**退货：**
[NodeCollection](../../com.aspose.words/nodecollection)
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getContainer() {#getContainer--}
```
public CompositeNode getContainer()
```




**退货：**
[CompositeNode](../../com.aspose.words/compositenode)
### getCoordOrigin() {#getCoordOrigin--}
```
public Point getCoordOrigin()
```


此形状的包含块左上角的坐标。

默认值为 (0,0)。

**退货：**
java.awt.Point - 对应的 java.awt.Point 值。
### getCoordSize() {#getCoordSize--}
```
public Dimension getCoordSize()
```


此形状的包含块内的坐标空间的宽度和高度。

默认值为 (1000, 1000)。

**退货：**
java.awt.Dimension - 相应的 java.awt.Dimension 值。
### getCount() {#getCount--}
```
public int getCount()
```


获取此节点的直接子节点数。

**退货：**
int - 此节点的直接子节点数。
### getCurrentNode() {#getCurrentNode--}
```
public Node getCurrentNode()
```




**退货：**
[Node](../../com.aspose.words/node)
### getCustomNodeId() {#getCustomNodeId--}
```
public int getCustomNodeId()
```


指定自定义节点标识符。

默认为零。

这个标识符可以任意设置和使用。例如，作为获取外部数据的密钥。

重要说明，指定的值不会保存到输出文件中，并且仅在节点生命周期内存在。

**退货：**
int - 相应的 int 值。
### getDashStyle() {#getDashStyle--}
```
public int getDashStyle()
```




**退货：**
整数
### getDirectRunAttr(int fontAttr) {#getDirectRunAttr-int-}
```
public Object getDirectRunAttr(int fontAttr)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontAttr | int |  |

**退货：**
java.lang.Object
### getDirectShapeAttr(int key) {#getDirectShapeAttr-int-}
```
public Object getDirectShapeAttr(int key)
```


保留供系统使用。 IShapeAttrSource。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货：**
java.lang.Object
### getDistanceBottom() {#getDistanceBottom--}
```
public double getDistanceBottom()
```


获取文档文本与形状底部边缘之间的距离（以磅为单位）。

默认值为 0。

仅对顶级形状有效。

**退货：**
double - 文档文本和形状底部边缘之间的距离（以磅为单位）。
### getDistanceLeft() {#getDistanceLeft--}
```
public double getDistanceLeft()
```


获取文档文本与形状左边缘之间的距离（以磅为单位）。

默认值为 1/8 英寸。

仅对顶级形状有效。

**退货：**
double - 文档文本和形状左边缘之间的距离（以磅为单位）。
### getDistanceRight() {#getDistanceRight--}
```
public double getDistanceRight()
```


获取文档文本与形状右边缘之间的距离（以磅为单位）。

默认值为 1/8 英寸。

仅对顶级形状有效。

**退货：**
double - 文档文本和形状右边缘之间的距离（以磅为单位）。
### getDistanceTop() {#getDistanceTop--}
```
public double getDistanceTop()
```


获取文档文本与形状上边缘之间的距离（以磅为单位）。

默认值为 0。

仅对顶级形状有效。

**退货：**
double - 文档文本和形状上边缘之间的距离（以磅为单位）。
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


获取此节点所属的文档。

该节点始终属于一个文档，即使它刚刚创建并且尚未添加到树中，或者如果它已从树中删除也是如此。

**退货：**
[DocumentBase](../../com.aspose.words/documentbase) - 该节点所属的文档。
### getDocument_IInline() {#getDocument-IInline--}
```
public DocumentBase getDocument_IInline()
```




**退货：**
[DocumentBase](../../com.aspose.words/documentbase)
### getEndArrowLength() {#getEndArrowLength--}
```
public int getEndArrowLength()
```




**退货：**
整数
### getEndArrowType() {#getEndArrowType--}
```
public int getEndArrowType()
```




**退货：**
整数
### getEndArrowWidth() {#getEndArrowWidth--}
```
public int getEndArrowWidth()
```




**退货：**
整数
### getEndCap() {#getEndCap--}
```
public int getEndCap()
```




**退货：**
整数
### getExtrusionEnabled() {#getExtrusionEnabled--}
```
public boolean getExtrusionEnabled()
```


如果启用了挤压效果，则返回 true。

**退货：**
boolean - 如果启用挤压效果则为 True。
### getFill() {#getFill--}
```
public Fill getFill()
```


获取形状的填充格式。

**退货：**
[Fill](../../com.aspose.words/fill) - 填充形状的格式。
### getFillColor() {#getFillColor--}
```
public Color getFillColor()
```


定义填充形状闭合路径的画笔颜色。

这是一个捷径[Fill.getColor()](../../com.aspose.words/fill\#getColor--) / [Fill.setColor(java.awt.Color)](../../com.aspose.words/fill\#setColor-java.awt.Color-)财产。

默认值为 。

**退货：**
java.awt.Color - 相应的 java.awt.Color 值。
### getFillType() {#getFillType--}
```
public int getFillType()
```




**退货：**
整数
### getFillableBackColor() {#getFillableBackColor--}
```
public Color getFillableBackColor()
```




**退货：**
java.awt.颜色
### getFillableForeColor() {#getFillableForeColor--}
```
public Color getFillableForeColor()
```




**退货：**
java.awt.颜色
### getFillableImageBytes() {#getFillableImageBytes--}
```
public byte[] getFillableImageBytes()
```




**退货：**
字节[]
### getFillableTransparency() {#getFillableTransparency--}
```
public double getFillableTransparency()
```




**退货：**
双倍的
### getFillableVisible() {#getFillableVisible--}
```
public boolean getFillableVisible()
```




**退货：**
布尔值
### getFilled() {#getFilled--}
```
public boolean getFilled()
```


确定是否填充形状的闭合路径。

这是一个捷径[Fill.getOn()](../../com.aspose.words/fill\#getOn--) / [Fill.setOn(boolean)](../../com.aspose.words/fill\#setOn-boolean-)财产。

默认值为**true**.

**退货：**
boolean - 相应的布尔值。
### getFilledColor() {#getFilledColor--}
```
public Color getFilledColor()
```




**退货：**
java.awt.颜色
### getFirstChild() {#getFirstChild--}
```
public Node getFirstChild()
```


获取节点的第一个子节点。如果没有第一个子节点，则返回 null。

**退货：**
[Node](../../com.aspose.words/node) - 节点的第一个孩子。
### getFirstParagraph() {#getFirstParagraph--}
```
public Paragraph getFirstParagraph()
```


获取形状中的第一段。

**退货：**
[Paragraph](../../com.aspose.words/paragraph) - 形状的第一段。
### getFlipOrientation() {#getFlipOrientation--}
```
public int getFlipOrientation()
```


切换形状的方向。

默认值为[FlipOrientation.NONE](../../com.aspose.words/fliporientation\#NONE).

**退货：**
 int - 相应的 int 值。返回值是按位组合[FlipOrientation](../../com.aspose.words/fliporientation)常数。
### getFont() {#getFont--}
```
public Font getFont()
```


提供对此对象的字体格式的访问。

**退货：**
[Font](../../com.aspose.words/font) - 相应的[Font](../../com.aspose.words/font)价值。
### getGradientAngle() {#getGradientAngle--}
```
public double getGradientAngle()
```




**退货：**
双倍的
### getGradientStops() {#getGradientStops--}
```
public GradientStopCollection getGradientStops()
```




**退货：**
[GradientStopCollection](../../com.aspose.words/gradientstopcollection)
### getGradientStyle() {#getGradientStyle--}
```
public int getGradientStyle()
```




**退货：**
整数
### getGradientVariant() {#getGradientVariant--}
```
public int getGradientVariant()
```




**退货：**
整数
### getHRef() {#getHRef--}
```
public String getHRef()
```


获取形状的完整超链接地址。

默认值为空字符串。

以下是此属性的有效值示例：

完整 URI：https://www.aspose.com/。

完整文件名：C:\\\\我的文件\\\\销售报告.doc 。

相对 URI：../../../resource.txt 

相对文件名：..\\\\我的文件\\\\销售报告.doc 。

另一个文档中的书签：https://www.aspose.com/Products/Default.aspx\#套房 

本文档中的书签：\#BookmakName 。

**退货：**
java.lang.String - 形状的完整超链接地址。
### getHeight() {#getHeight--}
```
public double getHeight()
```


获取形状包含块的高度。

对于顶级形状，该值以磅为单位。

对于组中的形状，该值位于父组的坐标空间和单位中。

默认值为 0。

**退货：**
double - 形状包含块的高度。
### getHorizontalAlignment() {#getHorizontalAlignment--}
```
public int getHorizontalAlignment()
```


指定形状如何水平放置。

默认值为[HorizontalAlignment.NONE](../../com.aspose.words/horizontalalignment\#NONE).

仅对顶级浮动形状有效。

**退货：**
int - 相应的 int 值。返回值是其中之一[HorizontalAlignment](../../com.aspose.words/horizontalalignment)常数。
### getHorizontalMargins_ITextBox() {#getHorizontalMargins-ITextBox--}
```
public float getHorizontalMargins_ITextBox()
```




**退货：**
漂浮
### getHorizontalRuleFormat() {#getHorizontalRuleFormat--}
```
public HorizontalRuleFormat getHorizontalRuleFormat()
```


提供对水平规则形状属性的访问。对于不是水平线的形状，返回 null。

**退货：**
[HorizontalRuleFormat](../../com.aspose.words/horizontalruleformat) - 相应的[HorizontalRuleFormat](../../com.aspose.words/horizontalruleformat)价值。
### getImageData() {#getImageData--}
```
public ImageData getImageData()
```


提供对形状图像的访问。如果形状不能包含图像，则返回 null。

**退货：**
[ImageData](../../com.aspose.words/imagedata) - 相应的[ImageData](../../com.aspose.words/imagedata)价值。
### getJoinStyle() {#getJoinStyle--}
```
public int getJoinStyle()
```




**退货：**
整数
### getLastChild() {#getLastChild--}
```
public Node getLastChild()
```


获取节点的最后一个子节点。如果没有最后一个子节点，则返回 null。

**退货：**
[Node](../../com.aspose.words/node) - 节点的最后一个孩子。
### getLastParagraph() {#getLastParagraph--}
```
public Paragraph getLastParagraph()
```


获取形状中的最后一段。

**退货：**
[Paragraph](../../com.aspose.words/paragraph) - 形状的最后一段。
### getLeft() {#getLeft--}
```
public double getLeft()
```


获取形状包含块左边缘的位置。

对于顶级形状，该值以点为单位并且相对于形状锚点。

对于组中的形状，该值位于父组的坐标空间和单位中。

默认值为 0。

仅对浮动形状有效。

**退货：**
double - 形状包含块的左边缘的位置。
### getLineFillType() {#getLineFillType--}
```
public int getLineFillType()
```




**退货：**
整数
### getLineStyle() {#getLineStyle--}
```
public int getLineStyle()
```




**退货：**
整数
### getMarkupLanguage() {#getMarkupLanguage--}
```
public byte getMarkupLanguage()
```


获取用于此图形对象的 MarkupLanguage。

**退货：**
 byte - 用于此图形对象的 MarkupLanguage。返回值是其中之一[ShapeMarkupLanguage](../../com.aspose.words/shapemarkuplanguage)常数。
### getMarkupLanguage_ITextBox() {#getMarkupLanguage-ITextBox--}
```
public byte getMarkupLanguage_ITextBox()
```




**退货：**
字节
### getName() {#getName--}
```
public String getName()
```


获取可选的形状名称。

默认为空字符串。

不能为空，但可以是空字符串。

**退货：**
java.lang.String - 可选的形状名称。
### getNextMatchingNode(Node curNode) {#getNextMatchingNode-com.aspose.words.Node-}
```
public Node getNextMatchingNode(Node curNode)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node) |  |

**退货：**
[Node](../../com.aspose.words/node)
### getNextSibling() {#getNextSibling--}
```
public Node getNextSibling()
```


获取紧跟在该节点之后的节点。如果没有下一个节点，则返回 null。

**退货：**
[Node](../../com.aspose.words/node) - 紧接此节点之后的节点。
### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


退货[NodeType.SHAPE](../../com.aspose.words/nodetype\#SHAPE).

**退货：**
整数 -\{[NodeType.SHAPE](../../com.aspose.words/nodetype\#SHAPE) .返回值是其中之一[NodeType](../../com.aspose.words/nodetype)常数。
### getOleFormat() {#getOleFormat--}
```
public OleFormat getOleFormat()
```


提供对形状的 OLE 数据的访问。对于不是 OLE 对象或 ActiveX 控件的形状，返回 null。

**退货：**
[OleFormat](../../com.aspose.words/oleformat) - 相应的[OleFormat](../../com.aspose.words/oleformat)价值。
### getOn() {#getOn--}
```
public boolean getOn()
```




**退货：**
布尔值
### getOpacity() {#getOpacity--}
```
public double getOpacity()
```




**退货：**
双倍的
### getParentNode() {#getParentNode--}
```
public CompositeNode getParentNode()
```


获取此节点的直接父级。

如果一个节点刚刚被创建并且还没有被添加到树中，或者如果它已经被从树中移除，则父节点为空。

**退货：**
[CompositeNode](../../com.aspose.words/compositenode) - 此节点的直接父节点。
### getParentParagraph() {#getParentParagraph--}
```
public Paragraph getParentParagraph()
```


返回直接父段落。对于组形状的子形状和 Office Math 对象的子形状，始终返回 null。

**退货：**
[Paragraph](../../com.aspose.words/paragraph) - 直接父段落。
### getParentParagraph_IInline() {#getParentParagraph-IInline--}
```
public Paragraph getParentParagraph_IInline()
```




**退货：**
[Paragraph](../../com.aspose.words/paragraph)
### getPatternType() {#getPatternType--}
```
public int getPatternType()
```




**退货：**
整数
### getPresetTexture() {#getPresetTexture--}
```
public int getPresetTexture()
```




**退货：**
整数
### getPreviousSibling() {#getPreviousSibling--}
```
public Node getPreviousSibling()
```


获取紧接在该节点之前的节点。如果前面没有节点，则返回 null。

**退货：**
[Node](../../com.aspose.words/node) - 紧接在该节点之前的节点。
### getRange() {#getRange--}
```
public Range getRange()
```


返回一个**Range**表示包含在该节点中的文档部分的对象。

**退货：**
[Range](../../com.aspose.words/range) - 一个**Range**表示包含在该节点中的文档部分的对象。
### getRelativeHorizontalPosition() {#getRelativeHorizontalPosition--}
```
public int getRelativeHorizontalPosition()
```


指定相对于形状的水平位置。

默认值为[RelativeHorizontalPosition.COLUMN](../../com.aspose.words/relativehorizontalposition\#COLUMN).

仅对顶级浮动形状有效。

**退货：**
int - 相应的 int 值。返回值是其中之一[RelativeHorizontalPosition](../../com.aspose.words/relativehorizontalposition)常数。
### getRelativeVerticalPosition() {#getRelativeVerticalPosition--}
```
public int getRelativeVerticalPosition()
```


指定相对于垂直放置的形状。

默认值为[RelativeVerticalPosition.PARAGRAPH](../../com.aspose.words/relativeverticalposition\#PARAGRAPH).

仅对顶级浮动形状有效。

**退货：**
int - 相应的 int 值。返回值是其中之一[RelativeVerticalPosition](../../com.aspose.words/relativeverticalposition)常数。
### getRight() {#getRight--}
```
public double getRight()
```


获取形状包含块右边缘的位置。

对于顶级形状，该值以点为单位并且相对于形状锚点。

对于组中的形状，该值位于父组的坐标空间和单位中。

**退货：**
double - 形状包含块的右边缘的位置。
### getRotateWithObject() {#getRotateWithObject--}
```
public boolean getRotateWithObject()
```




**退货：**
布尔值
### getRotation() {#getRotation--}
```
public double getRotation()
```


定义形状旋转的角度（以度为单位）。正值对应顺时针旋转角度。

默认值为 0。

**退货：**
double - 相应的双精度值。
### getScreenTip() {#getScreenTip--}
```
public String getScreenTip()
```


定义当鼠标指针移到形状上时显示的文本。

默认值为空字符串。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getShadowEnabled() {#getShadowEnabled--}
```
public boolean getShadowEnabled()
```


如果启用了阴影效果，则返回 true。

**退货：**
boolean - 如果启用了阴影效果则为 True。
### getShadowFormat() {#getShadowFormat--}
```
public ShadowFormat getShadowFormat()
```


获取形状的阴影格式。

**退货：**
[ShadowFormat](../../com.aspose.words/shadowformat) - 形状的阴影格式。
### getShapeRenderer() {#getShapeRenderer--}
```
public ShapeRenderer getShapeRenderer()
```


创建并返回可用于将此形状渲染成图像的对象。

这个方法只是调用[ShapeRenderer](../../com.aspose.words/shaperenderer)构造函数并将此对象作为参数传递。

**退货：**
[ShapeRenderer](../../com.aspose.words/shaperenderer) - 此形状的渲染器对象。
### getShapeType() {#getShapeType--}
```
public int getShapeType()
```


获取形状类型。

**退货：**
 int - 形状类型。返回值是其中之一[ShapeType](../../com.aspose.words/shapetype)常数。
### getSignatureLine() {#getSignatureLine--}
```
public SignatureLine getSignatureLine()
```


得到[getSignatureLine()](../../com.aspose.words/shape\#getSignatureLine--)如果形状是签名行，则对象。退货**null**否则。您可以使用将新的 SignatureLines 插入到文档中[DocumentBuilder.insertSignatureLine(com.aspose.words.SignatureLineOptions)](../../com.aspose.words/documentbuilder\#insertSignatureLine-com.aspose.words.SignatureLineOptions-)和**M:Aspose.Words.DocumentBuilder.InsertSignatureLine(Aspose.Words.SignatureLineOptions,Aspose.Words.Drawing.RelativeHorizontalPosition,System.Double,Aspose.Words.Drawing.RelativeVerticalPosition,System.Double,Aspose.Words.Drawing.WrapType)**

**退货：**
[SignatureLine](../../com.aspose.words/signatureline) -\{[getSignatureLine()](../../com.aspose.words/shape\#getSignatureLine--)如果形状是签名行，则对象。
### getSizeInPoints() {#getSizeInPoints--}
```
public Point2D.Float getSizeInPoints()
```


获取形状的大小（以磅为单位）。获取形状的大小（以磅为单位）。

 Point2D.Float 用作返回类型，因为我们在这里需要浮点尺寸值。应该假设 Point2D 的*x == width*和*y == height*.

**退货：**
java.awt.geom.Point2D.Float - 形状的大小（以磅为单位）。
### getStartArrowLength() {#getStartArrowLength--}
```
public int getStartArrowLength()
```




**退货：**
整数
### getStartArrowType() {#getStartArrowType--}
```
public int getStartArrowType()
```




**退货：**
整数
### getStartArrowWidth() {#getStartArrowWidth--}
```
public int getStartArrowWidth()
```




**退货：**
整数
### getStoryType() {#getStoryType--}
```
public int getStoryType()
```


退货[StoryType.TEXTBOX](../../com.aspose.words/storytype\#TEXTBOX).

**退货：**
整数 -\{[StoryType.TEXTBOX](../../com.aspose.words/storytype\#TEXTBOX) .返回值是其中之一[StoryType](../../com.aspose.words/storytype)常数。
### getStroke() {#getStroke--}
```
public Stroke getStroke()
```


定义形状的描边。

**退货：**
[Stroke](../../com.aspose.words/stroke) - 相应的[Stroke](../../com.aspose.words/stroke)价值。
### getStrokeColor() {#getStrokeColor--}
```
public Color getStrokeColor()
```


定义描边的颜色。

这是一个捷径[Stroke.getColor()](../../com.aspose.words/stroke\#getColor--) / [Stroke.setColor(java.awt.Color)](../../com.aspose.words/stroke\#setColor-java.awt.Color-)财产。

默认值为 。

**退货：**
java.awt.Color - 相应的 java.awt.Color 值。
### getStrokeImageBytes() {#getStrokeImageBytes--}
```
public byte[] getStrokeImageBytes()
```




**退货：**
字节[]
### getStrokeTransparency() {#getStrokeTransparency--}
```
public double getStrokeTransparency()
```




**退货：**
双倍的
### getStrokeVisible() {#getStrokeVisible--}
```
public boolean getStrokeVisible()
```




**退货：**
布尔值
### getStrokeWeight() {#getStrokeWeight--}
```
public double getStrokeWeight()
```


以点为单位定义描边形状路径的画笔厚度。

这是一个捷径[Stroke.getWeight()](../../com.aspose.words/stroke\#getWeight--) / [Stroke.setWeight(double)](../../com.aspose.words/stroke\#setWeight-double-)财产。

默认值为 0.75。

**退货：**
double - 相应的双精度值。
### getStroked() {#getStroked--}
```
public boolean getStroked()
```


定义是否将描边路径。

这是一个捷径[Stroke.getOn()](../../com.aspose.words/stroke\#getOn--) / [Stroke.setOn(boolean)](../../com.aspose.words/stroke\#setOn-boolean-)财产。

默认值为**true**.

**退货：**
boolean - 相应的布尔值。
### getTarget() {#getTarget--}
```
public String getTarget()
```


获取形状超链接的目标框架。

默认值为空字符串。

**退货：**
java.lang.String - 形状超链接的目标框架。
### getText() {#getText--}
```
public String getText()
```


获取此节点及其所有子节点的文本。

返回的字符串包括所有控制字符和特殊字符，如[ControlChar](../../com.aspose.words/controlchar).

**退货：**
java.lang.字符串
### getTextBox() {#getTextBox--}
```
public TextBox getTextBox()
```


定义指定文本如何在形状中显示的属性。

**退货：**
[TextBox](../../com.aspose.words/textbox) - 相应的[TextBox](../../com.aspose.words/textbox)价值。
### getTextBoxWrapMode_ITextBox() {#getTextBoxWrapMode-ITextBox--}
```
public int getTextBoxWrapMode_ITextBox()
```




**退货：**
整数
### getTextPath() {#getTextPath--}
```
public TextPath getTextPath()
```


定义文本路径的文本（艺术字对象的）。

**退货：**
[TextPath](../../com.aspose.words/textpath) - 相应的[TextPath](../../com.aspose.words/textpath)价值。
### getTextboxLayoutFlow_ITextBox() {#getTextboxLayoutFlow-ITextBox--}
```
public int getTextboxLayoutFlow_ITextBox()
```




**退货：**
整数
### getTextureAlignment() {#getTextureAlignment--}
```
public int getTextureAlignment()
```




**退货：**
整数
### getTitle() {#getTitle--}
```
public String getTitle()
```


获取当前形状对象的标题（标题）。

默认为空字符串。

不能为空，但可以是空字符串。

**退货：**
java.lang.String - 当前形状对象的标题（标题）。
### getTop() {#getTop--}
```
public double getTop()
```


获取形状包含块的上边缘位置。

对于顶级形状，该值以点为单位并且相对于形状锚点。

对于组中的形状，该值位于父组的坐标空间和单位中。

默认值为 0。

仅对浮动形状有效。

**退货：**
double - 形状包含块的顶部边缘的位置。
### getVerticalAlignment() {#getVerticalAlignment--}
```
public int getVerticalAlignment()
```


指定形状的垂直放置方式。

默认值为[VerticalAlignment.NONE](../../com.aspose.words/verticalalignment\#NONE).

仅对顶级浮动形状有效。

**退货：**
int - 相应的 int 值。返回值是其中之一[VerticalAlignment](../../com.aspose.words/verticalalignment)常数。
### getWeight() {#getWeight--}
```
public double getWeight()
```




**退货：**
双倍的
### getWidth() {#getWidth--}
```
public double getWidth()
```


获取形状包含块的宽度。

对于顶级形状，该值以磅为单位。

对于组中的形状，该值位于父组的坐标空间和单位中。

默认值为 0。

**退货：**
double - 形状包含块的宽度。
### getWrapSide() {#getWrapSide--}
```
public int getWrapSide()
```


指定文本环绕形状的方式。

默认值为[WrapSide.BOTH](../../com.aspose.words/wrapside\#BOTH).

仅对顶级形状有效。

**退货：**
int - 相应的 int 值。返回值是其中之一[WrapSide](../../com.aspose.words/wrapside)常数。
### getWrapType() {#getWrapType--}
```
public int getWrapType()
```


定义形状是内嵌的还是浮动的。对于浮动形状，定义形状周围文本的环绕模式。

默认值为[WrapType.NONE](../../com.aspose.words/wraptype\#NONE).

仅对顶级形状有效。

**退货：**
int - 相应的 int 值。返回值是其中之一[WrapType](../../com.aspose.words/wraptype)常数。
### getZOrder() {#getZOrder--}
```
public int getZOrder()
```


确定重叠形状的显示顺序。

仅对顶级形状有效。

默认值为 0。

数字代表堆叠优先级。数字较大的形状将显示为与数字较小的形状重叠（在“前面”）。

重叠形状的顺序与页眉和文档正文中的形状无关。

组形状中子形状的显示顺序由它们在组形状中的顺序决定。

**退货：**
int - 相应的 int 值。
### getZOrder_IShape() {#getZOrder-IShape--}
```
public int getZOrder_IShape()
```




**退货：**
整数
### hasChart() {#hasChart--}
```
public boolean hasChart()
```


如果此 Shape 有一个[getChart()](../../com.aspose.words/shape\#getChart--).

**退货：**
 boolean - 如果这个 Shape 有一个[getChart()](../../com.aspose.words/shape\#getChart--).
### hasChildNodes() {#hasChildNodes--}
```
public boolean hasChildNodes()
```


如果此节点有任何子节点，则返回 true。

**退货：**
boolean - 如果此节点有任何子节点则为真。
### hasImage() {#hasImage--}
```
public boolean hasImage()
```


如果形状有图像字节或链接图像，则返回 true。

**退货：**
boolean - 如果形状具有图像字节或链接图像，则为真。
### hasSmartArt() {#hasSmartArt--}
```
public boolean hasSmartArt()
```


如果此 Shape 具有 SmartArt 对象，则返回 true。

**退货：**
boolean - 如果此 Shape 具有 SmartArt 对象，则为 True。
### hasVerticalTextFlow_ITextBox() {#hasVerticalTextFlow-ITextBox--}
```
public boolean hasVerticalTextFlow_ITextBox()
```




**退货：**
布尔值
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### indexOf(Node child) {#indexOf-com.aspose.words.Node-}
```
public int indexOf(Node child)
```


返回子节点数组中指定子节点的索引。如果在子节点中找不到该节点，则返回 -1。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| child | [Node](../../com.aspose.words/node) |  |

**退货：**
整数
### insertAfter(Node newChild, Node refChild) {#insertAfter-com.aspose.words.Node-com.aspose.words.Node-}
```
public Node insertAfter(Node newChild, Node refChild)
```


在指定的引用节点之后立即插入指定的节点。

如果 refChild 为 null，则在子节点列表的开头插入 newChild。

如果 newChild 已经在树中，则首先将其删除。

如果被插入的节点是从另一个文档创建的，你应该使用**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**将节点导入当前文档。然后可以将导入的节点插入到当前文档中。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | 要插入的节点。 |
| refChild | [Node](../../com.aspose.words/node) | 作为参考节点的节点。 newNode 放置在 refNode 之后。 |

**退货：**
[Node](../../com.aspose.words/node) - 插入的节点。
### insertBefore(Node newChild, Node refChild) {#insertBefore-com.aspose.words.Node-com.aspose.words.Node-}
```
public Node insertBefore(Node newChild, Node refChild)
```


将指定节点插入到紧靠指定引用节点之前。

如果 refChild 为 null，则在子节点列表的末尾插入 newChild。

如果 newChild 已经在树中，则首先将其删除。

如果被插入的节点是从另一个文档创建的，你应该使用**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**将节点导入当前文档。然后可以将导入的节点插入到当前文档中。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | 要插入的节点。 |
| refChild | [Node](../../com.aspose.words/node) | 作为参考节点的节点。 newChild 放置在此节点之前。 |

**退货：**
[Node](../../com.aspose.words/node) - 插入的节点。
### isComposite() {#isComposite--}
```
public boolean isComposite()
```


返回 true，因为此节点可以有子节点。

**退货：**
boolean - True 因为这个节点可以有子节点。
### isDecorative() {#isDecorative--}
```
public boolean isDecorative()
```


获取指定形状在文档中是否为装饰性的标志。请注意，形状不为空[getAlternativeText()](../../com.aspose.words/shapebase\#getAlternativeText--) / [setAlternativeText(java.lang.String)](../../com.aspose.words/shapebase\#setAlternativeText-java.lang.String-)不能装饰。

**退货：**
boolean - 指定形状在文档中是否具有装饰性的标志。
### isDecorative(boolean value) {#isDecorative-boolean-}
```
public void isDecorative(boolean value)
```


设置指定形状在文档中是否具有装饰性的标志。请注意，形状不为空[getAlternativeText()](../../com.aspose.words/shapebase\#getAlternativeText--) / [setAlternativeText(java.lang.String)](../../com.aspose.words/shapebase\#setAlternativeText-java.lang.String-)不能装饰。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指定形状在文档中是否具有装饰性的标志。 |

### isDeleteRevision() {#isDeleteRevision--}
```
public boolean isDeleteRevision()
```


如果启用更改跟踪时此对象在 Microsoft Word 中被删除，则返回 true。

**退货：**
布尔值 - 如果在启用更改跟踪的情况下在 Microsoft Word 中删除了此对象，则为 True。
### isGroup() {#isGroup--}
```
public boolean isGroup()
```


如果这是一个组形状，则返回 true。

**退货：**
boolean - 如果这是一个组形状，则为真。
### isHorizontalRule() {#isHorizontalRule--}
```
public boolean isHorizontalRule()
```


如果此形状是水平规则，则返回 true。

**退货：**
boolean - 如果此形状是水平规则，则为真。
### isImage() {#isImage--}
```
public boolean isImage()
```


如果此形状是图像形状，则返回 true。

**退货：**
boolean - 如果此形状是图像形状，则为真。
### isInline() {#isInline--}
```
public boolean isInline()
```


一种快速确定此形状是否与文本内联的方法。

仅对顶级形状有效。

**退货：**
boolean - 相应的布尔值。
### isInsertRevision() {#isInsertRevision--}
```
public boolean isInsertRevision()
```


如果在启用更改跟踪时将此对象插入 Microsoft Word，则返回 true。

**退货：**
布尔值 - 如果在启用更改跟踪的情况下将此对象插入到 Microsoft Word 中，则为 True。
### isLayoutInCell() {#isLayoutInCell--}
```
public boolean isLayoutInCell()
```


获取一个标志，该标志指示形状是显示在表格内部还是表格外部。

默认值为**true**.

仅对顶级形状有效，该属性[getWrapType()](../../com.aspose.words/shapebase\#getWrapType--) / [setWrapType(int)](../../com.aspose.words/shapebase\#setWrapType-int-)其中的值设置为除[Inline](../../com.aspose.words/inline).

**退货：**
boolean - 指示形状是显示在表格内部还是表格外部的标志。
### isLayoutInCell(boolean value) {#isLayoutInCell-boolean-}
```
public void isLayoutInCell(boolean value)
```


设置一个标志，指示形状是显示在表格内部还是表格外部。

默认值为**true**.

仅对顶级形状有效，该属性[getWrapType()](../../com.aspose.words/shapebase\#getWrapType--) / [setWrapType(int)](../../com.aspose.words/shapebase\#setWrapType-int-)其中的值设置为除[Inline](../../com.aspose.words/inline).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示形状是显示在表格内部还是表格外部的标志。 |

### isMoveFromRevision() {#isMoveFromRevision--}
```
public boolean isMoveFromRevision()
```


退货**true**如果启用更改跟踪时此对象在 Microsoft Word 中被移动（删除）。

**退货：**
布尔值 -**true**如果启用更改跟踪时此对象在 Microsoft Word 中被移动（删除）。
### isMoveToRevision() {#isMoveToRevision--}
```
public boolean isMoveToRevision()
```


退货**true**如果启用更改跟踪时在 Microsoft Word 中移动（插入）此对象。

**退货：**
布尔值 -**true**如果启用更改跟踪时在 Microsoft Word 中移动（插入）此对象。
### isSignatureLine() {#isSignatureLine--}
```
public boolean isSignatureLine()
```


指示该形状是 SignatureLine。

**退货：**
boolean - 相应的布尔值。
### isTopLevel() {#isTopLevel--}
```
public boolean isTopLevel()
```


如果此形状不是组形状的子形状，则返回 true。

**退货：**
boolean - 如果此形状不是组形状的子项，则为 True。
### isWordArt() {#isWordArt--}
```
public boolean isWordArt()
```


如果此形状是艺术字对象，则返回 true。工作到 2007 兼容模式。在 2010 和更高版本的兼容模式下，艺术字只是一个带有精美字体的文本框。

**退货：**
boolean - 如果此形状是艺术字对象，则为 True。
### iterator() {#iterator--}
```
public Iterator iterator()
```


为该节点的子节点上的每个样式迭代提供支持。

**退货：**
java.util.迭代器
### localToParent(Point2D.Float value) {#localToParent-java.awt.geom.Point2D.Float-}
```
public Point2D.Float localToParent(Point2D.Float value)
```


将本地坐标空间中的值转换为父形状的坐标空间。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.geom.Point2D.Float |  |

**退货：**
java.awt.geom.Point2D.Float
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node-}
```
public Node nextPreOrder(Node rootNode)
```


根据前序树遍历算法获取下一个节点。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | 遍历的顶端节点（极限）。 |

**退货：**
[Node](../../com.aspose.words/node) - 预定顺序中的下一个节点。如果到达根节点则为空。
### nodeTypeToString(int nodeType) {#nodeTypeToString-int-}
```
public static String nodeTypeToString(int nodeType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| nodeType | int |  |

**退货：**
java.lang.字符串
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




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| style | int |  |
| variant | int |  |
| degree | double |  |

### patterned(int patternType) {#patterned-int-}
```
public void patterned(int patternType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| patternType | int |  |

### prependChild(Node newChild) {#prependChild-com.aspose.words.Node-}
```
public Node prependChild(Node newChild)
```


将指定节点添加到此节点的子节点列表的开头。

如果 newChild 已经在树中，则首先将其删除。

如果被插入的节点是从另一个文档创建的，你应该使用**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**将节点导入当前文档。然后可以将导入的节点插入到当前文档中。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | 要添加的节点。 |

**退货：**
[Node](../../com.aspose.words/node) - 添加的节点。
### presetTextured(int presetTexture) {#presetTextured-int-}
```
public void presetTextured(int presetTexture)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| presetTexture | int |  |

### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node-}
```
public Node previousPreOrder(Node rootNode)
```


根据前序树遍历算法获取上一个节点。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | 遍历的顶端节点（极限）。 |

**退货：**
[Node](../../com.aspose.words/node) 预购顺序中的前一个节点。如果到达根节点则为空。
### remove() {#remove--}
```
public void remove()
```


从父级中移除自身。

### removeAllChildren() {#removeAllChildren--}
```
public void removeAllChildren()
```


移除当前节点的所有子节点。

### removeChild(Node oldChild) {#removeChild-com.aspose.words.Node-}
```
public Node removeChild(Node oldChild)
```


删除指定的子节点。

删除节点后，oldChild 的父级设置为 null。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| oldChild | [Node](../../com.aspose.words/node) | 要删除的节点。 |

**退货：**
[Node](../../com.aspose.words/node) - 删除的节点。
### removeMoveRevisions() {#removeMoveRevisions--}
```
public void removeMoveRevisions()
```




### removeRunAttr(int key) {#removeRunAttr-int-}
```
public void removeRunAttr(int key)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

### removeShapeAttr(int key) {#removeShapeAttr-int-}
```
public void removeShapeAttr(int key)
```


保留供系统使用。 IShapeAttrSource。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

### removeSmartTags() {#removeSmartTags--}
```
public void removeSmartTags()
```


删除所有[SmartTag](../../com.aspose.words/smarttag)当前节点的后代节点。此方法不会删除智能标记的内容。

### selectNodes(String xpath) {#selectNodes-java.lang.String-}
```
public NodeList selectNodes(String xpath)
```


选择与 XPath 表达式匹配的节点列表。

目前仅支持带有元素名称的表达式。不支持使用属性名称的表达式。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xpath | java.lang.String | XPath 表达式。 |

**退货：**
[NodeList](../../com.aspose.words/nodelist) - 匹配 XPath 查询的节点列表。
### selectSingleNode(String xpath) {#selectSingleNode-java.lang.String-}
```
public Node selectSingleNode(String xpath)
```


选择与 XPath 表达式匹配的第一个节点。

目前仅支持带有元素名称的表达式。不支持使用属性名称的表达式。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xpath | java.lang.String | XPath 表达式。 |

**退货：**
[Node](../../com.aspose.words/node) - 与 XPath 查询匹配的第一个节点，如果未找到匹配节点，则为 null。
### setAllowOverlap(boolean value) {#setAllowOverlap-boolean-}
```
public void setAllowOverlap(boolean value)
```


设置一个值，该值指定此形状是否可以与其他形状重叠。

此属性会影响 Microsoft Word 中形状的行为。 Aspose.Words 忽略此属性的值。

此属性仅适用于顶级形状。

默认值为**true**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指定此形状是否可以与其他形状重叠的值。 |

### setAlternativeText(String value) {#setAlternativeText-java.lang.String-}
```
public void setAlternativeText(String value)
```


定义要显示的替代文本而不是图形。

默认值为空字符串。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setAnchorLocked(boolean value) {#setAnchorLocked-boolean-}
```
public void setAnchorLocked(boolean value)
```


指定形状的锚点是否被锁定。

默认值为**false**.

仅对顶级形状有效。

此属性会影响 Microsoft Word 中形状锚点的行为。当锚点未锁定时，在 Microsoft Word 中移动形状也可以移动形状的锚点。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setAspectRatioLocked(boolean value) {#setAspectRatioLocked-boolean-}
```
public void setAspectRatioLocked(boolean value)
```


指定形状的纵横比是否被锁定。

默认值取决于[getShapeType()](../../com.aspose.words/shapebase\#getShapeType--) 对于 ShapeType.Image 它是**true**但对于其他形状类型，它是**false**.

仅对顶级形状有效。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setBehindText(boolean value) {#setBehindText-boolean-}
```
public void setBehindText(boolean value)
```


指定形状是低于还是高于文本。

仅对顶级形状有效。

默认值为**false**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setBounds(Rectangle2D.Float value) {#setBounds-java.awt.geom.Rectangle2D.Float-}
```
public void setBounds(Rectangle2D.Float value)
```


设置形状包含块的位置和大小。设置时忽略纵横比锁定。

对于顶级形状，该值以点为单位并且相对于形状锚点。

对于组中的形状，该值位于父组的坐标空间和单位中。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.geom.Rectangle2D.Float | 形状包含块的位置和大小。 |

### setCoordOrigin(Point value) {#setCoordOrigin-java.awt.Point-}
```
public void setCoordOrigin(Point value)
```


此形状的包含块左上角的坐标。

默认值为 (0,0)。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Point | 对应的java.awt.Point值。 |

### setCoordSize(Dimension value) {#setCoordSize-java.awt.Dimension-}
```
public void setCoordSize(Dimension value)
```


此形状的包含块内的坐标空间的宽度和高度。

默认值为 (1000, 1000)。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Dimension | 对应的java.awt.Dimension值。 |

### setCustomNodeId(int value) {#setCustomNodeId-int-}
```
public void setCustomNodeId(int value)
```


指定自定义节点标识符。

默认为零。

这个标识符可以任意设置和使用。例如，作为获取外部数据的密钥。

重要说明，指定的值不会保存到输出文件中，并且仅在节点生命周期内存在。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。 |

### setDashStyle(int value) {#setDashStyle-int-}
```
public void setDashStyle(int value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int |  |

### setDistanceBottom(double value) {#setDistanceBottom-double-}
```
public void setDistanceBottom(double value)
```


设置文档文本和形状底部边缘之间的距离（以磅为单位）。

默认值为 0。

仅对顶级形状有效。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 文档文本与形状底部边缘之间的距离（以磅为单位）。 |

### setDistanceLeft(double value) {#setDistanceLeft-double-}
```
public void setDistanceLeft(double value)
```


设置文档文本和形状左边缘之间的距离（以磅为单位）。

默认值为 1/8 英寸。

仅对顶级形状有效。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 文档文本与形状左边缘之间的距离（以磅为单位）。 |

### setDistanceRight(double value) {#setDistanceRight-double-}
```
public void setDistanceRight(double value)
```


设置文档文本和形状右边缘之间的距离（以磅为单位）。

默认值为 1/8 英寸。

仅对顶级形状有效。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 文档文本与形状右边缘之间的距离（以磅为单位）。 |

### setDistanceTop(double value) {#setDistanceTop-double-}
```
public void setDistanceTop(double value)
```


设置文档文本和形状上边缘之间的距离（以磅为单位）。

默认值为 0。

仅对顶级形状有效。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 文档文本与形状上边缘之间的距离（以磅为单位）。 |

### setEndArrowLength(int value) {#setEndArrowLength-int-}
```
public void setEndArrowLength(int value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int |  |

### setEndArrowType(int value) {#setEndArrowType-int-}
```
public void setEndArrowType(int value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int |  |

### setEndArrowWidth(int value) {#setEndArrowWidth-int-}
```
public void setEndArrowWidth(int value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int |  |

### setEndCap(int value) {#setEndCap-int-}
```
public void setEndCap(int value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int |  |

### setFillColor(Color value) {#setFillColor-java.awt.Color-}
```
public void setFillColor(Color value)
```


定义填充形状闭合路径的画笔颜色。

这是一个捷径[Fill.getColor()](../../com.aspose.words/fill\#getColor--) / [Fill.setColor(java.awt.Color)](../../com.aspose.words/fill\#setColor-java.awt.Color-)财产。

默认值为 。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color | 对应的 java.awt.Color 值。 |

### setFillableBackColor(Color value) {#setFillableBackColor-java.awt.Color-}
```
public void setFillableBackColor(Color value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color |  |

### setFillableForeColor(Color value) {#setFillableForeColor-java.awt.Color-}
```
public void setFillableForeColor(Color value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color |  |

### setFillableTransparency(double value) {#setFillableTransparency-double-}
```
public void setFillableTransparency(double value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double |  |

### setFillableVisible(boolean value) {#setFillableVisible-boolean-}
```
public void setFillableVisible(boolean value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean |  |

### setFilled(boolean value) {#setFilled-boolean-}
```
public void setFilled(boolean value)
```


确定是否填充形状的闭合路径。

这是一个捷径[Fill.getOn()](../../com.aspose.words/fill\#getOn--) / [Fill.setOn(boolean)](../../com.aspose.words/fill\#setOn-boolean-)财产。

默认值为**true**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setFilledColor(Color value) {#setFilledColor-java.awt.Color-}
```
public void setFilledColor(Color value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color |  |

### setFlipOrientation(int value) {#setFlipOrientation-int-}
```
public void setFlipOrientation(int value)
```


切换形状的方向。

默认值为[FlipOrientation.NONE](../../com.aspose.words/fliporientation\#NONE).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。该值必须是按位组合[FlipOrientation](../../com.aspose.words/fliporientation)常数。 |

### setGradientAngle(double value) {#setGradientAngle-double-}
```
public void setGradientAngle(double value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double |  |

### setHRef(String value) {#setHRef-java.lang.String-}
```
public void setHRef(String value)
```


设置形状的完整超链接地址。

默认值为空字符串。

以下是此属性的有效值示例：

完整 URI：https://www.aspose.com/。

完整文件名：C:\\\\我的文件\\\\销售报告.doc 。

相对 URI：../../../resource.txt 

相对文件名：..\\\\我的文件\\\\销售报告.doc 。

另一个文档中的书签：https://www.aspose.com/Products/Default.aspx\#套房 

本文档中的书签：\#BookmakName 。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 形状的完整超链接地址。 |

### setHeight(double value) {#setHeight-double-}
```
public void setHeight(double value)
```


设置形状包含块的高度。

对于顶级形状，该值以磅为单位。

对于组中的形状，该值位于父组的坐标空间和单位中。

默认值为 0。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 形状包含块的高度。 |

### setHorizontalAlignment(int value) {#setHorizontalAlignment-int-}
```
public void setHorizontalAlignment(int value)
```


指定形状如何水平放置。

默认值为[HorizontalAlignment.NONE](../../com.aspose.words/horizontalalignment\#NONE).

仅对顶级浮动形状有效。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。该值必须是其中之一[HorizontalAlignment](../../com.aspose.words/horizontalalignment)常数。 |

### setImage(byte[] imageBytes) {#setImage-byte---}
```
public void setImage(byte[] imageBytes)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| imageBytes | byte[] |  |

### setJoinStyle(int value) {#setJoinStyle-int-}
```
public void setJoinStyle(int value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int |  |

### setLeft(double value) {#setLeft-double-}
```
public void setLeft(double value)
```


设置形状包含块左边缘的位置。

对于顶级形状，该值以点为单位并且相对于形状锚点。

对于组中的形状，该值位于父组的坐标空间和单位中。

默认值为 0。

仅对浮动形状有效。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 形状包含块左边缘的位置。 |

### setLineFillType(int value) {#setLineFillType-int-}
```
public void setLineFillType(int value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int |  |

### setLineStyle(int value) {#setLineStyle-int-}
```
public void setLineStyle(int value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int |  |

### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


设置可选的形状名称。

默认为空字符串。

不能为空，但可以是空字符串。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 可选的形状名称。 |

### setOn(boolean value) {#setOn-boolean-}
```
public void setOn(boolean value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean |  |

### setOpacity(double value) {#setOpacity-double-}
```
public void setOpacity(double value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double |  |

### setRelativeHorizontalPosition(int value) {#setRelativeHorizontalPosition-int-}
```
public void setRelativeHorizontalPosition(int value)
```


指定相对于形状的水平位置。

默认值为[RelativeHorizontalPosition.COLUMN](../../com.aspose.words/relativehorizontalposition\#COLUMN).

仅对顶级浮动形状有效。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。该值必须是其中之一[RelativeHorizontalPosition](../../com.aspose.words/relativehorizontalposition)常数。 |

### setRelativeVerticalPosition(int value) {#setRelativeVerticalPosition-int-}
```
public void setRelativeVerticalPosition(int value)
```


指定相对于垂直放置的形状。

默认值为[RelativeVerticalPosition.PARAGRAPH](../../com.aspose.words/relativeverticalposition\#PARAGRAPH).

仅对顶级浮动形状有效。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。该值必须是其中之一[RelativeVerticalPosition](../../com.aspose.words/relativeverticalposition)常数。 |

### setRotateWithObject(boolean value) {#setRotateWithObject-boolean-}
```
public void setRotateWithObject(boolean value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean |  |

### setRotation(double value) {#setRotation-double-}
```
public void setRotation(double value)
```


定义形状旋转的角度（以度为单位）。正值对应顺时针旋转角度。

默认值为 0。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 对应的双精度值。 |

### setRunAttr(int fontAttr, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int fontAttr, Object value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontAttr | int |  |
| value | java.lang.Object |  |

### setScreenTip(String value) {#setScreenTip-java.lang.String-}
```
public void setScreenTip(String value)
```


定义当鼠标指针移到形状上时显示的文本。

默认值为空字符串。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setShapeAttr(int key, Object value) {#setShapeAttr-int-java.lang.Object-}
```
public void setShapeAttr(int key, Object value)
```


保留供系统使用。 IShapeAttrSource。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setStartArrowLength(int value) {#setStartArrowLength-int-}
```
public void setStartArrowLength(int value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int |  |

### setStartArrowType(int value) {#setStartArrowType-int-}
```
public void setStartArrowType(int value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int |  |

### setStartArrowWidth(int value) {#setStartArrowWidth-int-}
```
public void setStartArrowWidth(int value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int |  |

### setStrokeColor(Color value) {#setStrokeColor-java.awt.Color-}
```
public void setStrokeColor(Color value)
```


定义描边的颜色。

这是一个捷径[Stroke.getColor()](../../com.aspose.words/stroke\#getColor--) / [Stroke.setColor(java.awt.Color)](../../com.aspose.words/stroke\#setColor-java.awt.Color-)财产。

默认值为 。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color | 对应的 java.awt.Color 值。 |

### setStrokeTransparency(double value) {#setStrokeTransparency-double-}
```
public void setStrokeTransparency(double value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double |  |

### setStrokeVisible(boolean value) {#setStrokeVisible-boolean-}
```
public void setStrokeVisible(boolean value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean |  |

### setStrokeWeight(double value) {#setStrokeWeight-double-}
```
public void setStrokeWeight(double value)
```


以点为单位定义描边形状路径的画笔厚度。

这是一个捷径[Stroke.getWeight()](../../com.aspose.words/stroke\#getWeight--) / [Stroke.setWeight(double)](../../com.aspose.words/stroke\#setWeight-double-)财产。

默认值为 0.75。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 对应的双精度值。 |

### setStroked(boolean value) {#setStroked-boolean-}
```
public void setStroked(boolean value)
```


定义是否将描边路径。

这是一个捷径[Stroke.getOn()](../../com.aspose.words/stroke\#getOn--) / [Stroke.setOn(boolean)](../../com.aspose.words/stroke\#setOn-boolean-)财产。

默认值为**true**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setTarget(String value) {#setTarget-java.lang.String-}
```
public void setTarget(String value)
```


设置形状超链接的目标框架。

默认值为空字符串。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 形状超链接的目标框架。 |

### setTextureAlignment(int value) {#setTextureAlignment-int-}
```
public void setTextureAlignment(int value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int |  |

### setTitle(String value) {#setTitle-java.lang.String-}
```
public void setTitle(String value)
```


设置当前形状对象的标题（标题）。

默认为空字符串。

不能为空，但可以是空字符串。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 当前形状对象的标题（标题）。 |

### setTop(double value) {#setTop-double-}
```
public void setTop(double value)
```


设置形状包含块的上边缘位置。

对于顶级形状，该值以点为单位并且相对于形状锚点。

对于组中的形状，该值位于父组的坐标空间和单位中。

默认值为 0。

仅对浮动形状有效。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 形状包含块的上边缘位置。 |

### setVerticalAlignment(int value) {#setVerticalAlignment-int-}
```
public void setVerticalAlignment(int value)
```


指定形状的垂直放置方式。

默认值为[VerticalAlignment.NONE](../../com.aspose.words/verticalalignment\#NONE).

仅对顶级浮动形状有效。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。该值必须是其中之一[VerticalAlignment](../../com.aspose.words/verticalalignment)常数。 |

### setWeight(double value) {#setWeight-double-}
```
public void setWeight(double value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double |  |

### setWidth(double value) {#setWidth-double-}
```
public void setWidth(double value)
```


设置形状包含块的宽度。

对于顶级形状，该值以磅为单位。

对于组中的形状，该值位于父组的坐标空间和单位中。

默认值为 0。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 形状包含块的宽度。 |

### setWrapSide(int value) {#setWrapSide-int-}
```
public void setWrapSide(int value)
```


指定文本环绕形状的方式。

默认值为[WrapSide.BOTH](../../com.aspose.words/wrapside\#BOTH).

仅对顶级形状有效。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。该值必须是其中之一[WrapSide](../../com.aspose.words/wrapside)常数。 |

### setWrapType(int value) {#setWrapType-int-}
```
public void setWrapType(int value)
```


定义形状是内嵌的还是浮动的。对于浮动形状，定义形状周围文本的环绕模式。

默认值为[WrapType.NONE](../../com.aspose.words/wraptype\#NONE).

仅对顶级形状有效。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。该值必须是其中之一[WrapType](../../com.aspose.words/wraptype)常数。 |

### setZOrder(int value) {#setZOrder-int-}
```
public void setZOrder(int value)
```


确定重叠形状的显示顺序。

仅对顶级形状有效。

默认值为 0。

数字代表堆叠优先级。数字较大的形状将显示为与数字较小的形状重叠（在“前面”）。

重叠形状的顺序与页眉和文档正文中的形状无关。

组形状中子形状的显示顺序由它们在组形状中的顺序决定。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。 |

### setZOrder_IShape(int value) {#setZOrder-IShape-int-}
```
public void setZOrder_IShape(int value)
```




**参数：**

| 范围 | 类型 | 描述 |
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




**退货：**
java.lang.字符串
### toString(SaveOptions saveOptions) {#toString-com.aspose.words.SaveOptions-}
```
public String toString(SaveOptions saveOptions)
```


使用指定的保存选项将节点的内容导出为字符串。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions) | 指定控制节点保存方式的选项。 |

**退货：**
java.lang.String - 指定格式的节点内容。
### toString(int saveFormat) {#toString-int-}
```
public String toString(int saveFormat)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| saveFormat | int |  |

**退货：**
java.lang.字符串
### twoColorGradient(int style, int variant) {#twoColorGradient-int-int-}
```
public void twoColorGradient(int style, int variant)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| style | int |  |
| variant | int |  |

### updateSmartArtDrawing() {#updateSmartArtDrawing--}
```
public void updateSmartArtDrawing()
```


使用 Aspose.Words 的 SmartArt 冷渲染引擎更新 SmartArt 预渲染绘图。 Microsoft Word 生成预渲染绘图并将其与 SmartArt 对象一起保存。但是，如果文档是由其他应用程序保存的，则预渲染的 SmartArt 绘图可能会丢失或不正确。如果预渲染绘图可用，则 Aspose.Words 使用它来渲染 SmartArt 对象。如果预渲染的绘图丢失，那么 Aspose.Words 会使用它自己的 SmartArt 冷渲染引擎来渲染 SmartArt 对象。如果预渲染图不正确，则需要调用该方法调用SmartArt冷渲染引擎。

### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
