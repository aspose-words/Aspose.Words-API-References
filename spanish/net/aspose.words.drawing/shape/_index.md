---
title: Shape
second_title: Referencia de API de Aspose.Words para .NET
description: Representa un objeto en la capa de dibujo como una autoforma cuadro de texto forma libre objeto OLE control ActiveX o imagen.
type: docs
weight: 1100
url: /es/net/aspose.words.drawing/shape/
---
## Shape class

Representa un objeto en la capa de dibujo, como una autoforma, cuadro de texto, forma libre, objeto OLE, control ActiveX o imagen.

```csharp
public sealed class Shape : ShapeBase
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [Shape](shape/)(DocumentBase, ShapeType) | Crea un nuevo objeto de forma. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AllowOverlap](../../aspose.words.drawing/shapebase/allowoverlap/) { get; set; } | Obtiene o establece un valor que especifica si esta forma puede superponerse a otras formas. |
| [AlternativeText](../../aspose.words.drawing/shapebase/alternativetext/) { get; set; } | Define el texto alternativo que se mostrará en lugar de un gráfico. |
| [AnchorLocked](../../aspose.words.drawing/shapebase/anchorlocked/) { get; set; } | Especifica si el ancla de la forma está bloqueada. |
| [AspectRatioLocked](../../aspose.words.drawing/shapebase/aspectratiolocked/) { get; set; } | Especifica si la relación de aspecto de la forma está bloqueada. |
| [BehindText](../../aspose.words.drawing/shapebase/behindtext/) { get; set; } | Especifica si la forma está debajo o encima del texto. |
| [Bottom](../../aspose.words.drawing/shapebase/bottom/) { get; } | Obtiene la posición del borde inferior del bloque contenedor de la forma. |
| [Bounds](../../aspose.words.drawing/shapebase/bounds/) { get; set; } | Obtiene o establece la ubicación y el tamaño del bloque contenedor de la forma. |
| [BoundsInPoints](../../aspose.words.drawing/shapebase/boundsinpoints/) { get; } | Obtiene la ubicación y el tamaño del bloque contenedor de la forma en puntos, en relación con el ancla de la forma superior. |
| [BoundsWithEffects](../../aspose.words.drawing/shapebase/boundswitheffects/) { get; } | Obtiene la extensión final que tiene este objeto de forma después de aplicar los efectos de dibujo. El valor se mide en puntos. |
| [CanHaveImage](../../aspose.words.drawing/shapebase/canhaveimage/) { get; } | Devuelve verdadero si el tipo de forma permite que la forma tenga una imagen. |
| [Chart](../../aspose.words.drawing/shape/chart/) { get; } | Proporciona acceso a las propiedades del gráfico si esta forma tiene un Gráfico. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Obtiene todos los nodos secundarios inmediatos de este nodo. |
| [CoordOrigin](../../aspose.words.drawing/shapebase/coordorigin/) { get; set; } | Las coordenadas en la esquina superior izquierda del bloque contenedor de esta forma. |
| [CoordSize](../../aspose.words.drawing/shapebase/coordsize/) { get; set; } | El ancho y alto del espacio de coordenadas dentro del bloque contenedor de esta forma. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtiene el número de hijos inmediatos de este nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Especifica el identificador de nodo personalizado. |
| [DistanceBottom](../../aspose.words.drawing/shapebase/distancebottom/) { get; set; } | Devuelve o establece la distancia (en puntos) entre el texto del documento y el borde inferior de la forma. |
| [DistanceLeft](../../aspose.words.drawing/shapebase/distanceleft/) { get; set; } | Devuelve o establece la distancia (en puntos) entre el texto del documento y el borde izquierdo de la forma. |
| [DistanceRight](../../aspose.words.drawing/shapebase/distanceright/) { get; set; } | Devuelve o establece la distancia (en puntos) entre el texto del documento y el borde derecho de la forma. |
| [DistanceTop](../../aspose.words.drawing/shapebase/distancetop/) { get; set; } | Devuelve o establece la distancia (en puntos) entre el texto del documento y el borde superior de la forma. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtiene el documento al que pertenece este nodo. |
| [ExtrusionEnabled](../../aspose.words.drawing/shape/extrusionenabled/) { get; } | Devuelve verdadero si se activa un efecto de extrusión. |
| [Fill](../../aspose.words.drawing/shapebase/fill/) { get; } | Obtiene el formato de relleno para la forma. |
| [FillColor](../../aspose.words.drawing/shape/fillcolor/) { get; set; } | Define el color del pincel que llena el camino cerrado de la forma. |
| [Filled](../../aspose.words.drawing/shape/filled/) { get; set; } | Determina si se rellenará la ruta cerrada de la forma. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtiene el primer hijo del nodo. |
| [FirstParagraph](../../aspose.words.drawing/shape/firstparagraph/) { get; } | Obtiene el primer párrafo de la forma. |
| [FlipOrientation](../../aspose.words.drawing/shapebase/fliporientation/) { get; set; } | Cambia la orientación de una forma. |
| [Font](../../aspose.words.drawing/shapebase/font/) { get; } | Proporciona acceso al formato de fuente de este objeto. |
| [HasChart](../../aspose.words.drawing/shape/haschart/) { get; } | Devuelve verdadero si esta Forma tiene un[`Chart`](./chart/) . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Devuelve verdadero si este nodo tiene nodos secundarios. |
| [HasImage](../../aspose.words.drawing/shape/hasimage/) { get; } | Devuelve verdadero si la forma tiene bytes de imagen o vincula una imagen. |
| [HasSmartArt](../../aspose.words.drawing/shape/hassmartart/) { get; } | Devuelve verdadero si esta Forma tiene un objeto SmartArt. |
| [Height](../../aspose.words.drawing/shapebase/height/) { get; set; } | Obtiene o establece la altura del bloque contenedor de la forma. |
| [HorizontalAlignment](../../aspose.words.drawing/shapebase/horizontalalignment/) { get; set; } | Especifica cómo se coloca la forma horizontalmente. |
| [HorizontalRuleFormat](../../aspose.words.drawing/shape/horizontalruleformat/) { get; } | Proporciona acceso a las propiedades de la forma de regla horizontal. Para una forma que no es una regla horizontal, devuelve nulo. |
| [HRef](../../aspose.words.drawing/shapebase/href/) { get; set; } | Obtiene o establece la dirección de hipervínculo completa para una forma. |
| [ImageData](../../aspose.words.drawing/shape/imagedata/) { get; } | Proporciona acceso a la imagen de la forma. Devuelve nulo si la forma no puede tener una imagen. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Devuelve verdadero ya que este nodo puede tener nodos secundarios. |
| [IsDecorative](../../aspose.words.drawing/shapebase/isdecorative/) { get; set; } | Obtiene o establece el indicador que especifica si la forma es decorativa en el documento. |
| [IsDeleteRevision](../../aspose.words.drawing/shapebase/isdeleterevision/) { get; } | Devuelve verdadero si este objeto se eliminó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsGroup](../../aspose.words.drawing/shapebase/isgroup/) { get; } | Devuelve verdadero si se trata de una forma de grupo. |
| [IsHorizontalRule](../../aspose.words.drawing/shapebase/ishorizontalrule/) { get; } | Devuelve verdadero si esta forma es una regla horizontal. |
| [IsImage](../../aspose.words.drawing/shapebase/isimage/) { get; } | Devuelve verdadero si esta forma es una forma de imagen. |
| [IsInline](../../aspose.words.drawing/shapebase/isinline/) { get; } | Una forma rápida de determinar si esta forma se coloca en línea con el texto. |
| [IsInsertRevision](../../aspose.words.drawing/shapebase/isinsertrevision/) { get; } | Devuelve verdadero si este objeto se insertó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsLayoutInCell](../../aspose.words.drawing/shapebase/islayoutincell/) { get; set; } | Obtiene o establece un indicador que indica si la figura se muestra dentro o fuera de una tabla. |
| [IsMoveFromRevision](../../aspose.words.drawing/shapebase/ismovefromrevision/) { get; } | Devoluciones **verdadero** si este objeto se movió (eliminó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsMoveToRevision](../../aspose.words.drawing/shapebase/ismovetorevision/) { get; } | Devoluciones **verdadero** si este objeto se movió (insertó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsSignatureLine](../../aspose.words.drawing/shapebase/issignatureline/) { get; } | Indica que la forma es una SignatureLine. |
| [IsTopLevel](../../aspose.words.drawing/shapebase/istoplevel/) { get; } | Devuelve verdadero si esta forma no es hija de una forma de grupo. |
| [IsWordArt](../../aspose.words.drawing/shapebase/iswordart/) { get; } | Devuelve verdadero si esta forma es un objeto de WordArt. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtiene el último hijo del nodo. |
| [LastParagraph](../../aspose.words.drawing/shape/lastparagraph/) { get; } | Obtiene el último párrafo de la forma. |
| [Left](../../aspose.words.drawing/shapebase/left/) { get; set; } | Obtiene o establece la posición del borde izquierdo del bloque contenedor de la forma. |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage/) { get; } | Obtiene MarkupLanguage utilizado para este objeto gráfico. |
| [Name](../../aspose.words.drawing/shapebase/name/) { get; set; } | Obtiene o establece el nombre de forma opcional. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtiene el nodo que sigue inmediatamente a este nodo. |
| override [NodeType](../../aspose.words.drawing/shape/nodetype/) { get; } | DevolucionesShape . |
| [OleFormat](../../aspose.words.drawing/shape/oleformat/) { get; } | Proporciona acceso a los datos OLE de una forma. Para una forma que no es un objeto OLE o un control ActiveX, devuelve nulo. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtiene el padre inmediato de este nodo. |
| [ParentParagraph](../../aspose.words.drawing/shapebase/parentparagraph/) { get; } | Devuelve el párrafo padre inmediato. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Devuelve un **Rango** objeto que representa la parte de un documento que está contenido en este nodo. |
| [RelativeHorizontalPosition](../../aspose.words.drawing/shapebase/relativehorizontalposition/) { get; set; } | Especifica en relación con la posición horizontal de la forma. |
| [RelativeVerticalPosition](../../aspose.words.drawing/shapebase/relativeverticalposition/) { get; set; } | Especifica en relación a qué forma se coloca verticalmente. |
| [Right](../../aspose.words.drawing/shapebase/right/) { get; } | Obtiene la posición del borde derecho del bloque contenedor de la forma. |
| [Rotation](../../aspose.words.drawing/shapebase/rotation/) { get; set; } | Define el ángulo (en grados) con el que se rota una forma. El valor positivo corresponde al ángulo de rotación en el sentido de las agujas del reloj. |
| [ScreenTip](../../aspose.words.drawing/shapebase/screentip/) { get; set; } | Define el texto que se muestra cuando el puntero del mouse se mueve sobre la forma. |
| [ShadowEnabled](../../aspose.words.drawing/shape/shadowenabled/) { get; } | Devuelve verdadero si un efecto de sombra está habilitado. |
| [ShadowFormat](../../aspose.words.drawing/shapebase/shadowformat/) { get; } | Obtiene el formato de sombra para la forma. |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype/) { get; } | Obtiene el tipo de forma. |
| [SignatureLine](../../aspose.words.drawing/shape/signatureline/) { get; } | Obtiene[`SignatureLine`](./signatureline/) objeto si la forma es una línea de firma. Devoluciones **nulo** de lo contrario. |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints/) { get; } | Obtiene el tamaño de la forma en puntos. |
| [StoryType](../../aspose.words.drawing/shape/storytype/) { get; } | DevolucionesTextbox . |
| [Stroke](../../aspose.words.drawing/shape/stroke/) { get; } | Define un trazo para una forma. |
| [StrokeColor](../../aspose.words.drawing/shape/strokecolor/) { get; set; } | Define el color de un trazo. |
| [Stroked](../../aspose.words.drawing/shape/stroked/) { get; set; } | Define si se trazará el trazado. |
| [StrokeWeight](../../aspose.words.drawing/shape/strokeweight/) { get; set; } | Define el grosor del pincel que traza el camino de una forma en puntos. |
| [Target](../../aspose.words.drawing/shapebase/target/) { get; set; } | Obtiene o establece el marco de destino para el hipervínculo de forma. |
| [TextBox](../../aspose.words.drawing/shape/textbox/) { get; } | Define atributos que especifican cómo se muestra el texto en una forma. |
| [TextPath](../../aspose.words.drawing/shape/textpath/) { get; } | Define el texto de la ruta de texto (de un objeto de WordArt). |
| [Title](../../aspose.words.drawing/shapebase/title/) { get; set; } | Obtiene o establece el título (título) del objeto de forma actual. |
| [Top](../../aspose.words.drawing/shapebase/top/) { get; set; } | Obtiene o establece la posición del borde superior del bloque contenedor de la forma. |
| [VerticalAlignment](../../aspose.words.drawing/shapebase/verticalalignment/) { get; set; } | Especifica cómo se coloca la forma verticalmente. |
| [Width](../../aspose.words.drawing/shapebase/width/) { get; set; } | Obtiene o establece el ancho del bloque contenedor de la forma. |
| [WrapSide](../../aspose.words.drawing/shapebase/wrapside/) { get; set; } | Especifica cómo se envuelve el texto alrededor de la forma. |
| [WrapType](../../aspose.words.drawing/shapebase/wraptype/) { get; set; } | Define si la forma es en línea o flotante. Para formas flotantes define el modo de ajuste para el texto alrededor de la forma. |
| [ZOrder](../../aspose.words.drawing/shapebase/zorder/) { get; set; } | Determina el orden de visualización de las formas superpuestas. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words.drawing/shape/accept/)(DocumentVisitor) | Acepta un visitante. |
| [AdjustWithEffects](../../aspose.words.drawing/shapebase/adjustwitheffects/)(RectangleF) | Agrega al rectángulo de origen los valores de la extensión del efecto y devuelve el rectángulo final. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Agrega el nodo especificado al final de la lista de nodos secundarios para este nodo. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicado del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Reservado para uso del sistema. IXPathNavigable. |
| [FetchInheritedShapeAttr](../../aspose.words.drawing/shapebase/fetchinheritedshapeattr/)(int) | Reservado para uso del sistema. IShapeAttrSource. |
| [FetchShapeAttr](../../aspose.words.drawing/shapebase/fetchshapeattr/)(int) | Reservado para uso del sistema. IShapeAttrSource. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Obtiene el primer ancestro del especificado[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Obtiene el primer ancestro del tipo de objeto especificado. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Devuelve un enésimo nodo secundario que coincide con el tipo especificado. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Devuelve una colección activa de nodos secundarios que coinciden con el tipo especificado. |
| [GetDirectShapeAttr](../../aspose.words.drawing/shapebase/getdirectshapeattr/)(int) | Reservado para uso del sistema. IShapeAttrSource. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Proporciona soporte para la iteración de cada estilo sobre los nodos secundarios de este nodo. |
| [GetShapeRenderer](../../aspose.words.drawing/shapebase/getshaperenderer/)() | Crea y devuelve un objeto que se puede usar para convertir esta forma en una imagen. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Obtiene el texto de este nodo y de todos sus hijos. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Devuelve el índice del nodo secundario especificado en la matriz de nodos secundarios. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Inserta el nodo especificado inmediatamente después del nodo de referencia especificado. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Inserta el nodo especificado inmediatamente antes del nodo de referencia especificado. |
| [LocalToParent](../../aspose.words.drawing/shapebase/localtoparent/)(PointF) | Convierte un valor del espacio de coordenadas local en el espacio de coordenadas de la forma principal. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Obtiene el siguiente nodo de acuerdo con el algoritmo de recorrido del árbol de pedido previo. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Agrega el nodo especificado al principio de la lista de nodos secundarios para este nodo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Obtiene el nodo anterior de acuerdo con el algoritmo de recorrido del árbol de pedido previo. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina a sí mismo del padre. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Elimina todos los nodos secundarios del nodo actual. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Elimina el nodo secundario especificado. |
| [RemoveShapeAttr](../../aspose.words.drawing/shapebase/removeshapeattr/)(int) | Reservado para uso del sistema. IShapeAttrSource. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Elimina todo[`SmartTag`](../../aspose.words.markup/smarttag/) nodos descendientes del nodo actual. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Selecciona una lista de nodos que coinciden con la expresión XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Selecciona el primer nodo que coincide con la expresión XPath. |
| [SetShapeAttr](../../aspose.words.drawing/shapebase/setshapeattr/)(int, object) | Reservado para uso del sistema. IShapeAttrSource. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporta el contenido del nodo a una cadena utilizando las opciones de guardado especificadas. |
| [UpdateSmartArtDrawing](../../aspose.words.drawing/shape/updatesmartartdrawing/)() | Actualiza el dibujo renderizado previamente de SmartArt mediante el uso del motor de renderizado en frío SmartArt de Aspose.Words. |

### Observaciones

Utilizando el[`Shape`](./shape/) clase puede crear o modificar formas en un documento de Microsoft Word.

Una propiedad importante de una forma es su[`ShapeType`](../shapebase/shapetype/). Las formas de diferentes tipos pueden tener diferentes capacidades en un documento de Word. Por ejemplo, solo la imagen y las formas OLE pueden tener imágenes en su interior. La mayoría de las formas pueden tener texto, pero no todas.

Las formas que pueden tener texto, pueden contener[`Paragraph`](../../aspose.words/paragraph/) y [`Table`](../../aspose.words.tables/table/) nodos cuando eran niños.

### Ejemplos

Muestra cómo insertar una imagen flotante en el centro de una página.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta una imagen flotante que aparecerá detrás del texto superpuesto y alinéala con el centro de la página.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Muestra cómo extraer imágenes de un documento y guardarlas en el sistema de archivos local como archivos individuales.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Obtener la colección de formas del documento,
// y guarde los datos de imagen de cada forma con una imagen como un archivo en el sistema de archivos local.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
        // Los datos de imagen de las formas pueden contener imágenes de muchos formatos de imagen posibles. 
        // Podemos determinar una extensión de archivo para cada imagen automáticamente, en función de su formato.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

Muestra cómo eliminar todas las formas de un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta dos formas junto con una forma de grupo con otra forma dentro.
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

// Eliminar todos los nodos de forma del documento.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
shapes.Clear();

// Todas las formas se han ido, pero la forma del grupo todavía está en el documento.
Assert.AreEqual(1, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);

// Elimina todas las formas del grupo por separado.
NodeCollection groupShapes = doc.GetChildNodes(NodeType.GroupShape, true);
groupShapes.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Ver también

* class [ShapeBase](../shapebase/)
* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
