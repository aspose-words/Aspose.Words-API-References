---
title: Class Shape
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.Shape klas. Stellt ein Objekt in der Zeichnungsebene dar z. B. eine AutoForm ein Textfeld eine Freiform ein OLEObjekt ein ActiveXSteuerelement oder ein Bild.
type: docs
weight: 1250
url: /de/net/aspose.words.drawing/shape/
---
## Shape class

Stellt ein Objekt in der Zeichnungsebene dar, z. B. eine AutoForm, ein Textfeld, eine Freiform, ein OLE-Objekt, ein ActiveX-Steuerelement oder ein Bild.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Formen](https://docs.aspose.com/words/net/working-with-shapes/) Dokumentationsartikel.

```csharp
public sealed class Shape : ShapeBase
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [Shape](shape/)(DocumentBase, ShapeType) | Erstellt ein neues Formobjekt. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AllowOverlap](../../aspose.words.drawing/shapebase/allowoverlap/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der angibt, ob diese Form andere Formen überlappen kann. |
| [AlternativeText](../../aspose.words.drawing/shapebase/alternativetext/) { get; set; } | Definiert alternativen Text, der anstelle einer Grafik angezeigt werden soll. |
| [AnchorLocked](../../aspose.words.drawing/shapebase/anchorlocked/) { get; set; } | Gibt an, ob der Anker der Form gesperrt ist. |
| [AspectRatioLocked](../../aspose.words.drawing/shapebase/aspectratiolocked/) { get; set; } | Gibt an, ob das Seitenverhältnis der Form gesperrt ist. |
| [BehindText](../../aspose.words.drawing/shapebase/behindtext/) { get; set; } | Gibt an, ob die Form unter oder über dem Text liegt. |
| [Bottom](../../aspose.words.drawing/shapebase/bottom/) { get; } | Ermittelt die Position der Unterkante des enthaltenden Blocks der Form. |
| [Bounds](../../aspose.words.drawing/shapebase/bounds/) { get; set; } | Ruft die Position und Größe des enthaltenden Blocks der Form ab oder legt diese fest. |
| [BoundsInPoints](../../aspose.words.drawing/shapebase/boundsinpoints/) { get; } | Ruft die Position und Größe des enthaltenden Blocks der Form in Punkten ab, relativ zum Anker der obersten Form. |
| [BoundsWithEffects](../../aspose.words.drawing/shapebase/boundswitheffects/) { get; } | Ruft die endgültige Ausdehnung ab, die dieses Formobjekt nach dem Anwenden von Zeichnungseffekten hat. Der Wert wird in Punkten gemessen. |
| [CanHaveImage](../../aspose.words.drawing/shapebase/canhaveimage/) { get; } | Gibt zurück`WAHR` wenn der Formtyp zulässt, dass die Form ein Bild hat. |
| [Chart](../../aspose.words.drawing/shape/chart/) { get; } | Bietet Zugriff auf die Diagrammeigenschaften, wenn diese Form über eine verfügt[`Chart`](../../aspose.words.drawing.charts/chart/) . |
| [CoordOrigin](../../aspose.words.drawing/shapebase/coordorigin/) { get; set; } | Die Koordinaten in der oberen linken Ecke des enthaltenden Blocks dieser Form. |
| [CoordSize](../../aspose.words.drawing/shapebase/coordsize/) { get; set; } | Die Breite und Höhe des Koordinatenraums innerhalb des enthaltenden Blocks dieser Form. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ruft die Anzahl der unmittelbaren Kinder dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| [DistanceBottom](../../aspose.words.drawing/shapebase/distancebottom/) { get; set; } | Gibt den Abstand (in Punkten) zwischen dem Dokumenttext und der Unterkante der Form zurück oder legt ihn fest. |
| [DistanceLeft](../../aspose.words.drawing/shapebase/distanceleft/) { get; set; } | Gibt den Abstand (in Punkten) zwischen dem Dokumenttext und dem linken Rand der Form zurück oder legt ihn fest. |
| [DistanceRight](../../aspose.words.drawing/shapebase/distanceright/) { get; set; } | Gibt den Abstand (in Punkten) zwischen dem Dokumenttext und dem rechten Rand der Form zurück oder legt ihn fest. |
| [DistanceTop](../../aspose.words.drawing/shapebase/distancetop/) { get; set; } | Gibt den Abstand (in Punkten) zwischen dem Dokumenttext und der Oberkante der Form zurück oder legt ihn fest. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [ExtrusionEnabled](../../aspose.words.drawing/shape/extrusionenabled/) { get; } | Gibt zurück`WAHR` wenn ein Extrusionseffekt aktiviert ist. |
| [Fill](../../aspose.words.drawing/shapebase/fill/) { get; } | Ruft die Füllformatierung für die Form ab. |
| [FillColor](../../aspose.words.drawing/shape/fillcolor/) { get; set; } | Definiert die Pinselfarbe, die den geschlossenen Pfad der Form ausfüllt. |
| [Filled](../../aspose.words.drawing/shape/filled/) { get; set; } | Legt fest, ob der geschlossene Pfad der Form gefüllt wird. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FirstParagraph](../../aspose.words.drawing/shape/firstparagraph/) { get; } | Ruft den ersten Absatz in der Form ab. |
| [FlipOrientation](../../aspose.words.drawing/shapebase/fliporientation/) { get; set; } | Ändert die Ausrichtung einer Form. |
| [Font](../../aspose.words.drawing/shapebase/font/) { get; } | Bietet Zugriff auf die Schriftartformatierung dieses Objekts. |
| [HasChart](../../aspose.words.drawing/shape/haschart/) { get; } | Gibt zurück`WAHR` wenn das`Shape` hat ein[`Chart`](../../aspose.words.drawing.charts/chart/) . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Gibt zurück`WAHR` wenn dieser Knoten untergeordnete Knoten hat. |
| [HasImage](../../aspose.words.drawing/shape/hasimage/) { get; } | Gibt zurück`WAHR` wenn die Form Bildbytes hat oder ein Bild verknüpft. |
| [HasSmartArt](../../aspose.words.drawing/shape/hassmartart/) { get; } | Gibt zurück`WAHR` wenn das`Shape` hat ein SmartArt-Objekt. |
| [Height](../../aspose.words.drawing/shapebase/height/) { get; set; } | Ruft die Höhe des enthaltenden Blocks der Form ab oder legt sie fest. |
| [HeightRelative](../../aspose.words.drawing/shapebase/heightrelative/) { get; set; } | Ruft den Wert ab, der den Prozentsatz der relativen Höhe der Form darstellt, oder legt diesen fest. |
| [HorizontalAlignment](../../aspose.words.drawing/shapebase/horizontalalignment/) { get; set; } | Gibt an, wie die Form horizontal positioniert wird. |
| [HorizontalRuleFormat](../../aspose.words.drawing/shape/horizontalruleformat/) { get; } | Bietet Zugriff auf die Eigenschaften der horizontalen Regelform. Für eine Form, die keine horizontale Regel ist, wird zurückgegeben`Null` . |
| [HRef](../../aspose.words.drawing/shapebase/href/) { get; set; } | Ruft die vollständige Hyperlink-Adresse für eine Form ab oder legt diese fest. |
| [ImageData](../../aspose.words.drawing/shape/imagedata/) { get; } | Bietet Zugriff auf das Bild der Form. Gibt zurück`Null` wenn die Form kein Bild haben kann. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Gibt zurück`WAHR` da dieser Knoten untergeordnete Knoten haben kann. |
| [IsDecorative](../../aspose.words.drawing/shapebase/isdecorative/) { get; set; } | Ruft das Flag ab, das angibt, ob die Form im Dokument dekorativ ist, oder legt dieses fest. |
| [IsDeleteRevision](../../aspose.words.drawing/shapebase/isdeleterevision/) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war. |
| [IsGroup](../../aspose.words.drawing/shapebase/isgroup/) { get; } | Gibt zurück`WAHR` wenn es sich um eine Gruppenform handelt. |
| [IsHorizontalRule](../../aspose.words.drawing/shapebase/ishorizontalrule/) { get; } | Gibt zurück`WAHR` wenn diese Form eine horizontale Regel ist. |
| [IsImage](../../aspose.words.drawing/shapebase/isimage/) { get; } | Gibt zurück`WAHR` wenn diese Form eine Bildform ist. |
| [IsInline](../../aspose.words.drawing/shapebase/isinline/) { get; } | Eine schnelle Möglichkeit, festzustellen, ob diese Form im Text positioniert ist. |
| [IsInsertRevision](../../aspose.words.drawing/shapebase/isinsertrevision/) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war. |
| [IsLayoutInCell](../../aspose.words.drawing/shapebase/islayoutincell/) { get; set; } | Ruft ein Flag ab oder setzt es, das angibt, ob die Form innerhalb oder außerhalb einer Tabelle angezeigt wird. |
| [IsMoveFromRevision](../../aspose.words.drawing/shapebase/ismovefromrevision/) { get; } | Gibt zurück`WAHR` wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsverfolgung aktiviert war. |
| [IsMoveToRevision](../../aspose.words.drawing/shapebase/ismovetorevision/) { get; } | Gibt zurück`WAHR` wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung aktiviert war. |
| [IsSignatureLine](../../aspose.words.drawing/shapebase/issignatureline/) { get; } | Gibt an, dass die Form ein ist[`SignatureLine`](../signatureline/) . |
| [IsTopLevel](../../aspose.words.drawing/shapebase/istoplevel/) { get; } | Gibt zurück`WAHR`wenn diese Form kein untergeordnetes Element einer Gruppenform ist. |
| [IsWordArt](../../aspose.words.drawing/shapebase/iswordart/) { get; } | Gibt zurück`WAHR` wenn diese Form ein WordArt-Objekt ist. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [LastParagraph](../../aspose.words.drawing/shape/lastparagraph/) { get; } | Ruft den letzten Absatz in der Form ab. |
| [Left](../../aspose.words.drawing/shapebase/left/) { get; set; } | Ruft die Position der linken Kante des enthaltenden Blocks der Form ab oder legt diese fest. |
| [LeftRelative](../../aspose.words.drawing/shapebase/leftrelative/) { get; set; } | Ruft den Wert ab, der die relative linke Position der Form in Prozent darstellt, oder legt diesen fest. |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage/) { get; } | Ruft die für dieses Grafikobjekt verwendete MarkupLanguage ab. |
| [Name](../../aspose.words.drawing/shapebase/name/) { get; set; } | Ruft den optionalen Formnamen ab oder legt ihn fest. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words.drawing/shape/nodetype/) { get; } | Gibt zurückShape . |
| [OleFormat](../../aspose.words.drawing/shape/oleformat/) { get; } | Bietet Zugriff auf die OLE-Daten einer Form. Für eine Form, die kein OLE-Objekt oder ActiveX-Steuerelement ist, wird zurückgegeben`Null` . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft das unmittelbare übergeordnete Element dieses Knotens ab. |
| [ParentParagraph](../../aspose.words.drawing/shapebase/parentparagraph/) { get; } | Gibt den unmittelbar übergeordneten Absatz zurück. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar vorangeht. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt a zurück[`Range`](../../aspose.words/range/) Objekt, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [RelativeHorizontalPosition](../../aspose.words.drawing/shapebase/relativehorizontalposition/) { get; set; } | Gibt relativ zur horizontalen Positionierung der Form an. |
| [RelativeHorizontalSize](../../aspose.words.drawing/shapebase/relativehorizontalsize/) { get; set; } | Ruft den Wert der relativen Größe der Form in horizontaler Richtung ab oder legt diesen fest. |
| [RelativeVerticalPosition](../../aspose.words.drawing/shapebase/relativeverticalposition/) { get; set; } | Gibt relativ zur vertikalen Positionierung der Form an. |
| [RelativeVerticalSize](../../aspose.words.drawing/shapebase/relativeverticalsize/) { get; set; } | Ruft den Wert der relativen Größe der Form in vertikaler Richtung ab oder legt diesen fest. |
| [Right](../../aspose.words.drawing/shapebase/right/) { get; } | Ermittelt die Position der rechten Kante des enthaltenden Blocks der Form. |
| [Rotation](../../aspose.words.drawing/shapebase/rotation/) { get; set; } | Definiert den Winkel (in Grad), um den eine Form gedreht wird. Positiver Wert entspricht dem Drehwinkel im Uhrzeigersinn. |
| [ScreenTip](../../aspose.words.drawing/shapebase/screentip/) { get; set; } | Definiert den Text, der angezeigt wird, wenn der Mauszeiger über die Form bewegt. |
| [ShadowEnabled](../../aspose.words.drawing/shape/shadowenabled/) { get; } | Gibt zurück`WAHR` wenn ein Schatteneffekt aktiviert ist. |
| [ShadowFormat](../../aspose.words.drawing/shapebase/shadowformat/) { get; } | Ruft die Schattenformatierung für die Form ab. |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype/) { get; } | Ruft den Formtyp ab. |
| [SignatureLine](../../aspose.words.drawing/shape/signatureline/) { get; } | Ruft ab[`SignatureLine`](../signatureline/) Objekt, wenn die Form eine Signaturlinie ist. Kehrt zurück`Null` sonst. |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints/) { get; } | Ermittelt die Größe der Form in Punkten. |
| [StoryType](../../aspose.words.drawing/shape/storytype/) { get; } | Gibt zurückTextbox . |
| [Stroke](../../aspose.words.drawing/shape/stroke/) { get; } | Definiert einen Strich für eine Form. |
| [StrokeColor](../../aspose.words.drawing/shape/strokecolor/) { get; set; } | Definiert die Farbe eines Strichs. |
| [Stroked](../../aspose.words.drawing/shape/stroked/) { get; set; } | Definiert, ob der Pfad gestrichen wird. |
| [StrokeWeight](../../aspose.words.drawing/shape/strokeweight/) { get; set; } | Definiert die Pinselstärke, die den Pfad einer Form in Punkten streicht. |
| [Target](../../aspose.words.drawing/shapebase/target/) { get; set; } | Ruft den Zielrahmen für den Form-Hyperlink ab oder legt diesen fest. |
| [TextBox](../../aspose.words.drawing/shape/textbox/) { get; } | Definiert Attribute, die angeben, wie Text in einer Form angezeigt wird. |
| [TextPath](../../aspose.words.drawing/shape/textpath/) { get; } | Definiert den Text des Textpfads (eines WordArt-Objekts). |
| [Title](../../aspose.words.drawing/shapebase/title/) { get; set; } | Ruft den Titel (Beschriftung) des aktuellen Formobjekts ab oder legt diesen fest. |
| [Top](../../aspose.words.drawing/shapebase/top/) { get; set; } | Ruft die Position der Oberkante des enthaltenden Blocks der Form ab oder legt diese fest. |
| [TopRelative](../../aspose.words.drawing/shapebase/toprelative/) { get; set; } | Ruft den Wert ab, der die relative obere Position der Form in Prozent darstellt, oder legt diesen fest. |
| [VerticalAlignment](../../aspose.words.drawing/shapebase/verticalalignment/) { get; set; } | Gibt an, wie die Form vertikal positioniert wird. |
| [Width](../../aspose.words.drawing/shapebase/width/) { get; set; } | Ruft die Breite des enthaltenden Blocks der Form ab oder legt sie fest. |
| [WidthRelative](../../aspose.words.drawing/shapebase/widthrelative/) { get; set; } | Ruft den Wert ab, der den Prozentsatz der relativen Breite der Form darstellt, oder legt diesen fest. |
| [WrapSide](../../aspose.words.drawing/shapebase/wrapside/) { get; set; } | Gibt an, wie der Text um die Form gewickelt wird. |
| [WrapType](../../aspose.words.drawing/shapebase/wraptype/) { get; set; } | Definiert, ob die Form inline oder schwebend ist. Für schwebende Formen definiert den Umbruchmodus für Text um die Form. |
| [ZOrder](../../aspose.words.drawing/shapebase/zorder/) { get; set; } | Bestimmt die Anzeigereihenfolge überlappender Formen. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words.drawing/shape/accept/)(DocumentVisitor) | Akzeptiert einen Besucher. |
| override [AcceptEnd](../../aspose.words.drawing/shape/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words.drawing/shape/acceptstart/)(DocumentVisitor) |  |
| [AdjustWithEffects](../../aspose.words.drawing/shapebase/adjustwitheffects/)(RectangleF) | Fügt zu den Quellrechteckwerten der Effektausdehnung hinzu und gibt das endgültige Rechteck zurück. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Erstellt einen Navigator, der zum Durchlaufen und Lesen von Knoten verwendet werden kann. |
| [FetchInheritedShapeAttr](../../aspose.words.drawing/shapebase/fetchinheritedshapeattr/)(int) | Reserviert für die Systemnutzung. IShapeAttrSource. |
| [FetchShapeAttr](../../aspose.words.drawing/shapebase/fetchshapeattr/)(int) | Reserviert für die Systemnutzung. IShapeAttrSource. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Ruft den ersten Vorfahren des angegebenen ab[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Gibt eine Live-Sammlung untergeordneter Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetDirectShapeAttr](../../aspose.words.drawing/shapebase/getdirectshapeattr/)(int) | Reserviert für die Systemnutzung. IShapeAttrSource. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bietet Unterstützung für die Iteration jedes Stils über die untergeordneten Knoten dieses Knotens. |
| [GetShapeRenderer](../../aspose.words.drawing/shapebase/getshaperenderer/)() | Erstellt ein Objekt und gibt es zurück, das zum Rendern dieser Form in ein Bild verwendet werden kann. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ruft den Text dieses Knotens und aller seiner untergeordneten Knoten ab. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knoten-Array zurück. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [LocalToParent](../../aspose.words.drawing/shapebase/localtoparent/)(PointF) | Konvertiert einen Wert aus dem lokalen Koordinatenraum in den Koordinatenraum der übergeordneten Form. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ruft den nächsten Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ruft den vorherigen Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Entfernt alle untergeordneten Knoten des aktuellen Knotens. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveShapeAttr](../../aspose.words.drawing/shapebase/removeshapeattr/)(int) | Reserviert für die Systemnutzung. IShapeAttrSource. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Entfernt alle[`SmartTag`](../../aspose.words.markup/smarttag/)Nachkommenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Wählt den ersten aus[`Node`](../../aspose.words/node/) das entspricht dem XPath-Ausdruck. |
| [SetShapeAttr](../../aspose.words.drawing/shapebase/setshapeattr/)(int, object) | Reserviert für die Systemnutzung. IShapeAttrSource. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exportiert den Inhalt des Knotens in einen String im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exportiert den Inhalt des Knotens mit den angegebenen Speicheroptionen in einen String. |
| [UpdateSmartArtDrawing](../../aspose.words.drawing/shape/updatesmartartdrawing/)() | Aktualisiert die vorgerenderte SmartArt-Zeichnung mithilfe der SmartArt-Cold-Rendering-Engine von Aspose.Words. |

### Bemerkungen

Verwendung der`Shape` Mit der Klasse können Sie Formen in einem Microsoft Word-Dokument erstellen oder ändern.

Eine wichtige Eigenschaft einer Form ist ihre[`ShapeType`](../shapebase/shapetype/)Formen verschiedener -Typen können in einem Word-Dokument unterschiedliche Funktionen haben. Beispielsweise können nur Bilder und OLE-Shapes Bilder enthalten. Die meisten Formen können Text enthalten, aber nicht alle.

Formen, die Text enthalten können, können enthalten[`Paragraph`](../../aspose.words/paragraph/) and [`Table`](../../aspose.words.tables/table/) Knoten als Kinder.

### Beispiele

Zeigt, wie man ein schwebendes Bild in der Mitte einer Seite einfügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein schwebendes Bild ein, das hinter dem überlappenden Text erscheint, und richten Sie es in der Mitte der Seite aus.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Zeigt, wie man Bilder aus einem Dokument extrahiert und sie als einzelne Dateien im lokalen Dateisystem speichert.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Holen Sie sich die Formensammlung aus dem Dokument,
// und die Bilddaten jeder Form mit einem Bild als Datei im lokalen Dateisystem speichern.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // Die Bilddaten von Formen können Bilder in vielen möglichen Bildformaten enthalten.
        // Wir können für jedes Bild automatisch eine Dateierweiterung anhand seines Formats ermitteln.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

Zeigt, wie alle Formen aus einem Dokument gelöscht werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Zwei Formen zusammen mit einer Gruppenform mit einer anderen Form darin einfügen.
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

// Alle Shape-Knoten aus dem Dokument entfernen.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
shapes.Clear();

// Alle Formen sind verschwunden, aber die Gruppenform ist immer noch im Dokument.
Assert.AreEqual(1, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);

// Alle Gruppenformen einzeln entfernen.
NodeCollection groupShapes = doc.GetChildNodes(NodeType.GroupShape, true);
groupShapes.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Siehe auch

* class [ShapeBase](../shapebase/)
* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)


