---
title: "Aspose::Words::Drawing::ShapeBase class"
linktitle: "ShapeBase"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ShapeBase class. Clase base para objetos en la capa de dibujo, como AutoShape, forma libre, objeto OLE, control ActiveX o imagen. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words.drawing/shapebase/
---
## ShapeBase class


Clase base para objetos en la capa de dibujo, como un AutoShape, forma libre, objeto OLE, control ActiveX o imagen. Para obtener más información, visite el artículo de documentación [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/).

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

## Métodos

| Método | Descripción |
| --- | --- |
| virtual [Accept](../../aspose.words/node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Acepta un visitante. |
| virtual [AcceptEnd](../../aspose.words/compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Cuando se implementa en una clase derivada, llama al método VisitXXXEnd del visitante de documento especificado. |
| virtual [AcceptStart](../../aspose.words/compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Cuando se implementa en una clase derivada, llama al método VisitXXXStart del visitante de documento especificado. |
| [AdjustWithEffects](./adjustwitheffects/)(System::Drawing::RectangleF) | Añade al rectángulo de origen los valores de la extensión del efecto y devuelve el rectángulo final. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicado del nodo. |
| [get_AllowOverlap](./get_allowoverlap/)() | Obtiene o establece un valor que especifica si esta forma puede superponerse a otras formas. |
| [get_AlternativeText](./get_alternativetext/)() | Define el texto alternativo que se mostrará en lugar de un gráfico. |
| [get_AnchorLocked](./get_anchorlocked/)() | Especifica si el ancla de la forma está bloqueada. |
| [get_AspectRatioLocked](./get_aspectratiolocked/)() | Especifica si la relación de aspecto de la forma está bloqueada. |
| [get_BehindText](./get_behindtext/)() | Especifica si la forma está debajo o encima del texto. |
| [get_Bottom](./get_bottom/)() | Obtiene la posición del borde inferior del bloque contenedor de la forma. |
| [get_Bounds](./get_bounds/)() | Obtiene o establece la ubicación y el tamaño del bloque contenedor de la forma. |
| [get_BoundsInPoints](./get_boundsinpoints/)() | Obtiene la ubicación y el tamaño del bloque contenedor de la forma en puntos, relativo al ancla de la forma más alta. |
| [get_BoundsWithEffects](./get_boundswitheffects/)() | Obtiene la extensión final que tiene este objeto forma después de aplicar efectos de dibujo. El valor se mide en puntos. |
| [get_CanHaveImage](./get_canhaveimage/)() | Devuelve **true** si el tipo de forma permite que la forma tenga una imagen. |
| [get_CoordOrigin](./get_coordorigin/)() | Las coordenadas en la esquina superior izquierda del bloque contenedor de esta forma. |
| [get_CoordSize](./get_coordsize/)() | El ancho y la altura del espacio de coordenadas dentro del bloque contenedor de esta forma. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Obtiene el número de hijos inmediatos de este nodo. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Especifica un identificador de nodo personalizado. |
| [get_DistanceBottom](./get_distancebottom/)() | Devuelve o establece la distancia (en puntos) entre el texto del documento y el borde inferior de la forma. |
| [get_DistanceLeft](./get_distanceleft/)() | Devuelve o establece la distancia (en puntos) entre el texto del documento y el borde izquierdo de la forma. |
| [get_DistanceRight](./get_distanceright/)() | Devuelve o establece la distancia (en puntos) entre el texto del documento y el borde derecho de la forma. |
| [get_DistanceTop](./get_distancetop/)() | Devuelve o establece la distancia (en puntos) entre el texto del documento y el borde superior de la forma. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Obtiene el documento al que pertenece este nodo. |
| [get_Fill](./get_fill/)() | Obtiene el formato de relleno de la forma. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Obtiene el primer hijo del nodo. |
| [get_FlipOrientation](./get_fliporientation/)() | Cambia la orientación de una forma. |
| [get_Font](./get_font/)() | Proporciona acceso al formato de fuente de este objeto. |
| [get_Glow](./get_glow/)() | Obtiene el formato de resplandor de la forma. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Devuelve **true** si este nodo tiene algún nodo hijo. |
| [get_Height](./get_height/)() | Obtiene o establece la altura del bloque contenedor de la forma. |
| [get_HeightRelative](./get_heightrelative/)() | Obtiene o establece el valor que representa el porcentaje de la altura relativa de la forma. |
| [get_Hidden](./get_hidden/)() | Obtiene o establece un valor booleano que indica si la forma es visible. |
| [get_HorizontalAlignment](./get_horizontalalignment/)() | Especifica cómo se posiciona horizontalmente la forma. |
| [get_HRef](./get_href/)() | Obtiene o establece la dirección completa del hipervínculo para una forma. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Devuelve **true** ya que este nodo puede tener nodos hijos. |
| [get_IsDecorative](./get_isdecorative/)() | Obtiene o establece la bandera que especifica si la forma es decorativa en el documento. |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | Devuelve true si este objeto fue eliminado en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsGroup](./get_isgroup/)() | Devuelve **true** si esto es una forma de grupo. |
| [get_IsHorizontalRule](./get_ishorizontalrule/)() | Devuelve **true** si esta forma es una regla horizontal. |
| [get_IsImage](./get_isimage/)() | Devuelve **true** si esta forma es una forma de imagen. |
| [get_IsInline](./get_isinline/)() | Una forma rápida de determinar si esta forma está posicionada en línea con el texto. |
| [get_IsInsertRevision](./get_isinsertrevision/)() | Devuelve true si este objeto fue insertado en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsLayoutInCell](./get_islayoutincell/)() | Obtiene o establece una bandera que indica si la forma se muestra dentro de una tabla o fuera de ella. |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | Devuelve **true** si este objeto fue movido (eliminado) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | Devuelve **true** si este objeto fue movido (insertado) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsSignatureLine](./get_issignatureline/)() | Indica que la forma es una [SignatureLine](../signatureline/). |
| [get_IsTopLevel](./get_istoplevel/)() | Devuelve **true** si esta forma no es un hijo de una forma de grupo. |
| [get_IsWordArt](./get_iswordart/)() | Devuelve **true** si esta forma es un objeto WordArt. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Obtiene el último hijo del nodo. |
| [get_Left](./get_left/)() | Obtiene o establece la posición del borde izquierdo del bloque contenedor de la forma. |
| [get_LeftRelative](./get_leftrelative/)() | Obtiene o establece el valor que representa la posición izquierda relativa de la forma en porcentaje. |
| [get_MarkupLanguage](./get_markuplanguage/)() const | Obtiene el MarkupLanguage usado para este objeto gráfico. |
| [get_Name](./get_name/)() | Obtiene o establece el nombre opcional de la forma. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Obtiene el nodo que sigue inmediatamente a este nodo. |
| virtual [get_NodeType](../../aspose.words/node/get_nodetype/)() const | Obtiene el tipo de este nodo. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Obtiene el padre inmediato de este nodo. |
| [get_ParentParagraph](./get_parentparagraph/)() | Devuelve el párrafo padre inmediato. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Obtiene el nodo que precede inmediatamente a este nodo. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Devuelve un objeto [Range](../../aspose.words/range/) que representa la porción de un documento que está contenida en este nodo. |
| [get_Reflection](./get_reflection/)() | Obtiene el formato de reflexión para la forma. |
| [get_RelativeHorizontalPosition](./get_relativehorizontalposition/)() | Especifica respecto a qué se posiciona horizontalmente la forma. |
| [get_RelativeHorizontalSize](./get_relativehorizontalsize/)() | Obtiene o establece el valor del tamaño relativo de la forma en dirección horizontal. |
| [get_RelativeVerticalPosition](./get_relativeverticalposition/)() | Especifica respecto a qué se posiciona verticalmente la forma. |
| [get_RelativeVerticalSize](./get_relativeverticalsize/)() | Obtiene o establece el valor del tamaño relativo de la forma en dirección vertical. |
| [get_Right](./get_right/)() | Obtiene la posición del borde derecho del bloque contenedor de la forma. |
| [get_Rotation](./get_rotation/)() | Define el ángulo (en grados) al que se rota una forma. Un valor positivo corresponde al ángulo de rotación en sentido horario. |
| [get_ScreenTip](./get_screentip/)() | Define el texto que se muestra cuando el puntero del ratón se desplaza sobre la forma. |
| [get_ShadowFormat](./get_shadowformat/)() | Obtiene el formato de sombra para la forma. |
| [get_ShapeType](./get_shapetype/)() | Obtiene el tipo de forma. |
| [get_SizeInPoints](./get_sizeinpoints/)() | Obtiene el tamaño de la forma en puntos. |
| [get_SoftEdge](./get_softedge/)() | Obtiene el formato de borde suave para la forma. |
| [get_Target](./get_target/)() | Obtiene o establece el marco de destino para el hipervínculo de la forma. |
| [get_Title](./get_title/)() | Obtiene o establece el título (leyenda) del objeto de forma actual. |
| [get_Top](./get_top/)() | Obtiene o establece la posición del borde superior del bloque contenedor de la forma. |
| [get_TopRelative](./get_toprelative/)() | Obtiene o establece el valor que representa la posición superior relativa de la forma en porcentaje. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Especifica cómo se posiciona verticalmente la forma. |
| [get_Width](./get_width/)() | Obtiene o establece el ancho del bloque contenedor de la forma. |
| [get_WidthRelative](./get_widthrelative/)() | Obtiene o establece el valor que representa el porcentaje del ancho relativo de la forma. |
| [get_WrapSide](./get_wrapside/)() | Especifica cómo se envuelve el texto alrededor de la forma. |
| [get_WrapType](./get_wraptype/)() | Define si la forma es en línea o flotante. Para formas flotantes define el modo de ajuste del texto alrededor de la forma. |
| [get_ZOrder](./get_zorder/)() | Determina el orden de visualización de las formas superpuestas. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Obtiene el primer ancestro del [NodeType](../../aspose.words/nodetype/) especificado. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Devuelve un nodo hijo N-ésimo que coincide con el tipo especificado. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Devuelve una colección en vivo de nodos hijos que coinciden con el tipo especificado. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Proporciona soporte para la iteración al estilo foreach sobre los nodos hijos de este nodo. |
| [GetShapeRenderer](./getshaperenderer/)() | Crea y devuelve un objeto que puede usarse para renderizar esta forma en una imagen. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Obtiene el texto de este nodo y de todos sus hijos. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Devuelve el índice del nodo hijo especificado en la matriz de nodos hijos. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [LocalToParent](./localtoparent/)(System::Drawing::PointF) | Convierte un valor del espacio de coordenadas local al espacio de coordenadas de la forma padre. |
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
| [set_AllowOverlap](./set_allowoverlap/)(bool) | Método setter para [Aspose::Words::Drawing::ShapeBase::get_AllowOverlap](./get_allowoverlap/). |
| [set_AlternativeText](./set_alternativetext/)(const System::String\&) | Método setter para [Aspose::Words::Drawing::ShapeBase::get_AlternativeText](./get_alternativetext/). |
| [set_AnchorLocked](./set_anchorlocked/)(bool) | Establecedor de [Aspose::Words::Drawing::ShapeBase::get_AnchorLocked](./get_anchorlocked/). |
| [set_AspectRatioLocked](./set_aspectratiolocked/)(bool) | Establecedor de [Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked](./get_aspectratiolocked/). |
| [set_BehindText](./set_behindtext/)(bool) | Establecedor de [Aspose::Words::Drawing::ShapeBase::get_BehindText](./get_behindtext/). |
| [set_Bounds](./set_bounds/)(System::Drawing::RectangleF) | Establecedor de [Aspose::Words::Drawing::ShapeBase::get_Bounds](./get_bounds/). |
| [set_CoordOrigin](./set_coordorigin/)(System::Drawing::Point) | Establecedor de [Aspose::Words::Drawing::ShapeBase::get_CoordOrigin](./get_coordorigin/). |
| [set_CoordSize](./set_coordsize/)(System::Drawing::Size) | Establecedor de [Aspose::Words::Drawing::ShapeBase::get_CoordSize](./get_coordsize/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Método set para [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_DistanceBottom](./set_distancebottom/)(double) | Establecedor de [Aspose::Words::Drawing::ShapeBase::get_DistanceBottom](./get_distancebottom/). |
| [set_DistanceLeft](./set_distanceleft/)(double) | Establecedor de [Aspose::Words::Drawing::ShapeBase::get_DistanceLeft](./get_distanceleft/). |
| [set_DistanceRight](./set_distanceright/)(double) | Establecedor de [Aspose::Words::Drawing::ShapeBase::get_DistanceRight](./get_distanceright/). |
| [set_DistanceTop](./set_distancetop/)(double) | Establecedor de [Aspose::Words::Drawing::ShapeBase::get_DistanceTop](./get_distancetop/). |
| [set_FlipOrientation](./set_fliporientation/)(Aspose::Words::Drawing::FlipOrientation) | Establecedor de [Aspose::Words::Drawing::ShapeBase::get_FlipOrientation](./get_fliporientation/). |
| [set_Height](./set_height/)(double) | Establecedor de [Aspose::Words::Drawing::ShapeBase::get_Height](./get_height/). |
| [set_HeightRelative](./set_heightrelative/)(float) | Establecedor de [Aspose::Words::Drawing::ShapeBase::get_HeightRelative](./get_heightrelative/). |
| [set_Hidden](./set_hidden/)(bool) | Establecedor de [Aspose::Words::Drawing::ShapeBase::get_Hidden](./get_hidden/). |
| [set_HorizontalAlignment](./set_horizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | Establecedor de [Aspose::Words::Drawing::ShapeBase::get_HorizontalAlignment](./get_horizontalalignment/). |
| [set_HRef](./set_href/)(const System::String\&) | Establecedor de [Aspose::Words::Drawing::ShapeBase::get_HRef](./get_href/). |
| [set_IsDecorative](./set_isdecorative/)(bool) | Establecedor de [Aspose::Words::Drawing::ShapeBase::get_IsDecorative](./get_isdecorative/). |
| [set_IsLayoutInCell](./set_islayoutincell/)(bool) | Establecedor de [Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell](./get_islayoutincell/). |
| [set_Left](./set_left/)(double) | Establecedor de [Aspose::Words::Drawing::ShapeBase::get_Left](./get_left/). |
| [set_LeftRelative](./set_leftrelative/)(float) | Establecedor de [Aspose::Words::Drawing::ShapeBase::get_LeftRelative](./get_leftrelative/). |
| [set_Name](./set_name/)(const System::String\&) | Establecedor de [Aspose::Words::Drawing::ShapeBase::get_Name](./get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_RelativeHorizontalPosition](./set_relativehorizontalposition/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | Establecedor de [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition](./get_relativehorizontalposition/). |
| [set_RelativeHorizontalSize](./set_relativehorizontalsize/)(Aspose::Words::Drawing::RelativeHorizontalSize) | Establecedor de [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize](./get_relativehorizontalsize/). |
| [set_RelativeVerticalPosition](./set_relativeverticalposition/)(Aspose::Words::Drawing::RelativeVerticalPosition) | Establecedor de [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition](./get_relativeverticalposition/). |
| [set_RelativeVerticalSize](./set_relativeverticalsize/)(Aspose::Words::Drawing::RelativeVerticalSize) | Establecedor de [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalSize](./get_relativeverticalsize/). |
| [set_Rotation](./set_rotation/)(double) | Establecedor para [Aspose::Words::Drawing::ShapeBase::get_Rotation](./get_rotation/). |
| [set_ScreenTip](./set_screentip/)(const System::String\&) | Establecedor para [Aspose::Words::Drawing::ShapeBase::get_ScreenTip](./get_screentip/). |
| [set_Target](./set_target/)(const System::String\&) | Establecedor para [Aspose::Words::Drawing::ShapeBase::get_Target](./get_target/). |
| [set_Title](./set_title/)(const System::String\&) | Establecedor para [Aspose::Words::Drawing::ShapeBase::get_Title](./get_title/). |
| [set_Top](./set_top/)(double) | Establecedor para [Aspose::Words::Drawing::ShapeBase::get_Top](./get_top/). |
| [set_TopRelative](./set_toprelative/)(float) | Establecedor para [Aspose::Words::Drawing::ShapeBase::get_TopRelative](./get_toprelative/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | Establecedor para [Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment](./get_verticalalignment/). |
| [set_Width](./set_width/)(double) | Establecedor para [Aspose::Words::Drawing::ShapeBase::get_Width](./get_width/). |
| [set_WidthRelative](./set_widthrelative/)(float) | Establecedor para [Aspose::Words::Drawing::ShapeBase::get_WidthRelative](./get_widthrelative/). |
| [set_WrapSide](./set_wrapside/)(Aspose::Words::Drawing::WrapSide) | Establecedor para [Aspose::Words::Drawing::ShapeBase::get_WrapSide](./get_wrapside/). |
| [set_WrapType](./set_wraptype/)(Aspose::Words::Drawing::WrapType) | Establecedor para [Aspose::Words::Drawing::ShapeBase::get_WrapType](./get_wraptype/). |
| [set_ZOrder](./set_zorder/)(int32_t) | Establecedor para [Aspose::Words::Drawing::ShapeBase::get_ZOrder](./get_zorder/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporta el contenido del nodo a una cadena usando las opciones de guardado especificadas. |
| static [Type](./type/)() |  |
## Observaciones


Esta es una clase abstracta. Las dos clases derivadas que puedes instanciar son [Shape](../shape/) y [GroupShape](../groupshape/).

Una forma es un nodo en el árbol del documento.

Si la forma es un hijo de un objeto [Paragraph](../../aspose.words/paragraph/), entonces se dice que la forma es "de nivel superior". Las formas de nivel superior se miden y posicionan en puntos.

Una forma también puede aparecer como hijo de un objeto [GroupShape](../groupshape/) cuando se agrupan varias formas. Las formas hijas de una forma de grupo se posicionan en el espacio de coordenadas y unidades definidas por las propiedades [CoordSize](./get_coordsize/) y [CoordOrigin](./get_coordorigin/) del grupo padre.

Una forma puede posicionarse en línea con el texto o flotante. El método de posicionamiento se controla mediante la propiedad [WrapType](./get_wraptype/).

Cuando una forma es flotante, se posiciona en relación a algo (p. ej., el párrafo actual, el margen o la página). El posicionamiento relativo de la forma se especifica usando las propiedades [RelativeHorizontalPosition](./get_relativehorizontalposition/) y [RelativeVerticalPosition](./get_relativeverticalposition/).

Una forma flotante se posiciona explícitamente usando las propiedades [Left](./get_left/) y [Top](./get_top/) o se alinea en relación a otro objeto usando las propiedades [HorizontalAlignment](./get_horizontalalignment/) y [VerticalAlignment](./get_verticalalignment/).

## Ejemplos



Muestra cómo insertar una imagen flotante en el centro de una página.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserta una imagen flotante que aparecerá detrás del texto superpuesto y alinéala al centro de la página.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## Ver también

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
