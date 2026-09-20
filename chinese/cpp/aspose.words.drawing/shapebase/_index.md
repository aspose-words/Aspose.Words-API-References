---
title: "Aspose::Words::Drawing::ShapeBase 类"
linktitle: "ShapeBase"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase 类。绘图层中对象的基类，例如 AutoShape、自由形状、OLE 对象、ActiveX 控件或图片。欲了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words.drawing/shapebase/
---
## ShapeBase class


绘图层中对象的基类，例如 AutoShape、自由形状、OLE 对象、ActiveX 控件或图片。要了解更多信息，请访问 [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/) 文档文章。

```cpp
class ShapeBase : public Aspose::Words::CompositeNode,
                  public Aspose::Words::IInline,
                  public Aspose::Words::Drawing::Core::IShape,
                  public Aspose::Words::IShapeAttrSource,
                  public Aspose::Words::Revisions::ITrackableNode,
                  public Aspose::Words::Drawing::Core::IFillable,
                  public Aspose::Words::Drawing::Core::IGlow,
                  public Aspose::Words::Drawing::Core::IReflection,
                  public Aspose::Words::Drawing::Core::ISoftEdge,
                  public Aspose::Words::Drawing::Core::IShadow
```

## 方法

| 方法 | 描述 |
| --- | --- |
| virtual [Accept](../../aspose.words/node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | 接受访问者。 |
| virtual [AcceptEnd](../../aspose.words/compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | 当在派生类中实现时，调用指定文档访问器的 VisitXXXEnd 方法。 |
| virtual [AcceptStart](../../aspose.words/compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | 当在派生类中实现时，调用指定文档访问器的 VisitXXXStart 方法。 |
| [AdjustWithEffects](./adjustwitheffects/)(System::Drawing::RectangleF) | 将效果范围的值添加到源矩形，并返回最终矩形。 |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | 创建节点的副本。 |
| [get_AllowOverlap](./get_allowoverlap/)() | 获取或设置指定此形状是否可以覆盖其他形状的值。 |
| [get_AlternativeText](./get_alternativetext/)() | 定义在图形显示时的替代文本。 |
| [get_AnchorLocked](./get_anchorlocked/)() | 指定形状锚点是否被锁定。 |
| [get_AspectRatioLocked](./get_aspectratiolocked/)() | 指定形状的宽高比是否被锁定。 |
| [get_BehindText](./get_behindtext/)() | 指定形状是位于文本下方还是上方。 |
| [get_Bottom](./get_bottom/)() | 获取形状所在包含块底部边缘的位置。 |
| [get_Bounds](./get_bounds/)() | 获取或设置形状所在包含块的位置和大小。 |
| [get_BoundsInPoints](./get_boundsinpoints/)() | 获取形状所在包含块的位置和大小（单位为点），相对于最上层形状的锚点。 |
| [get_BoundsWithEffects](./get_boundswitheffects/)() | 获取此形状对象在应用绘图效果后最终的范围。值以点为单位。 |
| [get_CanHaveImage](./get_canhaveimage/)() | 如果形状类型允许形状具有图像，则返回 **true**。 |
| [get_CoordOrigin](./get_coordorigin/)() | 此形状的包含块左上角的坐标。 |
| [get_CoordSize](./get_coordsize/)() | 此形状的包含块内部坐标空间的宽度和高度。 |
| [get_Count](../../aspose.words/compositenode/get_count/)() | 获取此节点的直接子节点数量。 |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | 指定自定义节点标识符。 |
| [get_DistanceBottom](./get_distancebottom/)() | 返回或设置文档文本与形状底部边缘之间的距离（单位为点）。 |
| [get_DistanceLeft](./get_distanceleft/)() | 返回或设置文档文本与形状左侧边缘之间的距离（单位为点）。 |
| [get_DistanceRight](./get_distanceright/)() | 返回或设置文档文本与形状右侧边缘之间的距离（单位为点）。 |
| [get_DistanceTop](./get_distancetop/)() | 返回或设置文档文本与形状顶部边缘之间的距离（单位为点）。 |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | 获取此节点所属的文档。 |
| [get_Fill](./get_fill/)() | 获取形状的填充格式。 |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | 获取节点的第一个子节点。 |
| [get_FlipOrientation](./get_fliporientation/)() | 切换形状的方向。 |
| [get_Font](./get_font/)() | 提供对该对象字体格式的访问。 |
| [get_Glow](./get_glow/)() | 获取形状的发光格式。 |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | 如果此节点有任何子节点，则返回 **true**。 |
| [get_Height](./get_height/)() | 获取或设置形状包含块的高度。 |
| [get_HeightRelative](./get_heightrelative/)() | 获取或设置表示形状相对高度百分比的值。 |
| [get_Hidden](./get_hidden/)() | 获取或设置一个布尔值，指示形状是否可见。 |
| [get_HorizontalAlignment](./get_horizontalalignment/)() | 指定形状的水平定位方式。 |
| [get_HRef](./get_href/)() | 获取或设置形状的完整超链接地址。 |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | 因为此节点可以拥有子节点，返回 **true**。 |
| [get_IsDecorative](./get_isdecorative/)() | 获取或设置指定形状在文档中是否为装饰性的标志。 |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | 如果在启用更改跟踪的 Microsoft Word 中删除了此对象，则返回 true。 |
| [get_IsGroup](./get_isgroup/)() | 如果这是组形状，则返回 **true**。 |
| [get_IsHorizontalRule](./get_ishorizontalrule/)() | 如果此形状是水平线，则返回 **true**。 |
| [get_IsImage](./get_isimage/)() | 如果此形状是图像形状，则返回 **true**。 |
| [get_IsInline](./get_isinline/)() | 一种快速判断此形状是否与文本内联定位的方法。 |
| [get_IsInsertRevision](./get_isinsertrevision/)() | 如果在启用更改跟踪的 Microsoft Word 中插入了此对象，则返回 true。 |
| [get_IsLayoutInCell](./get_islayoutincell/)() | 获取或设置指示形状是显示在表格内部还是外部的标志。 |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | 如果在启用更改跟踪的 Microsoft Word 中移动（删除）了此对象，则返回 **true**。 |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | 如果在启用更改跟踪的 Microsoft Word 中移动（插入）了此对象，则返回 **true**。 |
| [get_IsSignatureLine](./get_issignatureline/)() | 指示该形状是一个 [SignatureLine](../signatureline/)。 |
| [get_IsTopLevel](./get_istoplevel/)() | 如果此形状不是组形状的子形状，则返回 **true**。 |
| [get_IsWordArt](./get_iswordart/)() | 如果此形状是 WordArt 对象，则返回 **true**。 |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | 获取节点的最后一个子节点。 |
| [get_Left](./get_left/)() | 获取或设置形状所在包含块的左边缘位置。 |
| [get_LeftRelative](./get_leftrelative/)() | 获取或设置表示形状相对左侧位置的百分比值。 |
| [get_MarkupLanguage](./get_markuplanguage/)() const | 获取用于此图形对象的 MarkupLanguage。 |
| [get_Name](./get_name/)() | 获取或设置可选的形状名称。 |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | 获取紧随此节点之后的节点。 |
| virtual [get_NodeType](../../aspose.words/node/get_nodetype/)() const | 获取此节点的类型。 |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | 获取此节点的直接父节点。 |
| [get_ParentParagraph](./get_parentparagraph/)() | 返回直接父段落。 |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | 获取紧挨此节点之前的节点。 |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | 返回一个表示包含在此节点中的文档部分的 [Range](../../aspose.words/range/) 对象。 |
| [get_Reflection](./get_reflection/)() | 获取形状的反射格式设置。 |
| [get_RelativeHorizontalPosition](./get_relativehorizontalposition/)() | 指定形状在水平方向上相对于何物进行定位。 |
| [get_RelativeHorizontalSize](./get_relativehorizontalsize/)() | 获取或设置形状在水平方向上的相对大小值。 |
| [get_RelativeVerticalPosition](./get_relativeverticalposition/)() | 指定形状在垂直方向上相对于何物进行定位。 |
| [get_RelativeVerticalSize](./get_relativeverticalsize/)() | 获取或设置形状在垂直方向上的相对大小值。 |
| [get_Right](./get_right/)() | 获取形状所在包含块的右边缘位置。 |
| [get_Rotation](./get_rotation/)() | 定义形状旋转的角度（以度为单位）。正值对应顺时针旋转角度。 |
| [get_ScreenTip](./get_screentip/)() | 定义鼠标指针悬停在形状上时显示的文本。 |
| [get_ShadowFormat](./get_shadowformat/)() | 获取形状的阴影格式设置。 |
| [get_ShapeType](./get_shapetype/)() | 获取形状类型。 |
| [get_SizeInPoints](./get_sizeinpoints/)() | 获取形状的尺寸（以点为单位）。 |
| [get_SoftEdge](./get_softedge/)() | 获取形状的柔化边缘格式设置。 |
| [get_Target](./get_target/)() | 获取或设置形状超链接的目标框架。 |
| [get_Title](./get_title/)() | 获取或设置当前形状对象的标题（说明）。 |
| [get_Top](./get_top/)() | 获取或设置形状所在包含块的顶部边缘位置。 |
| [get_TopRelative](./get_toprelative/)() | 获取或设置表示形状相对顶部位置的百分比值。 |
| [get_VerticalAlignment](./get_verticalalignment/)() | 指定形状在垂直方向上的定位方式。 |
| [get_Width](./get_width/)() | 获取或设置形状所在包含块的宽度。 |
| [get_WidthRelative](./get_widthrelative/)() | 获取或设置表示形状相对宽度百分比的值。 |
| [get_WrapSide](./get_wrapside/)() | 指定文本环绕形状的方式。 |
| [get_WrapType](./get_wraptype/)() | 定义形状是内联还是浮动。对于浮动形状，定义文本环绕形状的换行模式。 |
| [get_ZOrder](./get_zorder/)() | 确定重叠形状的显示顺序。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | 获取指定 [NodeType](../../aspose.words/nodetype/) 的第一个祖先节点。 |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | 返回匹配指定类型的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | 返回匹配指定类型的子节点的实时集合。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | 提供对该节点的子节点进行 foreach 样式迭代的支持。 |
| [GetShapeRenderer](./getshaperenderer/)() | 创建并返回一个可用于将此形状渲染为图像的对象。 |
| [GetText](../../aspose.words/compositenode/gettext/)() override | 获取此节点及其所有子节点的文本。 |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 返回指定子节点在子节点数组中的索引。 |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [LocalToParent](./localtoparent/)(System::Drawing::PointF) | 将值从本地坐标空间转换为父形状的坐标空间。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 根据先序树遍历算法获取下一个节点。 |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | 一个将节点类型枚举值转换为用户友好字符串的实用方法。 |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 根据先序树遍历算法获取上一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 从父节点中移除自身。 |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | 移除当前节点的所有子节点。 |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | 移除当前节点的所有 [SmartTag](../../aspose.words.markup/smarttag/) 后代节点。 |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | 选择匹配 XPath 表达式的节点列表。 |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | 选择第一个匹配 XPath 表达式的 [Node](../../aspose.words/node/)。 |
| [set_AllowOverlap](./set_allowoverlap/)(bool) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_AllowOverlap](./get_allowoverlap/)。 |
| [set_AlternativeText](./set_alternativetext/)(const System::String\&) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_AlternativeText](./get_alternativetext/)。 |
| [set_AnchorLocked](./set_anchorlocked/)(bool) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_AnchorLocked](./get_anchorlocked/)。 |
| [set_AspectRatioLocked](./set_aspectratiolocked/)(bool) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked](./get_aspectratiolocked/)。 |
| [set_BehindText](./set_behindtext/)(bool) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_BehindText](./get_behindtext/)。 |
| [set_Bounds](./set_bounds/)(System::Drawing::RectangleF) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_Bounds](./get_bounds/)。 |
| [set_CoordOrigin](./set_coordorigin/)(System::Drawing::Point) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_CoordOrigin](./get_coordorigin/)。 |
| [set_CoordSize](./set_coordsize/)(System::Drawing::Size) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_CoordSize](./get_coordsize/)。 |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | 用于设置 [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/) 的 setter。 |
| [set_DistanceBottom](./set_distancebottom/)(double) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_DistanceBottom](./get_distancebottom/)。 |
| [set_DistanceLeft](./set_distanceleft/)(double) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_DistanceLeft](./get_distanceleft/)。 |
| [set_DistanceRight](./set_distanceright/)(double) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_DistanceRight](./get_distanceright/)。 |
| [set_DistanceTop](./set_distancetop/)(double) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_DistanceTop](./get_distancetop/)。 |
| [set_FlipOrientation](./set_fliporientation/)(Aspose::Words::Drawing::FlipOrientation) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_FlipOrientation](./get_fliporientation/)。 |
| [set_Height](./set_height/)(double) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_Height](./get_height/)。 |
| [set_HeightRelative](./set_heightrelative/)(float) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_HeightRelative](./get_heightrelative/). |
| [set_Hidden](./set_hidden/)(bool) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_Hidden](./get_hidden/). |
| [set_HorizontalAlignment](./set_horizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_HorizontalAlignment](./get_horizontalalignment/). |
| [set_HRef](./set_href/)(const System::String\&) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_HRef](./get_href/). |
| [set_IsDecorative](./set_isdecorative/)(bool) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_IsDecorative](./get_isdecorative/). |
| [set_IsLayoutInCell](./set_islayoutincell/)(bool) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell](./get_islayoutincell/). |
| [set_Left](./set_left/)(double) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_Left](./get_left/). |
| [set_LeftRelative](./set_leftrelative/)(float) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_LeftRelative](./get_leftrelative/). |
| [set_Name](./set_name/)(const System::String\&) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_Name](./get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_RelativeHorizontalPosition](./set_relativehorizontalposition/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition](./get_relativehorizontalposition/). |
| [set_RelativeHorizontalSize](./set_relativehorizontalsize/)(Aspose::Words::Drawing::RelativeHorizontalSize) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize](./get_relativehorizontalsize/). |
| [set_RelativeVerticalPosition](./set_relativeverticalposition/)(Aspose::Words::Drawing::RelativeVerticalPosition) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition](./get_relativeverticalposition/). |
| [set_RelativeVerticalSize](./set_relativeverticalsize/)(Aspose::Words::Drawing::RelativeVerticalSize) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalSize](./get_relativeverticalsize/). |
| [set_Rotation](./set_rotation/)(double) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_Rotation](./get_rotation/). |
| [set_ScreenTip](./set_screentip/)(const System::String\&) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_ScreenTip](./get_screentip/). |
| [set_Target](./set_target/)(const System::String\&) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_Target](./get_target/). |
| [set_Title](./set_title/)(const System::String\&) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_Title](./get_title/). |
| [set_Top](./set_top/)(double) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_Top](./get_top/). |
| [set_TopRelative](./set_toprelative/)(float) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_TopRelative](./get_toprelative/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment](./get_verticalalignment/). |
| [set_Width](./set_width/)(double) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_Width](./get_width/). |
| [set_WidthRelative](./set_widthrelative/)(float) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_WidthRelative](./get_widthrelative/). |
| [set_WrapSide](./set_wrapside/)(Aspose::Words::Drawing::WrapSide) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_WrapSide](./get_wrapside/). |
| [set_WrapType](./set_wraptype/)(Aspose::Words::Drawing::WrapType) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_WrapType](./get_wraptype/). |
| [set_ZOrder](./set_zorder/)(int32_t) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_ZOrder](./get_zorder/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | 以指定格式将节点内容导出为字符串。 |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的保存选项将节点内容导出为字符串。 |
| static [Type](./type/)() |  |
## 备注


这是一个抽象类。您可以实例化的两个派生类是 [Shape](../shape/) 和 [GroupShape](../groupshape/)。

形状是文档树中的一个节点。

如果形状是 [Paragraph](../../aspose.words/paragraph/) 对象的子对象，则该形状被称为“顶层”。顶层形状以点为单位进行测量和定位。

当多个形状被分组时，形状也可以作为 [GroupShape](../groupshape/) 对象的子对象出现。组形状的子形状在父组形状的 [CoordSize](./get_coordsize/) 和 [CoordOrigin](./get_coordorigin/) 属性定义的坐标空间和单位中定位。

形状可以与文本内联定位或浮动定位。定位方式通过 [WrapType](./get_wraptype/) 属性进行控制。

当形状为浮动时，它相对于某些对象（例如当前段落、页边距或页面）进行定位。形状的相对定位使用 [RelativeHorizontalPosition](./get_relativehorizontalposition/) 和 [RelativeVerticalPosition](./get_relativeverticalposition/) 属性指定。

浮动形状可以使用 [Left](./get_left/) 和 [Top](./get_top/) 属性显式定位，或使用 [HorizontalAlignment](./get_horizontalalignment/) 和 [VerticalAlignment](./get_verticalalignment/) 属性相对于其他对象对齐。

## 示例



展示如何在页面中心插入浮动图像。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入一个浮动图像，使其出现在重叠文本后面，并将其对齐到页面中心。
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## 另见

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
