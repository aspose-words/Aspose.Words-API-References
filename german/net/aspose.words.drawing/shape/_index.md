---
title: Shape
second_title: Aspose.Words für .NET-API-Referenz
description: Stellt ein Objekt in der Zeichnungsebene dar z. B. eine AutoForm ein Textfeld eine Freiform ein OLE-Objekt ein ActiveX-Steuerelement oder ein Bild.
type: docs
weight: 1100
url: /de/net/aspose.words.drawing/shape/
---
## Shape class

Stellt ein Objekt in der Zeichnungsebene dar, z. B. eine AutoForm, ein Textfeld, eine Freiform, ein OLE-Objekt, ein ActiveX-Steuerelement oder ein Bild.

```csharp
public sealed class Shape : ShapeBase
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [Shape](shape)(DocumentBase, ShapeType) | Erstellt ein neues Formobjekt. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AllowOverlap](../../aspose.words.drawing/shapebase/allowoverlap) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob diese Form andere Formen überlappen kann. |
| [AlternativeText](../../aspose.words.drawing/shapebase/alternativetext) { get; set; } | Definiert alternativen Text, der anstelle einer Grafik angezeigt werden soll. |
| [AnchorLocked](../../aspose.words.drawing/shapebase/anchorlocked) { get; set; } | Gibt an, ob der Anker der Form gesperrt ist. |
| [AspectRatioLocked](../../aspose.words.drawing/shapebase/aspectratiolocked) { get; set; } | Gibt an, ob das Seitenverhältnis der Form gesperrt ist. |
| [BehindText](../../aspose.words.drawing/shapebase/behindtext) { get; set; } | Gibt an, ob sich die Form unter oder über Text befindet. |
| [Bottom](../../aspose.words.drawing/shapebase/bottom) { get; } | Ruft die Position der Unterkante des umgebenden Blocks der Form ab. |
| [Bounds](../../aspose.words.drawing/shapebase/bounds) { get; set; } | Ruft die Position und Größe des umgebenden Blocks der Form ab oder legt sie fest. |
| [BoundsInPoints](../../aspose.words.drawing/shapebase/boundsinpoints) { get; } | Ruft die Position und Größe des umgebenden Blocks der Form in Punkt relativ zum Anker der obersten Form ab. |
| [BoundsWithEffects](../../aspose.words.drawing/shapebase/boundswitheffects) { get; } | Ruft die endgültige Ausdehnung ab, die dieses Formobjekt nach dem Anwenden von Zeichnungseffekten hat. Der Wert wird in Punkten gemessen. |
| [CanHaveImage](../../aspose.words.drawing/shapebase/canhaveimage) { get; } | Gibt „true“ zurück, wenn der Formtyp zulässt, dass die Form ein Bild hat. |
| [Chart](../../aspose.words.drawing/shape/chart) { get; } | Bietet Zugriff auf die Diagrammeigenschaften, wenn diese Form über ein Diagramm verfügt. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Ruft alle unmittelbar untergeordneten Knoten dieses Knotens ab. |
| [CoordOrigin](../../aspose.words.drawing/shapebase/coordorigin) { get; set; } | Die Koordinaten in der linken oberen Ecke des umgebenden Blocks dieser Form. |
| [CoordSize](../../aspose.words.drawing/shapebase/coordsize) { get; set; } | Die Breite und Höhe des Koordinatenraums innerhalb des umgebenden Blocks dieser Form. |
| [Count](../../aspose.words/compositenode/count) { get; } | Ruft die Anzahl der unmittelbaren Kinder dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| [DistanceBottom](../../aspose.words.drawing/shapebase/distancebottom) { get; set; } | Gibt den Abstand (in Punkt) zwischen dem Dokumenttext und der Unterkante der Form zurück oder legt ihn fest. |
| [DistanceLeft](../../aspose.words.drawing/shapebase/distanceleft) { get; set; } | Gibt den Abstand (in Punkt) zwischen dem Dokumenttext und der linken Kante der Form zurück oder legt ihn fest. |
| [DistanceRight](../../aspose.words.drawing/shapebase/distanceright) { get; set; } | Gibt den Abstand (in Punkt) zwischen dem Dokumenttext und der rechten Kante der Form zurück oder legt ihn fest. |
| [DistanceTop](../../aspose.words.drawing/shapebase/distancetop) { get; set; } | Gibt den Abstand (in Punkt) zwischen dem Dokumenttext und der Oberkante der Form zurück oder legt ihn fest. |
| virtual [Document](../../aspose.words/node/document) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [ExtrusionEnabled](../../aspose.words.drawing/shape/extrusionenabled) { get; } | Gibt wahr zurück, wenn ein Extrusionseffekt aktiviert ist. |
| [Fill](../../aspose.words.drawing/shapebase/fill) { get; } | Ruft die Füllformatierung für die Form ab. |
| [FillColor](../../aspose.words.drawing/shape/fillcolor) { get; set; } | Definiert die Pinselfarbe, die den geschlossenen Pfad der Form ausfüllt. |
| [Filled](../../aspose.words.drawing/shape/filled) { get; set; } | Legt fest, ob der geschlossene Pfad der Form gefüllt wird. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FirstParagraph](../../aspose.words.drawing/shape/firstparagraph) { get; } | Ruft den ersten Absatz in der Form ab. |
| [FlipOrientation](../../aspose.words.drawing/shapebase/fliporientation) { get; set; } | Ändert die Ausrichtung einer Form. |
| [Font](../../aspose.words.drawing/shapebase/font) { get; } | Bietet Zugriff auf die Schriftformatierung dieses Objekts. |
| [HasChart](../../aspose.words.drawing/shape/haschart) { get; } | Gibt wahr zurück, wenn diese Form ein hat[`Chart`](./chart) . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Gibt wahr zurück, wenn dieser Knoten untergeordnete Knoten hat. |
| [HasImage](../../aspose.words.drawing/shape/hasimage) { get; } | Gibt „true“ zurück, wenn die Form Bildbytes enthält oder ein Bild verknüpft. |
| [HasSmartArt](../../aspose.words.drawing/shape/hassmartart) { get; } | Gibt wahr zurück, wenn diese Form ein SmartArt-Objekt hat. |
| [Height](../../aspose.words.drawing/shapebase/height) { get; set; } | Ruft die Höhe des umgebenden Blocks der Form ab oder legt sie fest. |
| [HorizontalAlignment](../../aspose.words.drawing/shapebase/horizontalalignment) { get; set; } | Gibt an, wie die Form horizontal positioniert wird. |
| [HorizontalRuleFormat](../../aspose.words.drawing/shape/horizontalruleformat) { get; } | Bietet Zugriff auf die Eigenschaften der Form der horizontalen Linie. Gibt für eine Form, die keine horizontale Linie ist, null zurück. |
| [HRef](../../aspose.words.drawing/shapebase/href) { get; set; } | Ruft die vollständige Hyperlink-Adresse für eine Form ab oder legt sie fest. |
| [ImageData](../../aspose.words.drawing/shape/imagedata) { get; } | Bietet Zugriff auf das Bild der Form. Gibt null zurück, wenn die Form kein Bild haben kann. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Gibt wahr zurück, da dieser Knoten untergeordnete Knoten haben kann. |
| [IsDecorative](../../aspose.words.drawing/shapebase/isdecorative) { get; set; } | Ruft das Flag ab oder setzt es, das angibt, ob die Form im Dokument dekorativ ist. |
| [IsDeleteRevision](../../aspose.words.drawing/shapebase/isdeleterevision) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsnachverfolgung aktiviert war. |
| [IsGroup](../../aspose.words.drawing/shapebase/isgroup) { get; } | Gibt „true“ zurück, wenn es sich um eine Gruppenform handelt. |
| [IsHorizontalRule](../../aspose.words.drawing/shapebase/ishorizontalrule) { get; } | Gibt wahr zurück, wenn diese Form eine horizontale Linie ist. |
| [IsImage](../../aspose.words.drawing/shapebase/isimage) { get; } | Gibt wahr zurück, wenn diese Form eine Bildform ist. |
| [IsInline](../../aspose.words.drawing/shapebase/isinline) { get; } | Eine schnelle Möglichkeit festzustellen, ob diese Form inline mit Text positioniert ist. |
| [IsInsertRevision](../../aspose.words.drawing/shapebase/isinsertrevision) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war. |
| [IsLayoutInCell](../../aspose.words.drawing/shapebase/islayoutincell) { get; set; } | Ruft ein Flag ab oder setzt es, das angibt, ob die Form innerhalb oder außerhalb einer Tabelle angezeigt wird. |
| [IsMoveFromRevision](../../aspose.words.drawing/shapebase/ismovefromrevision) { get; } | gibt zurück **Stimmt** wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsnachverfolgung aktiviert war. |
| [IsMoveToRevision](../../aspose.words.drawing/shapebase/ismovetorevision) { get; } | gibt zurück **Stimmt** wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsnachverfolgung aktiviert war. |
| [IsSignatureLine](../../aspose.words.drawing/shapebase/issignatureline) { get; } | Gibt an, dass die Form eine SignatureLine ist. |
| [IsTopLevel](../../aspose.words.drawing/shapebase/istoplevel) { get; } | Gibt wahr zurück, wenn diese Form kein untergeordnetes Element einer Gruppenform ist. |
| [IsWordArt](../../aspose.words.drawing/shapebase/iswordart) { get; } | Gibt wahr zurück, wenn diese Form ein WordArt-Objekt ist. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [LastParagraph](../../aspose.words.drawing/shape/lastparagraph) { get; } | Ruft den letzten Absatz in der Form ab. |
| [Left](../../aspose.words.drawing/shapebase/left) { get; set; } | Ruft die Position der linken Kante des umgebenden Blocks der Form ab oder legt sie fest. |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage) { get; } | Ruft die für dieses Grafikobjekt verwendete MarkupLanguage ab. |
| [Name](../../aspose.words.drawing/shapebase/name) { get; set; } | Ruft den optionalen Formnamen ab oder legt ihn fest. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words.drawing/shape/nodetype) { get; } | gibt zurückShape . |
| [OleFormat](../../aspose.words.drawing/shape/oleformat) { get; } | Bietet Zugriff auf die OLE-Daten einer Form. Gibt für eine Form, die kein OLE-Objekt oder ActiveX-Steuerelement ist, null zurück. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [ParentParagraph](../../aspose.words.drawing/shapebase/parentparagraph) { get; } | Gibt den unmittelbar übergeordneten Absatz zurück. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Ruft den Knoten unmittelbar vor diesem Knoten ab. |
| [Range](../../aspose.words/node/range) { get; } | Gibt a zurück **Bereich** Objekt, das den Teil eines Dokuments darstellt, das in diesem Knoten enthalten ist. |
| [RelativeHorizontalPosition](../../aspose.words.drawing/shapebase/relativehorizontalposition) { get; set; } | Gibt an, in welchem Verhältnis die Form horizontal positioniert ist. |
| [RelativeVerticalPosition](../../aspose.words.drawing/shapebase/relativeverticalposition) { get; set; } | Gibt an, in welchem Verhältnis die Form vertikal positioniert ist. |
| [Right](../../aspose.words.drawing/shapebase/right) { get; } | Ruft die Position der rechten Kante des umgebenden Blocks der Form ab. |
| [Rotation](../../aspose.words.drawing/shapebase/rotation) { get; set; } | Definiert den Winkel (in Grad), um den eine Form gedreht wird. Ein positiver Wert entspricht einem Drehwinkel im Uhrzeigersinn. |
| [ScreenTip](../../aspose.words.drawing/shapebase/screentip) { get; set; } | Definiert den Text, der angezeigt wird, wenn der Mauszeiger über die Form bewegt wird. |
| [ShadowEnabled](../../aspose.words.drawing/shape/shadowenabled) { get; } | Gibt wahr zurück, wenn ein Schatteneffekt aktiviert ist. |
| [ShadowFormat](../../aspose.words.drawing/shapebase/shadowformat) { get; } | Ruft die Schattenformatierung für die Form ab. |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype) { get; } | Ruft den Formtyp ab. |
| [SignatureLine](../../aspose.words.drawing/shape/signatureline) { get; } | erhält[`SignatureLine`](./signatureline) Objekt, wenn die Form eine Signaturlinie ist. Kehrt zurück **Null** andernfalls. |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints) { get; } | Ruft die Größe der Form in Punkten ab. |
| [StoryType](../../aspose.words.drawing/shape/storytype) { get; } | gibt zurückTextbox . |
| [Stroke](../../aspose.words.drawing/shape/stroke) { get; } | Definiert einen Strich für eine Form. |
| [StrokeColor](../../aspose.words.drawing/shape/strokecolor) { get; set; } | Definiert die Farbe eines Strichs. |
| [Stroked](../../aspose.words.drawing/shape/stroked) { get; set; } | Definiert, ob der Pfad gestrichelt wird. |
| [StrokeWeight](../../aspose.words.drawing/shape/strokeweight) { get; set; } | Definiert die Pinselstärke, die den Pfad einer Form in Punkten streicht. |
| [Target](../../aspose.words.drawing/shapebase/target) { get; set; } | Ruft den Zielrahmen für den Form-Hyperlink ab oder legt ihn fest. |
| [TextBox](../../aspose.words.drawing/shape/textbox) { get; } | Definiert Attribute, die angeben, wie Text in einer Form angezeigt wird. |
| [TextPath](../../aspose.words.drawing/shape/textpath) { get; } | Definiert den Text des Textpfades (eines WordArt-Objekts). |
| [Title](../../aspose.words.drawing/shapebase/title) { get; set; } | Ruft den Titel (Beschriftung) des aktuellen Formobjekts ab oder legt ihn fest. |
| [Top](../../aspose.words.drawing/shapebase/top) { get; set; } | Ruft die Position der Oberkante des umgebenden Blocks der Form ab oder legt sie fest. |
| [VerticalAlignment](../../aspose.words.drawing/shapebase/verticalalignment) { get; set; } | Gibt an, wie die Form vertikal positioniert wird. |
| [Width](../../aspose.words.drawing/shapebase/width) { get; set; } | Ruft die Breite des umschließenden Blocks der Form ab oder legt sie fest. |
| [WrapSide](../../aspose.words.drawing/shapebase/wrapside) { get; set; } | Gibt an, wie der Text um die Form gewickelt wird. |
| [WrapType](../../aspose.words.drawing/shapebase/wraptype) { get; set; } | Definiert, ob die Form eingebettet oder schwebend ist. Für schwebende Formen definiert den Umbruchmodus für Text um die Form. |
| [ZOrder](../../aspose.words.drawing/shapebase/zorder) { get; set; } | Bestimmt die Anzeigereihenfolge überlappender Formen. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words.drawing/shape/accept)(DocumentVisitor) | Akzeptiert einen Besucher. |
| [AdjustWithEffects](../../aspose.words.drawing/shapebase/adjustwitheffects)(RectangleF) | Addiert die Quellrechteckwerte der Effektausdehnung und gibt das endgültige Rechteck zurück. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [Clone](../../aspose.words/node/clone)(bool) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Reserviert für Systemnutzung. IXPfadNavigierbar. |
| [FetchInheritedShapeAttr](../../aspose.words.drawing/shapebase/fetchinheritedshapeattr)(int) | Reserviert für Systemnutzung. IShapeAttrSource. |
| [FetchShapeAttr](../../aspose.words.drawing/shapebase/fetchshapeattr)(int) | Reserviert für Systemnutzung. IShapeAttrSource. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Ruft den ersten Vorfahren der angegebenen ab[`NodeType`](../../aspose.words/nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Gibt eine Live-Sammlung von untergeordneten Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetDirectShapeAttr](../../aspose.words.drawing/shapebase/getdirectshapeattr)(int) | Reserviert für Systemnutzung. IShapeAttrSource. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Bietet Unterstützung für die Iteration für jeden Stil über die untergeordneten Knoten dieses Knotens. |
| [GetShapeRenderer](../../aspose.words.drawing/shapebase/getshaperenderer)() | Erstellt ein Objekt und gibt es zurück, das verwendet werden kann, um diese Form in ein Bild zu rendern. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Ruft den Text dieses Knotens und aller seiner Kinder ab. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knotenarray zurück. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein. |
| [LocalToParent](../../aspose.words.drawing/shapebase/localtoparent)(PointF) | Konvertiert einen Wert aus dem lokalen Koordinatenraum in den Koordinatenraum der übergeordneten Form. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Ruft den nächsten Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Fügt den angegebenen Knoten am Anfang der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Ruft den vorherigen Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [Remove](../../aspose.words/node/remove)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Entfernt alle untergeordneten Knoten des aktuellen Knotens. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Entfernt den angegebenen untergeordneten Knoten. |
| [RemoveShapeAttr](../../aspose.words.drawing/shapebase/removeshapeattr)(int) | Reserviert für Systemnutzung. IShapeAttrSource. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Entfernt alle[`SmartTag`](../../aspose.words.markup/smarttag) Nachkommenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Wählt eine Liste von Knoten aus, die mit dem XPath-Ausdruck übereinstimmen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Wählt den ersten Knoten aus, der mit dem XPath-Ausdruck übereinstimmt. |
| [SetShapeAttr](../../aspose.words.drawing/shapebase/setshapeattr)(int, object) | Reserviert für Systemnutzung. IShapeAttrSource. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exportiert den Inhalt des Knotens in einen String im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in einen String. |
| [UpdateSmartArtDrawing](../../aspose.words.drawing/shape/updatesmartartdrawing)() | Aktualisiert vorgerenderte SmartArt-Zeichnungen mithilfe der SmartArt-Cold-Rendering-Engine von Aspose.Words. |

### Bemerkungen

Verwendung der[`Shape`](../shape) Klasse können Sie Formen in einem Microsoft Word-Dokument erstellen oder ändern.

Eine wichtige Eigenschaft einer Form ist ihre[`ShapeType`](../shapebase/shapetype). Formen verschiedener -Typen können in einem Word-Dokument unterschiedliche Funktionen haben. Beispielsweise können nur Bild und OLE-Formen Bilder enthalten. Die meisten Formen können Text enthalten, aber nicht alle.

Formen, die Text haben können, können enthalten[`Paragraph`](../../aspose.words/paragraph) and [`Table`](../../aspose.words.tables/table) Knoten als Kinder.

### Beispiele

Zeigt, wie ein schwebendes Bild in der Mitte einer Seite eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein schwebendes Bild ein, das hinter dem überlappenden Text angezeigt wird, und richten Sie es an der Mitte der Seite aus.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Zeigt, wie Bilder aus einem Dokument extrahiert und als einzelne Dateien im lokalen Dateisystem gespeichert werden.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Holen Sie sich die Sammlung von Formen aus dem Dokument,
// und die Bilddaten jeder Form mit einem Bild als Datei im lokalen Dateisystem speichern.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
        // Die Bilddaten von Formen können Bilder in vielen möglichen Bildformaten enthalten. 
        // Wir können für jedes Bild automatisch eine Dateierweiterung basierend auf seinem Format bestimmen.
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

// Fügen Sie zwei Formen zusammen mit einer Gruppenform mit einer anderen Form darin ein.
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

// Alle Gruppenformen separat entfernen.
NodeCollection groupShapes = doc.GetChildNodes(NodeType.GroupShape, true);
groupShapes.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Siehe auch

* class [ShapeBase](../shapebase)
* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
