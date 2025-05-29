---
title: Shape Class
linktitle: Shape
articleTitle: Shape
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.Shape 类，轻松在您的项目中创建多功能绘图对象，如自动图形、文本框和图像。
type: docs
weight: 1640
url: /zh/net/aspose.words.drawing/shape/
---
## Shape class

代表绘图层中的对象，例如自选图形、文本框、自由图形、OLE 对象、ActiveX 控件或图片。

要了解更多信息，请访问[使用形状](https://docs.aspose.com/words/net/working-with-shapes/)文档文章。

```csharp
public sealed class Shape : ShapeBase
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [Shape](shape/)(*[DocumentBase](../../aspose.words/documentbase/), [ShapeType](../shapetype/)*) | 创建一个新的形状对象。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Adjustments](../../aspose.words.drawing/shape/adjustments/) { get; } | 提供对形状的调整原始值的访问。 对于不包含任何调整原始值的形状，它将返回一个空集合。 |
| [AllowOverlap](../../aspose.words.drawing/shapebase/allowoverlap/) { get; set; } | 获取或设置一个值，指定此形状是否可以与其他形状重叠。 |
| [AlternativeText](../../aspose.words.drawing/shapebase/alternativetext/) { get; set; } | 定义要显示的替代图形的文本。 |
| [AnchorLocked](../../aspose.words.drawing/shapebase/anchorlocked/) { get; set; } | 指定形状的锚点是否被锁定。 |
| [AspectRatioLocked](../../aspose.words.drawing/shapebase/aspectratiolocked/) { get; set; } | 指定形状的纵横比是否被锁定。 |
| [BehindText](../../aspose.words.drawing/shapebase/behindtext/) { get; set; } | 指定形状位于文本下方还是上方。 |
| [Bottom](../../aspose.words.drawing/shapebase/bottom/) { get; } | 获取形状包含块底边的位置。 |
| [Bounds](../../aspose.words.drawing/shapebase/bounds/) { get; set; } | 获取或设置形状包含块的位置和大小。 |
| [BoundsInPoints](../../aspose.words.drawing/shapebase/boundsinpoints/) { get; } | 获取形状包含块的位置和大小（以点为单位），相对于最顶层形状的锚点。 |
| [BoundsWithEffects](../../aspose.words.drawing/shapebase/boundswitheffects/) { get; } | 获取此形状对象应用绘图效果后的最终范围。 值以点为单位。 |
| [CanHaveImage](../../aspose.words.drawing/shapebase/canhaveimage/) { get; } | 返回`真的`如果形状类型允许形状具有图像。 |
| [Chart](../../aspose.words.drawing/shape/chart/) { get; } | 如果此形状具有[`Chart`](../../aspose.words.drawing.charts/chart/). |
| [CoordOrigin](../../aspose.words.drawing/shapebase/coordorigin/) { get; set; } | 此形状包含块的左上角坐标。 |
| [CoordSize](../../aspose.words.drawing/shapebase/coordsize/) { get; set; } | 此形状的包含块内的坐标空间的宽度和高度。 |
| [Count](../../aspose.words/compositenode/count/) { get; } | 获取此节点的直属子节点的数量。 |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| [DistanceBottom](../../aspose.words.drawing/shapebase/distancebottom/) { get; set; } | 返回或设置文档文本和形状底边之间的距离（以点为单位）。 |
| [DistanceLeft](../../aspose.words.drawing/shapebase/distanceleft/) { get; set; } | 返回或设置文档文本和形状左边缘之间的距离（以点为单位）。 |
| [DistanceRight](../../aspose.words.drawing/shapebase/distanceright/) { get; set; } | 返回或设置文档文本和形状右边缘之间的距离（以点为单位）。 |
| [DistanceTop](../../aspose.words.drawing/shapebase/distancetop/) { get; set; } | 返回或设置文档文本和形状顶部边缘之间的距离（以点为单位）。 |
| virtual [Document](../../aspose.words/node/document/) { get; } | 获取此节点所属的文档。 |
| [ExtrusionEnabled](../../aspose.words.drawing/shape/extrusionenabled/) { get; } | 返回`真的`如果启用了挤压效果。 |
| [Fill](../../aspose.words.drawing/shapebase/fill/) { get; } | 获取形状的填充格式。 |
| [FillColor](../../aspose.words.drawing/shape/fillcolor/) { get; set; } | 定义填充形状闭合路径的画笔颜色。 |
| [Filled](../../aspose.words.drawing/shape/filled/) { get; set; } | 确定形状的封闭路径是否将被填充。 |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | 获取节点的第一个子节点。 |
| [FirstParagraph](../../aspose.words.drawing/shape/firstparagraph/) { get; } | 获取形状中的第一个段落。 |
| [FlipOrientation](../../aspose.words.drawing/shapebase/fliporientation/) { get; set; } | 切换形状的方向。 |
| [Font](../../aspose.words.drawing/shapebase/font/) { get; } | 提供对此对象的字体格式的访问。 |
| [Glow](../../aspose.words.drawing/shapebase/glow/) { get; } | 获取形状的发光格式。 |
| [HasChart](../../aspose.words.drawing/shape/haschart/) { get; } | 返回`真的`如果这个`Shape`有一个[`Chart`](../../aspose.words.drawing.charts/chart/). |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | 返回`真的`如果此节点有任何子节点。 |
| [HasImage](../../aspose.words.drawing/shape/hasimage/) { get; } | 返回`真的`如果形状有图像字节或链接图像。 |
| [HasSmartArt](../../aspose.words.drawing/shape/hassmartart/) { get; } | 返回`真的`如果这个`Shape`有一个 SmartArt 对象。 |
| [Height](../../aspose.words.drawing/shapebase/height/) { get; set; } | 获取或设置形状包含块的高度。 |
| [HeightRelative](../../aspose.words.drawing/shapebase/heightrelative/) { get; set; } | 获取或设置表示形状相对高度百分比的值。 |
| [Hidden](../../aspose.words.drawing/shapebase/hidden/) { get; set; } | 获取或设置一个布尔值，指示形状是否可见。 |
| [HorizontalAlignment](../../aspose.words.drawing/shapebase/horizontalalignment/) { get; set; } | 指定形状的水平定位方式。 |
| [HorizontalRuleFormat](../../aspose.words.drawing/shape/horizontalruleformat/) { get; } | 提供对水平规则形状属性的访问。 对于非水平规则的形状，返回`无效的`. |
| [HRef](../../aspose.words.drawing/shapebase/href/) { get; set; } | 获取或设置形状的完整超链接地址。 |
| [ImageData](../../aspose.words.drawing/shape/imagedata/) { get; } | 提供对形状图像的访问。 返回`无效的`如果形状不能有图像。 |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | 返回`真的`因为这个节点可以有子节点。 |
| [IsDecorative](../../aspose.words.drawing/shapebase/isdecorative/) { get; set; } | 获取或设置指定形状在文档中是否具有装饰性的标志。 |
| [IsDeleteRevision](../../aspose.words.drawing/shapebase/isdeleterevision/) { get; } | 如果在启用更改跟踪的情况下在 Microsoft Word 中删除了此对象，则返回 true。 |
| [IsGroup](../../aspose.words.drawing/shapebase/isgroup/) { get; } | 返回`真的`如果这是一个组形状。 |
| [IsHorizontalRule](../../aspose.words.drawing/shapebase/ishorizontalrule/) { get; } | 返回`真的`如果此形状是水平规则。 |
| [IsImage](../../aspose.words.drawing/shapebase/isimage/) { get; } | 返回`真的`如果此形状是图像形状。 |
| [IsInline](../../aspose.words.drawing/shapebase/isinline/) { get; } | 快速确定此形状是否与文本对齐。 |
| [IsInsertRevision](../../aspose.words.drawing/shapebase/isinsertrevision/) { get; } | 如果在启用更改跟踪的情况下将此对象插入 Microsoft Word，则返回 true。 |
| [IsLayoutInCell](../../aspose.words.drawing/shapebase/islayoutincell/) { get; set; } | 获取或设置一个标志，指示形状是显示在表格内部还是外部。 |
| [IsMoveFromRevision](../../aspose.words.drawing/shapebase/ismovefromrevision/) { get; } | 返回`真的`如果在启用更改跟踪的情况下在 Microsoft Word 中移动（删除）此对象。 |
| [IsMoveToRevision](../../aspose.words.drawing/shapebase/ismovetorevision/) { get; } | 返回`真的`如果在启用更改跟踪的情况下在 Microsoft Word 中移动（插入）此对象。 |
| [IsSignatureLine](../../aspose.words.drawing/shapebase/issignatureline/) { get; } | 表示形状是[`SignatureLine`](../signatureline/). |
| [IsTopLevel](../../aspose.words.drawing/shapebase/istoplevel/) { get; } | 返回`真的`如果此形状不是组形状的子形状。 |
| [IsWordArt](../../aspose.words.drawing/shapebase/iswordart/) { get; } | 返回`真的`如果此形状是艺术字对象。 |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | 获取节点的最后一个子节点。 |
| [LastParagraph](../../aspose.words.drawing/shape/lastparagraph/) { get; } | 获取形状中的最后一段。 |
| [Left](../../aspose.words.drawing/shapebase/left/) { get; set; } | 获取或设置形状包含块左边缘的位置。 |
| [LeftRelative](../../aspose.words.drawing/shapebase/leftrelative/) { get; set; } | 获取或设置表示形状相对左侧位置的百分比值。 |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage/) { get; } | 获取此图形对象使用的标记语言。 |
| [Name](../../aspose.words.drawing/shapebase/name/) { get; set; } | 获取或设置可选形状名称。 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧随此节点之后的节点。 |
| override [NodeType](../../aspose.words.drawing/shape/nodetype/) { get; } | 返回Shape. |
| [OleFormat](../../aspose.words.drawing/shape/oleformat/) { get; } | 提供对形状的 OLE 数据的访问。对于非 OLE 对象或 ActiveX 控件的形状，返回`无效的`. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [ParentParagraph](../../aspose.words.drawing/shapebase/parentparagraph/) { get; } | 返回直接父段落。 |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取此节点前一个节点。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回[`Range`](../../aspose.words/range/)表示此节点中包含的文档部分的对象。 |
| [Reflection](../../aspose.words.drawing/shapebase/reflection/) { get; } | 获取形状的反射格式。 |
| [RelativeHorizontalPosition](../../aspose.words.drawing/shapebase/relativehorizontalposition/) { get; set; } | 指定形状相对于水平方向的位置。 |
| [RelativeHorizontalSize](../../aspose.words.drawing/shapebase/relativehorizontalsize/) { get; set; } | 获取或设置形状在水平方向上的相对大小值。 |
| [RelativeVerticalPosition](../../aspose.words.drawing/shapebase/relativeverticalposition/) { get; set; } | 指定形状的垂直定位。 |
| [RelativeVerticalSize](../../aspose.words.drawing/shapebase/relativeverticalsize/) { get; set; } | 获取或设置形状在垂直方向上的相对大小值。 |
| [Right](../../aspose.words.drawing/shapebase/right/) { get; } | 获取形状包含块右边缘的位置。 |
| [Rotation](../../aspose.words.drawing/shapebase/rotation/) { get; set; } | 定义形状旋转的角度（以度为单位）。 正值对应顺时针旋转角度。 |
| [ScreenTip](../../aspose.words.drawing/shapebase/screentip/) { get; set; } | 定义鼠标指针移到形状上时显示的文本。 |
| [ShadowEnabled](../../aspose.words.drawing/shape/shadowenabled/) { get; } | 返回`真的`如果启用了阴影效果。 |
| [ShadowFormat](../../aspose.words.drawing/shapebase/shadowformat/) { get; } | 获取形状的阴影格式。 |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype/) { get; } | 获取形状类型。 |
| [SignatureLine](../../aspose.words.drawing/shape/signatureline/) { get; } | 获取[`SignatureLine`](../signatureline/)如果形状是签名线，则返回对象。返回`无效的`否则。 |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints/) { get; } | 获取形状的大小（以点为单位）。 |
| [SoftEdge](../../aspose.words.drawing/shapebase/softedge/) { get; } | 获取形状的软边缘格式。 |
| [StoryType](../../aspose.words.drawing/shape/storytype/) { get; } | 返回Textbox. |
| [Stroke](../../aspose.words.drawing/shape/stroke/) { get; } | 定义形状的描边。 |
| [StrokeColor](../../aspose.words.drawing/shape/strokecolor/) { get; set; } | 定义笔触的颜色。 |
| [Stroked](../../aspose.words.drawing/shape/stroked/) { get; set; } | 定义路径是否将被描边。 |
| [StrokeWeight](../../aspose.words.drawing/shape/strokeweight/) { get; set; } | 定义描边形状路径的画笔粗细（以点为单位）。 |
| [Target](../../aspose.words.drawing/shapebase/target/) { get; set; } | 获取或设置形状超链接的目标框架。 |
| [TextBox](../../aspose.words.drawing/shape/textbox/) { get; } | 定义指定文本在形状中显示方式的属性。 |
| [TextPath](../../aspose.words.drawing/shape/textpath/) { get; } | 定义文本路径（艺术字对象）的文本。 |
| [Title](../../aspose.words.drawing/shapebase/title/) { get; set; } | 获取或设置当前形状对象的标题（标题）。 |
| [Top](../../aspose.words.drawing/shapebase/top/) { get; set; } | 获取或设置形状包含块的顶边位置。 |
| [TopRelative](../../aspose.words.drawing/shapebase/toprelative/) { get; set; } | 获取或设置表示形状相对顶部位置的百分比值。 |
| [VerticalAlignment](../../aspose.words.drawing/shapebase/verticalalignment/) { get; set; } | 指定形状的垂直定位方式。 |
| [Width](../../aspose.words.drawing/shapebase/width/) { get; set; } | 获取或设置形状包含块的宽度。 |
| [WidthRelative](../../aspose.words.drawing/shapebase/widthrelative/) { get; set; } | 获取或设置表示形状相对宽度百分比的值。 |
| [WrapSide](../../aspose.words.drawing/shapebase/wrapside/) { get; set; } | 指定文本如何环绕形状。 |
| [WrapType](../../aspose.words.drawing/shapebase/wraptype/) { get; set; } | 定义形状是内联的还是浮动的。对于浮动形状，定义文本环绕形状的环绕模式。 |
| [ZOrder](../../aspose.words.drawing/shapebase/zorder/) { get; set; } | 确定重叠形状的显示顺序。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words.drawing/shape/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | 接受访客。 |
| override [AcceptEnd](../../aspose.words.drawing/shape/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | 接受访客访问形状的末尾。 |
| override [AcceptStart](../../aspose.words.drawing/shape/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | 接受访客访问形状的起点。 |
| [AdjustWithEffects](../../aspose.words.drawing/shapebase/adjustwitheffects/)(*RectangleF*) | 将效果范围的源矩形值添加到并返回最终矩形。 |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | 将指定节点添加到此节点的子节点列表的末尾。 |
| [Clone](../../aspose.words/node/clone/)(*bool*) | 创建节点的副本。 |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | 创建可用于遍历和读取节点的导航器。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | 获取指定的第一个祖先[`NodeType`](../../aspose.words/nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | 获取指定对象类型的第一个祖先。 |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | 返回与指定类型匹配的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | 返回与指定类型匹配的子节点的实时集合。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | 为该节点的子节点提供对每个样式迭代的支持。 |
| [GetShapeRenderer](../../aspose.words.drawing/shapebase/getshaperenderer/)() | 创建并返回可用于将此形状渲染为图像的对象。 |
| override [GetText](../../aspose.words/compositenode/gettext/)() | 获取此节点及其所有子节点的文本。 |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | 返回子节点数组中指定子节点的索引。 |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | 在指定的参考节点后立即插入指定的节点。 |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | 在指定的参考节点之前立即插入指定的节点。 |
| [LocalToParent](../../aspose.words.drawing/shapebase/localtoparent/)(*PointF*) | 将值从本地坐标空间转换为父形状的坐标空间。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | 根据前序树遍历算法获取下一个节点。 |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | 将指定节点添加到此节点的子节点列表的开头。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | 根据前序树遍历算法获取前一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 将自身从父级中移除。 |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | 删除当前节点的所有子节点。 |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | 删除指定的子节点。 |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | 删除所有[`SmartTag`](../../aspose.words.markup/smarttag/)当前节点的后代节点。 |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | 选择与 XPath 表达式匹配的节点列表。 |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | 选择第一个[`Node`](../../aspose.words/node/)与 XPath 表达式匹配。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | 使用指定的保存选项将节点内容导出为字符串。 |
| [UpdateSmartArtDrawing](../../aspose.words.drawing/shape/updatesmartartdrawing/)() | 使用 Aspose.Words 的 SmartArt 冷渲染引擎更新 SmartArt 预渲染绘图。 |

## 评论

使用`Shape`类，您可以在 Microsoft Word 文档中创建或修改形状。

形状的一个重要属性是[`ShapeType`](../shapebase/shapetype/)不同类型的形状在 Word 文档中可以具有不同的功能。例如，只有图像和 OLE 形状可以在其中包含图像。大多数形状可以包含文本，但并非所有形状都可以。

可以包含文本的形状，可以包含[`Paragraph`](../../aspose.words/paragraph/)and [`Table`](../../aspose.words.tables/table/)节点作为子节点。

## 例子

展示如何将浮动图像插入到页面的中心。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个浮动图像，该图像将出现在重叠文本后面，并将其与页面的中心对齐。
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

展示如何从文档中提取图像，并将其作为单独的文件保存到本地文件系统。

```csharp
Document doc = new Document(MyDir + "Images.docx");

// 从文档中获取形状集合，
// 并将每个带有图像的形状的图像数据作为文件保存到本地文件系统。
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // 形状的图像数据可能包含多种可能的图像格式的图像。
        // 我们可以根据每个图像的格式自动确定其文件扩展名。
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

展示如何从文档中删除所有形状。

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

// 从文档中删除所有形状节点。
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
shapes.Clear();

// 所有形状都消失了，但组形状仍然在文档中。
Assert.AreEqual(1, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);

// 分别删除所有组形状。
NodeCollection groupShapes = doc.GetChildNodes(NodeType.GroupShape, true);
groupShapes.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### 也可以看看

* class [ShapeBase](../shapebase/)
* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
