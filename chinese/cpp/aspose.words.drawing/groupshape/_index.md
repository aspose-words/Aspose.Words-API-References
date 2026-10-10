---
title: "Aspose::Words::Drawing::GroupShape 类"
linktitle: "GroupShape"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::GroupShape 类。表示文档中一组形状。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.drawing/groupshape/
---
## GroupShape class


表示文档中的一组形状。要了解更多信息，请访问 [How to Add Group Shape into a Word Document](https://docs.aspose.com/words/cpp/how-to-add-group-shape-into-a-word-document/) 文档文章。

```cpp
class GroupShape : public Aspose::Words::Drawing::ShapeBase
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者。 |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者以访问 [GroupShape](./) 的结束位置。 |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者以访问 [GroupShape](./) 的起始位置。 |
| [AdjustWithEffects](../shapebase/adjustwitheffects/)(System::Drawing::RectangleF) | 将效果范围的值添加到源矩形，并返回最终矩形。 |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | 创建节点的副本。 |
| [get_AllowOverlap](../shapebase/get_allowoverlap/)() | 获取或设置指定此形状是否可以覆盖其他形状的值。 |
| [get_AlternativeText](../shapebase/get_alternativetext/)() | 定义在图形显示时的替代文本。 |
| [get_AnchorLocked](../shapebase/get_anchorlocked/)() | 指定形状锚点是否被锁定。 |
| [get_AspectRatioLocked](../shapebase/get_aspectratiolocked/)() | 指定形状的宽高比是否被锁定。 |
| [get_BehindText](../shapebase/get_behindtext/)() | 指定形状是位于文本下方还是上方。 |
| [get_Bottom](../shapebase/get_bottom/)() | 获取形状所在包含块底部边缘的位置。 |
| [get_Bounds](../shapebase/get_bounds/)() | 获取或设置形状所在包含块的位置和大小。 |
| [get_BoundsInPoints](../shapebase/get_boundsinpoints/)() | 获取形状所在包含块的位置和大小（单位为点），相对于最上层形状的锚点。 |
| [get_BoundsWithEffects](../shapebase/get_boundswitheffects/)() | 获取此形状对象在应用绘图效果后最终的范围。值以点为单位。 |
| [get_CanHaveImage](../shapebase/get_canhaveimage/)() | 如果形状类型允许形状具有图像，则返回 **true**。 |
| [get_CoordOrigin](../shapebase/get_coordorigin/)() | 此形状的包含块左上角的坐标。 |
| [get_CoordSize](../shapebase/get_coordsize/)() | 此形状的包含块内部坐标空间的宽度和高度。 |
| [get_Count](../../aspose.words/compositenode/get_count/)() | 获取此节点的直接子节点数量。 |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | 指定自定义节点标识符。 |
| [get_DistanceBottom](../shapebase/get_distancebottom/)() | 返回或设置文档文本与形状底部边缘之间的距离（单位为点）。 |
| [get_DistanceLeft](../shapebase/get_distanceleft/)() | 返回或设置文档文本与形状左侧边缘之间的距离（单位为点）。 |
| [get_DistanceRight](../shapebase/get_distanceright/)() | 返回或设置文档文本与形状右侧边缘之间的距离（单位为点）。 |
| [get_DistanceTop](../shapebase/get_distancetop/)() | 返回或设置文档文本与形状顶部边缘之间的距离（单位为点）。 |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | 获取此节点所属的文档。 |
| [get_Fill](../shapebase/get_fill/)() | 获取形状的填充格式。 |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | 获取节点的第一个子节点。 |
| [get_FlipOrientation](../shapebase/get_fliporientation/)() | 切换形状的方向。 |
| [get_Font](../shapebase/get_font/)() | 提供对该对象字体格式的访问。 |
| [get_Glow](../shapebase/get_glow/)() | 获取形状的发光格式。 |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | 如果此节点有任何子节点，则返回 **true**。 |
| [get_Height](../shapebase/get_height/)() | 获取或设置形状包含块的高度。 |
| [get_HeightRelative](../shapebase/get_heightrelative/)() | 获取或设置表示形状相对高度百分比的值。 |
| [get_Hidden](../shapebase/get_hidden/)() | 获取或设置一个布尔值，指示形状是否可见。 |
| [get_HorizontalAlignment](../shapebase/get_horizontalalignment/)() | 指定形状的水平定位方式。 |
| [get_HRef](../shapebase/get_href/)() | 获取或设置形状的完整超链接地址。 |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | 因为此节点可以拥有子节点，返回 **true**。 |
| [get_IsDecorative](../shapebase/get_isdecorative/)() | 获取或设置指定形状在文档中是否为装饰性的标志。 |
| [get_IsDeleteRevision](../shapebase/get_isdeleterevision/)() | 如果在启用更改跟踪的 Microsoft Word 中删除了此对象，则返回 true。 |
| [get_IsGroup](../shapebase/get_isgroup/)() | 如果这是组形状，则返回 **true**。 |
| [get_IsHorizontalRule](../shapebase/get_ishorizontalrule/)() | 如果此形状是水平线，则返回 **true**。 |
| [get_IsImage](../shapebase/get_isimage/)() | 如果此形状是图像形状，则返回 **true**。 |
| [get_IsInline](../shapebase/get_isinline/)() | 一种快速判断此形状是否与文本内联定位的方法。 |
| [get_IsInsertRevision](../shapebase/get_isinsertrevision/)() | 如果在启用更改跟踪的 Microsoft Word 中插入了此对象，则返回 true。 |
| [get_IsLayoutInCell](../shapebase/get_islayoutincell/)() | 获取或设置指示形状是显示在表格内部还是外部的标志。 |
| [get_IsMoveFromRevision](../shapebase/get_ismovefromrevision/)() | 如果在启用更改跟踪的 Microsoft Word 中移动（删除）了此对象，则返回 **true**。 |
| [get_IsMoveToRevision](../shapebase/get_ismovetorevision/)() | 如果在启用更改跟踪的 Microsoft Word 中移动（插入）了此对象，则返回 **true**。 |
| [get_IsSignatureLine](../shapebase/get_issignatureline/)() | 指示该形状是一个 [SignatureLine](../signatureline/)。 |
| [get_IsTopLevel](../shapebase/get_istoplevel/)() | 如果此形状不是组形状的子形状，则返回 **true**。 |
| [get_IsWordArt](../shapebase/get_iswordart/)() | 如果此形状是 WordArt 对象，则返回 **true**。 |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | 获取节点的最后一个子节点。 |
| [get_Left](../shapebase/get_left/)() | 获取或设置形状所在包含块的左边缘位置。 |
| [get_LeftRelative](../shapebase/get_leftrelative/)() | 获取或设置表示形状相对左侧位置的百分比值。 |
| [get_MarkupLanguage](../shapebase/get_markuplanguage/)() const | 获取用于此图形对象的 MarkupLanguage。 |
| [get_Name](../shapebase/get_name/)() | 获取或设置可选的形状名称。 |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | 获取紧随此节点之后的节点。 |
| [get_NodeType](./get_nodetype/)() const override | 返回 [GroupShape](../../aspose.words/nodetype/)。 |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | 获取此节点的直接父节点。 |
| [get_ParentParagraph](../shapebase/get_parentparagraph/)() | 返回直接父段落。 |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | 获取紧挨此节点之前的节点。 |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | 返回一个表示包含在此节点中的文档部分的 [Range](../../aspose.words/range/) 对象。 |
| [get_Reflection](../shapebase/get_reflection/)() | 获取形状的反射格式设置。 |
| [get_RelativeHorizontalPosition](../shapebase/get_relativehorizontalposition/)() | 指定形状在水平方向上相对于何物进行定位。 |
| [get_RelativeHorizontalSize](../shapebase/get_relativehorizontalsize/)() | 获取或设置形状在水平方向上的相对大小值。 |
| [get_RelativeVerticalPosition](../shapebase/get_relativeverticalposition/)() | 指定形状在垂直方向上相对于何物进行定位。 |
| [get_RelativeVerticalSize](../shapebase/get_relativeverticalsize/)() | 获取或设置形状在垂直方向上的相对大小值。 |
| [get_Right](../shapebase/get_right/)() | 获取形状所在包含块的右边缘位置。 |
| [get_Rotation](../shapebase/get_rotation/)() | 定义形状旋转的角度（以度为单位）。正值对应顺时针旋转角度。 |
| [get_ScreenTip](../shapebase/get_screentip/)() | 定义鼠标指针悬停在形状上时显示的文本。 |
| [get_ShadowFormat](../shapebase/get_shadowformat/)() | 获取形状的阴影格式设置。 |
| [get_ShapeType](../shapebase/get_shapetype/)() | 获取形状类型。 |
| [get_SizeInPoints](../shapebase/get_sizeinpoints/)() | 获取形状的尺寸（以点为单位）。 |
| [get_SoftEdge](../shapebase/get_softedge/)() | 获取形状的柔化边缘格式设置。 |
| [get_Target](../shapebase/get_target/)() | 获取或设置形状超链接的目标框架。 |
| [get_Title](../shapebase/get_title/)() | 获取或设置当前形状对象的标题（说明）。 |
| [get_Top](../shapebase/get_top/)() | 获取或设置形状所在包含块的顶部边缘位置。 |
| [get_TopRelative](../shapebase/get_toprelative/)() | 获取或设置表示形状相对顶部位置的百分比值。 |
| [get_VerticalAlignment](../shapebase/get_verticalalignment/)() | 指定形状在垂直方向上的定位方式。 |
| [get_Width](../shapebase/get_width/)() | 获取或设置形状所在包含块的宽度。 |
| [get_WidthRelative](../shapebase/get_widthrelative/)() | 获取或设置表示形状相对宽度百分比的值。 |
| [get_WrapSide](../shapebase/get_wrapside/)() | 指定文本环绕形状的方式。 |
| [get_WrapType](../shapebase/get_wraptype/)() | 定义形状是内联还是浮动。对于浮动形状，定义文本环绕形状的换行模式。 |
| [get_ZOrder](../shapebase/get_zorder/)() | 确定重叠形状的显示顺序。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | 获取指定 [NodeType](../../aspose.words/nodetype/) 的第一个祖先节点。 |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | 返回匹配指定类型的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | 返回匹配指定类型的子节点的实时集合。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | 提供对该节点的子节点进行 foreach 样式迭代的支持。 |
| [GetShapeRenderer](../shapebase/getshaperenderer/)() | 创建并返回一个可用于将此形状渲染为图像的对象。 |
| [GetText](../../aspose.words/compositenode/gettext/)() override | 获取此节点及其所有子节点的文本。 |
| [GetType](./gettype/)() const override |  |
| [GroupShape](./groupshape/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | 创建一个新的组合形状。 |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 返回指定子节点在子节点数组中的索引。 |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [LocalToParent](../shapebase/localtoparent/)(System::Drawing::PointF) | 将值从本地坐标空间转换为父形状的坐标空间。 |
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
| [set_AllowOverlap](../shapebase/set_allowoverlap/)(bool) | 为 [Aspose::Words::Drawing::ShapeBase::get_AllowOverlap](../shapebase/get_allowoverlap/) 设置。 |
| [set_AlternativeText](../shapebase/set_alternativetext/)(const System::String\&) | 为 [Aspose::Words::Drawing::ShapeBase::get_AlternativeText](../shapebase/get_alternativetext/) 设置。 |
| [set_AnchorLocked](../shapebase/set_anchorlocked/)(bool) | 为 [Aspose::Words::Drawing::ShapeBase::get_AnchorLocked](../shapebase/get_anchorlocked/) 设置。 |
| [set_AspectRatioLocked](../shapebase/set_aspectratiolocked/)(bool) | 为 [Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked](../shapebase/get_aspectratiolocked/) 设置。 |
| [set_BehindText](../shapebase/set_behindtext/)(bool) | 为 [Aspose::Words::Drawing::ShapeBase::get_BehindText](../shapebase/get_behindtext/) 设置。 |
| [set_Bounds](../shapebase/set_bounds/)(System::Drawing::RectangleF) | 为 [Aspose::Words::Drawing::ShapeBase::get_Bounds](../shapebase/get_bounds/) 设置。 |
| [set_CoordOrigin](../shapebase/set_coordorigin/)(System::Drawing::Point) | 为 [Aspose::Words::Drawing::ShapeBase::get_CoordOrigin](../shapebase/get_coordorigin/) 设置。 |
| [set_CoordSize](../shapebase/set_coordsize/)(System::Drawing::Size) | 为 [Aspose::Words::Drawing::ShapeBase::get_CoordSize](../shapebase/get_coordsize/) 设置。 |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | 用于设置 [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/) 的 setter。 |
| [set_DistanceBottom](../shapebase/set_distancebottom/)(double) | 为 [Aspose::Words::Drawing::ShapeBase::get_DistanceBottom](../shapebase/get_distancebottom/) 设置。 |
| [set_DistanceLeft](../shapebase/set_distanceleft/)(double) | 为 [Aspose::Words::Drawing::ShapeBase::get_DistanceLeft](../shapebase/get_distanceleft/) 设置。 |
| [set_DistanceRight](../shapebase/set_distanceright/)(double) | 为 [Aspose::Words::Drawing::ShapeBase::get_DistanceRight](../shapebase/get_distanceright/) 设置。 |
| [set_DistanceTop](../shapebase/set_distancetop/)(double) | 为 [Aspose::Words::Drawing::ShapeBase::get_DistanceTop](../shapebase/get_distancetop/) 设置。 |
| [set_FlipOrientation](../shapebase/set_fliporientation/)(Aspose::Words::Drawing::FlipOrientation) | 为 [Aspose::Words::Drawing::ShapeBase::get_FlipOrientation](../shapebase/get_fliporientation/) 设置。 |
| [set_Height](../shapebase/set_height/)(double) | 为 [Aspose::Words::Drawing::ShapeBase::get_Height](../shapebase/get_height/) 设置。 |
| [set_HeightRelative](../shapebase/set_heightrelative/)(float) | 为 [Aspose::Words::Drawing::ShapeBase::get_HeightRelative](../shapebase/get_heightrelative/) 设置。 |
| [set_Hidden](../shapebase/set_hidden/)(bool) | 为 [Aspose::Words::Drawing::ShapeBase::get_Hidden](../shapebase/get_hidden/) 设置。 |
| [set_HorizontalAlignment](../shapebase/set_horizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | 为 [Aspose::Words::Drawing::ShapeBase::get_HorizontalAlignment](../shapebase/get_horizontalalignment/) 设置。 |
| [set_HRef](../shapebase/set_href/)(const System::String\&) | 为 [Aspose::Words::Drawing::ShapeBase::get_HRef](../shapebase/get_href/) 设置。 |
| [set_IsDecorative](../shapebase/set_isdecorative/)(bool) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_IsDecorative](../shapebase/get_isdecorative/)。 |
| [set_IsLayoutInCell](../shapebase/set_islayoutincell/)(bool) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell](../shapebase/get_islayoutincell/)。 |
| [set_Left](../shapebase/set_left/)(double) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_Left](../shapebase/get_left/)。 |
| [set_LeftRelative](../shapebase/set_leftrelative/)(float) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_LeftRelative](../shapebase/get_leftrelative/)。 |
| [set_Name](../shapebase/set_name/)(const System::String\&) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_Name](../shapebase/get_name/)。 |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_RelativeHorizontalPosition](../shapebase/set_relativehorizontalposition/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition](../shapebase/get_relativehorizontalposition/)。 |
| [set_RelativeHorizontalSize](../shapebase/set_relativehorizontalsize/)(Aspose::Words::Drawing::RelativeHorizontalSize) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize](../shapebase/get_relativehorizontalsize/)。 |
| [set_RelativeVerticalPosition](../shapebase/set_relativeverticalposition/)(Aspose::Words::Drawing::RelativeVerticalPosition) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition](../shapebase/get_relativeverticalposition/)。 |
| [set_RelativeVerticalSize](../shapebase/set_relativeverticalsize/)(Aspose::Words::Drawing::RelativeVerticalSize) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalSize](../shapebase/get_relativeverticalsize/)。 |
| [set_Rotation](../shapebase/set_rotation/)(double) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_Rotation](../shapebase/get_rotation/)。 |
| [set_ScreenTip](../shapebase/set_screentip/)(const System::String\&) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_ScreenTip](../shapebase/get_screentip/)。 |
| [set_Target](../shapebase/set_target/)(const System::String\&) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_Target](../shapebase/get_target/)。 |
| [set_Title](../shapebase/set_title/)(const System::String\&) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_Title](../shapebase/get_title/)。 |
| [set_Top](../shapebase/set_top/)(double) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_Top](../shapebase/get_top/)。 |
| [set_TopRelative](../shapebase/set_toprelative/)(float) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_TopRelative](../shapebase/get_toprelative/)。 |
| [set_VerticalAlignment](../shapebase/set_verticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment](../shapebase/get_verticalalignment/)。 |
| [set_Width](../shapebase/set_width/)(double) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_Width](../shapebase/get_width/)。 |
| [set_WidthRelative](../shapebase/set_widthrelative/)(float) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_WidthRelative](../shapebase/get_widthrelative/)。 |
| [set_WrapSide](../shapebase/set_wrapside/)(Aspose::Words::Drawing::WrapSide) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_WrapSide](../shapebase/get_wrapside/)。 |
| [set_WrapType](../shapebase/set_wraptype/)(Aspose::Words::Drawing::WrapType) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_WrapType](../shapebase/get_wraptype/)。 |
| [set_ZOrder](../shapebase/set_zorder/)(int32_t) | 用于设置 [Aspose::Words::Drawing::ShapeBase::get_ZOrder](../shapebase/get_zorder/)。 |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | 以指定格式将节点内容导出为字符串。 |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的保存选项将节点内容导出为字符串。 |
| static [Type](./type/)() |  |
## 备注


一个 [GroupShape](./) 是复合节点，并且可以拥有 [Shape](../shape/) 和 [GroupShape](./) 节点作为子节点。

每个 [GroupShape](./) 为其子形状定义一个新的坐标系。坐标系使用 [CoordSize](../shapebase/get_coordsize/) 和 [CoordOrigin](../shapebase/get_coordorigin/) 属性定义。

## 另见

* Class [ShapeBase](../shapebase/)
* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
