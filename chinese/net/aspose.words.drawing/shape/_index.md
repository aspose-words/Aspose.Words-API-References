---
title: Shape
second_title: Aspose.Words for .NET API 参考
description: 表示绘图层中的对象例如自选图形文本框自由格式OLE 对象ActiveX 控件或图片
type: docs
weight: 1080
url: /zh/net/aspose.words.drawing/shape/
---
## Shape class

表示绘图层中的对象，例如自选图形、文本框、自由格式、OLE 对象、ActiveX 控件或图片。

```csharp
public sealed class Shape : ShapeBase
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [Shape](shape)(DocumentBase, ShapeType) | 创建一个新的形状对象。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AllowOverlap](../../aspose.words.drawing/shapebase/allowoverlap) { get; set; } | 获取或设置一个值，该值指定此形状是否可以与其他形状重叠。 |
| [AlternativeText](../../aspose.words.drawing/shapebase/alternativetext) { get; set; } | 定义要显示的替代文本而不是图形。 |
| [AnchorLocked](../../aspose.words.drawing/shapebase/anchorlocked) { get; set; } | 指定形状的锚点是否被锁定。 |
| [AspectRatioLocked](../../aspose.words.drawing/shapebase/aspectratiolocked) { get; set; } | 指定形状的纵横比是否被锁定。 |
| [BehindText](../../aspose.words.drawing/shapebase/behindtext) { get; set; } | 指定形状是低于还是高于文本。 |
| [Bottom](../../aspose.words.drawing/shapebase/bottom) { get; } | 获取形状包含块的底边位置。 |
| [Bounds](../../aspose.words.drawing/shapebase/bounds) { get; set; } | 获取或设置形状包含块的位置和大小。 |
| [BoundsInPoints](../../aspose.words.drawing/shapebase/boundsinpoints) { get; } | 获取形状包含块的位置和大小，以点为单位，相对于最顶部形状的锚点。 |
| [BoundsWithEffects](../../aspose.words.drawing/shapebase/boundswitheffects) { get; } | 获取此形状对象在应用绘图效果后的最终范围。 值以点为单位。 |
| [CanHaveImage](../../aspose.words.drawing/shapebase/canhaveimage) { get; } | 如果形状类型允许形状具有图像，则返回 true。 |
| [Chart](../../aspose.words.drawing/shape/chart) { get; } | 如果此形状具有图表，则提供对图表属性的访问。 |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | 获取该节点的所有直接子节点。 |
| [CoordOrigin](../../aspose.words.drawing/shapebase/coordorigin) { get; set; } | 此形状的包含块左上角的坐标。 |
| [CoordSize](../../aspose.words.drawing/shapebase/coordsize) { get; set; } | 此形状的包含块内坐标空间的宽度和高度。 |
| [Count](../../aspose.words/compositenode/count) { get; } | 获取此节点的直接子节点数。 |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | 指定自定义节点标识符。 |
| [DistanceBottom](../../aspose.words.drawing/shapebase/distancebottom) { get; set; } | 返回或设置文档文本和形状底部边缘之间的距离（以磅为单位）。 |
| [DistanceLeft](../../aspose.words.drawing/shapebase/distanceleft) { get; set; } | 返回或设置文档文本与形状左边缘之间的距离（以磅为单位）。 |
| [DistanceRight](../../aspose.words.drawing/shapebase/distanceright) { get; set; } | 返回或设置文档文本和形状右边缘之间的距离（以磅为单位）。 |
| [DistanceTop](../../aspose.words.drawing/shapebase/distancetop) { get; set; } | 返回或设置文档文本和形状上边缘之间的距离（以磅为单位）。 |
| virtual [Document](../../aspose.words/node/document) { get; } | 获取该节点所属的文档。 |
| [ExtrusionEnabled](../../aspose.words.drawing/shape/extrusionenabled) { get; } | 如果启用了挤压效果，则返回 true。 |
| [Fill](../../aspose.words.drawing/shapebase/fill) { get; } | 获取形状的填充格式。 |
| [FillColor](../../aspose.words.drawing/shape/fillcolor) { get; set; } | 定义填充形状闭合路径的画笔颜色。 |
| [Filled](../../aspose.words.drawing/shape/filled) { get; set; } | 确定是否填充形状的闭合路径。 |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | 获取节点的第一个子节点。 |
| [FirstParagraph](../../aspose.words.drawing/shape/firstparagraph) { get; } | 获取形状中的第一段。 |
| [FlipOrientation](../../aspose.words.drawing/shapebase/fliporientation) { get; set; } | 切换形状的方向。 |
| [Font](../../aspose.words.drawing/shapebase/font) { get; } | 提供对该对象的字体格式的访问。 |
| [HasChart](../../aspose.words.drawing/shape/haschart) { get; } | 如果此 Shape 有[`Chart`](./chart)则返回 true。 |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | 如果此节点有任何子节点，则返回 true。 |
| [HasImage](../../aspose.words.drawing/shape/hasimage) { get; } | 如果形状具有图像字节或链接图像，则返回 true。 |
| [HasSmartArt](../../aspose.words.drawing/shape/hassmartart) { get; } | 如果此 Shape 具有 SmartArt 对象，则返回 true。 |
| [Height](../../aspose.words.drawing/shapebase/height) { get; set; } | 获取或设置形状包含块的高度。 |
| [HorizontalAlignment](../../aspose.words.drawing/shapebase/horizontalalignment) { get; set; } | 指定形状如何水平放置。 |
| [HorizontalRuleFormat](../../aspose.words.drawing/shape/horizontalruleformat) { get; } | 提供对水平规则形状属性的访问。 对于不是水平规则的形状，返回 null。 |
| [HRef](../../aspose.words.drawing/shapebase/href) { get; set; } | 获取或设置形状的完整超链接地址。 |
| [ImageData](../../aspose.words.drawing/shape/imagedata) { get; } | 提供对形状图像的访问。 如果形状不能有图像，则返回 null。 |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | 返回真，因为该节点可以有子节点。 |
| [IsDecorative](../../aspose.words.drawing/shapebase/isdecorative) { get; set; } | 获取或设置指定形状在文档中是否具有装饰性的标志。 |
| [IsDeleteRevision](../../aspose.words.drawing/shapebase/isdeleterevision) { get; } | 如果在启用更改跟踪时在 Microsoft Word 中删除了此对象，则返回 true。 |
| [IsGroup](../../aspose.words.drawing/shapebase/isgroup) { get; } | 如果这是一个组形状，则返回 true。 |
| [IsHorizontalRule](../../aspose.words.drawing/shapebase/ishorizontalrule) { get; } | 如果此形状是水平规则，则返回 true。 |
| [IsImage](../../aspose.words.drawing/shapebase/isimage) { get; } | 如果此形状是图像形状，则返回 true。 |
| [IsInline](../../aspose.words.drawing/shapebase/isinline) { get; } | 一种快速确定此形状是否与文本内联的方法。 |
| [IsInsertRevision](../../aspose.words.drawing/shapebase/isinsertrevision) { get; } | 如果在启用更改跟踪时将此对象插入 Microsoft Word，则返回 true。 |
| [IsLayoutInCell](../../aspose.words.drawing/shapebase/islayoutincell) { get; set; } | 获取或设置一个标志，指示形状是显示在表格内部还是表格外部。 |
| [IsMoveFromRevision](../../aspose.words.drawing/shapebase/ismovefromrevision) { get; } | 返回 **true** 如果在启用更改跟踪时在 Microsoft Word 中移动（删除）此对象。 |
| [IsMoveToRevision](../../aspose.words.drawing/shapebase/ismovetorevision) { get; } | 返回 **true** 如果此对象在 Microsoft Word 中被移动（插入）而启用更改跟踪。 |
| [IsSignatureLine](../../aspose.words.drawing/shapebase/issignatureline) { get; } | 表示 shape 是 SignatureLine。 |
| [IsTopLevel](../../aspose.words.drawing/shapebase/istoplevel) { get; } | 如果此形状不是组形状的子形状，则返回 true。 |
| [IsWordArt](../../aspose.words.drawing/shapebase/iswordart) { get; } | 如果此形状是艺术字对象，则返回 true。 |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | 获取节点的最后一个子节点。 |
| [LastParagraph](../../aspose.words.drawing/shape/lastparagraph) { get; } | 获取形状中的最后一段。 |
| [Left](../../aspose.words.drawing/shapebase/left) { get; set; } | 获取或设置形状包含块的左边缘位置。 |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage) { get; } | 获取用于此图形对象的 MarkupLanguage。 |
| [Name](../../aspose.words.drawing/shapebase/name) { get; set; } | 获取或设置可选的形状名称。 |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | 获取紧跟该节点的节点。 |
| override [NodeType](../../aspose.words.drawing/shape/nodetype) { get; } | 返回Shape。 |
| [OleFormat](../../aspose.words.drawing/shape/oleformat) { get; } | 提供对形状的 OLE 数据的访问。对于不是 OLE 对象或 ActiveX 控件的形状，返回 null。 |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | 获取此节点的直接父节点。 |
| [ParentParagraph](../../aspose.words.drawing/shapebase/parentparagraph) { get; } | 返回直接父段落。 |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | 获取紧接在此节点之前的节点。 |
| [Range](../../aspose.words/node/range) { get; } | 返回 **Range** 对象，该对象表示包含在此节点中的文档部分。 |
| [RelativeHorizontalPosition](../../aspose.words.drawing/shapebase/relativehorizontalposition) { get; set; } | 指定相对于水平放置的形状。 |
| [RelativeVerticalPosition](../../aspose.words.drawing/shapebase/relativeverticalposition) { get; set; } | 指定相对于垂直放置的形状。 |
| [Right](../../aspose.words.drawing/shapebase/right) { get; } | 获取形状包含块的右边缘位置。 |
| [Rotation](../../aspose.words.drawing/shapebase/rotation) { get; set; } | 定义形状旋转的角度（以度为单位）。 正值对应顺时针旋转角度。 |
| [ScreenTip](../../aspose.words.drawing/shapebase/screentip) { get; set; } | 定义当鼠标指针移到形状上时显示的文本。 |
| [ShadowEnabled](../../aspose.words.drawing/shape/shadowenabled) { get; } | 如果启用了阴影效果，则返回 true。 |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype) { get; } | 获取形状类型。 |
| [SignatureLine](../../aspose.words.drawing/shape/signatureline) { get; } | 如果形状是签名线，则获取[`SignatureLine`](./signatureline)对象。返回 **null** 否则。 |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints) { get; } | 获取形状的大小（以磅为单位）。 |
| [StoryType](../../aspose.words.drawing/shape/storytype) { get; } | 返回Textbox。 |
| [Stroke](../../aspose.words.drawing/shape/stroke) { get; } | 定义形状的笔触。 |
| [StrokeColor](../../aspose.words.drawing/shape/strokecolor) { get; set; } | 定义描边的颜色。 |
| [Stroked](../../aspose.words.drawing/shape/stroked) { get; set; } | 定义路径是否会被描边。 |
| [StrokeWeight](../../aspose.words.drawing/shape/strokeweight) { get; set; } | 以点为单位定义描边形状路径的画笔厚度。 |
| [Target](../../aspose.words.drawing/shapebase/target) { get; set; } | 获取或设置形状超链接的目标框架。 |
| [TextBox](../../aspose.words.drawing/shape/textbox) { get; } | 定义指定文本如何在形状中显示的属性。 |
| [TextPath](../../aspose.words.drawing/shape/textpath) { get; } | 定义文本路径的文本（艺术字对象）。 |
| [Title](../../aspose.words.drawing/shapebase/title) { get; set; } | 获取或设置当前形状对象的标题（标题）。 |
| [Top](../../aspose.words.drawing/shapebase/top) { get; set; } | 获取或设置形状包含块的上边缘的位置。 |
| [VerticalAlignment](../../aspose.words.drawing/shapebase/verticalalignment) { get; set; } | 指定形状垂直放置的方式。 |
| [Width](../../aspose.words.drawing/shapebase/width) { get; set; } | 获取或设置形状包含块的宽度。 |
| [WrapSide](../../aspose.words.drawing/shapebase/wrapside) { get; set; } | 指定文本如何环绕形状。 |
| [WrapType](../../aspose.words.drawing/shapebase/wraptype) { get; set; } | 定义形状是内联的还是浮动的。对于浮动形状，定义形状周围文本的环绕模式。 |
| [ZOrder](../../aspose.words.drawing/shapebase/zorder) { get; set; } | 确定重叠形状的显示顺序。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words.drawing/shape/accept)(DocumentVisitor) | 接受访问者。 |
| [AdjustWithEffects](../../aspose.words.drawing/shapebase/adjustwitheffects)(RectangleF) | 添加到效果范围的源矩形值并返回最终矩形。 |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | 将指定节点添加到此节点的子节点列表的末尾。 |
| [Clone](../../aspose.words/node/clone)(bool) | 创建节点的副本。 |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | 保留供系统使用。 IXPath 可导航。 |
| [FetchInheritedShapeAttr](../../aspose.words.drawing/shapebase/fetchinheritedshapeattr)(int) | 保留供系统使用。 IShapeAttrSource。 |
| [FetchShapeAttr](../../aspose.words.drawing/shapebase/fetchshapeattr)(int) | 保留供系统使用。 IShapeAttrSource。 |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | 获取指定[`NodeType`](../../aspose.words/nodetype)的第一个祖先。 |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | 获取指定对象类型的第一个祖先。 |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | 返回匹配指定类型的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | 返回与指定类型匹配的子节点的实时集合。 |
| [GetDirectShapeAttr](../../aspose.words.drawing/shapebase/getdirectshapeattr)(int) | 保留供系统使用。 IShapeAttrSource。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | 为在此节点的子节点上的每个样式迭代提供支持。 |
| [GetShapeRenderer](../../aspose.words.drawing/shapebase/getshaperenderer)() | 创建并返回一个可用于将此形状渲染为图像的对象。 |
| override [GetText](../../aspose.words/compositenode/gettext)() | 获取该节点及其所有子节点的文本。 |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | 返回子节点数组中指定子节点的索引。 |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | 在指定参考节点之后立即插入指定节点。 |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | 在指定参考节点之前插入指定节点。 |
| [LocalToParent](../../aspose.words.drawing/shapebase/localtoparent)(PointF) | 将值从本地坐标空间转换为父形状的坐标空间。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | 根据前序树遍历算法获取下一个节点。 |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | 将指定节点添加到该节点的子节点列表的开头。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | 根据前序树遍历算法获取上一个节点。 |
| [Remove](../../aspose.words/node/remove)() | 从父级中移除自身。 |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | 移除当前节点的所有子节点。 |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | 移除指定的子节点。 |
| [RemoveShapeAttr](../../aspose.words.drawing/shapebase/removeshapeattr)(int) | 保留供系统使用。 IShapeAttrSource。 |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | 删除当前节点的所有[`SmartTag`](../../aspose.words.markup/smarttag)后代节点。 |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | 选择与 XPath 表达式匹配的节点列表。 |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | 选择与 XPath 表达式匹配的第一个节点。 |
| [SetShapeAttr](../../aspose.words.drawing/shapebase/setshapeattr)(int, object) | 保留供系统使用。 IShapeAttrSource。 |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | 使用指定的保存选项将节点的内容导出为字符串。 |
| [UpdateSmartArtDrawing](../../aspose.words.drawing/shape/updatesmartartdrawing)() | 使用 Aspose.Words 的 SmartArt 冷渲染引擎更新 SmartArt 预渲染绘图。 |

### 评论

使用[`Shape`](../shape)类，您可以在 Microsoft Word 文档中创建或修改形状。

形状的一个重要属性是它的[`ShapeType`](../shapebase/shapetype)。不同 类型的形状在 Word 文档中可以具有不同的功能。例如，只有图像和 OLE 形状 可以在其中包含图像。大多数形状都可以有文本，但不是全部。

可以包含文本的形状，可以包含[`Paragraph`](../../aspose.words/paragraph)和 [`Table`](../../aspose.words.tables/table)节点作为子节点。

### 例子

显示如何将浮动图像插入页面中心。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入两个形状以及一个包含另一个形状的组形状。
builder.InsertShape(ShapeType.Rectangle, 400, 200);
builder.InsertShape(ShapeType.Star, 300, 300);

GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 50, 200, 100);
group.CoordOrigin = new Point(-1000, -500);

Shape subShape = new Shape(doc, ShapeType.Cube);
subShape.Width = 500;
subShape.Height = 700;
subShape.Left = 0;
subShape.Top = 0;

group.AppendChild(subShape);
builder.InsertNode(group);

Assert.AreEqual(3, doc.GetChildNodes(NodeType.Shape, true).Count);
Assert.AreEqual(1, doc.GetChildNodes(NodeType.GroupShape, true).Count);

// 从文档中删除所有 Shape 节点。
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
shapes.Clear();

// 所有形状都消失了，但组形状仍在文档中。
Assert.AreEqual(1, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);

// 分别删除所有组形状。
NodeCollection groupShapes = doc.GetChildNodes(NodeType.GroupShape, true);
groupShapes.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

展示如何从文档中提取图像，并将它们作为单个文件保存到本地文件系统。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入两个形状以及一个包含另一个形状的组形状。
builder.InsertShape(ShapeType.Rectangle, 400, 200);
builder.InsertShape(ShapeType.Star, 300, 300);

GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 50, 200, 100);
group.CoordOrigin = new Point(-1000, -500);

Shape subShape = new Shape(doc, ShapeType.Cube);
subShape.Width = 500;
subShape.Height = 700;
subShape.Left = 0;
subShape.Top = 0;

group.AppendChild(subShape);
builder.InsertNode(group);

Assert.AreEqual(3, doc.GetChildNodes(NodeType.Shape, true).Count);
Assert.AreEqual(1, doc.GetChildNodes(NodeType.GroupShape, true).Count);

// 从文档中删除所有 Shape 节点。
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
shapes.Clear();

// 所有形状都消失了，但组形状仍在文档中。
Assert.AreEqual(1, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);

// 分别删除所有组形状。
NodeCollection groupShapes = doc.GetChildNodes(NodeType.GroupShape, true);
groupShapes.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

显示如何从文档中删除所有形状。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入两个形状以及一个包含另一个形状的组形状。
builder.InsertShape(ShapeType.Rectangle, 400, 200);
builder.InsertShape(ShapeType.Star, 300, 300);

GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 50, 200, 100);
group.CoordOrigin = new Point(-1000, -500);

Shape subShape = new Shape(doc, ShapeType.Cube);
subShape.Width = 500;
subShape.Height = 700;
subShape.Left = 0;
subShape.Top = 0;

group.AppendChild(subShape);
builder.InsertNode(group);

Assert.AreEqual(3, doc.GetChildNodes(NodeType.Shape, true).Count);
Assert.AreEqual(1, doc.GetChildNodes(NodeType.GroupShape, true).Count);

// 从文档中删除所有 Shape 节点。
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
shapes.Clear();

// 所有形状都消失了，但组形状仍在文档中。
Assert.AreEqual(1, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);

// 分别删除所有组形状。
NodeCollection groupShapes = doc.GetChildNodes(NodeType.GroupShape, true);
groupShapes.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### 也可以看看

* class [ShapeBase](../shapebase)
* namespace [Aspose.Words.Drawing](../../aspose.words.drawing)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
