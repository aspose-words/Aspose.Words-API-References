---
title: GroupShape Class
linktitle: GroupShape
articleTitle: GroupShape
second_title: Aspose.Words para .NET
description: Aspose.Words.Drawing.GroupShape clase. Representa un grupo de formas en un documento en C#.
type: docs
weight: 1020
url: /es/net/aspose.words.drawing/groupshape/
---
## GroupShape class

Representa un grupo de formas en un documento.

Para obtener más información, visite el[Cómo agregar una forma de grupo a un documento de Word](https://docs.aspose.com/words/net/how-to-add-group-shape-into-a-word-document/) artículo de documentación.

```csharp
public class GroupShape : ShapeBase
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [GroupShape](groupshape/)(*[DocumentBase](../../aspose.words/documentbase/)*) | Crea una nueva forma de grupo. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AllowOverlap](../../aspose.words.drawing/shapebase/allowoverlap/) { get; set; } | Obtiene o establece un valor que especifica si esta forma puede superponerse a otras formas. |
| [AlternativeText](../../aspose.words.drawing/shapebase/alternativetext/) { get; set; } | Define texto alternativo que se mostrará en lugar de un gráfico. |
| [AnchorLocked](../../aspose.words.drawing/shapebase/anchorlocked/) { get; set; } | Especifica si el ancla de la forma está bloqueada. |
| [AspectRatioLocked](../../aspose.words.drawing/shapebase/aspectratiolocked/) { get; set; } | Especifica si la relación de aspecto de la forma está bloqueada. |
| [BehindText](../../aspose.words.drawing/shapebase/behindtext/) { get; set; } | Especifica si la forma está debajo o encima del texto. |
| [Bottom](../../aspose.words.drawing/shapebase/bottom/) { get; } | Obtiene la posición del borde inferior del bloque contenedor de la forma. |
| [Bounds](../../aspose.words.drawing/shapebase/bounds/) { get; set; } | Obtiene o establece la ubicación y el tamaño del bloque contenedor de la forma. |
| [BoundsInPoints](../../aspose.words.drawing/shapebase/boundsinpoints/) { get; } | Obtiene la ubicación y el tamaño del bloque contenedor de la forma en puntos, en relación con el ancla de la forma superior. |
| [BoundsWithEffects](../../aspose.words.drawing/shapebase/boundswitheffects/) { get; } | Obtiene la extensión final que tiene este objeto de forma después de aplicar efectos de dibujo. El valor se mide en puntos. |
| [CanHaveImage](../../aspose.words.drawing/shapebase/canhaveimage/) { get; } | Devoluciones`verdadero` si el tipo de forma permite que la forma tenga una imagen. |
| [CoordOrigin](../../aspose.words.drawing/shapebase/coordorigin/) { get; set; } | Las coordenadas en la esquina superior izquierda del bloque que contiene esta forma. |
| [CoordSize](../../aspose.words.drawing/shapebase/coordsize/) { get; set; } | El ancho y alto del espacio de coordenadas dentro del bloque contenedor de esta forma. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtiene el número de hijos inmediatos de este nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Especifica el identificador de nodo personalizado. |
| [DistanceBottom](../../aspose.words.drawing/shapebase/distancebottom/) { get; set; } | Devuelve o establece la distancia (en puntos) entre el texto del documento y el borde inferior de la forma. |
| [DistanceLeft](../../aspose.words.drawing/shapebase/distanceleft/) { get; set; } | Devuelve o establece la distancia (en puntos) entre el texto del documento y el borde izquierdo de la forma. |
| [DistanceRight](../../aspose.words.drawing/shapebase/distanceright/) { get; set; } | Devuelve o establece la distancia (en puntos) entre el texto del documento y el borde derecho de la forma. |
| [DistanceTop](../../aspose.words.drawing/shapebase/distancetop/) { get; set; } | Devuelve o establece la distancia (en puntos) entre el texto del documento y el borde superior de la forma. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtiene el documento al que pertenece este nodo. |
| [Fill](../../aspose.words.drawing/shapebase/fill/) { get; } | Obtiene el formato de relleno para la forma. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtiene el primer hijo del nodo. |
| [FlipOrientation](../../aspose.words.drawing/shapebase/fliporientation/) { get; set; } | Cambia la orientación de una forma. |
| [Font](../../aspose.words.drawing/shapebase/font/) { get; } | Proporciona acceso al formato de fuente de este objeto. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Devoluciones`verdadero` si este nodo tiene nodos secundarios. |
| [Height](../../aspose.words.drawing/shapebase/height/) { get; set; } | Obtiene o establece la altura del bloque contenedor de la forma. |
| [HeightRelative](../../aspose.words.drawing/shapebase/heightrelative/) { get; set; } | Obtiene o establece el valor que representa el porcentaje de la altura relativa de la forma. |
| [HorizontalAlignment](../../aspose.words.drawing/shapebase/horizontalalignment/) { get; set; } | Especifica cómo se coloca la forma horizontalmente. |
| [HRef](../../aspose.words.drawing/shapebase/href/) { get; set; } | Obtiene o establece la dirección completa del hipervínculo para una forma. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Devoluciones`verdadero` ya que este nodo puede tener nodos secundarios. |
| [IsDecorative](../../aspose.words.drawing/shapebase/isdecorative/) { get; set; } | Obtiene o establece la bandera que especifica si la forma es decorativa en el documento. |
| [IsDeleteRevision](../../aspose.words.drawing/shapebase/isdeleterevision/) { get; } | Devuelve verdadero si este objeto se eliminó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsGroup](../../aspose.words.drawing/shapebase/isgroup/) { get; } | Devoluciones`verdadero` si se trata de una forma de grupo. |
| [IsHorizontalRule](../../aspose.words.drawing/shapebase/ishorizontalrule/) { get; } | Devoluciones`verdadero` si esta forma es una regla horizontal. |
| [IsImage](../../aspose.words.drawing/shapebase/isimage/) { get; } | Devoluciones`verdadero` si esta forma es una forma de imagen. |
| [IsInline](../../aspose.words.drawing/shapebase/isinline/) { get; } | Una forma rápida de determinar si esta forma está colocada en línea con el texto. |
| [IsInsertRevision](../../aspose.words.drawing/shapebase/isinsertrevision/) { get; } | Devuelve verdadero si este objeto se insertó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsLayoutInCell](../../aspose.words.drawing/shapebase/islayoutincell/) { get; set; } | Obtiene o establece una bandera que indica si la forma se muestra dentro o fuera de una tabla. |
| [IsMoveFromRevision](../../aspose.words.drawing/shapebase/ismovefromrevision/) { get; } | Devoluciones`verdadero` si este objeto se movió (eliminó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsMoveToRevision](../../aspose.words.drawing/shapebase/ismovetorevision/) { get; } | Devoluciones`verdadero` si este objeto se movió (insertó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsSignatureLine](../../aspose.words.drawing/shapebase/issignatureline/) { get; } | Indica que la forma es una[`SignatureLine`](../signatureline/) . |
| [IsTopLevel](../../aspose.words.drawing/shapebase/istoplevel/) { get; } | Devoluciones`verdadero`si esta forma no es hija de una forma de grupo. |
| [IsWordArt](../../aspose.words.drawing/shapebase/iswordart/) { get; } | Devoluciones`verdadero` si esta forma es un objeto de WordArt. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtiene el último hijo del nodo. |
| [Left](../../aspose.words.drawing/shapebase/left/) { get; set; } | Obtiene o establece la posición del borde izquierdo del bloque contenedor de la forma. |
| [LeftRelative](../../aspose.words.drawing/shapebase/leftrelative/) { get; set; } | Obtiene o establece el valor que representa la posición relativa izquierda de la forma en porcentaje. |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage/) { get; } | Obtiene MarkupLanguage utilizado para este objeto gráfico. |
| [Name](../../aspose.words.drawing/shapebase/name/) { get; set; } | Obtiene o establece el nombre de la forma opcional. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtiene el nodo que sigue inmediatamente a este nodo. |
| override [NodeType](../../aspose.words.drawing/groupshape/nodetype/) { get; } | DevolucionesGroupShape . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtiene el padre inmediato de este nodo. |
| [ParentParagraph](../../aspose.words.drawing/shapebase/parentparagraph/) { get; } | Devuelve el párrafo padre inmediato. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Devuelve un[`Range`](../../aspose.words/range/) objeto que representa la parte de un documento contenido en este nodo. |
| [RelativeHorizontalPosition](../../aspose.words.drawing/shapebase/relativehorizontalposition/) { get; set; } | Especifica en relación con la posición horizontal de la forma. |
| [RelativeHorizontalSize](../../aspose.words.drawing/shapebase/relativehorizontalsize/) { get; set; } | Obtiene o establece el valor del tamaño relativo de la forma en dirección horizontal. |
| [RelativeVerticalPosition](../../aspose.words.drawing/shapebase/relativeverticalposition/) { get; set; } | Especifica en relación con la posición vertical de la forma. |
| [RelativeVerticalSize](../../aspose.words.drawing/shapebase/relativeverticalsize/) { get; set; } | Obtiene o establece el valor del tamaño relativo de la forma en dirección vertical. |
| [Right](../../aspose.words.drawing/shapebase/right/) { get; } | Obtiene la posición del borde derecho del bloque contenedor de la forma. |
| [Rotation](../../aspose.words.drawing/shapebase/rotation/) { get; set; } | Define el ángulo (en grados) en el que se gira una forma. El valor positivo corresponde al ángulo de rotación en el sentido de las agujas del reloj. |
| [ScreenTip](../../aspose.words.drawing/shapebase/screentip/) { get; set; } | Define el texto que se muestra cuando el puntero del mouse se mueve sobre la forma. |
| [ShadowFormat](../../aspose.words.drawing/shapebase/shadowformat/) { get; } | Obtiene el formato de sombra para la forma. |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype/) { get; } | Obtiene el tipo de forma. |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints/) { get; } | Obtiene el tamaño de la forma en puntos. |
| [Target](../../aspose.words.drawing/shapebase/target/) { get; set; } | Obtiene o establece el marco de destino para el hipervínculo de forma. |
| [Title](../../aspose.words.drawing/shapebase/title/) { get; set; } | Obtiene o establece el título (título) del objeto de forma actual. |
| [Top](../../aspose.words.drawing/shapebase/top/) { get; set; } | Obtiene o establece la posición del borde superior del bloque contenedor de la forma. |
| [TopRelative](../../aspose.words.drawing/shapebase/toprelative/) { get; set; } | Obtiene o establece el valor que representa la posición superior relativa de la forma en porcentaje. |
| [VerticalAlignment](../../aspose.words.drawing/shapebase/verticalalignment/) { get; set; } | Especifica cómo se coloca la forma verticalmente. |
| [Width](../../aspose.words.drawing/shapebase/width/) { get; set; } | Obtiene o establece el ancho del bloque contenedor de la forma. |
| [WidthRelative](../../aspose.words.drawing/shapebase/widthrelative/) { get; set; } | Obtiene o establece el valor que representa el porcentaje del ancho relativo de la forma. |
| [WrapSide](../../aspose.words.drawing/shapebase/wrapside/) { get; set; } | Especifica cómo se ajusta el texto alrededor de la forma. |
| [WrapType](../../aspose.words.drawing/shapebase/wraptype/) { get; set; } | Define si la forma está en línea o flotante. Para formas flotantes, define el modo de ajuste del texto alrededor de la forma. |
| [ZOrder](../../aspose.words.drawing/shapebase/zorder/) { get; set; } | Determina el orden de visualización de las formas superpuestas. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words.drawing/groupshape/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Acepta un visitante. |
| [AdjustWithEffects](../../aspose.words.drawing/shapebase/adjustwitheffects/)(*RectangleF*) | Agrega al rectángulo de origen los valores de la extensión del efecto y devuelve el rectángulo final. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../../aspose.words/node/)*) | Agrega el nodo especificado al final de la lista de nodos secundarios para este nodo. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicado del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crea un navegador que se puede utilizar para atravesar y leer nodos. |
| [FetchInheritedShapeAttr](../../aspose.words.drawing/shapebase/fetchinheritedshapeattr/)(*int*) | Reservado para uso del sistema. IShapeAttrSource. |
| [FetchShapeAttr](../../aspose.words.drawing/shapebase/fetchshapeattr/)(*int*) | Reservado para uso del sistema. IShapeAttrSource. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Obtiene el primer ancestro del especificado[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Obtiene el primer antepasado del tipo de objeto especificado. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Devuelve un enésimo nodo secundario que coincide con el tipo especificado. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Devuelve una colección activa de nodos secundarios que coinciden con el tipo especificado. |
| [GetDirectShapeAttr](../../aspose.words.drawing/shapebase/getdirectshapeattr/)(*int*) | Reservado para uso del sistema. IShapeAttrSource. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Proporciona soporte para cada iteración de estilo sobre los nodos secundarios de este nodo. |
| [GetShapeRenderer](../../aspose.words.drawing/shapebase/getshaperenderer/)() | Crea y devuelve un objeto que se puede utilizar para representar esta forma en una imagen. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Obtiene el texto de este nodo y de todos sus hijos. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Devuelve el índice del nodo secundario especificado en la matriz de nodos secundarios. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | Inserta el nodo especificado inmediatamente después del nodo de referencia especificado. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | Inserta el nodo especificado inmediatamente antes del nodo de referencia especificado. |
| [LocalToParent](../../aspose.words.drawing/shapebase/localtoparent/)(*PointF*) | Convierte un valor del espacio de coordenadas local al espacio de coordenadas de la forma principal. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Obtiene el siguiente nodo según el algoritmo transversal del árbol de pedidos anticipados. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../../aspose.words/node/)*) | Agrega el nodo especificado al principio de la lista de nodos secundarios para este nodo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Obtiene el nodo anterior según el algoritmo transversal del árbol de pedidos anticipados. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina del padre. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Elimina todos los nodos secundarios del nodo actual. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../../aspose.words/node/)*) | Elimina el nodo secundario especificado. |
| [RemoveShapeAttr](../../aspose.words.drawing/shapebase/removeshapeattr/)(*int*) | Reservado para uso del sistema. IShapeAttrSource. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Elimina todo[`SmartTag`](../../aspose.words.markup/smarttag/)nodos descendientes del nodo actual. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Selecciona una lista de nodos que coinciden con la expresión XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Selecciona el primero[`Node`](../../aspose.words/node/) que coincide con la expresión XPath. |
| [SetShapeAttr](../../aspose.words.drawing/shapebase/setshapeattr/)(*int, object*) | Reservado para uso del sistema. IShapeAttrSource. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporta el contenido del nodo a una cadena usando las opciones de guardado especificadas. |

## Observaciones

A`GroupShape` es un nodo compuesto y puede tener[`Shape`](../shape/) y `GroupShape` nodos cuando eran niños.

Cada`GroupShape` define un nuevo sistema de coordenadas para sus formas secundarias. El sistema de coordenadas se define utilizando el[`CoordSize`](../shapebase/coordsize/) y [`CoordOrigin`](../shapebase/coordorigin/) propiedades.

## Ejemplos

Muestra cómo crear un grupo de formas e imprimir su contenido utilizando un visitante de documentos.

```csharp
public void GroupOfShapes()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Si necesita crear formas "no primitivas", como SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
    // TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, DiagonalCornersRounded
    // utilice los métodos DocumentBuilder.InsertShape.
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
/// Imprime el contenido de un grupo de formas visitado en la consola.
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

### Ver también

* class [ShapeBase](../shapebase/)
* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
