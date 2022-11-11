---
title: GroupShape
second_title: Aspose.Words for Java API 参考
description:表示文档中的一组形状。
type: docs
weight: 314
url: /zh/java/com.aspose.words/groupshape/
---

**遗产:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode), [com.aspose.words.ShapeBase](../../com.aspose.words/shapebase)
```
public class GroupShape extends ShapeBase
```

表示文档中的一组形状。

要了解更多信息，请访问**How to Add Group Shape into a Word Document**文档文章。

一个[GroupShape](../../com.aspose.words/groupshape)是一个复合节点，可以有[Shape](../../com.aspose.words/shape)和[GroupShape](../../com.aspose.words/groupshape)节点作为子节点。

每个[GroupShape](../../com.aspose.words/groupshape)为其子形状定义一个新的坐标系。坐标系是使用定义的[ShapeBase.getCoordSize()](../../com.aspose.words/shapebase\#getCoordSize--) / [ShapeBase.setCoordSize(java.awt.Dimension)](../../com.aspose.words/shapebase\#setCoordSize-java.awt.Dimension-)和[ShapeBase.getCoordOrigin()](../../com.aspose.words/shapebase\#getCoordOrigin--) / [ShapeBase.setCoordOrigin(java.awt.Point)](../../com.aspose.words/shapebase\#setCoordOrigin-java.awt.Point-)特性。
## 构造函数s

| 构造函数 | 描述 |
| --- | --- |
| [GroupShape(DocumentBase doc)](#GroupShape-com.aspose.words.DocumentBase-) | 创建一个新的组形状。 |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | 接受访客。 |
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
| [getAncestor(int ancestor类型)](#getAncestor-int-) |  |
| [getAncestor(班级 ancestor类型)](#getAncestor-java.lang.班级-) | 获取指定对象类型的第一个祖先。 |
| [getAnchorLocked()](#getAnchorLocked--) | 指定形状的锚点是否被锁定。 |
| [getAspectRatioLocked()](#getAspectRatioLocked--) | 指定形状的纵横比是否被锁定。 |
| [getBehindText()](#getBehindText--) | 指定形状是低于还是高于文本。 |
| [getBottom()](#getBottom--) | 获取形状包含块的底部边缘的位置。 |
| [getBounds()](#getBounds--) | 获取形状包含块的位置和大小。 |
| [getBoundsInPoints()](#getBoundsInPoints--) | 获取形状包含块的位置和大小，以点为单位，相对于最顶部形状的锚点。 |
| [getBoundsWithEffects()](#getBoundsWithEffects--) | 获取此形状对象在应用绘图效果后的最终范围。 |
| [getChild(int node类型, int index, boolean isDeep)](#getChild-int-int-boolean-) |  |
| [getChildNodes()](#getChildNodes--) | 获取此节点的所有直接子节点。 |
| [getChildNodes(int node类型, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [get班级()](#get班级--) |  |
| [getContainer()](#getContainer--) |  |
| [getCoordOrigin()](#getCoordOrigin--) | 此形状的包含块左上角的坐标。 |
| [getCoordSize()](#getCoordSize--) | 此形状的包含块内的坐标空间的宽度和高度。 |
| [getCount()](#getCount--) | 获取此节点的直接子节点数。 |
| [getCurrentNode()](#getCurrentNode--) |  |
| [getCustomNodeId()](#getCustomNodeId--) | 指定自定义节点标识符。 |
| [getDirectRunAttr(int fontAttr)](#getDirectRunAttr-int-) |  |
| [getDirectShapeAttr(int key)](#getDirectShapeAttr-int-) | 保留供系统使用。 |
| [getDistanceBottom()](#getDistanceBottom--) | 获取文档文本和形状底部边缘之间的距离（以磅为单位）。 |
| [getDistanceLeft()](#getDistanceLeft--) | 获取文档文本与形状左边缘之间的距离（以磅为单位）。 |
| [getDistanceRight()](#getDistanceRight--) | 获取文档文本和形状右边缘之间的距离（以磅为单位）。 |
| [getDistanceTop()](#getDistanceTop--) | 获取文档文本和形状上边缘之间的距离（以磅为单位）。 |
| [getDocument()](#getDocument--) | 获取该节点所属的文档。 |
| [getDocument_IInline()](#getDocument-IInline--) |  |
| [getFill()](#getFill--) | 获取形状的填充格式。 |
| [getFill类型()](#getFill类型--) |  |
| [getFillableBackColor()](#getFillableBackColor--) |  |
| [getFillableForeColor()](#getFillableForeColor--) |  |
| [getFillableImageBytes()](#getFillableImageBytes--) |  |
| [getFillableTransparency()](#getFillableTransparency--) |  |
| [getFillableVisible()](#getFillableVisible--) |  |
| [getFilledColor()](#getFilledColor--) |  |
| [getFirstChild()](#getFirstChild--) | 获取节点的第一个子节点。 |
| [getFlipOrientation()](#getFlipOrientation--) | 切换形状的方向。 |
| [getFont()](#getFont--) | 提供对此对象的字体格式的访问。 |
| [getGradientAngle()](#getGradientAngle--) |  |
| [getGradientStops()](#getGradientStops--) |  |
| [getGradientStyle()](#getGradientStyle--) |  |
| [getGradientVariant()](#getGradientVariant--) |  |
| [getHRef()](#getHRef--) | 获取形状的完整超链接地址。 |
| [getHeight()](#getHeight--) | 获取形状包含块的高度。 |
| [getHorizontalAlignment()](#getHorizontalAlignment--) | 指定形状如何水平放置。 |
| [getLastChild()](#getLastChild--) | 获取节点的最后一个子节点。 |
| [getLeft()](#getLeft--) | 获取形状包含块的左边缘的位置。 |
| [getMarkupLanguage()](#getMarkupLanguage--) | 获取用于此图形对象的 MarkupLanguage。 |
| [getName()](#getName--) | 获取可选的形状名称。 |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node-) |  |
| [getNextSibling()](#getNextSibling--) | 获取紧跟此节点的节点。 |
| [getNode类型()](#getNode类型--) | 退货[Node类型.GROUP\_SHAPE](../../com.aspose.words/nodetype\#GROUP-SHAPE). |
| [getOn()](#getOn--) |  |
| [getOpacity()](#getOpacity--) |  |
| [getParentNode()](#getParentNode--) | 获取此节点的直接父节点。 |
| [getParentParagraph()](#getParentParagraph--) | 返回直接父段落。 |
| [getParentParagraph_IInline()](#getParentParagraph-IInline--) |  |
| [getPattern类型()](#getPattern类型--) |  |
| [getPresetTexture()](#getPresetTexture--) |  |
| [getPreviousSibling()](#getPreviousSibling--) | 获取紧接在此节点之前的节点。 |
| [getRange()](#getRange--) | 返回一个**Range**表示包含在此节点中的文档部分的对象。 |
| [getRelativeHorizontalPosition()](#getRelativeHorizontalPosition--) | 指定相对于水平放置的形状。 |
| [getRelativeVerticalPosition()](#getRelativeVerticalPosition--) | 指定相对于形状垂直定位的位置。 |
| [getRight()](#getRight--) | 获取形状包含块的右边缘的位置。 |
| [getRotateWithObject()](#getRotateWithObject--) |  |
| [getRotation()](#getRotation--) | 定义形状旋转的角度（以度为单位）。 |
| [getScreenTip()](#getScreenTip--) | 定义当鼠标指针移到形状上时显示的文本。 |
| [getShadowFormat()](#getShadowFormat--) | 获取形状的阴影格式。 |
| [getShapeRenderer()](#getShapeRenderer--) | 创建并返回可用于将此形状渲染为图像的对象。 |
| [getShape类型()](#getShape类型--) | 获取形状类型。 |
| [getSizeInPoints()](#getSizeInPoints--) | 以点为单位获取形状的大小。 |
| [getTarget()](#getTarget--) | 获取形状超链接的目标框架。 |
| [getText()](#getText--) | 获取此节点及其所有子节点的文本。 |
| [getTextureAlignment()](#getTextureAlignment--) |  |
| [getTitle()](#getTitle--) | 获取当前形状对象的标题（标题）。 |
| [getTop()](#getTop--) | 获取形状包含块的上边缘的位置。 |
| [getVerticalAlignment()](#getVerticalAlignment--) | 指定形状垂直放置的方式。 |
| [getWidth()](#getWidth--) | 获取形状包含块的宽度。 |
| [getWrapSide()](#getWrapSide--) | 指定文本如何环绕形状。 |
| [getWrap类型()](#getWrap类型--) | 定义形状是内联的还是浮动的。 |
| [getZOrder()](#getZOrder--) | 确定重叠形状的显示顺序。 |
| [getZOrder_IShape()](#getZOrder-IShape--) |  |
| [hasChildNodes()](#hasChildNodes--) | 如果此节点有任何子节点，则返回 true。 |
| [hashCode()](#hashCode--) |  |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node-) | 返回子节点数组中指定子节点的索引。 |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node-) | 在指定的参考节点之后立即插入指定的节点。 |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node-) | 在指定的参考节点之前插入指定的节点。 |
| [isComposite()](#isComposite--) | 返回 true，因为此节点可以有子节点。 |
| [isDecorative()](#isDecorative--) | 获取指定形状在文档中是否具有装饰性的标志。 |
| [isDecorative(boolean value)](#isDecorative-boolean-) | 设置指定形状在文档中是否具有装饰性的标志。 |
| [isDeleteRevision()](#isDeleteRevision--) | 如果在启用更改跟踪时在 Microsoft Word 中删除了此对象，则返回 true。 |
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
| [iterator()](#iterator--) | 为在此节点的子节点上的每个样式迭代提供支持。 |
| [localToParent(Point2D.Float value)](#localToParent-java.awt.geom.Point2D.Float-) | 将本地坐标空间中的值转换为父形状的坐标空间。 |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node-) | 根据前序树遍历算法获取下一个节点。 |
| [node类型ToString(int node类型)](#node类型ToString-int-) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [oneColorGradient(int style, int variant, double degree)](#oneColorGradient-int-int-double-) |  |
| [patterned(int pattern类型)](#patterned-int-) |  |
| [prependChild(Node newChild)](#prependChild-com.aspose.words.Node-) | 将指定节点添加到此节点的子节点列表的开头。 |
| [presetTextured(int presetTexture)](#presetTextured-int-) |  |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node-) | 根据前序树遍历算法获取上一个节点。 |
| [remove()](#remove--) | 从父级中移除自身。 |
| [removeAllChildren()](#removeAllChildren--) | 移除当前节点的所有子节点。 |
| [removeChild(Node oldChild)](#removeChild-com.aspose.words.Node-) | 移除指定的子节点。 |
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
| [setDistanceBottom(double value)](#setDistanceBottom-double-) | 设置文档文本和形状底部边缘之间的距离（以磅为单位）。 |
| [setDistanceLeft(double value)](#setDistanceLeft-double-) | 设置文档文本和形状左边缘之间的距离（以磅为单位）。 |
| [setDistanceRight(double value)](#setDistanceRight-double-) | 设置文档文本和形状右边缘之间的距离（以磅为单位）。 |
| [setDistanceTop(double value)](#setDistanceTop-double-) | 设置文档文本和形状上边缘之间的距离（以磅为单位）。 |
| [setFillableBackColor(Color value)](#setFillableBackColor-java.awt.Color-) |  |
| [setFillableForeColor(Color value)](#setFillableForeColor-java.awt.Color-) |  |
| [setFillableTransparency(double value)](#setFillableTransparency-double-) |  |
| [setFillableVisible(boolean value)](#setFillableVisible-boolean-) |  |
| [setFilledColor(Color value)](#setFilledColor-java.awt.Color-) |  |
| [setFlipOrientation(int value)](#setFlipOrientation-int-) | 切换形状的方向。 |
| [setGradientAngle(double value)](#setGradientAngle-double-) |  |
| [setHRef(String value)](#setHRef-java.lang.String-) | 设置形状的完整超链接地址。 |
| [setHeight(double value)](#setHeight-double-) | 设置形状包含块的高度。 |
| [setHorizontalAlignment(int value)](#setHorizontalAlignment-int-) | 指定形状如何水平放置。 |
| [setImage(byte[] imageBytes)](#setImage-byte---) |  |
| [setLeft(double value)](#setLeft-double-) | 设置形状包含块的左边缘的位置。 |
| [setName(String value)](#setName-java.lang.String-) | 设置可选的形状名称。 |
| [setOn(boolean value)](#setOn-boolean-) |  |
| [setOpacity(double value)](#setOpacity-double-) |  |
| [setRelativeHorizontalPosition(int value)](#setRelativeHorizontalPosition-int-) | 指定相对于水平放置的形状。 |
| [setRelativeVerticalPosition(int value)](#setRelativeVerticalPosition-int-) | 指定相对于形状垂直定位的位置。 |
| [setRotateWithObject(boolean value)](#setRotateWithObject-boolean-) |  |
| [setRotation(double value)](#setRotation-double-) | 定义形状旋转的角度（以度为单位）。 |
| [setRunAttr(int fontAttr, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [setScreenTip(String value)](#setScreenTip-java.lang.String-) | 定义当鼠标指针移到形状上时显示的文本。 |
| [setShapeAttr(int key, Object value)](#setShapeAttr-int-java.lang.Object-) | 保留供系统使用。 |
| [setTarget(String value)](#setTarget-java.lang.String-) | 设置形状超链接的目标框架。 |
| [setTextureAlignment(int value)](#setTextureAlignment-int-) |  |
| [setTitle(String value)](#setTitle-java.lang.String-) | 设置当前形状对象的标题（标题）。 |
| [setTop(double value)](#setTop-double-) | 设置形状包含块的上边缘的位置。 |
| [setVerticalAlignment(int value)](#setVerticalAlignment-int-) | 指定形状垂直放置的方式。 |
| [setWidth(double value)](#setWidth-double-) | 设置形状包含块的宽度。 |
| [setWrapSide(int value)](#setWrapSide-int-) | 指定文本如何环绕形状。 |
| [setWrap类型(int value)](#setWrap类型-int-) | 定义形状是内联的还是浮动的。 |
| [setZOrder(int value)](#setZOrder-int-) | 确定重叠形状的显示顺序。 |
| [setZOrder_IShape(int value)](#setZOrder-IShape-int-) |  |
| [solid()](#solid--) |  |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | 使用指定的保存选项将节点的内容导出为字符串。 |
| [toString(int saveFormat)](#toString-int-) |  |
| [twoColorGradient(int style, int variant)](#twoColorGradient-int-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### GroupShape(DocumentBase doc) {#GroupShape-com.aspose.words.DocumentBase-}
```
public GroupShape(DocumentBase doc)
```


创建一个新的组形状。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) | 所有者文件。

默认情况下，形状是浮动的，并且具有默认位置和大小。

您应该在创建形状后指定所需的形状属性。|

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public boolean accept(DocumentVisitor visitor)
```


接受访客。

枚举此节点及其所有子节点。每个节点调用 DocumentVisitor 上的相应方法。

有关更多信息，请参阅访问者设计模式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | 将访问节点的访问者。 |

**退货:**
 boolean - 如果所有节点都被访问，则为真；如果 DocumentVisitor 在访问所有节点之前停止操作，则返回 false。来电[DocumentVisitor.visitGroupShapeStart(com.aspose.words.GroupShape)](../../com.aspose.words/documentvisitor\#visitGroupShapeStart-com.aspose.words.GroupShape-) ，然后调用[Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node\#accept-com.aspose.words.DocumentVisitor-)对于该组形状的所有子形状并调用[DocumentVisitor.visitGroupShapeEnd(com.aspose.words.GroupShape)](../../com.aspose.words/documentvisitor\#visitGroupShapeEnd-com.aspose.words.GroupShape-)在最后。
### adjustWithEffects(Rectangle2D.Float source) {#adjustWithEffects-java.awt.geom.Rectangle2D.Float-}
```
public Rectangle2D.Float adjustWithEffects(Rectangle2D.Float source)
```


添加到效果范围的源矩形值并返回最终矩形。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| source | java.awt.geom.Rectangle2D.Float |  |

**退货:**
java.awt.geom.Rectangle2D.Float
### appendChild(Node newChild) {#appendChild-com.aspose.words.Node-}
```
public Node appendChild(Node newChild)
```


将指定节点添加到此节点的子节点列表的末尾。

如果 newChild 已经在树中，则首先将其移除。

如果要插入的节点是从另一个文档创建的，您应该使用**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**将节点导入当前文档。然后可以将导入的节点插入到当前文档中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | 要添加的节点。 |

**退货:**
[Node](../../com.aspose.words/node) - 添加的节点。
### canHaveImage() {#canHaveImage--}
```
public boolean canHaveImage()
```


如果形状类型允许形状具有图像，则返回 true。

尽管 Microsoft Word 有一种特殊的图像形状类型，但似乎在 Microsoft Word 文档中，除了组形状之外的任何形状都可以有图像，因此对于所有形状，除了[GroupShape](../../com.aspose.words/groupshape).

**退货:**
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

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| isCloneChildren | boolean | True 递归克隆指定节点下的子树； false 仅克隆节点本身。 |

**退货:**
[Node](../../com.aspose.words/node) - 克隆的节点。
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
布尔值
### fetchInheritedRunAttr(int fontAttr) {#fetchInheritedRunAttr-int-}
```
public Object fetchInheritedRunAttr(int fontAttr)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontAttr | int |  |

**退货:**
java.lang.Object
### fetchInheritedShapeAttr(int key) {#fetchInheritedShapeAttr-int-}
```
public Object fetchInheritedShapeAttr(int key)
```


保留供系统使用。 IShapeAttrSource。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### fetchShapeAttr(int key) {#fetchShapeAttr-int-}
```
public Object fetchShapeAttr(int key)
```


保留供系统使用。 IShapeAttrSource。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### getAllowOverlap() {#getAllowOverlap--}
```
public boolean getAllowOverlap()
```


获取一个值，该值指定此形状是否可以与其他形状重叠。

此属性会影响 Microsoft Word 中形状的行为。 Aspose.Words 忽略此属性的值。

此属性仅适用于顶级形状。

默认值为**true**.

**退货:**
boolean - 指定此形状是否可以与其他形状重叠的值。
### getAlternativeText() {#getAlternativeText--}
```
public String getAlternativeText()
```


定义要显示的替代文本而不是图形。

默认值为空字符串。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getAncestor(int ancestor类型) {#getAncestor-int-}
```
public CompositeNode getAncestor(int ancestor类型)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| ancestor类型 | int |  |

**退货:**
[CompositeNode](../../com.aspose.words/compositenode)
### getAncestor(班级 ancestor类型) {#getAncestor-java.lang.班级-}
```
public CompositeNode getAncestor(班级 ancestor类型)
```


获取指定对象类型的第一个祖先。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| ancestor类型 | java.lang.班级 | 要检索的祖先的对象类型。 |

**退货:**
[CompositeNode](../../com.aspose.words/compositenode) - 指定类型的祖先，如果没有找到该类型的祖先，则返回 null。

如果祖先类型等于祖先类型或从祖先类型派生，则祖先类型匹配。
### getAnchorLocked() {#getAnchorLocked--}
```
public boolean getAnchorLocked()
```


指定形状的锚点是否被锁定。

默认值为**false**.

仅对顶级形状有效。

此属性会影响 Microsoft Word 中形状锚点的行为。当锚点未锁定时，在 Microsoft Word 中移动形状也可以移动形状的锚点。

**退货:**
boolean - 对应的布尔值。
### getAspectRatioLocked() {#getAspectRatioLocked--}
```
public boolean getAspectRatioLocked()
```


指定形状的纵横比是否被锁定。

默认值取决于[getShape类型()](../../com.aspose.words/shapebase\#getShape类型--) 对于 Shape类型.Image 它是**true**但对于其他形状类型，它是**false**.

仅对顶级形状有效。

**退货:**
boolean - 对应的布尔值。
### getBehindText() {#getBehindText--}
```
public boolean getBehindText()
```


指定形状是低于还是高于文本。

仅对顶级形状有效。

默认值为**false**.

**退货:**
boolean - 对应的布尔值。
### getBottom() {#getBottom--}
```
public double getBottom()
```


获取形状包含块的底部边缘的位置。

对于顶级形状，该值以点为单位并且相对于形状锚点。

对于组中的形状，该值位于父组的坐标空间和单位中。

**退货:**
double - 形状包含块的底部边缘的位置。
### getBounds() {#getBounds--}
```
public Rectangle2D.Float getBounds()
```


获取形状包含块的位置和大小。设置时忽略纵横比锁定。

对于顶级形状，该值以点为单位并且相对于形状锚点。

对于组中的形状，该值位于父组的坐标空间和单位中。

**退货:**
java.awt.geom.Rectangle2D.Float - 形状包含块的位置和大小。
### getBoundsInPoints() {#getBoundsInPoints--}
```
public Rectangle2D.Float getBoundsInPoints()
```


获取形状包含块的位置和大小，以点为单位，相对于最顶部形状的锚点。

**退货:**
java.awt.geom.Rectangle2D.Float - 形状包含块的位置和大小，以点为单位，相对于最顶部形状的锚点。
### getBoundsWithEffects() {#getBoundsWithEffects--}
```
public Rectangle2D.Float getBoundsWithEffects()
```


获取此形状对象在应用绘图效果后的最终范围。价值以点为单位。

**退货:**
java.awt.geom.Rectangle2D.Float - 此形状对象在应用绘图效果后的最终范围。
### getChild(int node类型, int index, boolean isDeep) {#getChild-int-int-boolean-}
```
public Node getChild(int node类型, int index, boolean isDeep)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| node类型 | int |  |
| index | int |  |
| isDeep | boolean |  |

**退货:**
[Node](../../com.aspose.words/node)
### getChildNodes() {#getChildNodes--}
```
public NodeCollection getChildNodes()
```


获取此节点的所有直接子节点。

笔记，[getChildNodes()](../../com.aspose.words/compositenode\#getChildNodes--)相当于调用 GetChildNodes(Node类型.Any, false) 并在每次访问时创建并返回一个新集合。

如果没有子节点，则此属性返回一个空集合。

**退货:**
[NodeCollection](../../com.aspose.words/nodecollection) - 该节点的所有直接子节点。
### getChildNodes(int node类型, boolean isDeep) {#getChildNodes-int-boolean-}
```
public NodeCollection getChildNodes(int node类型, boolean isDeep)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| node类型 | int |  |
| isDeep | boolean |  |

**退货:**
[NodeCollection](../../com.aspose.words/nodecollection)
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getContainer() {#getContainer--}
```
public CompositeNode getContainer()
```




**退货:**
[CompositeNode](../../com.aspose.words/compositenode)
### getCoordOrigin() {#getCoordOrigin--}
```
public Point getCoordOrigin()
```


此形状的包含块左上角的坐标。

默认值为 (0,0)。

**退货:**
java.awt.Point - 对应的 java.awt.Point 值。
### getCoordSize() {#getCoordSize--}
```
public Dimension getCoordSize()
```


此形状的包含块内的坐标空间的宽度和高度。

默认值为 (1000, 1000)。

**退货:**
java.awt.Dimension - 对应的 java.awt.Dimension 值。
### getCount() {#getCount--}
```
public int getCount()
```


获取此节点的直接子节点数。

**退货:**
int - 此节点的直接子节点数。
### getCurrentNode() {#getCurrentNode--}
```
public Node getCurrentNode()
```




**退货:**
[Node](../../com.aspose.words/node)
### getCustomNodeId() {#getCustomNodeId--}
```
public int getCustomNodeId()
```


指定自定义节点标识符。

默认为零。

这个标识符可以任意设置和使用。例如，作为获取外部数据的键。

重要说明，指定的值不会保存到输出文件中，并且仅在节点生命周期内存在。

**退货:**
int - 对应的 int 值。
### getDirectRunAttr(int fontAttr) {#getDirectRunAttr-int-}
```
public Object getDirectRunAttr(int fontAttr)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontAttr | int |  |

**退货:**
java.lang.Object
### getDirectShapeAttr(int key) {#getDirectShapeAttr-int-}
```
public Object getDirectShapeAttr(int key)
```


保留供系统使用。 IShapeAttrSource。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### getDistanceBottom() {#getDistanceBottom--}
```
public double getDistanceBottom()
```


获取文档文本和形状底部边缘之间的距离（以磅为单位）。

默认值为 0。

仅对顶级形状有效。

**退货:**
double - 文档文本和形状底部边缘之间的距离（以磅为单位）。
### getDistanceLeft() {#getDistanceLeft--}
```
public double getDistanceLeft()
```


获取文档文本与形状左边缘之间的距离（以磅为单位）。

默认值为 1/8 英寸。

仅对顶级形状有效。

**退货:**
double - 文档文本与形状左边缘之间的距离（以磅为单位）。
### getDistanceRight() {#getDistanceRight--}
```
public double getDistanceRight()
```


获取文档文本和形状右边缘之间的距离（以磅为单位）。

默认值为 1/8 英寸。

仅对顶级形状有效。

**退货:**
double - 文档文本与形状右边缘之间的距离（以磅为单位）。
### getDistanceTop() {#getDistanceTop--}
```
public double getDistanceTop()
```


获取文档文本和形状上边缘之间的距离（以磅为单位）。

默认值为 0。

仅对顶级形状有效。

**退货:**
double - 文档文本和形状上边缘之间的距离（以磅为单位）。
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


获取该节点所属的文档。

该节点始终属于一个文档，即使它刚刚创建但尚未添加到树中，或者已从树中删除。

**退货:**
[DocumentBase](../../com.aspose.words/documentbase) - 该节点所属的文档。
### getDocument_IInline() {#getDocument-IInline--}
```
public DocumentBase getDocument_IInline()
```




**退货:**
[DocumentBase](../../com.aspose.words/documentbase)
### getFill() {#getFill--}
```
public Fill getFill()
```


获取形状的填充格式。

**退货:**
[Fill](../../com.aspose.words/fill) - 填充形状的格式。
### getFill类型() {#getFill类型--}
```
public int getFill类型()
```




**退货:**
整数
### getFillableBackColor() {#getFillableBackColor--}
```
public Color getFillableBackColor()
```




**退货:**
java.awt.颜色
### getFillableForeColor() {#getFillableForeColor--}
```
public Color getFillableForeColor()
```




**退货:**
java.awt.颜色
### getFillableImageBytes() {#getFillableImageBytes--}
```
public byte[] getFillableImageBytes()
```




**退货:**
字节[]
### getFillableTransparency() {#getFillableTransparency--}
```
public double getFillableTransparency()
```




**退货:**
双倍的
### getFillableVisible() {#getFillableVisible--}
```
public boolean getFillableVisible()
```




**退货:**
布尔值
### getFilledColor() {#getFilledColor--}
```
public Color getFilledColor()
```




**退货:**
java.awt.颜色
### getFirstChild() {#getFirstChild--}
```
public Node getFirstChild()
```


获取节点的第一个子节点。如果没有第一个子节点，则返回 null。

**退货:**
[Node](../../com.aspose.words/node) - 节点的第一个子节点。
### getFlipOrientation() {#getFlipOrientation--}
```
public int getFlipOrientation()
```


切换形状的方向。

默认值为[FlipOrientation.NONE](../../com.aspose.words/fliporientation\#NONE).

**退货:**
 int - 对应的 int 值。返回值是按位组合[FlipOrientation](../../com.aspose.words/fliporientation)常数。
### getFont() {#getFont--}
```
public Font getFont()
```


提供对此对象的字体格式的访问。

**退货:**
[Font](../../com.aspose.words/font) - 相应的[Font](../../com.aspose.words/font)价值。
### getGradientAngle() {#getGradientAngle--}
```
public double getGradientAngle()
```




**退货:**
双倍的
### getGradientStops() {#getGradientStops--}
```
public GradientStopCollection getGradientStops()
```




**退货:**
[GradientStopCollection](../../com.aspose.words/gradientstopcollection)
### getGradientStyle() {#getGradientStyle--}
```
public int getGradientStyle()
```




**退货:**
整数
### getGradientVariant() {#getGradientVariant--}
```
public int getGradientVariant()
```




**退货:**
整数
### getHRef() {#getHRef--}
```
public String getHRef()
```


获取形状的完整超链接地址。

默认值为空字符串。

以下是此属性的有效值示例：

完整的 URI： https://www.aspose.com/ 。

文件全名：C:\\\\我的文件\\\\销售报告.doc 。

相对 URI：../../../resource.txt 

相对文件名：..\\\\我的文件\\\\销售报告.doc 。

在另一个文档中添加书签：https://www.aspose.com/Products/Default.aspx\#套房 

本文档中的书签：\#BookmakName 。

**退货:**
java.lang.String - 形状的完整超链接地址。
### getHeight() {#getHeight--}
```
public double getHeight()
```


获取形状包含块的高度。

对于顶级形状，该值以磅为单位。

对于组中的形状，该值位于父组的坐标空间和单位中。

默认值为 0。

**退货:**
double - 形状包含块的高度。
### getHorizontalAlignment() {#getHorizontalAlignment--}
```
public int getHorizontalAlignment()
```


指定形状如何水平放置。

默认值为[HorizontalAlignment.NONE](../../com.aspose.words/horizontalalignment\#NONE).

仅对顶级浮动形状有效。

**退货:**
int - 对应的 int 值。返回值是以下之一[HorizontalAlignment](../../com.aspose.words/horizontalalignment)常数。
### getLastChild() {#getLastChild--}
```
public Node getLastChild()
```


获取节点的最后一个子节点。如果没有最后一个子节点，则返回 null。

**退货:**
[Node](../../com.aspose.words/node) - 节点的最后一个子节点。
### getLeft() {#getLeft--}
```
public double getLeft()
```


获取形状包含块的左边缘的位置。

对于顶级形状，该值以点为单位并且相对于形状锚点。

对于组中的形状，该值位于父组的坐标空间和单位中。

默认值为 0。

仅对浮动形状有效。

**退货:**
double - 形状包含块的左边缘的位置。
### getMarkupLanguage() {#getMarkupLanguage--}
```
public byte getMarkupLanguage()
```


获取用于此图形对象的 MarkupLanguage。

**退货:**
 byte - 用于此图形对象的 MarkupLanguage。返回值是以下之一[ShapeMarkupLanguage](../../com.aspose.words/shapemarkuplanguage)常数。
### getName() {#getName--}
```
public String getName()
```


获取可选的形状名称。

默认为空字符串。

不能为空，但可以是空字符串。

**退货:**
java.lang.String - 可选的形状名称。
### getNextMatchingNode(Node curNode) {#getNextMatchingNode-com.aspose.words.Node-}
```
public Node getNextMatchingNode(Node curNode)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node) |  |

**退货:**
[Node](../../com.aspose.words/node)
### getNextSibling() {#getNextSibling--}
```
public Node getNextSibling()
```


获取紧跟此节点的节点。如果没有下一个节点，则返回 null。

**退货:**
[Node](../../com.aspose.words/node) - 紧跟该节点的节点。
### getNode类型() {#getNode类型--}
```
public int getNode类型()
```


退货[Node类型.GROUP\_SHAPE](../../com.aspose.words/nodetype\#GROUP-SHAPE).

**退货:**
诠释 -\{[Node类型.GROUP\_SHAPE](../../com.aspose.words/nodetype\#GROUP-SHAPE) .返回值是以下之一[Node类型](../../com.aspose.words/nodetype)常数。
### getOn() {#getOn--}
```
public boolean getOn()
```




**退货:**
布尔值
### getOpacity() {#getOpacity--}
```
public double getOpacity()
```




**退货:**
双倍的
### getParentNode() {#getParentNode--}
```
public CompositeNode getParentNode()
```


获取此节点的直接父节点。

如果一个节点刚刚创建但尚未添加到树中，或者它已从树中删除，则父节点为空。

**退货:**
[CompositeNode](../../com.aspose.words/compositenode) - 该节点的直接父节点。
### getParentParagraph() {#getParentParagraph--}
```
public Paragraph getParentParagraph()
```


返回直接父段落。对于组形状的子形状和 Office Math 对象的子形状，始终返回 null。

**退货:**
[Paragraph](../../com.aspose.words/paragraph) - 直接父段落。
### getParentParagraph_IInline() {#getParentParagraph-IInline--}
```
public Paragraph getParentParagraph_IInline()
```




**退货:**
[Paragraph](../../com.aspose.words/paragraph)
### getPattern类型() {#getPattern类型--}
```
public int getPattern类型()
```




**退货:**
整数
### getPresetTexture() {#getPresetTexture--}
```
public int getPresetTexture()
```




**退货:**
整数
### getPreviousSibling() {#getPreviousSibling--}
```
public Node getPreviousSibling()
```


获取紧接在此节点之前的节点。如果没有前面的节点，则返回 null。

**退货:**
[Node](../../com.aspose.words/node) - 紧接在此节点之前的节点。
### getRange() {#getRange--}
```
public Range getRange()
```


返回一个**Range**表示包含在此节点中的文档部分的对象。

**退货:**
[Range](../../com.aspose.words/range) - 一个**Range**表示包含在此节点中的文档部分的对象。
### getRelativeHorizontalPosition() {#getRelativeHorizontalPosition--}
```
public int getRelativeHorizontalPosition()
```


指定相对于水平放置的形状。

默认值为[RelativeHorizontalPosition.COLUMN](../../com.aspose.words/relativehorizontalposition\#COLUMN).

仅对顶级浮动形状有效。

**退货:**
int - 对应的 int 值。返回值是以下之一[RelativeHorizontalPosition](../../com.aspose.words/relativehorizontalposition)常数。
### getRelativeVerticalPosition() {#getRelativeVerticalPosition--}
```
public int getRelativeVerticalPosition()
```


指定相对于形状垂直定位的位置。

默认值为[RelativeVerticalPosition.PARAGRAPH](../../com.aspose.words/relativeverticalposition\#PARAGRAPH).

仅对顶级浮动形状有效。

**退货:**
int - 对应的 int 值。返回值是以下之一[RelativeVerticalPosition](../../com.aspose.words/relativeverticalposition)常数。
### getRight() {#getRight--}
```
public double getRight()
```


获取形状包含块的右边缘的位置。

对于顶级形状，该值以点为单位并且相对于形状锚点。

对于组中的形状，该值位于父组的坐标空间和单位中。

**退货:**
double - 形状包含块的右边缘的位置。
### getRotateWithObject() {#getRotateWithObject--}
```
public boolean getRotateWithObject()
```




**退货:**
布尔值
### getRotation() {#getRotation--}
```
public double getRotation()
```


定义形状旋转的角度（以度为单位）。正值对应顺时针旋转角度。

默认值为 0。

**退货:**
double - 对应的双精度值。
### getScreenTip() {#getScreenTip--}
```
public String getScreenTip()
```


定义当鼠标指针移到形状上时显示的文本。

默认值为空字符串。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getShadowFormat() {#getShadowFormat--}
```
public ShadowFormat getShadowFormat()
```


获取形状的阴影格式。

**退货:**
[ShadowFormat](../../com.aspose.words/shadowformat) - 形状的阴影格式。
### getShapeRenderer() {#getShapeRenderer--}
```
public ShapeRenderer getShapeRenderer()
```


创建并返回可用于将此形状渲染为图像的对象。

这个方法只是调用[ShapeRenderer](../../com.aspose.words/shaperenderer)构造函数并将此对象作为参数传递。

**退货:**
[ShapeRenderer](../../com.aspose.words/shaperenderer) - 此形状的渲染器对象。
### getShape类型() {#getShape类型--}
```
public int getShape类型()
```


获取形状类型。

**退货:**
 int - 形状类型。返回值是以下之一[Shape类型](../../com.aspose.words/shapetype)常数。
### getSizeInPoints() {#getSizeInPoints--}
```
public Point2D.Float getSizeInPoints()
```


以点为单位获取形状的大小。以点为单位获取形状的大小。

 Point2D.Float 用作返回类型，因为我们在这里需要浮点尺寸值。应该假设 Point2D 的*x == width*和*y == height*.

**退货:**
java.awt.geom.Point2D.Float - 形状的大小（以磅为单位）。
### getTarget() {#getTarget--}
```
public String getTarget()
```


获取形状超链接的目标框架。

默认值为空字符串。

**退货:**
java.lang.String - 形状超链接的目标框架。
### getText() {#getText--}
```
public String getText()
```


获取此节点及其所有子节点的文本。

返回的字符串包括所有控制和特殊字符，如[ControlChar](../../com.aspose.words/controlchar).

**退货:**
java.lang.String
### getTextureAlignment() {#getTextureAlignment--}
```
public int getTextureAlignment()
```




**退货:**
整数
### getTitle() {#getTitle--}
```
public String getTitle()
```


获取当前形状对象的标题（标题）。

默认为空字符串。

不能为空，但可以是空字符串。

**退货:**
java.lang.String - 当前形状对象的标题（标题）。
### getTop() {#getTop--}
```
public double getTop()
```


获取形状包含块的上边缘的位置。

对于顶级形状，该值以点为单位并且相对于形状锚点。

对于组中的形状，该值位于父组的坐标空间和单位中。

默认值为 0。

仅对浮动形状有效。

**退货:**
double - 形状包含块的顶部边缘的位置。
### getVerticalAlignment() {#getVerticalAlignment--}
```
public int getVerticalAlignment()
```


指定形状垂直放置的方式。

默认值为[VerticalAlignment.NONE](../../com.aspose.words/verticalalignment\#NONE).

仅对顶级浮动形状有效。

**退货:**
int - 对应的 int 值。返回值是以下之一[VerticalAlignment](../../com.aspose.words/verticalalignment)常数。
### getWidth() {#getWidth--}
```
public double getWidth()
```


获取形状包含块的宽度。

对于顶级形状，该值以磅为单位。

对于组中的形状，该值位于父组的坐标空间和单位中。

默认值为 0。

**退货:**
double - 形状包含块的宽度。
### getWrapSide() {#getWrapSide--}
```
public int getWrapSide()
```


指定文本如何环绕形状。

默认值为[WrapSide.BOTH](../../com.aspose.words/wrapside\#BOTH).

仅对顶级形状有效。

**退货:**
int - 对应的 int 值。返回值是以下之一[WrapSide](../../com.aspose.words/wrapside)常数。
### getWrap类型() {#getWrap类型--}
```
public int getWrap类型()
```


定义形状是内联的还是浮动的。对于浮动形状，定义形状周围文本的环绕模式。

默认值为[Wrap类型.NONE](../../com.aspose.words/wraptype\#NONE).

仅对顶级形状有效。

**退货:**
int - 对应的 int 值。返回值是以下之一[Wrap类型](../../com.aspose.words/wraptype)常数。
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

**退货:**
int - 对应的 int 值。
### getZOrder_IShape() {#getZOrder-IShape--}
```
public int getZOrder_IShape()
```




**退货:**
整数
### hasChildNodes() {#hasChildNodes--}
```
public boolean hasChildNodes()
```


如果此节点有任何子节点，则返回 true。

**退货:**
boolean - 如果此节点有任何子节点，则为真。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### indexOf(Node child) {#indexOf-com.aspose.words.Node-}
```
public int indexOf(Node child)
```


返回子节点数组中指定子节点的索引。如果在子节点中未找到该节点，则返回 -1。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| child | [Node](../../com.aspose.words/node) |  |

**退货:**
整数
### insertAfter(Node newChild, Node refChild) {#insertAfter-com.aspose.words.Node-com.aspose.words.Node-}
```
public Node insertAfter(Node newChild, Node refChild)
```


在指定的参考节点之后立即插入指定的节点。

如果 refChild 为 null，则在子节点列表的开头插入 newChild。

如果 newChild 已经在树中，则首先将其移除。

如果要插入的节点是从另一个文档创建的，您应该使用**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**将节点导入当前文档。然后可以将导入的节点插入到当前文档中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | 要插入的节点。 |
| refChild | [Node](../../com.aspose.words/node) | 作为参考节点的节点。 newNode 放在 refNode 之后。 |

**退货:**
[Node](../../com.aspose.words/node) - 插入的节点。
### insertBefore(Node newChild, Node refChild) {#insertBefore-com.aspose.words.Node-com.aspose.words.Node-}
```
public Node insertBefore(Node newChild, Node refChild)
```


在指定的参考节点之前插入指定的节点。

如果 refChild 为 null，则在子节点列表的末尾插入 newChild。

如果 newChild 已经在树中，则首先将其移除。

如果要插入的节点是从另一个文档创建的，您应该使用**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**将节点导入当前文档。然后可以将导入的节点插入到当前文档中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | 要插入的节点。 |
| refChild | [Node](../../com.aspose.words/node) | 作为参考节点的节点。 newChild 放置在此节点之前。 |

**退货:**
[Node](../../com.aspose.words/node) - 插入的节点。
### isComposite() {#isComposite--}
```
public boolean isComposite()
```


返回 true，因为此节点可以有子节点。

**退货:**
boolean - True 因为这个节点可以有子节点。
### isDecorative() {#isDecorative--}
```
public boolean isDecorative()
```


获取指定形状在文档中是否具有装饰性的标志。请注意，形状不为空[getAlternativeText()](../../com.aspose.words/shapebase\#getAlternativeText--) / [setAlternativeText(java.lang.String)](../../com.aspose.words/shapebase\#setAlternativeText-java.lang.String-)不能装饰。

**退货:**
boolean - 指定形状在文档中是否具有装饰性的标志。
### isDecorative(boolean value) {#isDecorative-boolean-}
```
public void isDecorative(boolean value)
```


设置指定形状在文档中是否具有装饰性的标志。请注意，形状不为空[getAlternativeText()](../../com.aspose.words/shapebase\#getAlternativeText--) / [setAlternativeText(java.lang.String)](../../com.aspose.words/shapebase\#setAlternativeText-java.lang.String-)不能装饰。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指定形状在文档中是否具有装饰性的标志。 |

### isDeleteRevision() {#isDeleteRevision--}
```
public boolean isDeleteRevision()
```


如果在启用更改跟踪时在 Microsoft Word 中删除了此对象，则返回 true。

**退货:**
boolean - 如果在启用更改跟踪时在 Microsoft Word 中删除了此对象，则为 True。
### isGroup() {#isGroup--}
```
public boolean isGroup()
```


如果这是一个组形状，则返回 true。

**退货:**
boolean - 如果这是一个组形状，则为真。
### isHorizontalRule() {#isHorizontalRule--}
```
public boolean isHorizontalRule()
```


如果此形状是水平规则，则返回 true。

**退货:**
boolean - 如果此形状是水平规则，则为真。
### isImage() {#isImage--}
```
public boolean isImage()
```


如果此形状是图像形状，则返回 true。

**退货:**
boolean - 如果此形状是图像形状，则为真。
### isInline() {#isInline--}
```
public boolean isInline()
```


一种快速确定此形状是否与文本内联的方法。

仅对顶级形状有效。

**退货:**
boolean - 对应的布尔值。
### isInsertRevision() {#isInsertRevision--}
```
public boolean isInsertRevision()
```


如果在启用更改跟踪时将此对象插入 Microsoft Word，则返回 true。

**退货:**
boolean - 如果在启用更改跟踪时将此对象插入 Microsoft Word，则为真。
### isLayoutInCell() {#isLayoutInCell--}
```
public boolean isLayoutInCell()
```


获取一个标志，该标志指示形状是显示在表格内部还是表格外部。

默认值为**true**.

仅对顶层形状有效，属性[getWrap类型()](../../com.aspose.words/shapebase\#getWrap类型--) / [setWrap类型(int)](../../com.aspose.words/shapebase\#setWrap类型-int-)其中设置为除[Inline](../../com.aspose.words/inline).

**退货:**
boolean - 指示形状是显示在表格内部还是表格外部的标志。
### isLayoutInCell(boolean value) {#isLayoutInCell-boolean-}
```
public void isLayoutInCell(boolean value)
```


设置一个标志，指示形状是显示在表格内部还是表格外部。

默认值为**true**.

仅对顶层形状有效，属性[getWrap类型()](../../com.aspose.words/shapebase\#getWrap类型--) / [setWrap类型(int)](../../com.aspose.words/shapebase\#setWrap类型-int-)其中设置为除[Inline](../../com.aspose.words/inline).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示形状是显示在表格内部还是表格外部的标志。 |

### isMoveFromRevision() {#isMoveFromRevision--}
```
public boolean isMoveFromRevision()
```


退货**true**如果启用更改跟踪时此对象在 Microsoft Word 中被移动（删除）。

**退货:**
布尔值 -**true**如果启用更改跟踪时此对象在 Microsoft Word 中被移动（删除）。
### isMoveToRevision() {#isMoveToRevision--}
```
public boolean isMoveToRevision()
```


退货**true**如果启用更改跟踪时在 Microsoft Word 中移动（插入）此对象。

**退货:**
布尔值 -**true**如果启用更改跟踪时在 Microsoft Word 中移动（插入）此对象。
### isSignatureLine() {#isSignatureLine--}
```
public boolean isSignatureLine()
```


指示该形状是 SignatureLine。

**退货:**
boolean - 对应的布尔值。
### isTopLevel() {#isTopLevel--}
```
public boolean isTopLevel()
```


如果此形状不是组形状的子形状，则返回 true。

**退货:**
boolean - 如果此形状不是组形状的子形状，则为真。
### isWordArt() {#isWordArt--}
```
public boolean isWordArt()
```


如果此形状是艺术字对象，则返回 true。工作到 2007 兼容模式。在 2010 和更高的兼容模式中，艺术字只是一个带有精美字体的文本框。

**退货:**
布尔值 - 如果此形状是艺术字对象，则为真。
### iterator() {#iterator--}
```
public Iterator iterator()
```


为在此节点的子节点上的每个样式迭代提供支持。

**退货:**
java.util.Iterator
### localToParent(Point2D.Float value) {#localToParent-java.awt.geom.Point2D.Float-}
```
public Point2D.Float localToParent(Point2D.Float value)
```


将本地坐标空间中的值转换为父形状的坐标空间。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.geom.Point2D.Float |  |

**退货:**
java.awt.geom.Point2D.Float
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node-}
```
public Node nextPreOrder(Node rootNode)
```


根据前序树遍历算法获取下一个节点。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | 遍历的顶部节点（极限）。 |

**退货:**
[Node](../../com.aspose.words/node) - 预购订单中的下一个节点。如果到达 rootNode，则为 Null。
### node类型ToString(int node类型) {#node类型ToString-int-}
```
public static String node类型ToString(int node类型)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| node类型 | int |  |

**退货:**
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




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| style | int |  |
| variant | int |  |
| degree | double |  |

### patterned(int pattern类型) {#patterned-int-}
```
public void patterned(int pattern类型)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pattern类型 | int |  |

### prependChild(Node newChild) {#prependChild-com.aspose.words.Node-}
```
public Node prependChild(Node newChild)
```


将指定节点添加到此节点的子节点列表的开头。

如果 newChild 已经在树中，则首先将其移除。

如果要插入的节点是从另一个文档创建的，您应该使用**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**将节点导入当前文档。然后可以将导入的节点插入到当前文档中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | 要添加的节点。 |

**退货:**
[Node](../../com.aspose.words/node) - 添加的节点。
### presetTextured(int presetTexture) {#presetTextured-int-}
```
public void presetTextured(int presetTexture)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| presetTexture | int |  |

### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node-}
```
public Node previousPreOrder(Node rootNode)
```


根据前序树遍历算法获取上一个节点。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | 遍历的顶部节点（极限）。 |

**退货:**
[Node](../../com.aspose.words/node) - 预购订单中的上一个节点。如果到达 rootNode，则为 Null。
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


移除指定的子节点。

删除节点后，oldChild 的父级设置为 null。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| oldChild | [Node](../../com.aspose.words/node) | 要移除的节点。 |

**退货:**
[Node](../../com.aspose.words/node) - 删除的节点。
### removeMoveRevisions() {#removeMoveRevisions--}
```
public void removeMoveRevisions()
```




### removeRunAttr(int key) {#removeRunAttr-int-}
```
public void removeRunAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

### removeShapeAttr(int key) {#removeShapeAttr-int-}
```
public void removeShapeAttr(int key)
```


保留供系统使用。 IShapeAttrSource。

**参数:**
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

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xpath | java.lang.String | XPath 表达式。 |

**退货:**
[NodeList](../../com.aspose.words/nodelist) - 与 XPath 查询匹配的节点列表。
### selectSingleNode(String xpath) {#selectSingleNode-java.lang.String-}
```
public Node selectSingleNode(String xpath)
```


选择与 XPath 表达式匹配的第一个节点。

目前仅支持带有元素名称的表达式。不支持使用属性名称的表达式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xpath | java.lang.String | XPath 表达式。 |

**退货:**
[Node](../../com.aspose.words/node) - 与 XPath 查询匹配的第一个节点，如果未找到匹配节点，则为 null。
### setAllowOverlap(boolean value) {#setAllowOverlap-boolean-}
```
public void setAllowOverlap(boolean value)
```


设置一个值，该值指定此形状是否可以与其他形状重叠。

此属性会影响 Microsoft Word 中形状的行为。 Aspose.Words 忽略此属性的值。

此属性仅适用于顶级形状。

默认值为**true**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个值，指定此形状是否可以与其他形状重叠。 |

### setAlternativeText(String value) {#setAlternativeText-java.lang.String-}
```
public void setAlternativeText(String value)
```


定义要显示的替代文本而不是图形。

默认值为空字符串。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setAnchorLocked(boolean value) {#setAnchorLocked-boolean-}
```
public void setAnchorLocked(boolean value)
```


指定形状的锚点是否被锁定。

默认值为**false**.

仅对顶级形状有效。

此属性会影响 Microsoft Word 中形状锚点的行为。当锚点未锁定时，在 Microsoft Word 中移动形状也可以移动形状的锚点。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setAspectRatioLocked(boolean value) {#setAspectRatioLocked-boolean-}
```
public void setAspectRatioLocked(boolean value)
```


指定形状的纵横比是否被锁定。

默认值取决于[getShape类型()](../../com.aspose.words/shapebase\#getShape类型--) 对于 Shape类型.Image 它是**true**但对于其他形状类型，它是**false**.

仅对顶级形状有效。

**参数:**
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

**参数:**
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

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.geom.Rectangle2D.Float | 形状的包含块的位置和大小。 |

### setCoordOrigin(Point value) {#setCoordOrigin-java.awt.Point-}
```
public void setCoordOrigin(Point value)
```


此形状的包含块左上角的坐标。

默认值为 (0,0)。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Point | 对应的 java.awt.Point 值。 |

### setCoordSize(Dimension value) {#setCoordSize-java.awt.Dimension-}
```
public void setCoordSize(Dimension value)
```


此形状的包含块内的坐标空间的宽度和高度。

默认值为 (1000, 1000)。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Dimension | 对应的 java.awt.Dimension 值。 |

### setCustomNodeId(int value) {#setCustomNodeId-int-}
```
public void setCustomNodeId(int value)
```


指定自定义节点标识符。

默认为零。

这个标识符可以任意设置和使用。例如，作为获取外部数据的键。

重要说明，指定的值不会保存到输出文件中，并且仅在节点生命周期内存在。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。 |

### setDistanceBottom(double value) {#setDistanceBottom-double-}
```
public void setDistanceBottom(double value)
```


设置文档文本和形状底部边缘之间的距离（以磅为单位）。

默认值为 0。

仅对顶级形状有效。

**参数:**
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

**参数:**
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

**参数:**
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

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 文档文本与形状上边缘之间的距离（以磅为单位）。 |

### setFillableBackColor(Color value) {#setFillableBackColor-java.awt.Color-}
```
public void setFillableBackColor(Color value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color |  |

### setFillableForeColor(Color value) {#setFillableForeColor-java.awt.Color-}
```
public void setFillableForeColor(Color value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color |  |

### setFillableTransparency(double value) {#setFillableTransparency-double-}
```
public void setFillableTransparency(double value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double |  |

### setFillableVisible(boolean value) {#setFillableVisible-boolean-}
```
public void setFillableVisible(boolean value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean |  |

### setFilledColor(Color value) {#setFilledColor-java.awt.Color-}
```
public void setFilledColor(Color value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color |  |

### setFlipOrientation(int value) {#setFlipOrientation-int-}
```
public void setFlipOrientation(int value)
```


切换形状的方向。

默认值为[FlipOrientation.NONE](../../com.aspose.words/fliporientation\#NONE).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是按位组合[FlipOrientation](../../com.aspose.words/fliporientation)常数。 |

### setGradientAngle(double value) {#setGradientAngle-double-}
```
public void setGradientAngle(double value)
```




**参数:**
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

完整的 URI： https://www.aspose.com/ 。

文件全名：C:\\\\我的文件\\\\销售报告.doc 。

相对 URI：../../../resource.txt 

相对文件名：..\\\\我的文件\\\\销售报告.doc 。

在另一个文档中添加书签：https://www.aspose.com/Products/Default.aspx\#套房 

本文档中的书签：\#BookmakName 。

**参数:**
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

**参数:**
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

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[HorizontalAlignment](../../com.aspose.words/horizontalalignment)常数。 |

### setImage(byte[] imageBytes) {#setImage-byte---}
```
public void setImage(byte[] imageBytes)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| imageBytes | byte[] |  |

### setLeft(double value) {#setLeft-double-}
```
public void setLeft(double value)
```


设置形状包含块的左边缘的位置。

对于顶级形状，该值以点为单位并且相对于形状锚点。

对于组中的形状，该值位于父组的坐标空间和单位中。

默认值为 0。

仅对浮动形状有效。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 形状的包含块的左边缘的位置。 |

### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


设置可选的形状名称。

默认为空字符串。

不能为空，但可以是空字符串。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 可选的形状名称。 |

### setOn(boolean value) {#setOn-boolean-}
```
public void setOn(boolean value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean |  |

### setOpacity(double value) {#setOpacity-double-}
```
public void setOpacity(double value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double |  |

### setRelativeHorizontalPosition(int value) {#setRelativeHorizontalPosition-int-}
```
public void setRelativeHorizontalPosition(int value)
```


指定相对于水平放置的形状。

默认值为[RelativeHorizontalPosition.COLUMN](../../com.aspose.words/relativehorizontalposition\#COLUMN).

仅对顶级浮动形状有效。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[RelativeHorizontalPosition](../../com.aspose.words/relativehorizontalposition)常数。 |

### setRelativeVerticalPosition(int value) {#setRelativeVerticalPosition-int-}
```
public void setRelativeVerticalPosition(int value)
```


指定相对于形状垂直定位的位置。

默认值为[RelativeVerticalPosition.PARAGRAPH](../../com.aspose.words/relativeverticalposition\#PARAGRAPH).

仅对顶级浮动形状有效。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[RelativeVerticalPosition](../../com.aspose.words/relativeverticalposition)常数。 |

### setRotateWithObject(boolean value) {#setRotateWithObject-boolean-}
```
public void setRotateWithObject(boolean value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean |  |

### setRotation(double value) {#setRotation-double-}
```
public void setRotation(double value)
```


定义形状旋转的角度（以度为单位）。正值对应顺时针旋转角度。

默认值为 0。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 对应的双精度值。 |

### setRunAttr(int fontAttr, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int fontAttr, Object value)
```




**参数:**
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

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setShapeAttr(int key, Object value) {#setShapeAttr-int-java.lang.Object-}
```
public void setShapeAttr(int key, Object value)
```


保留供系统使用。 IShapeAttrSource。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setTarget(String value) {#setTarget-java.lang.String-}
```
public void setTarget(String value)
```


设置形状超链接的目标框架。

默认值为空字符串。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 形状超链接的目标框架。 |

### setTextureAlignment(int value) {#setTextureAlignment-int-}
```
public void setTextureAlignment(int value)
```




**参数:**
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

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 当前形状对象的标题（标题）。 |

### setTop(double value) {#setTop-double-}
```
public void setTop(double value)
```


设置形状包含块的上边缘的位置。

对于顶级形状，该值以点为单位并且相对于形状锚点。

对于组中的形状，该值位于父组的坐标空间和单位中。

默认值为 0。

仅对浮动形状有效。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 形状包含块的上边缘的位置。 |

### setVerticalAlignment(int value) {#setVerticalAlignment-int-}
```
public void setVerticalAlignment(int value)
```


指定形状垂直放置的方式。

默认值为[VerticalAlignment.NONE](../../com.aspose.words/verticalalignment\#NONE).

仅对顶级浮动形状有效。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[VerticalAlignment](../../com.aspose.words/verticalalignment)常数。 |

### setWidth(double value) {#setWidth-double-}
```
public void setWidth(double value)
```


设置形状包含块的宽度。

对于顶级形状，该值以磅为单位。

对于组中的形状，该值位于父组的坐标空间和单位中。

默认值为 0。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 形状包含块的宽度。 |

### setWrapSide(int value) {#setWrapSide-int-}
```
public void setWrapSide(int value)
```


指定文本如何环绕形状。

默认值为[WrapSide.BOTH](../../com.aspose.words/wrapside\#BOTH).

仅对顶级形状有效。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[WrapSide](../../com.aspose.words/wrapside)常数。 |

### setWrap类型(int value) {#setWrap类型-int-}
```
public void setWrap类型(int value)
```


定义形状是内联的还是浮动的。对于浮动形状，定义形状周围文本的环绕模式。

默认值为[Wrap类型.NONE](../../com.aspose.words/wraptype\#NONE).

仅对顶级形状有效。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[Wrap类型](../../com.aspose.words/wraptype)常数。 |

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

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。 |

### setZOrder_IShape(int value) {#setZOrder-IShape-int-}
```
public void setZOrder_IShape(int value)
```




**参数:**
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




**退货:**
java.lang.String
### toString(SaveOptions saveOptions) {#toString-com.aspose.words.SaveOptions-}
```
public String toString(SaveOptions saveOptions)
```


使用指定的保存选项将节点的内容导出为字符串。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions) | 指定控制节点保存方式的选项。 |

**退货:**
java.lang.String - 指定格式的节点内容。
### toString(int saveFormat) {#toString-int-}
```
public String toString(int saveFormat)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| saveFormat | int |  |

**退货:**
java.lang.String
### twoColorGradient(int style, int variant) {#twoColorGradient-int-int-}
```
public void twoColorGradient(int style, int variant)
```




**参数:**
| 范围 | 类型 | 描述 |
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




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
