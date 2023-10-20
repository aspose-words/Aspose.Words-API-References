---
title: GroupShape Class
linktitle: GroupShape
articleTitle: GroupShape
second_title: Aspose.Words für .NET
description: Aspose.Words.Drawing.GroupShape klas. Stellt eine Gruppe von Formen in einem Dokument dar in C#.
type: docs
weight: 1020
url: /de/net/aspose.words.drawing/groupshape/
---
## GroupShape class

Stellt eine Gruppe von Formen in einem Dokument dar.

Um mehr zu erfahren, besuchen Sie die[So fügen Sie einem Word-Dokument eine Gruppenform hinzu](https://docs.aspose.com/words/net/how-to-add-group-shape-into-a-word-document/) Dokumentationsartikel.

```csharp
public class GroupShape : ShapeBase
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [GroupShape](groupshape/)(*[DocumentBase](../../aspose.words/documentbase/)*) | Erstellt eine neue Gruppenform. |

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
| [CoordOrigin](../../aspose.words.drawing/shapebase/coordorigin/) { get; set; } | Die Koordinaten in der oberen linken Ecke des enthaltenden Blocks dieser Form. |
| [CoordSize](../../aspose.words.drawing/shapebase/coordsize/) { get; set; } | Die Breite und Höhe des Koordinatenraums innerhalb des enthaltenden Blocks dieser Form. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ruft die Anzahl der unmittelbaren Kinder dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| [DistanceBottom](../../aspose.words.drawing/shapebase/distancebottom/) { get; set; } | Gibt den Abstand (in Punkten) zwischen dem Dokumenttext und der Unterkante der Form zurück oder legt ihn fest. |
| [DistanceLeft](../../aspose.words.drawing/shapebase/distanceleft/) { get; set; } | Gibt den Abstand (in Punkten) zwischen dem Dokumenttext und dem linken Rand der Form zurück oder legt ihn fest. |
| [DistanceRight](../../aspose.words.drawing/shapebase/distanceright/) { get; set; } | Gibt den Abstand (in Punkten) zwischen dem Dokumenttext und dem rechten Rand der Form zurück oder legt ihn fest. |
| [DistanceTop](../../aspose.words.drawing/shapebase/distancetop/) { get; set; } | Gibt den Abstand (in Punkten) zwischen dem Dokumenttext und der Oberkante der Form zurück oder legt ihn fest. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [Fill](../../aspose.words.drawing/shapebase/fill/) { get; } | Ruft die Füllformatierung für die Form ab. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FlipOrientation](../../aspose.words.drawing/shapebase/fliporientation/) { get; set; } | Ändert die Ausrichtung einer Form. |
| [Font](../../aspose.words.drawing/shapebase/font/) { get; } | Bietet Zugriff auf die Schriftartformatierung dieses Objekts. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Gibt zurück`WAHR` wenn dieser Knoten untergeordnete Knoten hat. |
| [Height](../../aspose.words.drawing/shapebase/height/) { get; set; } | Ruft die Höhe des enthaltenden Blocks der Form ab oder legt sie fest. |
| [HeightRelative](../../aspose.words.drawing/shapebase/heightrelative/) { get; set; } | Ruft den Wert ab, der den Prozentsatz der relativen Höhe der Form darstellt, oder legt diesen fest. |
| [HorizontalAlignment](../../aspose.words.drawing/shapebase/horizontalalignment/) { get; set; } | Gibt an, wie die Form horizontal positioniert wird. |
| [HRef](../../aspose.words.drawing/shapebase/href/) { get; set; } | Ruft die vollständige Hyperlink-Adresse für eine Form ab oder legt diese fest. |
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
| [Left](../../aspose.words.drawing/shapebase/left/) { get; set; } | Ruft die Position der linken Kante des enthaltenden Blocks der Form ab oder legt diese fest. |
| [LeftRelative](../../aspose.words.drawing/shapebase/leftrelative/) { get; set; } | Ruft den Wert ab, der die relative linke Position der Form in Prozent darstellt, oder legt diesen fest. |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage/) { get; } | Ruft die für dieses Grafikobjekt verwendete MarkupLanguage ab. |
| [Name](../../aspose.words.drawing/shapebase/name/) { get; set; } | Ruft den optionalen Formnamen ab oder legt ihn fest. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words.drawing/groupshape/nodetype/) { get; } | Gibt zurückGroupShape . |
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
| [ShadowFormat](../../aspose.words.drawing/shapebase/shadowformat/) { get; } | Ruft die Schattenformatierung für die Form ab. |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype/) { get; } | Ruft den Formtyp ab. |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints/) { get; } | Ermittelt die Größe der Form in Punkten. |
| [Target](../../aspose.words.drawing/shapebase/target/) { get; set; } | Ruft den Zielrahmen für den Form-Hyperlink ab oder legt diesen fest. |
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
| override [Accept](../../aspose.words.drawing/groupshape/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Akzeptiert einen Besucher. |
| [AdjustWithEffects](../../aspose.words.drawing/shapebase/adjustwitheffects/)(*RectangleF*) | Fügt zu den Quellrechteckwerten der Effektausdehnung hinzu und gibt das endgültige Rechteck zurück. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../../aspose.words/node/)*) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Erstellt einen Navigator, der zum Durchlaufen und Lesen von Knoten verwendet werden kann. |
| [FetchInheritedShapeAttr](../../aspose.words.drawing/shapebase/fetchinheritedshapeattr/)(*int*) | Reserviert für die Systemnutzung. IShapeAttrSource. |
| [FetchShapeAttr](../../aspose.words.drawing/shapebase/fetchshapeattr/)(*int*) | Reserviert für die Systemnutzung. IShapeAttrSource. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Ruft den ersten Vorfahren des angegebenen ab[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Gibt eine Live-Sammlung untergeordneter Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetDirectShapeAttr](../../aspose.words.drawing/shapebase/getdirectshapeattr/)(*int*) | Reserviert für die Systemnutzung. IShapeAttrSource. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bietet Unterstützung für die Iteration jedes Stils über die untergeordneten Knoten dieses Knotens. |
| [GetShapeRenderer](../../aspose.words.drawing/shapebase/getshaperenderer/)() | Erstellt ein Objekt und gibt es zurück, das zum Rendern dieser Form in ein Bild verwendet werden kann. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ruft den Text dieses Knotens und aller seiner untergeordneten Knoten ab. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knoten-Array zurück. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein. |
| [LocalToParent](../../aspose.words.drawing/shapebase/localtoparent/)(*PointF*) | Konvertiert einen Wert aus dem lokalen Koordinatenraum in den Koordinatenraum der übergeordneten Form. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Ruft den nächsten Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../../aspose.words/node/)*) | Fügt den angegebenen Knoten am Anfang der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Ruft den vorherigen Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Entfernt alle untergeordneten Knoten des aktuellen Knotens. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../../aspose.words/node/)*) | Entfernt den angegebenen untergeordneten Knoten. |
| [RemoveShapeAttr](../../aspose.words.drawing/shapebase/removeshapeattr/)(*int*) | Reserviert für die Systemnutzung. IShapeAttrSource. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Entfernt alle[`SmartTag`](../../aspose.words.markup/smarttag/)Nachkommenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Wählt den ersten aus[`Node`](../../aspose.words/node/) das entspricht dem XPath-Ausdruck. |
| [SetShapeAttr](../../aspose.words.drawing/shapebase/setshapeattr/)(*int, object*) | Reserviert für die Systemnutzung. IShapeAttrSource. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exportiert den Inhalt des Knotens in einen String im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exportiert den Inhalt des Knotens mit den angegebenen Speicheroptionen in einen String. |

## Bemerkungen

A`GroupShape` ist ein zusammengesetzter Knoten und kann haben[`Shape`](../shape/) and `GroupShape` Knoten als Kinder.

Jede`GroupShape` Definiert ein neues Koordinatensystem für seine untergeordneten Formen. Das Koordinatensystem wird mithilfe von definiert[`CoordSize`](../shapebase/coordsize/) und [`CoordOrigin`](../shapebase/coordorigin/) Eigenschaften.

## Beispiele

Zeigt, wie eine Gruppe von Formen erstellt und deren Inhalt mithilfe eines Dokumentbesuchers gedruckt wird.

```csharp
public void GroupOfShapes()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Wenn Sie „nicht-primitive“ Formen erstellen müssen, z. B. SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
    // TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, DiagonalCornersRounded
    // Bitte verwenden Sie DocumentBuilder.InsertShape-Methoden.
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
/// Gibt den Inhalt einer besuchten Formgruppe an die Konsole aus.
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

### Siehe auch

* class [ShapeBase](../shapebase/)
* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
