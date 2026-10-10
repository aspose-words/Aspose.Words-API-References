---
title: "Aspose::Words::Drawing::Shape 类"
linktitle: "形状"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Shape 类。表示绘图层中的对象，例如 AutoShape、textbox、freeform、OLE object、ActiveX control 或 picture。要了解更多，请访问 C++ 中的文档文章。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words.drawing/shape/
---
## Shape class


表示绘图层中的对象，例如 AutoShape、文本框、自由形状、OLE 对象、ActiveX 控件或图片。要了解更多信息，请访问 [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/) 文档文章。

```cpp
class Shape : public Aspose::Words::Drawing::ShapeBase,
              public Aspose::Words::Drawing::Core::ITextBox,
              public Aspose::Words::Drawing::Core::IStrokable
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者。 |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者以访问形状的结束端。 |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者以访问形状的起始端。 |
| [AdjustWithEffects](../shapebase/adjustwitheffects/)(System::Drawing::RectangleF) | 将效果范围的值添加到源矩形，并返回最终矩形。 |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | 创建节点的副本。 |
| [get_Adjustments](./get_adjustments/)() | 提供对形状的调整原始值的访问。对于不包含任何调整原始值的形状，它返回空集合。 |
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
| [get_Chart](./get_chart/)() | 如果此形状具有[Chart](../../aspose.words.drawing.charts/chart/)，则提供对图表属性的访问。 |
| [get_CoordOrigin](../shapebase/get_coordorigin/)() | 此形状的包含块左上角的坐标。 |
| [get_CoordSize](../shapebase/get_coordsize/)() | 此形状的包含块内部坐标空间的宽度和高度。 |
| [get_Count](../../aspose.words/compositenode/get_count/)() | 获取此节点的直接子节点数量。 |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | 指定自定义节点标识符。 |
| [get_DistanceBottom](../shapebase/get_distancebottom/)() | 返回或设置文档文本与形状底部边缘之间的距离（单位为点）。 |
| [get_DistanceLeft](../shapebase/get_distanceleft/)() | 返回或设置文档文本与形状左侧边缘之间的距离（单位为点）。 |
| [get_DistanceRight](../shapebase/get_distanceright/)() | 返回或设置文档文本与形状右侧边缘之间的距离（单位为点）。 |
| [get_DistanceTop](../shapebase/get_distancetop/)() | 返回或设置文档文本与形状顶部边缘之间的距离（单位为点）。 |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | 获取此节点所属的文档。 |
| [get_ExtrusionEnabled](./get_extrusionenabled/)() | 如果已启用挤压效果，则返回 **true**。 |
| [get_Fill](../shapebase/get_fill/)() | 获取形状的填充格式。 |
| [get_FillColor](./get_fillcolor/)() | 定义填充形状闭合路径的画笔颜色。 |
| [get_Filled](./get_filled/)() | 确定是否填充形状的闭合路径。 |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | 获取节点的第一个子节点。 |
| [get_FirstParagraph](./get_firstparagraph/)() | 获取形状中的第一段。 |
| [get_FlipOrientation](../shapebase/get_fliporientation/)() | 切换形状的方向。 |
| [get_Font](../shapebase/get_font/)() | 提供对该对象字体格式的访问。 |
| [get_Glow](../shapebase/get_glow/)() | 获取形状的发光格式。 |
| [get_HasChart](./get_haschart/)() | 如果此[Shape](./)具有[Chart](../../aspose.words.drawing.charts/chart/)，则返回 **true**。 |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | 如果此节点有任何子节点，则返回 **true**。 |
| [get_HasImage](./get_hasimage/)() | 如果形状具有图像字节或链接了图像，则返回 **true**。 |
| [get_HasSmartArt](./get_hassmartart/)() | 如果此[Shape](./)具有 SmartArt 对象，则返回 **true**。 |
| [get_Height](../shapebase/get_height/)() | 获取或设置形状包含块的高度。 |
| [get_HeightRelative](../shapebase/get_heightrelative/)() | 获取或设置表示形状相对高度百分比的值。 |
| [get_Hidden](../shapebase/get_hidden/)() | 获取或设置一个布尔值，指示形状是否可见。 |
| [get_HorizontalAlignment](../shapebase/get_horizontalalignment/)() | 指定形状的水平定位方式。 |
| [get_HorizontalRuleFormat](./get_horizontalruleformat/)() | 提供对水平线形状属性的访问。对于不是水平线的形状，返回 **null**。 |
| [get_HRef](../shapebase/get_href/)() | 获取或设置形状的完整超链接地址。 |
| [get_ImageData](./get_imagedata/)() | 提供对形状图像的访问。如果形状无法拥有图像，则返回 **null**。 |
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
| [get_LastParagraph](./get_lastparagraph/)() | 获取形状中的最后一段。 |
| [get_Left](../shapebase/get_left/)() | 获取或设置形状所在包含块的左边缘位置。 |
| [get_LeftRelative](../shapebase/get_leftrelative/)() | 获取或设置表示形状相对左侧位置的百分比值。 |
| [get_MarkupLanguage](../shapebase/get_markuplanguage/)() const | 获取用于此图形对象的 MarkupLanguage。 |
| [get_Name](../shapebase/get_name/)() | 获取或设置可选的形状名称。 |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | 获取紧随此节点之后的节点。 |
| [get_NodeType](./get_nodetype/)() const override | 返回 [Shape](../../aspose.words/nodetype/)。 |
| [get_OleFormat](./get_oleformat/)() | 提供对形状的 OLE 数据的访问。对于不是 OLE 对象或 ActiveX 控件的形状，返回 **null**。 |
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
| [get_ShadowEnabled](./get_shadowenabled/)() | 如果启用了阴影效果，则返回 **true**。 |
| [get_ShadowFormat](../shapebase/get_shadowformat/)() | 获取形状的阴影格式设置。 |
| [get_ShapeType](../shapebase/get_shapetype/)() | 获取形状类型。 |
| [get_SignatureLine](./get_signatureline/)() | 如果形状是签名线，则获取 [SignatureLine](../signatureline/) 对象。否则返回 **null**。 |
| [get_SizeInPoints](../shapebase/get_sizeinpoints/)() | 获取形状的尺寸（以点为单位）。 |
| [get_SoftEdge](../shapebase/get_softedge/)() | 获取形状的柔化边缘格式设置。 |
| [get_StoryType](./get_storytype/)() | 返回 [Textbox](../../aspose.words/storytype/)。 |
| [get_Stroke](./get_stroke/)() | 为形状定义描边。 |
| [get_StrokeColor](./get_strokecolor/)() | 定义描边的颜色。 |
| [get_Stroked](./get_stroked/)() | 定义路径是否将被描边。 |
| [get_StrokeWeight](./get_strokeweight/)() | 定义以点为单位描绘形状路径的笔刷粗细。 |
| [get_Target](../shapebase/get_target/)() | 获取或设置形状超链接的目标框架。 |
| [get_TextBox](./get_textbox/)() | 定义指定文本在形状中显示方式的属性。 |
| [get_TextPath](./get_textpath/)() | 定义文本路径（WordArt 对象）的文本。 |
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
| [set_FillColor](./set_fillcolor/)(System::Drawing::Color) | 用于设置 [Aspose::Words::Drawing::Shape::get_FillColor](./get_fillcolor/) 的 setter。 |
| [set_Filled](./set_filled/)(bool) | 用于设置 [Aspose::Words::Drawing::Shape::get_Filled](./get_filled/) 的 setter。 |
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
| [set_StrokeColor](./set_strokecolor/)(System::Drawing::Color) | 用于设置 [Aspose::Words::Drawing::Shape::get_StrokeColor](./get_strokecolor/) 的 setter。 |
| [set_Stroked](./set_stroked/)(bool) | 用于设置 [Aspose::Words::Drawing::Shape::get_Stroked](./get_stroked/) 的 setter。 |
| [set_StrokeWeight](./set_strokeweight/)(double) | 用于设置 [Aspose::Words::Drawing::Shape::get_StrokeWeight](./get_strokeweight/) 的 setter。 |
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
| [Shape](./shape/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::Drawing::ShapeType) | 创建一个新的形状对象。 |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | 以指定格式将节点内容导出为字符串。 |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的保存选项将节点内容导出为字符串。 |
| static [Type](./type/)() |  |
| [UpdateSmartArtDrawing](./updatesmartartdrawing/)() | 通过使用 [Aspose.Words](../../aspose.words/) 的 SmartArt 冷渲染引擎来更新 SmartArt 预渲染绘图。 |
## 备注


使用 [Shape](./) 类，您可以在 Microsoft Word 文档中创建或修改形状。

形状的一个重要属性是其 [ShapeType](../shapebase/get_shapetype/)。不同类型的形状在 Word 文档中可能具有不同的功能。例如，只有图像和 OLE 形状可以在其中包含图像。大多数形状可以包含文本，但并非全部。

能够包含文本的形状，可以包含 [Paragraph](../../aspose.words/paragraph/) 和 [Table](../../aspose.words.tables/table/) 节点作为子节点。

## 示例



展示如何从文档中提取图像，并将它们保存为本地文件系统中的单独文件。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// 从文档中获取形状集合，
// 并将每个包含图像的形状的图像数据保存为本地文件系统中的文件。
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);

ASSERT_EQ(9, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> s)>>([](System::SharedPtr<Aspose::Words::Node> s) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Drawing::Shape>(s))->get_HasImage();
}))));

int32_t imageIndex = 0;
for (auto&& shape : System::IterateOver(shapes->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    if (shape->get_HasImage())
    {
        // 形状的图像数据可能包含多种可能的图像格式。
        // 我们可以根据图像的格式自动确定每个图像的文件扩展名。
        System::String imageFileName = System::String::Format(u"File.ExtractImages.{0}{1}", imageIndex, Aspose::Words::FileFormatUtil::ImageTypeToExtension(shape->get_ImageData()->get_ImageType()));
        shape->get_ImageData()->Save(get_ArtifactsDir() + imageFileName);
        imageIndex++;
    }
}
```


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


展示如何从文档中删除所有形状。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入两个形状以及一个包含另一个形状的组形状。
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 400, 200);
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Star, 300, 300);

auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->set_Bounds(System::Drawing::RectangleF(100.0f, 50.0f, 200.0f, 100.0f));
group->set_CoordOrigin(System::Drawing::Point(-1000, -500));

auto subShape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Cube);
subShape->set_Width(500);
subShape->set_Height(700);
subShape->set_Left(0);
subShape->set_Top(0);

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(subShape);
builder->InsertNode(group);

ASSERT_EQ(3, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
ASSERT_EQ(1, doc->GetChildNodes(Aspose::Words::NodeType::GroupShape, true)->get_Count());

// 从文档中移除所有 Shape 节点。
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);
shapes->Clear();

// 所有形状已被删除，但组形状仍然在文档中。
ASSERT_EQ(1, doc->GetChildNodes(Aspose::Words::NodeType::GroupShape, true)->get_Count());
ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// 单独移除所有组形状。
System::SharedPtr<Aspose::Words::NodeCollection> groupShapes = doc->GetChildNodes(Aspose::Words::NodeType::GroupShape, true);
groupShapes->Clear();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::GroupShape, true)->get_Count());
ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## 另见

* Class [ShapeBase](../shapebase/)
* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
