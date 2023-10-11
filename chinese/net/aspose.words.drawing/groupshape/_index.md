---
title: Class GroupShape
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Drawing.GroupShape 班级. 表示文档中的一组形状
type: docs
weight: 1020
url: /zh/net/aspose.words.drawing/groupshape/
---
## GroupShape class

表示文档中的一组形状。

要了解更多信息，请访问[如何将组形状添加到 Word 文档中](https://docs.aspose.com/words/net/how-to-add-group-shape-into-a-word-document/)文档文章。

```csharp
public class GroupShape : ShapeBase
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [GroupShape](groupshape/)(DocumentBase) | 创建一个新的组形状。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AllowOverlap](../../aspose.words.drawing/shapebase/allowoverlap/) { get; set; } | 获取或设置一个值，该值指定此形状是否可以与其他形状重叠。 |
| [AlternativeText](../../aspose.words.drawing/shapebase/alternativetext/) { get; set; } | 定义要显示的替代文本，而不是图形。 |
| [AnchorLocked](../../aspose.words.drawing/shapebase/anchorlocked/) { get; set; } | 指定形状的锚点是否被锁定。 |
| [AspectRatioLocked](../../aspose.words.drawing/shapebase/aspectratiolocked/) { get; set; } | 指定是否锁定形状的纵横比。 |
| [BehindText](../../aspose.words.drawing/shapebase/behindtext/) { get; set; } | 指定形状是在文本下方还是上方。 |
| [Bottom](../../aspose.words.drawing/shapebase/bottom/) { get; } | 获取形状包含块的底部边缘的位置。 |
| [Bounds](../../aspose.words.drawing/shapebase/bounds/) { get; set; } | 获取或设置形状包含块的位置和大小。 |
| [BoundsInPoints](../../aspose.words.drawing/shapebase/boundsinpoints/) { get; } | 获取形状的包含块相对于最顶部形状的锚点的位置和大小（以点为单位）。 |
| [BoundsWithEffects](../../aspose.words.drawing/shapebase/boundswitheffects/) { get; } | 获取该形状对象在应用绘图效果后的最终范围。 值以点为单位进行测量。 |
| [CanHaveImage](../../aspose.words.drawing/shapebase/canhaveimage/) { get; } | 返回`真的`如果形状类型允许形状具有图像。 |
| [CoordOrigin](../../aspose.words.drawing/shapebase/coordorigin/) { get; set; } | 该形状的包含块左上角的坐标。 |
| [CoordSize](../../aspose.words.drawing/shapebase/coordsize/) { get; set; } | 该形状的包含块内坐标空间的宽度和高度。 |
| [Count](../../aspose.words/compositenode/count/) { get; } | 获取此节点的直接子节点的数量。 |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| [DistanceBottom](../../aspose.words.drawing/shapebase/distancebottom/) { get; set; } | 返回或设置文档文本与形状底部边缘之间的距离（以磅为单位）。 |
| [DistanceLeft](../../aspose.words.drawing/shapebase/distanceleft/) { get; set; } | 返回或设置文档文本与形状左边缘之间的距离（以磅为单位）。 |
| [DistanceRight](../../aspose.words.drawing/shapebase/distanceright/) { get; set; } | 返回或设置文档文本与形状右边缘之间的距离（以磅为单位）。 |
| [DistanceTop](../../aspose.words.drawing/shapebase/distancetop/) { get; set; } | 返回或设置文档文本与形状上边缘之间的距离（以磅为单位）。 |
| virtual [Document](../../aspose.words/node/document/) { get; } | 获取该节点所属的文档。 |
| [Fill](../../aspose.words.drawing/shapebase/fill/) { get; } | 获取形状的填充格式。 |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | 获取节点的第一个子节点。 |
| [FlipOrientation](../../aspose.words.drawing/shapebase/fliporientation/) { get; set; } | 切换形状的方向。 |
| [Font](../../aspose.words.drawing/shapebase/font/) { get; } | 提供对此对象的字体格式的访问。 |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | 返回`真的`如果该节点有任何子节点. |
| [Height](../../aspose.words.drawing/shapebase/height/) { get; set; } | 获取或设置形状包含块的高度。 |
| [HeightRelative](../../aspose.words.drawing/shapebase/heightrelative/) { get; set; } | 获取或设置表示形状相对高度百分比的值。 |
| [HorizontalAlignment](../../aspose.words.drawing/shapebase/horizontalalignment/) { get; set; } | 指定形状如何水平定位。 |
| [HRef](../../aspose.words.drawing/shapebase/href/) { get; set; } | 获取或设置形状的完整超链接地址。 |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | 返回`真的`因为该节点可以有子节点。 |
| [IsDecorative](../../aspose.words.drawing/shapebase/isdecorative/) { get; set; } | 获取或设置指定形状在文档中是否为装饰性的标志。 |
| [IsDeleteRevision](../../aspose.words.drawing/shapebase/isdeleterevision/) { get; } | 如果在启用更改跟踪时在 Microsoft Word 中删除了此对象，则返回 true。 |
| [IsGroup](../../aspose.words.drawing/shapebase/isgroup/) { get; } | 返回`真的`如果这是一个团体形状. |
| [IsHorizontalRule](../../aspose.words.drawing/shapebase/ishorizontalrule/) { get; } | 返回`真的`如果这个形状是水平尺. |
| [IsImage](../../aspose.words.drawing/shapebase/isimage/) { get; } | 返回`真的`如果这个形状是图像形状. |
| [IsInline](../../aspose.words.drawing/shapebase/isinline/) { get; } | 确定此形状是否与文本内联放置的快速方法。 |
| [IsInsertRevision](../../aspose.words.drawing/shapebase/isinsertrevision/) { get; } | 如果在启用更改跟踪的情况下将此对象插入到 Microsoft Word 中，则返回 true。 |
| [IsLayoutInCell](../../aspose.words.drawing/shapebase/islayoutincell/) { get; set; } | 获取或设置一个标志，指示形状是显示在表格内部还是表格外部。 |
| [IsMoveFromRevision](../../aspose.words.drawing/shapebase/ismovefromrevision/) { get; } | 返回`真的`如果启用更改跟踪时在 Microsoft Word 中移动（删除）此对象。 |
| [IsMoveToRevision](../../aspose.words.drawing/shapebase/ismovetorevision/) { get; } | 返回`真的`如果在启用更改跟踪的情况下在 Microsoft Word 中移动（插入）此对象。 |
| [IsSignatureLine](../../aspose.words.drawing/shapebase/issignatureline/) { get; } | 表示形状是[`SignatureLine`](../signatureline/). |
| [IsTopLevel](../../aspose.words.drawing/shapebase/istoplevel/) { get; } | 返回`真的`如果此形状不是组形状的子项. |
| [IsWordArt](../../aspose.words.drawing/shapebase/iswordart/) { get; } | 返回`真的`如果此形状是艺术字对象. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | 获取节点的最后一个子节点。 |
| [Left](../../aspose.words.drawing/shapebase/left/) { get; set; } | 获取或设置形状包含块的左边缘位置。 |
| [LeftRelative](../../aspose.words.drawing/shapebase/leftrelative/) { get; set; } | 获取或设置表示形状相对左侧位置（以百分比表示）的值。 |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage/) { get; } | 获取用于此图形对象的 MarkupLanguage。 |
| [Name](../../aspose.words.drawing/shapebase/name/) { get; set; } | 获取或设置可选形状名称。 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧随该节点的下一个节点。 |
| override [NodeType](../../aspose.words.drawing/groupshape/nodetype/) { get; } | 返回GroupShape. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [ParentParagraph](../../aspose.words.drawing/shapebase/parentparagraph/) { get; } | 返回直接父段落。 |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取紧邻此节点之前的节点。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回一个[`Range`](../../aspose.words/range/)表示此节点中包含的文档部分的对象。 |
| [RelativeHorizontalPosition](../../aspose.words.drawing/shapebase/relativehorizontalposition/) { get; set; } | 指定形状相对于水平位置的位置。 |
| [RelativeHorizontalSize](../../aspose.words.drawing/shapebase/relativehorizontalsize/) { get; set; } | 获取或设置形状在水平方向的相对大小值。 |
| [RelativeVerticalPosition](../../aspose.words.drawing/shapebase/relativeverticalposition/) { get; set; } | 指定相对于形状垂直定位的位置。 |
| [RelativeVerticalSize](../../aspose.words.drawing/shapebase/relativeverticalsize/) { get; set; } | 获取或设置形状在垂直方向的相对大小值。 |
| [Right](../../aspose.words.drawing/shapebase/right/) { get; } | 获取形状包含块的右边缘位置。 |
| [Rotation](../../aspose.words.drawing/shapebase/rotation/) { get; set; } | 定义形状旋转的角度（以度为单位）。 正值对应于顺时针旋转角度。 |
| [ScreenTip](../../aspose.words.drawing/shapebase/screentip/) { get; set; } | 定义当鼠标指针移动到形状上时显示的文本。 |
| [ShadowFormat](../../aspose.words.drawing/shapebase/shadowformat/) { get; } | 获取形状的阴影格式。 |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype/) { get; } | 获取形状类型。 |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints/) { get; } | 获取形状的大小（以磅为单位）。 |
| [Target](../../aspose.words.drawing/shapebase/target/) { get; set; } | 获取或设置形状超链接的目标框架。 |
| [Title](../../aspose.words.drawing/shapebase/title/) { get; set; } | 获取或设置当前形状对象的标题 (caption)。 |
| [Top](../../aspose.words.drawing/shapebase/top/) { get; set; } | 获取或设置形状包含块的顶部边缘的位置。 |
| [TopRelative](../../aspose.words.drawing/shapebase/toprelative/) { get; set; } | 获取或设置表示形状相对顶部位置（以百分比表示）的值。 |
| [VerticalAlignment](../../aspose.words.drawing/shapebase/verticalalignment/) { get; set; } | 指定形状如何垂直定位。 |
| [Width](../../aspose.words.drawing/shapebase/width/) { get; set; } | 获取或设置形状包含块的宽度。 |
| [WidthRelative](../../aspose.words.drawing/shapebase/widthrelative/) { get; set; } | 获取或设置表示形状相对宽度百分比的值。 |
| [WrapSide](../../aspose.words.drawing/shapebase/wrapside/) { get; set; } | 指定文本如何环绕形状。 |
| [WrapType](../../aspose.words.drawing/shapebase/wraptype/) { get; set; } | 定义形状是内联还是浮动。对于浮动形状，定义形状周围文本的环绕模式。 |
| [ZOrder](../../aspose.words.drawing/shapebase/zorder/) { get; set; } | 确定重叠形状的显示顺序。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words.drawing/groupshape/accept/)(DocumentVisitor) | 接受访客。 |
| override [AcceptEnd](../../aspose.words.drawing/groupshape/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words.drawing/groupshape/acceptstart/)(DocumentVisitor) |  |
| [AdjustWithEffects](../../aspose.words.drawing/shapebase/adjustwitheffects/)(RectangleF) | 添加效果范围的源矩形值并返回最终矩形。 |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | 创建节点的副本。 |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | 创建可用于遍历和读取节点的导航器。 |
| [FetchInheritedShapeAttr](../../aspose.words.drawing/shapebase/fetchinheritedshapeattr/)(int) | 保留供系统使用。 IShapeAttrSource. |
| [FetchShapeAttr](../../aspose.words.drawing/shapebase/fetchshapeattr/)(int) | 保留供系统使用。 IShapeAttrSource. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | 获取指定的第一个祖先[`NodeType`](../../aspose.words/nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | 获取指定对象类型的第一个祖先。 |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | 返回与指定类型匹配的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | 返回与指定类型匹配的子节点的实时集合。 |
| [GetDirectShapeAttr](../../aspose.words.drawing/shapebase/getdirectshapeattr/)(int) | 保留供系统使用。 IShapeAttrSource. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | 为该节点的子节点上的每个样式迭代提供支持。 |
| [GetShapeRenderer](../../aspose.words.drawing/shapebase/getshaperenderer/)() | 创建并返回一个可用于将此形状渲染为图像的对象。 |
| override [GetText](../../aspose.words/compositenode/gettext/)() | 获取此节点及其所有子节点的文本。 |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | 返回子节点数组中指定子节点的索引。 |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [LocalToParent](../../aspose.words.drawing/shapebase/localtoparent/)(PointF) | 将局部坐标空间中的值转换为父形状的坐标空间。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | 根据先序树遍历算法获取下一个节点。 |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | 根据先序树遍历算法获取前一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 将自身从父级中删除。 |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | 删除当前节点的所有子节点。 |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveShapeAttr](../../aspose.words.drawing/shapebase/removeshapeattr/)(int) | 保留供系统使用。 IShapeAttrSource. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | 删除所有[`SmartTag`](../../aspose.words.markup/smarttag/)当前节点的后代节点. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | 选择与 XPath 表达式匹配的节点列表。 |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | 选择第一个[`Node`](../../aspose.words/node/)与 XPath 表达式匹配。 |
| [SetShapeAttr](../../aspose.words.drawing/shapebase/setshapeattr/)(int, object) | 保留供系统使用。 IShapeAttrSource. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | 使用指定的保存选项将节点的内容导出到字符串中。 |

### 评论

A`GroupShape`是一个复合节点并且可以有[`Shape`](../shape/)和 `GroupShape`节点作为子节点。

每个`GroupShape`为其子形状定义一个新的坐标系。 坐标系是使用[`CoordSize`](../shapebase/coordsize/)和 [`CoordOrigin`](../shapebase/coordorigin/)特性。

### 例子

演示如何创建一组形状，并使用文档访问者打印其内容。

```csharp
public void GroupOfShapes()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 如果需要创建“NonPrimitive”形状，例如 SingleCornerSnipped、TopCornersSnipped、DiagonalCornersSnipped，
    // TopCornersOneRoundedOneSnipped、SingleCornerRounded、TopCornersRounded、DiagonalCornersRounded
    // 请使用 DocumentBuilder.InsertShape 方法。
    Shape balloon = new Shape(doc, ShapeType.Balloon)
    {
        Width = 200, 
        Height = 200,
        Stroke = { Color = Color.Red }
    };

    Shape cube = new Shape(doc, ShapeType.Cube)
    {
        Width = 100, 
        Height = 100,
        Stroke = { Color = Color.Blue }
    };

    GroupShape group = new GroupShape(doc);
    group.AppendChild(balloon);
    group.AppendChild(cube);

    Assert.True(group.IsGroup);

    builder.InsertNode(group);

    ShapeGroupPrinter printer = new ShapeGroupPrinter();
    group.Accept(printer);

    Console.WriteLine(printer.GetText());
}

/// <summary>
/// 将访问过的形状组的内容打印到控制台。
/// </summary>
public class ShapeGroupPrinter : DocumentVisitor
{
    public ShapeGroupPrinter()
    {
        mBuilder = new StringBuilder();
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        mBuilder.AppendLine("Shape group started:");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitGroupShapeEnd(GroupShape groupShape)
    {
        mBuilder.AppendLine("End of shape group");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitShapeStart(Shape shape)
    {
        mBuilder.AppendLine("\tShape - " + shape.ShapeType + ":");
        mBuilder.AppendLine("\t\tWidth: " + shape.Width);
        mBuilder.AppendLine("\t\tHeight: " + shape.Height);
        mBuilder.AppendLine("\t\tStroke color: " + shape.Stroke.Color);
        mBuilder.AppendLine("\t\tFill color: " + shape.Fill.ForeColor);
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitShapeEnd(Shape shape)
    {
        mBuilder.AppendLine("\tEnd of shape");
        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
}
```

### 也可以看看

* class [ShapeBase](../shapebase/)
* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)


