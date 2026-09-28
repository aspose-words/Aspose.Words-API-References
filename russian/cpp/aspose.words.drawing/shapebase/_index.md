---
title: "Aspose::Words::Drawing::ShapeBase class"
linktitle: "ShapeBase"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ShapeBase class. Базовый класс для объектов в слое рисования, таких как AutoShape, свободная форма, объект OLE, элемент управления ActiveX или изображение. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words.drawing/shapebase/
---
## ShapeBase class


Базовый класс для объектов в слое рисования, таких как AutoShape, произвольная форма, OLE‑объект, элемент управления ActiveX или изображение. Чтобы узнать больше, посетите статью документации [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/) .

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

## Методы

| Метод | Описание |
| --- | --- |
| virtual [Accept](../../aspose.words/node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Принимает посетителя. |
| virtual [AcceptEnd](../../aspose.words/compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Когда реализовано в производном классе, вызывает метод VisitXXXEnd указанного посетителя документа. |
| virtual [AcceptStart](../../aspose.words/compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Когда реализовано в производном классе, вызывает метод VisitXXXStart указанного посетителя документа. |
| [AdjustWithEffects](./adjustwitheffects/)(System::Drawing::RectangleF) | Добавляет к исходному прямоугольнику значения области эффекта и возвращает конечный прямоугольник. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Создаёт дубликат узла. |
| [get_AllowOverlap](./get_allowoverlap/)() | Получает или задает значение, указывающее, может ли эта фигура перекрывать другие фигуры. |
| [get_AlternativeText](./get_alternativetext/)() | Определяет альтернативный текст, отображаемый вместо графики. |
| [get_AnchorLocked](./get_anchorlocked/)() | Указывает, зафиксирован ли якорь фигуры. |
| [get_AspectRatioLocked](./get_aspectratiolocked/)() | Указывает, зафиксировано ли соотношение сторон фигуры. |
| [get_BehindText](./get_behindtext/)() | Указывает, находится ли фигура ниже или выше текста. |
| [get_Bottom](./get_bottom/)() | Получает позицию нижнего края содержащего блока фигуры. |
| [get_Bounds](./get_bounds/)() | Получает или задает расположение и размер содержащего блока фигуры. |
| [get_BoundsInPoints](./get_boundsinpoints/)() | Получает расположение и размер содержащего блока фигуры в пунктах, относительно якоря самой верхней фигуры. |
| [get_BoundsWithEffects](./get_boundswitheffects/)() | Получает окончательный размер этого объекта фигуры после применения эффектов рисования. Значение измеряется в пунктах. |
| [get_CanHaveImage](./get_canhaveimage/)() | Возвращает **true**, если тип фигуры позволяет ей иметь изображение. |
| [get_CoordOrigin](./get_coordorigin/)() | Координаты в левом верхнем углу содержащего блока этой фигуры. |
| [get_CoordSize](./get_coordsize/)() | Ширина и высота координатного пространства внутри содержащего блока этой фигуры. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Возвращает количество непосредственных дочерних элементов этого узла. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Указывает пользовательский идентификатор узла. |
| [get_DistanceBottom](./get_distancebottom/)() | Возвращает или задает расстояние (в пунктах) между текстом документа и нижним краем фигуры. |
| [get_DistanceLeft](./get_distanceleft/)() | Возвращает или задает расстояние (в пунктах) между текстом документа и левым краем фигуры. |
| [get_DistanceRight](./get_distanceright/)() | Возвращает или задает расстояние (в пунктах) между текстом документа и правым краем фигуры. |
| [get_DistanceTop](./get_distancetop/)() | Возвращает или задает расстояние (в пунктах) между текстом документа и верхним краем фигуры. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Возвращает документ, к которому принадлежит этот узел. |
| [get_Fill](./get_fill/)() | Получает формат заливки для фигуры. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Возвращает первого дочернего узла. |
| [get_FlipOrientation](./get_fliporientation/)() | Изменяет ориентацию фигуры. |
| [get_Font](./get_font/)() | Предоставляет доступ к форматированию шрифта этого объекта. |
| [get_Glow](./get_glow/)() | Получает формат свечения для фигуры. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Возвращает **true**, если у этого узла есть дочерние узлы. |
| [get_Height](./get_height/)() | Получает или задает высоту содержащего блока фигуры. |
| [get_HeightRelative](./get_heightrelative/)() | Получает или задает значение, представляющее процент относительной высоты фигуры. |
| [get_Hidden](./get_hidden/)() | Получает или задает логическое значение, указывающее, видима ли фигура. |
| [get_HorizontalAlignment](./get_horizontalalignment/)() | Указывает, как фигура позиционируется по горизонтали. |
| [get_HRef](./get_href/)() | Получает или задает полный адрес гиперссылки для фигуры. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Возвращает **true**, поскольку этот узел может иметь дочерние узлы. |
| [get_IsDecorative](./get_isdecorative/)() | Получает или задает флаг, указывающий, является ли фигура декоративной в документе. |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | Возвращает true, если этот объект был удалён в Microsoft Word при включённом отслеживании изменений. |
| [get_IsGroup](./get_isgroup/)() | Возвращает **true**, если это групповая фигура. |
| [get_IsHorizontalRule](./get_ishorizontalrule/)() | Возвращает **true**, если эта фигура является горизонтальной линией. |
| [get_IsImage](./get_isimage/)() | Возвращает **true**, если эта фигура является изображением. |
| [get_IsInline](./get_isinline/)() | Быстрый способ определить, позиционирована ли эта фигура в строке с текстом. |
| [get_IsInsertRevision](./get_isinsertrevision/)() | Возвращает true, если этот объект был вставлен в Microsoft Word при включённом отслеживании изменений. |
| [get_IsLayoutInCell](./get_islayoutincell/)() | Получает или задает флаг, указывающий, отображается ли фигура внутри таблицы или снаружи. |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | Возвращает **true**, если этот объект был перемещён (удалён) в Microsoft Word при включённом отслеживании изменений. |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | Возвращает **true**, если этот объект был перемещён (вставлен) в Microsoft Word при включённом отслеживании изменений. |
| [get_IsSignatureLine](./get_issignatureline/)() | Указывает, что фигура является [SignatureLine](../signatureline/). |
| [get_IsTopLevel](./get_istoplevel/)() | Возвращает **true**, если эта фигура не является дочерней для групповой фигуры. |
| [get_IsWordArt](./get_iswordart/)() | Возвращает **true**, если эта фигура является объектом WordArt. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Возвращает последнего дочернего узла. |
| [get_Left](./get_left/)() | Получает или задает позицию левого края содержащего блока фигуры. |
| [get_LeftRelative](./get_leftrelative/)() | Получает или задает значение, представляющее относительное левое положение фигуры в процентах. |
| [get_MarkupLanguage](./get_markuplanguage/)() const | Получает MarkupLanguage, используемый для этого графического объекта. |
| [get_Name](./get_name/)() | Получает или задает необязательное имя фигуры. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Возвращает узел, непосредственно следующий за этим узлом. |
| virtual [get_NodeType](../../aspose.words/node/get_nodetype/)() const | Возвращает тип этого узла. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Возвращает непосредственного родителя этого узла. |
| [get_ParentParagraph](./get_parentparagraph/)() | Возвращает непосредственный родительский абзац. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Возвращает узел, непосредственно предшествующий этому узлу. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Возвращает объект [Range](../../aspose.words/range/), представляющий часть документа, содержащуюся в этом узле. |
| [get_Reflection](./get_reflection/)() | Получает форматирование отражения для фигуры. |
| [get_RelativeHorizontalPosition](./get_relativehorizontalposition/)() | Указывает, относительно чего фигура позиционируется по горизонтали. |
| [get_RelativeHorizontalSize](./get_relativehorizontalsize/)() | Получает или задает значение относительного размера фигуры в горизонтальном направлении. |
| [get_RelativeVerticalPosition](./get_relativeverticalposition/)() | Указывает, относительно чего фигура позиционируется по вертикали. |
| [get_RelativeVerticalSize](./get_relativeverticalsize/)() | Получает или задает значение относительного размера фигуры в вертикальном направлении. |
| [get_Right](./get_right/)() | Получает позицию правого края содержащего блока фигуры. |
| [get_Rotation](./get_rotation/)() | Определяет угол (в градусах), на который повернута фигура. Положительное значение соответствует углу вращения по часовой стрелке. |
| [get_ScreenTip](./get_screentip/)() | Определяет текст, отображаемый при наведении указателя мыши на фигуру. |
| [get_ShadowFormat](./get_shadowformat/)() | Получает форматирование тени для фигуры. |
| [get_ShapeType](./get_shapetype/)() | Получает тип фигуры. |
| [get_SizeInPoints](./get_sizeinpoints/)() | Получает размер фигуры в пунктах. |
| [get_SoftEdge](./get_softedge/)() | Получает форматирование мягких краёв для фигуры. |
| [get_Target](./get_target/)() | Получает или задаёт целевой фрейм для гиперссылки фигуры. |
| [get_Title](./get_title/)() | Получает или задаёт заголовок (подпись) текущего объекта фигуры. |
| [get_Top](./get_top/)() | Получает или задаёт позицию верхнего края содержащего блока фигуры. |
| [get_TopRelative](./get_toprelative/)() | Получает или задаёт значение, представляющее относительное верхнее положение фигуры в процентах. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Указывает, как фигура позиционируется вертикально. |
| [get_Width](./get_width/)() | Получает или задаёт ширину содержащего блока фигуры. |
| [get_WidthRelative](./get_widthrelative/)() | Получает или задаёт значение, представляющее процент относительной ширины фигуры. |
| [get_WrapSide](./get_wrapside/)() | Указывает, как текст обтекает фигуру. |
| [get_WrapType](./get_wraptype/)() | Определяет, является ли фигура встроенной или плавающей. Для плавающих фигур определяет режим обтекания текста вокруг фигуры. |
| [get_ZOrder](./get_zorder/)() | Определяет порядок отображения перекрывающихся фигур. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Возвращает первого предка указанного [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Возвращает N‑й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Обеспечивает поддержку итерации в стиле foreach по дочерним узлам этого узла. |
| [GetShapeRenderer](./getshaperenderer/)() | Создаёт и возвращает объект, который можно использовать для отрисовки этой фигуры в изображение. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Получает текст этого узла и всех его дочерних узлов. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [LocalToParent](./localtoparent/)(System::Drawing::PointF) | Преобразует значение из локального пространства координат в пространство координат родительской фигуры. |
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
| [set_AllowOverlap](./set_allowoverlap/)(bool) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_AllowOverlap](./get_allowoverlap/). |
| [set_AlternativeText](./set_alternativetext/)(const System::String\&) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_AlternativeText](./get_alternativetext/). |
| [set_AnchorLocked](./set_anchorlocked/)(bool) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_AnchorLocked](./get_anchorlocked/). |
| [set_AspectRatioLocked](./set_aspectratiolocked/)(bool) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked](./get_aspectratiolocked/). |
| [set_BehindText](./set_behindtext/)(bool) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_BehindText](./get_behindtext/). |
| [set_Bounds](./set_bounds/)(System::Drawing::RectangleF) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_Bounds](./get_bounds/). |
| [set_CoordOrigin](./set_coordorigin/)(System::Drawing::Point) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_CoordOrigin](./get_coordorigin/). |
| [set_CoordSize](./set_coordsize/)(System::Drawing::Size) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_CoordSize](./get_coordsize/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Сеттер для [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_DistanceBottom](./set_distancebottom/)(double) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_DistanceBottom](./get_distancebottom/). |
| [set_DistanceLeft](./set_distanceleft/)(double) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_DistanceLeft](./get_distanceleft/). |
| [set_DistanceRight](./set_distanceright/)(double) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_DistanceRight](./get_distanceright/). |
| [set_DistanceTop](./set_distancetop/)(double) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_DistanceTop](./get_distancetop/). |
| [set_FlipOrientation](./set_fliporientation/)(Aspose::Words::Drawing::FlipOrientation) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_FlipOrientation](./get_fliporientation/). |
| [set_Height](./set_height/)(double) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_Height](./get_height/). |
| [set_HeightRelative](./set_heightrelative/)(float) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_HeightRelative](./get_heightrelative/). |
| [set_Hidden](./set_hidden/)(bool) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_Hidden](./get_hidden/). |
| [set_HorizontalAlignment](./set_horizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_HorizontalAlignment](./get_horizontalalignment/). |
| [set_HRef](./set_href/)(const System::String\&) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_HRef](./get_href/). |
| [set_IsDecorative](./set_isdecorative/)(bool) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_IsDecorative](./get_isdecorative/). |
| [set_IsLayoutInCell](./set_islayoutincell/)(bool) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell](./get_islayoutincell/). |
| [set_Left](./set_left/)(double) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_Left](./get_left/). |
| [set_LeftRelative](./set_leftrelative/)(float) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_LeftRelative](./get_leftrelative/). |
| [set_Name](./set_name/)(const System::String\&) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_Name](./get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_RelativeHorizontalPosition](./set_relativehorizontalposition/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition](./get_relativehorizontalposition/). |
| [set_RelativeHorizontalSize](./set_relativehorizontalsize/)(Aspose::Words::Drawing::RelativeHorizontalSize) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize](./get_relativehorizontalsize/). |
| [set_RelativeVerticalPosition](./set_relativeverticalposition/)(Aspose::Words::Drawing::RelativeVerticalPosition) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition](./get_relativeverticalposition/). |
| [set_RelativeVerticalSize](./set_relativeverticalsize/)(Aspose::Words::Drawing::RelativeVerticalSize) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalSize](./get_relativeverticalsize/). |
| [set_Rotation](./set_rotation/)(double) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_Rotation](./get_rotation/). |
| [set_ScreenTip](./set_screentip/)(const System::String\&) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_ScreenTip](./get_screentip/). |
| [set_Target](./set_target/)(const System::String\&) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_Target](./get_target/). |
| [set_Title](./set_title/)(const System::String\&) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_Title](./get_title/). |
| [set_Top](./set_top/)(double) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_Top](./get_top/). |
| [set_TopRelative](./set_toprelative/)(float) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_TopRelative](./get_toprelative/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment](./get_verticalalignment/). |
| [set_Width](./set_width/)(double) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_Width](./get_width/). |
| [set_WidthRelative](./set_widthrelative/)(float) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_WidthRelative](./get_widthrelative/). |
| [set_WrapSide](./set_wrapside/)(Aspose::Words::Drawing::WrapSide) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_WrapSide](./get_wrapside/). |
| [set_WrapType](./set_wraptype/)(Aspose::Words::Drawing::WrapType) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_WrapType](./get_wraptype/). |
| [set_ZOrder](./set_zorder/)(int32_t) | Сеттер для [Aspose::Words::Drawing::ShapeBase::get_ZOrder](./get_zorder/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| static [Type](./type/)() |  |
## Примечания


Это абстрактный класс. Два производных класса, которые вы можете создать, — это [Shape](../shape/) и [GroupShape](../groupshape/).

Фигура является узлом в дереве документа.

Если фигура является дочерним элементом объекта [Paragraph](../../aspose.words/paragraph/), то говорят, что фигура является "top-level". Фигуры верхнего уровня измеряются и позиционируются в пунктах.

Фигура также может быть дочерним элементом объекта [GroupShape](../groupshape/), когда несколько фигур объединены в группу. Дочерние фигуры групповой фигуры позиционируются в координатном пространстве и единицах, определённых свойствами [CoordSize](./get_coordsize/) и [CoordOrigin](./get_coordorigin/) родительской групповой фигуры.

Фигура может быть расположена в строке с текстом или плавающей. Метод позиционирования управляется с помощью свойства [WrapType](./get_wraptype/).

Когда фигура плавает, она позиционируется относительно чего‑то (например, текущего абзаца, поля или страницы). Относительное позиционирование фигуры указывается с помощью свойств [RelativeHorizontalPosition](./get_relativehorizontalposition/) и [RelativeVerticalPosition](./get_relativeverticalposition/).

Плавающая фигура может быть явно позиционирована с помощью свойств [Left](./get_left/) и [Top](./get_top/) или выровнена относительно другого объекта с помощью свойств [HorizontalAlignment](./get_horizontalalignment/) и [VerticalAlignment](./get_verticalalignment/).

## Примеры



Показывает, как вставить плавающее изображение в центр страницы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте плавающее изображение, которое будет находиться позади перекрывающего текста, и выровняйте его по центру страницы.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## См. также

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
