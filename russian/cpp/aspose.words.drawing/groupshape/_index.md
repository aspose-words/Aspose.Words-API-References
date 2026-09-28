---
title: "Aspose::Words::Drawing::GroupShape class"
linktitle: "GroupShape"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::GroupShape class. Представляет группу фигур в документе. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.drawing/groupshape/
---
## GroupShape class


Представляет группу фигур в документе. Чтобы узнать больше, посетите статью документации [How to Add Group Shape into a Word Document](https://docs.aspose.com/words/cpp/how-to-add-group-shape-into-a-word-document/).

```cpp
class GroupShape : public Aspose::Words::Drawing::ShapeBase
```

## Методы

| Метод | Описание |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя для посещения конца [GroupShape](./). |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя для посещения начала [GroupShape](./). |
| [AdjustWithEffects](../shapebase/adjustwitheffects/)(System::Drawing::RectangleF) | Добавляет к исходному прямоугольнику значения области эффекта и возвращает конечный прямоугольник. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Создаёт дубликат узла. |
| [get_AllowOverlap](../shapebase/get_allowoverlap/)() | Получает или задает значение, указывающее, может ли эта фигура перекрывать другие фигуры. |
| [get_AlternativeText](../shapebase/get_alternativetext/)() | Определяет альтернативный текст, отображаемый вместо графики. |
| [get_AnchorLocked](../shapebase/get_anchorlocked/)() | Указывает, зафиксирован ли якорь фигуры. |
| [get_AspectRatioLocked](../shapebase/get_aspectratiolocked/)() | Указывает, зафиксировано ли соотношение сторон фигуры. |
| [get_BehindText](../shapebase/get_behindtext/)() | Указывает, находится ли фигура ниже или выше текста. |
| [get_Bottom](../shapebase/get_bottom/)() | Получает позицию нижнего края содержащего блока фигуры. |
| [get_Bounds](../shapebase/get_bounds/)() | Получает или задает расположение и размер содержащего блока фигуры. |
| [get_BoundsInPoints](../shapebase/get_boundsinpoints/)() | Получает расположение и размер содержащего блока фигуры в пунктах, относительно якоря самой верхней фигуры. |
| [get_BoundsWithEffects](../shapebase/get_boundswitheffects/)() | Получает окончательный размер этого объекта фигуры после применения эффектов рисования. Значение измеряется в пунктах. |
| [get_CanHaveImage](../shapebase/get_canhaveimage/)() | Возвращает **true**, если тип фигуры позволяет ей иметь изображение. |
| [get_CoordOrigin](../shapebase/get_coordorigin/)() | Координаты в левом верхнем углу содержащего блока этой фигуры. |
| [get_CoordSize](../shapebase/get_coordsize/)() | Ширина и высота координатного пространства внутри содержащего блока этой фигуры. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Возвращает количество непосредственных дочерних элементов этого узла. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Указывает пользовательский идентификатор узла. |
| [get_DistanceBottom](../shapebase/get_distancebottom/)() | Возвращает или задает расстояние (в пунктах) между текстом документа и нижним краем фигуры. |
| [get_DistanceLeft](../shapebase/get_distanceleft/)() | Возвращает или задает расстояние (в пунктах) между текстом документа и левым краем фигуры. |
| [get_DistanceRight](../shapebase/get_distanceright/)() | Возвращает или задает расстояние (в пунктах) между текстом документа и правым краем фигуры. |
| [get_DistanceTop](../shapebase/get_distancetop/)() | Возвращает или задает расстояние (в пунктах) между текстом документа и верхним краем фигуры. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Возвращает документ, к которому принадлежит этот узел. |
| [get_Fill](../shapebase/get_fill/)() | Получает формат заливки для фигуры. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Возвращает первого дочернего узла. |
| [get_FlipOrientation](../shapebase/get_fliporientation/)() | Изменяет ориентацию фигуры. |
| [get_Font](../shapebase/get_font/)() | Предоставляет доступ к форматированию шрифта этого объекта. |
| [get_Glow](../shapebase/get_glow/)() | Получает формат свечения для фигуры. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Возвращает **true**, если у этого узла есть дочерние узлы. |
| [get_Height](../shapebase/get_height/)() | Получает или задает высоту содержащего блока фигуры. |
| [get_HeightRelative](../shapebase/get_heightrelative/)() | Получает или задает значение, представляющее процент относительной высоты фигуры. |
| [get_Hidden](../shapebase/get_hidden/)() | Получает или задает логическое значение, указывающее, видима ли фигура. |
| [get_HorizontalAlignment](../shapebase/get_horizontalalignment/)() | Указывает, как фигура позиционируется по горизонтали. |
| [get_HRef](../shapebase/get_href/)() | Получает или задает полный адрес гиперссылки для фигуры. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Возвращает **true**, поскольку этот узел может иметь дочерние узлы. |
| [get_IsDecorative](../shapebase/get_isdecorative/)() | Получает или задает флаг, указывающий, является ли фигура декоративной в документе. |
| [get_IsDeleteRevision](../shapebase/get_isdeleterevision/)() | Возвращает true, если этот объект был удалён в Microsoft Word при включённом отслеживании изменений. |
| [get_IsGroup](../shapebase/get_isgroup/)() | Возвращает **true**, если это групповая фигура. |
| [get_IsHorizontalRule](../shapebase/get_ishorizontalrule/)() | Возвращает **true**, если эта фигура является горизонтальной линией. |
| [get_IsImage](../shapebase/get_isimage/)() | Возвращает **true**, если эта фигура является изображением. |
| [get_IsInline](../shapebase/get_isinline/)() | Быстрый способ определить, позиционирована ли эта фигура в строке с текстом. |
| [get_IsInsertRevision](../shapebase/get_isinsertrevision/)() | Возвращает true, если этот объект был вставлен в Microsoft Word при включённом отслеживании изменений. |
| [get_IsLayoutInCell](../shapebase/get_islayoutincell/)() | Получает или задает флаг, указывающий, отображается ли фигура внутри таблицы или снаружи. |
| [get_IsMoveFromRevision](../shapebase/get_ismovefromrevision/)() | Возвращает **true**, если этот объект был перемещён (удалён) в Microsoft Word при включённом отслеживании изменений. |
| [get_IsMoveToRevision](../shapebase/get_ismovetorevision/)() | Возвращает **true**, если этот объект был перемещён (вставлен) в Microsoft Word при включённом отслеживании изменений. |
| [get_IsSignatureLine](../shapebase/get_issignatureline/)() | Указывает, что фигура является [SignatureLine](../signatureline/). |
| [get_IsTopLevel](../shapebase/get_istoplevel/)() | Возвращает **true**, если эта фигура не является дочерней для групповой фигуры. |
| [get_IsWordArt](../shapebase/get_iswordart/)() | Возвращает **true**, если эта фигура является объектом WordArt. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Возвращает последнего дочернего узла. |
| [get_Left](../shapebase/get_left/)() | Получает или задает позицию левого края содержащего блока фигуры. |
| [get_LeftRelative](../shapebase/get_leftrelative/)() | Получает или задает значение, представляющее относительное левое положение фигуры в процентах. |
| [get_MarkupLanguage](../shapebase/get_markuplanguage/)() const | Получает MarkupLanguage, используемый для этого графического объекта. |
| [get_Name](../shapebase/get_name/)() | Получает или задает необязательное имя фигуры. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Возвращает узел, непосредственно следующий за этим узлом. |
| [get_NodeType](./get_nodetype/)() const override | Возвращает [GroupShape](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Возвращает непосредственного родителя этого узла. |
| [get_ParentParagraph](../shapebase/get_parentparagraph/)() | Возвращает непосредственный родительский абзац. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Возвращает узел, непосредственно предшествующий этому узлу. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Возвращает объект [Range](../../aspose.words/range/), представляющий часть документа, содержащуюся в этом узле. |
| [get_Reflection](../shapebase/get_reflection/)() | Получает форматирование отражения для фигуры. |
| [get_RelativeHorizontalPosition](../shapebase/get_relativehorizontalposition/)() | Указывает, относительно чего фигура позиционируется по горизонтали. |
| [get_RelativeHorizontalSize](../shapebase/get_relativehorizontalsize/)() | Получает или задает значение относительного размера фигуры в горизонтальном направлении. |
| [get_RelativeVerticalPosition](../shapebase/get_relativeverticalposition/)() | Указывает, относительно чего фигура позиционируется по вертикали. |
| [get_RelativeVerticalSize](../shapebase/get_relativeverticalsize/)() | Получает или задает значение относительного размера фигуры в вертикальном направлении. |
| [get_Right](../shapebase/get_right/)() | Получает позицию правого края содержащего блока фигуры. |
| [get_Rotation](../shapebase/get_rotation/)() | Определяет угол (в градусах), на который повернута фигура. Положительное значение соответствует углу вращения по часовой стрелке. |
| [get_ScreenTip](../shapebase/get_screentip/)() | Определяет текст, отображаемый при наведении указателя мыши на фигуру. |
| [get_ShadowFormat](../shapebase/get_shadowformat/)() | Получает форматирование тени для фигуры. |
| [get_ShapeType](../shapebase/get_shapetype/)() | Получает тип фигуры. |
| [get_SizeInPoints](../shapebase/get_sizeinpoints/)() | Получает размер фигуры в пунктах. |
| [get_SoftEdge](../shapebase/get_softedge/)() | Получает форматирование мягких краёв для фигуры. |
| [get_Target](../shapebase/get_target/)() | Получает или задаёт целевой фрейм для гиперссылки фигуры. |
| [get_Title](../shapebase/get_title/)() | Получает или задаёт заголовок (подпись) текущего объекта фигуры. |
| [get_Top](../shapebase/get_top/)() | Получает или задаёт позицию верхнего края содержащего блока фигуры. |
| [get_TopRelative](../shapebase/get_toprelative/)() | Получает или задаёт значение, представляющее относительное верхнее положение фигуры в процентах. |
| [get_VerticalAlignment](../shapebase/get_verticalalignment/)() | Указывает, как фигура позиционируется вертикально. |
| [get_Width](../shapebase/get_width/)() | Получает или задаёт ширину содержащего блока фигуры. |
| [get_WidthRelative](../shapebase/get_widthrelative/)() | Получает или задаёт значение, представляющее процент относительной ширины фигуры. |
| [get_WrapSide](../shapebase/get_wrapside/)() | Указывает, как текст обтекает фигуру. |
| [get_WrapType](../shapebase/get_wraptype/)() | Определяет, является ли фигура встроенной или плавающей. Для плавающих фигур определяет режим обтекания текста вокруг фигуры. |
| [get_ZOrder](../shapebase/get_zorder/)() | Определяет порядок отображения перекрывающихся фигур. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Возвращает первого предка указанного [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Возвращает N‑й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Обеспечивает поддержку итерации в стиле foreach по дочерним узлам этого узла. |
| [GetShapeRenderer](../shapebase/getshaperenderer/)() | Создаёт и возвращает объект, который можно использовать для отрисовки этой фигуры в изображение. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Получает текст этого узла и всех его дочерних узлов. |
| [GetType](./gettype/)() const override |  |
| [GroupShape](./groupshape/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Создаёт новую групповую фигуру. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [LocalToParent](../shapebase/localtoparent/)(System::Drawing::PointF) | Преобразует значение из локального пространства координат в пространство координат родительской фигуры. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает следующий узел согласно алгоритму обхода дерева в порядке предобхода. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Вспомогательный метод, преобразующий значение перечисления типа узла в удобочитаемую строку. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает предыдущий узел согласно алгоритму обхода дерева в порядке предобхода. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя из родительского узла. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Удаляет все дочерние узлы [SmartTag](../../aspose.words.markup/smarttag/) текущего узла. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Выбирает список узлов, соответствующих XPath-выражению. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Выбирает первый [Node](../../aspose.words/node/), соответствующий XPath-выражению. |
| [set_AllowOverlap](../shapebase/set_allowoverlap/)(bool) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_AllowOverlap](../shapebase/get_allowoverlap/). |
| [set_AlternativeText](../shapebase/set_alternativetext/)(const System::String\&) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_AlternativeText](../shapebase/get_alternativetext/). |
| [set_AnchorLocked](../shapebase/set_anchorlocked/)(bool) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_AnchorLocked](../shapebase/get_anchorlocked/). |
| [set_AspectRatioLocked](../shapebase/set_aspectratiolocked/)(bool) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked](../shapebase/get_aspectratiolocked/). |
| [set_BehindText](../shapebase/set_behindtext/)(bool) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_BehindText](../shapebase/get_behindtext/). |
| [set_Bounds](../shapebase/set_bounds/)(System::Drawing::RectangleF) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_Bounds](../shapebase/get_bounds/). |
| [set_CoordOrigin](../shapebase/set_coordorigin/)(System::Drawing::Point) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_CoordOrigin](../shapebase/get_coordorigin/). |
| [set_CoordSize](../shapebase/set_coordsize/)(System::Drawing::Size) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_CoordSize](../shapebase/get_coordsize/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Сеттер для [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_DistanceBottom](../shapebase/set_distancebottom/)(double) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_DistanceBottom](../shapebase/get_distancebottom/). |
| [set_DistanceLeft](../shapebase/set_distanceleft/)(double) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_DistanceLeft](../shapebase/get_distanceleft/). |
| [set_DistanceRight](../shapebase/set_distanceright/)(double) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_DistanceRight](../shapebase/get_distanceright/). |
| [set_DistanceTop](../shapebase/set_distancetop/)(double) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_DistanceTop](../shapebase/get_distancetop/). |
| [set_FlipOrientation](../shapebase/set_fliporientation/)(Aspose::Words::Drawing::FlipOrientation) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_FlipOrientation](../shapebase/get_fliporientation/). |
| [set_Height](../shapebase/set_height/)(double) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_Height](../shapebase/get_height/). |
| [set_HeightRelative](../shapebase/set_heightrelative/)(float) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_HeightRelative](../shapebase/get_heightrelative/). |
| [set_Hidden](../shapebase/set_hidden/)(bool) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_Hidden](../shapebase/get_hidden/). |
| [set_HorizontalAlignment](../shapebase/set_horizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_HorizontalAlignment](../shapebase/get_horizontalalignment/). |
| [set_HRef](../shapebase/set_href/)(const System::String\&) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_HRef](../shapebase/get_href/). |
| [set_IsDecorative](../shapebase/set_isdecorative/)(bool) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_IsDecorative](../shapebase/get_isdecorative/). |
| [set_IsLayoutInCell](../shapebase/set_islayoutincell/)(bool) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell](../shapebase/get_islayoutincell/). |
| [set_Left](../shapebase/set_left/)(double) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_Left](../shapebase/get_left/). |
| [set_LeftRelative](../shapebase/set_leftrelative/)(float) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_LeftRelative](../shapebase/get_leftrelative/). |
| [set_Name](../shapebase/set_name/)(const System::String\&) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_Name](../shapebase/get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_RelativeHorizontalPosition](../shapebase/set_relativehorizontalposition/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition](../shapebase/get_relativehorizontalposition/). |
| [set_RelativeHorizontalSize](../shapebase/set_relativehorizontalsize/)(Aspose::Words::Drawing::RelativeHorizontalSize) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize](../shapebase/get_relativehorizontalsize/). |
| [set_RelativeVerticalPosition](../shapebase/set_relativeverticalposition/)(Aspose::Words::Drawing::RelativeVerticalPosition) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition](../shapebase/get_relativeverticalposition/). |
| [set_RelativeVerticalSize](../shapebase/set_relativeverticalsize/)(Aspose::Words::Drawing::RelativeVerticalSize) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalSize](../shapebase/get_relativeverticalsize/). |
| [set_Rotation](../shapebase/set_rotation/)(double) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_Rotation](../shapebase/get_rotation/). |
| [set_ScreenTip](../shapebase/set_screentip/)(const System::String\&) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_ScreenTip](../shapebase/get_screentip/). |
| [set_Target](../shapebase/set_target/)(const System::String\&) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_Target](../shapebase/get_target/). |
| [set_Title](../shapebase/set_title/)(const System::String\&) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_Title](../shapebase/get_title/). |
| [set_Top](../shapebase/set_top/)(double) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_Top](../shapebase/get_top/). |
| [set_TopRelative](../shapebase/set_toprelative/)(float) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_TopRelative](../shapebase/get_toprelative/). |
| [set_VerticalAlignment](../shapebase/set_verticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment](../shapebase/get_verticalalignment/). |
| [set_Width](../shapebase/set_width/)(double) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_Width](../shapebase/get_width/). |
| [set_WidthRelative](../shapebase/set_widthrelative/)(float) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_WidthRelative](../shapebase/get_widthrelative/). |
| [set_WrapSide](../shapebase/set_wrapside/)(Aspose::Words::Drawing::WrapSide) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_WrapSide](../shapebase/get_wrapside/). |
| [set_WrapType](../shapebase/set_wraptype/)(Aspose::Words::Drawing::WrapType) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_WrapType](../shapebase/get_wraptype/). |
| [set_ZOrder](../shapebase/set_zorder/)(int32_t) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_ZOrder](../shapebase/get_zorder/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| static [Type](./type/)() |  |
## Примечания


Объект [GroupShape](./) является составным узлом и может иметь дочерние узлы [Shape](../shape/) и [GroupShape](./).

Каждый [GroupShape](./) определяет новую систему координат для своих дочерних фигур. Система координат задаётся с помощью свойств [CoordSize](../shapebase/get_coordsize/) и [CoordOrigin](../shapebase/get_coordorigin/).

## См. также

* Class [ShapeBase](../shapebase/)
* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
