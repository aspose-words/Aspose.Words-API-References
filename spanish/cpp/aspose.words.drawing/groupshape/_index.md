---
title: "Aspose::Words::Drawing::GroupShape class"
linktitle: "GroupShape"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Drawing::GroupShape. Representa un grupo de formas en un documento. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.drawing/groupshape/
---
## GroupShape class


Representa un grupo de formas en un documento. Para obtener más información, visite el artículo de documentación [How to Add Group Shape into a Word Document](https://docs.aspose.com/words/cpp/how-to-add-group-shape-into-a-word-document/).

```cpp
class GroupShape : public Aspose::Words::Drawing::ShapeBase
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Acepta un visitante. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Acepta un visitante para visitar el final del [GroupShape](./). |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Acepta un visitante para visitar el inicio del [GroupShape](./). |
| [AdjustWithEffects](../shapebase/adjustwitheffects/)(System::Drawing::RectangleF) | Añade al rectángulo de origen los valores de la extensión del efecto y devuelve el rectángulo final. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicado del nodo. |
| [get_AllowOverlap](../shapebase/get_allowoverlap/)() | Obtiene o establece un valor que especifica si esta forma puede superponerse a otras formas. |
| [get_AlternativeText](../shapebase/get_alternativetext/)() | Define el texto alternativo que se mostrará en lugar de un gráfico. |
| [get_AnchorLocked](../shapebase/get_anchorlocked/)() | Especifica si el ancla de la forma está bloqueada. |
| [get_AspectRatioLocked](../shapebase/get_aspectratiolocked/)() | Especifica si la relación de aspecto de la forma está bloqueada. |
| [get_BehindText](../shapebase/get_behindtext/)() | Especifica si la forma está debajo o encima del texto. |
| [get_Bottom](../shapebase/get_bottom/)() | Obtiene la posición del borde inferior del bloque contenedor de la forma. |
| [get_Bounds](../shapebase/get_bounds/)() | Obtiene o establece la ubicación y el tamaño del bloque contenedor de la forma. |
| [get_BoundsInPoints](../shapebase/get_boundsinpoints/)() | Obtiene la ubicación y el tamaño del bloque contenedor de la forma en puntos, relativo al ancla de la forma más alta. |
| [get_BoundsWithEffects](../shapebase/get_boundswitheffects/)() | Obtiene la extensión final que tiene este objeto forma después de aplicar efectos de dibujo. El valor se mide en puntos. |
| [get_CanHaveImage](../shapebase/get_canhaveimage/)() | Devuelve **true** si el tipo de forma permite que la forma tenga una imagen. |
| [get_CoordOrigin](../shapebase/get_coordorigin/)() | Las coordenadas en la esquina superior izquierda del bloque contenedor de esta forma. |
| [get_CoordSize](../shapebase/get_coordsize/)() | El ancho y la altura del espacio de coordenadas dentro del bloque contenedor de esta forma. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Obtiene el número de hijos inmediatos de este nodo. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Especifica un identificador de nodo personalizado. |
| [get_DistanceBottom](../shapebase/get_distancebottom/)() | Devuelve o establece la distancia (en puntos) entre el texto del documento y el borde inferior de la forma. |
| [get_DistanceLeft](../shapebase/get_distanceleft/)() | Devuelve o establece la distancia (en puntos) entre el texto del documento y el borde izquierdo de la forma. |
| [get_DistanceRight](../shapebase/get_distanceright/)() | Devuelve o establece la distancia (en puntos) entre el texto del documento y el borde derecho de la forma. |
| [get_DistanceTop](../shapebase/get_distancetop/)() | Devuelve o establece la distancia (en puntos) entre el texto del documento y el borde superior de la forma. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Obtiene el documento al que pertenece este nodo. |
| [get_Fill](../shapebase/get_fill/)() | Obtiene el formato de relleno de la forma. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Obtiene el primer hijo del nodo. |
| [get_FlipOrientation](../shapebase/get_fliporientation/)() | Cambia la orientación de una forma. |
| [get_Font](../shapebase/get_font/)() | Proporciona acceso al formato de fuente de este objeto. |
| [get_Glow](../shapebase/get_glow/)() | Obtiene el formato de resplandor de la forma. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Devuelve **true** si este nodo tiene algún nodo hijo. |
| [get_Height](../shapebase/get_height/)() | Obtiene o establece la altura del bloque contenedor de la forma. |
| [get_HeightRelative](../shapebase/get_heightrelative/)() | Obtiene o establece el valor que representa el porcentaje de la altura relativa de la forma. |
| [get_Hidden](../shapebase/get_hidden/)() | Obtiene o establece un valor booleano que indica si la forma es visible. |
| [get_HorizontalAlignment](../shapebase/get_horizontalalignment/)() | Especifica cómo se posiciona horizontalmente la forma. |
| [get_HRef](../shapebase/get_href/)() | Obtiene o establece la dirección completa del hipervínculo para una forma. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Devuelve **true** ya que este nodo puede tener nodos hijos. |
| [get_IsDecorative](../shapebase/get_isdecorative/)() | Obtiene o establece la bandera que especifica si la forma es decorativa en el documento. |
| [get_IsDeleteRevision](../shapebase/get_isdeleterevision/)() | Devuelve true si este objeto fue eliminado en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsGroup](../shapebase/get_isgroup/)() | Devuelve **true** si esto es una forma de grupo. |
| [get_IsHorizontalRule](../shapebase/get_ishorizontalrule/)() | Devuelve **true** si esta forma es una regla horizontal. |
| [get_IsImage](../shapebase/get_isimage/)() | Devuelve **true** si esta forma es una forma de imagen. |
| [get_IsInline](../shapebase/get_isinline/)() | Una forma rápida de determinar si esta forma está posicionada en línea con el texto. |
| [get_IsInsertRevision](../shapebase/get_isinsertrevision/)() | Devuelve true si este objeto fue insertado en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsLayoutInCell](../shapebase/get_islayoutincell/)() | Obtiene o establece una bandera que indica si la forma se muestra dentro de una tabla o fuera de ella. |
| [get_IsMoveFromRevision](../shapebase/get_ismovefromrevision/)() | Devuelve **true** si este objeto fue movido (eliminado) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsMoveToRevision](../shapebase/get_ismovetorevision/)() | Devuelve **true** si este objeto fue movido (insertado) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsSignatureLine](../shapebase/get_issignatureline/)() | Indica que la forma es una [SignatureLine](../signatureline/). |
| [get_IsTopLevel](../shapebase/get_istoplevel/)() | Devuelve **true** si esta forma no es un hijo de una forma de grupo. |
| [get_IsWordArt](../shapebase/get_iswordart/)() | Devuelve **true** si esta forma es un objeto WordArt. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Obtiene el último hijo del nodo. |
| [get_Left](../shapebase/get_left/)() | Obtiene o establece la posición del borde izquierdo del bloque contenedor de la forma. |
| [get_LeftRelative](../shapebase/get_leftrelative/)() | Obtiene o establece el valor que representa la posición izquierda relativa de la forma en porcentaje. |
| [get_MarkupLanguage](../shapebase/get_markuplanguage/)() const | Obtiene el MarkupLanguage usado para este objeto gráfico. |
| [get_Name](../shapebase/get_name/)() | Obtiene o establece el nombre opcional de la forma. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Obtiene el nodo que sigue inmediatamente a este nodo. |
| [get_NodeType](./get_nodetype/)() const override | Devuelve [GroupShape](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Obtiene el padre inmediato de este nodo. |
| [get_ParentParagraph](../shapebase/get_parentparagraph/)() | Devuelve el párrafo padre inmediato. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Obtiene el nodo que precede inmediatamente a este nodo. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Devuelve un objeto [Range](../../aspose.words/range/) que representa la porción de un documento que está contenida en este nodo. |
| [get_Reflection](../shapebase/get_reflection/)() | Obtiene el formato de reflexión para la forma. |
| [get_RelativeHorizontalPosition](../shapebase/get_relativehorizontalposition/)() | Especifica respecto a qué se posiciona horizontalmente la forma. |
| [get_RelativeHorizontalSize](../shapebase/get_relativehorizontalsize/)() | Obtiene o establece el valor del tamaño relativo de la forma en dirección horizontal. |
| [get_RelativeVerticalPosition](../shapebase/get_relativeverticalposition/)() | Especifica respecto a qué se posiciona verticalmente la forma. |
| [get_RelativeVerticalSize](../shapebase/get_relativeverticalsize/)() | Obtiene o establece el valor del tamaño relativo de la forma en dirección vertical. |
| [get_Right](../shapebase/get_right/)() | Obtiene la posición del borde derecho del bloque contenedor de la forma. |
| [get_Rotation](../shapebase/get_rotation/)() | Define el ángulo (en grados) al que se rota una forma. Un valor positivo corresponde al ángulo de rotación en sentido horario. |
| [get_ScreenTip](../shapebase/get_screentip/)() | Define el texto que se muestra cuando el puntero del ratón se desplaza sobre la forma. |
| [get_ShadowFormat](../shapebase/get_shadowformat/)() | Obtiene el formato de sombra para la forma. |
| [get_ShapeType](../shapebase/get_shapetype/)() | Obtiene el tipo de forma. |
| [get_SizeInPoints](../shapebase/get_sizeinpoints/)() | Obtiene el tamaño de la forma en puntos. |
| [get_SoftEdge](../shapebase/get_softedge/)() | Obtiene el formato de borde suave para la forma. |
| [get_Target](../shapebase/get_target/)() | Obtiene o establece el marco de destino para el hipervínculo de la forma. |
| [get_Title](../shapebase/get_title/)() | Obtiene o establece el título (leyenda) del objeto de forma actual. |
| [get_Top](../shapebase/get_top/)() | Obtiene o establece la posición del borde superior del bloque contenedor de la forma. |
| [get_TopRelative](../shapebase/get_toprelative/)() | Obtiene o establece el valor que representa la posición superior relativa de la forma en porcentaje. |
| [get_VerticalAlignment](../shapebase/get_verticalalignment/)() | Especifica cómo se posiciona verticalmente la forma. |
| [get_Width](../shapebase/get_width/)() | Obtiene o establece el ancho del bloque contenedor de la forma. |
| [get_WidthRelative](../shapebase/get_widthrelative/)() | Obtiene o establece el valor que representa el porcentaje del ancho relativo de la forma. |
| [get_WrapSide](../shapebase/get_wrapside/)() | Especifica cómo se envuelve el texto alrededor de la forma. |
| [get_WrapType](../shapebase/get_wraptype/)() | Define si la forma es en línea o flotante. Para formas flotantes define el modo de ajuste del texto alrededor de la forma. |
| [get_ZOrder](../shapebase/get_zorder/)() | Determina el orden de visualización de las formas superpuestas. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Obtiene el primer ancestro del [NodeType](../../aspose.words/nodetype/) especificado. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Devuelve un nodo hijo N-ésimo que coincide con el tipo especificado. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Devuelve una colección en vivo de nodos hijos que coinciden con el tipo especificado. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Proporciona soporte para la iteración al estilo foreach sobre los nodos hijos de este nodo. |
| [GetShapeRenderer](../shapebase/getshaperenderer/)() | Crea y devuelve un objeto que puede usarse para renderizar esta forma en una imagen. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Obtiene el texto de este nodo y de todos sus hijos. |
| [GetType](./gettype/)() const override |  |
| [GroupShape](./groupshape/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Crea una nueva forma de grupo. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Devuelve el índice del nodo hijo especificado en la matriz de nodos hijos. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [LocalToParent](../shapebase/localtoparent/)(System::Drawing::PointF) | Convierte un valor del espacio de coordenadas local al espacio de coordenadas de la forma padre. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtiene el nodo siguiente según el algoritmo de recorrido en preorden del árbol. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Un método de utilidad que convierte un valor de enumeración de tipo de nodo en una cadena legible para el usuario. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtiene el nodo anterior según el algoritmo de recorrido en preorden del árbol. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina a sí mismo del nodo padre. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Elimina todos los nodos hijos del nodo actual. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Elimina todos los nodos descendientes de [SmartTag](../../aspose.words.markup/smarttag/) del nodo actual. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Selecciona una lista de nodos que coinciden con la expresión XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Selecciona el primer [Node](../../aspose.words/node/) que coincide con la expresión XPath. |
| [set_AllowOverlap](../shapebase/set_allowoverlap/)(bool) | Método set para [Aspose::Words::Drawing::ShapeBase::get_AllowOverlap](../shapebase/get_allowoverlap/). |
| [set_AlternativeText](../shapebase/set_alternativetext/)(const System::String\&) | Método set para [Aspose::Words::Drawing::ShapeBase::get_AlternativeText](../shapebase/get_alternativetext/). |
| [set_AnchorLocked](../shapebase/set_anchorlocked/)(bool) | Método set para [Aspose::Words::Drawing::ShapeBase::get_AnchorLocked](../shapebase/get_anchorlocked/). |
| [set_AspectRatioLocked](../shapebase/set_aspectratiolocked/)(bool) | Método set para [Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked](../shapebase/get_aspectratiolocked/). |
| [set_BehindText](../shapebase/set_behindtext/)(bool) | Método set para [Aspose::Words::Drawing::ShapeBase::get_BehindText](../shapebase/get_behindtext/). |
| [set_Bounds](../shapebase/set_bounds/)(System::Drawing::RectangleF) | Método set para [Aspose::Words::Drawing::ShapeBase::get_Bounds](../shapebase/get_bounds/). |
| [set_CoordOrigin](../shapebase/set_coordorigin/)(System::Drawing::Point) | Método setter para [Aspose::Words::Drawing::ShapeBase::get_CoordOrigin](../shapebase/get_coordorigin/). |
| [set_CoordSize](../shapebase/set_coordsize/)(System::Drawing::Size) | Método setter para [Aspose::Words::Drawing::ShapeBase::get_CoordSize](../shapebase/get_coordsize/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Método set para [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_DistanceBottom](../shapebase/set_distancebottom/)(double) | Método setter para [Aspose::Words::Drawing::ShapeBase::get_DistanceBottom](../shapebase/get_distancebottom/). |
| [set_DistanceLeft](../shapebase/set_distanceleft/)(double) | Método setter para [Aspose::Words::Drawing::ShapeBase::get_DistanceLeft](../shapebase/get_distanceleft/). |
| [set_DistanceRight](../shapebase/set_distanceright/)(double) | Método setter para [Aspose::Words::Drawing::ShapeBase::get_DistanceRight](../shapebase/get_distanceright/). |
| [set_DistanceTop](../shapebase/set_distancetop/)(double) | Método setter para [Aspose::Words::Drawing::ShapeBase::get_DistanceTop](../shapebase/get_distancetop/). |
| [set_FlipOrientation](../shapebase/set_fliporientation/)(Aspose::Words::Drawing::FlipOrientation) | Método setter para [Aspose::Words::Drawing::ShapeBase::get_FlipOrientation](../shapebase/get_fliporientation/). |
| [set_Height](../shapebase/set_height/)(double) | Método setter para [Aspose::Words::Drawing::ShapeBase::get_Height](../shapebase/get_height/). |
| [set_HeightRelative](../shapebase/set_heightrelative/)(float) | Método setter para [Aspose::Words::Drawing::ShapeBase::get_HeightRelative](../shapebase/get_heightrelative/). |
| [set_Hidden](../shapebase/set_hidden/)(bool) | Método setter para [Aspose::Words::Drawing::ShapeBase::get_Hidden](../shapebase/get_hidden/). |
| [set_HorizontalAlignment](../shapebase/set_horizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | Método setter para [Aspose::Words::Drawing::ShapeBase::get_HorizontalAlignment](../shapebase/get_horizontalalignment/). |
| [set_HRef](../shapebase/set_href/)(const System::String\&) | Método setter para [Aspose::Words::Drawing::ShapeBase::get_HRef](../shapebase/get_href/). |
| [set_IsDecorative](../shapebase/set_isdecorative/)(bool) | Método setter para [Aspose::Words::Drawing::ShapeBase::get_IsDecorative](../shapebase/get_isdecorative/). |
| [set_IsLayoutInCell](../shapebase/set_islayoutincell/)(bool) | Método setter para [Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell](../shapebase/get_islayoutincell/). |
| [set_Left](../shapebase/set_left/)(double) | Método setter para [Aspose::Words::Drawing::ShapeBase::get_Left](../shapebase/get_left/). |
| [set_LeftRelative](../shapebase/set_leftrelative/)(float) | Método setter para [Aspose::Words::Drawing::ShapeBase::get_LeftRelative](../shapebase/get_leftrelative/). |
| [set_Name](../shapebase/set_name/)(const System::String\&) | Método setter para [Aspose::Words::Drawing::ShapeBase::get_Name](../shapebase/get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_RelativeHorizontalPosition](../shapebase/set_relativehorizontalposition/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | Método setter para [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition](../shapebase/get_relativehorizontalposition/). |
| [set_RelativeHorizontalSize](../shapebase/set_relativehorizontalsize/)(Aspose::Words::Drawing::RelativeHorizontalSize) | Método setter para [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize](../shapebase/get_relativehorizontalsize/). |
| [set_RelativeVerticalPosition](../shapebase/set_relativeverticalposition/)(Aspose::Words::Drawing::RelativeVerticalPosition) | Método setter para [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition](../shapebase/get_relativeverticalposition/). |
| [set_RelativeVerticalSize](../shapebase/set_relativeverticalsize/)(Aspose::Words::Drawing::RelativeVerticalSize) | Método setter para [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalSize](../shapebase/get_relativeverticalsize/). |
| [set_Rotation](../shapebase/set_rotation/)(double) | Método setter para [Aspose::Words::Drawing::ShapeBase::get_Rotation](../shapebase/get_rotation/). |
| [set_ScreenTip](../shapebase/set_screentip/)(const System::String\&) | Método setter para [Aspose::Words::Drawing::ShapeBase::get_ScreenTip](../shapebase/get_screentip/). |
| [set_Target](../shapebase/set_target/)(const System::String\&) | Método setter para [Aspose::Words::Drawing::ShapeBase::get_Target](../shapebase/get_target/). |
| [set_Title](../shapebase/set_title/)(const System::String\&) | Método setter para [Aspose::Words::Drawing::ShapeBase::get_Title](../shapebase/get_title/). |
| [set_Top](../shapebase/set_top/)(double) | Método set para [Aspose::Words::Drawing::ShapeBase::get_Top](../shapebase/get_top/). |
| [set_TopRelative](../shapebase/set_toprelative/)(float) | Método set para [Aspose::Words::Drawing::ShapeBase::get_TopRelative](../shapebase/get_toprelative/). |
| [set_VerticalAlignment](../shapebase/set_verticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | Método set para [Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment](../shapebase/get_verticalalignment/). |
| [set_Width](../shapebase/set_width/)(double) | Método set para [Aspose::Words::Drawing::ShapeBase::get_Width](../shapebase/get_width/). |
| [set_WidthRelative](../shapebase/set_widthrelative/)(float) | Método set para [Aspose::Words::Drawing::ShapeBase::get_WidthRelative](../shapebase/get_widthrelative/). |
| [set_WrapSide](../shapebase/set_wrapside/)(Aspose::Words::Drawing::WrapSide) | Método set para [Aspose::Words::Drawing::ShapeBase::get_WrapSide](../shapebase/get_wrapside/). |
| [set_WrapType](../shapebase/set_wraptype/)(Aspose::Words::Drawing::WrapType) | Método set para [Aspose::Words::Drawing::ShapeBase::get_WrapType](../shapebase/get_wraptype/). |
| [set_ZOrder](../shapebase/set_zorder/)(int32_t) | Método set para [Aspose::Words::Drawing::ShapeBase::get_ZOrder](../shapebase/get_zorder/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporta el contenido del nodo a una cadena usando las opciones de guardado especificadas. |
| static [Type](./type/)() |  |
## Observaciones


Un [GroupShape](./) es un nodo compuesto y puede tener nodos [Shape](../shape/) y [GroupShape](./) como hijos.

Cada [GroupShape](./) define un nuevo sistema de coordenadas para sus formas hijas. El sistema de coordenadas se define usando las propiedades [CoordSize](../shapebase/get_coordsize/) y [CoordOrigin](../shapebase/get_coordorigin/).

## Ver también

* Class [ShapeBase](../shapebase/)
* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
