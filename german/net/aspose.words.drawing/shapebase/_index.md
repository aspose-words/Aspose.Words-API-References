---
title: ShapeBase Class
linktitle: ShapeBase
articleTitle: ShapeBase
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.ShapeBase, Ihre Grundlage zum Erstellen dynamischer Zeichnungen, einschließlich AutoShapes, OLE-Objekten und ActiveX-Steuerelementen.
type: docs
weight: 1650
url: /de/net/aspose.words.drawing/shapebase/
---
## ShapeBase class

Basisklasse für Objekte in der Zeichenebene, z. B. eine AutoForm, eine Freiform, ein OLE-Objekt, ein ActiveX-Steuerelement oder ein Bild.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Formen](https://docs.aspose.com/words/net/working-with-shapes/) Dokumentationsartikel.

```csharp
public abstract class ShapeBase : CompositeNode
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AllowOverlap](../../aspose.words.drawing/shapebase/allowoverlap/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob diese Form andere Formen überlappen kann. |
| [AlternativeText](../../aspose.words.drawing/shapebase/alternativetext/) { get; set; } | Definiert alternativen Text, der anstelle einer Grafik angezeigt werden soll. |
| [AnchorLocked](../../aspose.words.drawing/shapebase/anchorlocked/) { get; set; } | Gibt an, ob der Anker der Form gesperrt ist. |
| [AspectRatioLocked](../../aspose.words.drawing/shapebase/aspectratiolocked/) { get; set; } | Gibt an, ob das Seitenverhältnis der Form gesperrt ist. |
| [BehindText](../../aspose.words.drawing/shapebase/behindtext/) { get; set; } | Gibt an, ob sich die Form unter oder über dem Text befindet. |
| [Bottom](../../aspose.words.drawing/shapebase/bottom/) { get; } | Ruft die Position der Unterkante des umschließenden Blocks der Form ab. |
| [Bounds](../../aspose.words.drawing/shapebase/bounds/) { get; set; } | Ruft die Position und Größe des umgebenden Blocks der Form ab oder legt diese fest. |
| [BoundsInPoints](../../aspose.words.drawing/shapebase/boundsinpoints/) { get; } | Ruft die Position und Größe des umgebenden Blocks der Form in Punkten relativ zum Anker der obersten Form ab. |
| [BoundsWithEffects](../../aspose.words.drawing/shapebase/boundswitheffects/) { get; } | Ruft die endgültige Ausdehnung dieses Formobjekts nach dem Anwenden von Zeicheneffekten ab. Der Wert wird in Punkten gemessen. |
| [CanHaveImage](../../aspose.words.drawing/shapebase/canhaveimage/) { get; } | Rückgaben`WAHR` wenn der Formtyp es zulässt, dass die Form ein Bild enthält. |
| [CoordOrigin](../../aspose.words.drawing/shapebase/coordorigin/) { get; set; } | Die Koordinaten in der oberen linken Ecke des umschließenden Blocks dieser Form. |
| [CoordSize](../../aspose.words.drawing/shapebase/coordsize/) { get; set; } | Die Breite und Höhe des Koordinatenraums innerhalb des umschließenden Blocks dieser Form. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ruft die Anzahl der unmittelbar untergeordneten Elemente dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| [DistanceBottom](../../aspose.words.drawing/shapebase/distancebottom/) { get; set; } | Gibt den Abstand (in Punkten) zwischen dem Dokumenttext und der Unterkante der Form zurück oder legt ihn fest. |
| [DistanceLeft](../../aspose.words.drawing/shapebase/distanceleft/) { get; set; } | Gibt den Abstand (in Punkten) zwischen dem Dokumenttext und dem linken Rand der Form zurück oder legt ihn fest. |
| [DistanceRight](../../aspose.words.drawing/shapebase/distanceright/) { get; set; } | Gibt den Abstand (in Punkten) zwischen dem Dokumenttext und dem rechten Rand der Form zurück oder legt ihn fest. |
| [DistanceTop](../../aspose.words.drawing/shapebase/distancetop/) { get; set; } | Gibt den Abstand (in Punkten) zwischen dem Dokumenttext und der Oberkante der Form zurück oder legt ihn fest. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [Fill](../../aspose.words.drawing/shapebase/fill/) { get; } | Ruft die Füllformatierung für die Form ab. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FlipOrientation](../../aspose.words.drawing/shapebase/fliporientation/) { get; set; } | Ändert die Ausrichtung einer Form. |
| [Font](../../aspose.words.drawing/shapebase/font/) { get; } | Bietet Zugriff auf die Schriftformatierung dieses Objekts. |
| [Glow](../../aspose.words.drawing/shapebase/glow/) { get; } | Ruft die Leuchtformatierung für die Form ab. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Rückgaben`WAHR` wenn dieser Knoten untergeordnete Knoten hat. |
| [Height](../../aspose.words.drawing/shapebase/height/) { get; set; } | Ruft die Höhe des umgebenden Blocks der Form ab oder legt sie fest. |
| [HeightRelative](../../aspose.words.drawing/shapebase/heightrelative/) { get; set; } | Ruft den Wert ab oder legt ihn fest, der den Prozentsatz der relativen Höhe der Form darstellt. |
| [Hidden](../../aspose.words.drawing/shapebase/hidden/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob die Form sichtbar ist. |
| [HorizontalAlignment](../../aspose.words.drawing/shapebase/horizontalalignment/) { get; set; } | Gibt an, wie die Form horizontal positioniert wird. |
| [HRef](../../aspose.words.drawing/shapebase/href/) { get; set; } | Ruft die vollständige Hyperlinkadresse für eine Form ab oder legt sie fest. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Rückgaben`WAHR` da dieser Knoten untergeordnete Knoten haben kann. |
| [IsDecorative](../../aspose.words.drawing/shapebase/isdecorative/) { get; set; } | Ruft das Flag ab oder legt es fest, das angibt, ob die Form im Dokument dekorativ ist. |
| [IsDeleteRevision](../../aspose.words.drawing/shapebase/isdeleterevision/) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war. |
| [IsGroup](../../aspose.words.drawing/shapebase/isgroup/) { get; } | Rückgaben`WAHR` wenn dies eine Gruppenform ist. |
| [IsHorizontalRule](../../aspose.words.drawing/shapebase/ishorizontalrule/) { get; } | Rückgaben`WAHR` wenn diese Form eine horizontale Linie ist. |
| [IsImage](../../aspose.words.drawing/shapebase/isimage/) { get; } | Rückgaben`WAHR` wenn diese Form eine Bildform ist. |
| [IsInline](../../aspose.words.drawing/shapebase/isinline/) { get; } | Eine schnelle Möglichkeit, festzustellen, ob diese Form inline mit Text positioniert ist. |
| [IsInsertRevision](../../aspose.words.drawing/shapebase/isinsertrevision/) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war. |
| [IsLayoutInCell](../../aspose.words.drawing/shapebase/islayoutincell/) { get; set; } | Ruft ein Flag ab oder legt es fest, das angibt, ob die Form innerhalb oder außerhalb einer Tabelle angezeigt wird. |
| [IsMoveFromRevision](../../aspose.words.drawing/shapebase/ismovefromrevision/) { get; } | Rückgaben`WAHR` wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsverfolgung aktiviert war. |
| [IsMoveToRevision](../../aspose.words.drawing/shapebase/ismovetorevision/) { get; } | Rückgaben`WAHR` wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung aktiviert war. |
| [IsSignatureLine](../../aspose.words.drawing/shapebase/issignatureline/) { get; } | Gibt an, dass die Form eine[`SignatureLine`](../signatureline/) . |
| [IsTopLevel](../../aspose.words.drawing/shapebase/istoplevel/) { get; } | Rückgaben`WAHR` wenn diese Form kein untergeordnetes Element einer Gruppenform ist. |
| [IsWordArt](../../aspose.words.drawing/shapebase/iswordart/) { get; } | Rückgaben`WAHR` wenn diese Form ein WordArt-Objekt ist. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [Left](../../aspose.words.drawing/shapebase/left/) { get; set; } | Ruft die Position der linken Kante des umschließenden Blocks der Form ab oder legt sie fest. |
| [LeftRelative](../../aspose.words.drawing/shapebase/leftrelative/) { get; set; } | Ruft den Wert ab oder legt ihn fest, der die relative linke Position der Form in Prozent darstellt. |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage/) { get; } | Ruft die für dieses Grafikobjekt verwendete MarkupLanguage ab. |
| [Name](../../aspose.words.drawing/shapebase/name/) { get; set; } | Ruft den optionalen Formnamen ab oder legt ihn fest. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Ruft den Typ dieses Knotens ab. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [ParentParagraph](../../aspose.words.drawing/shapebase/parentparagraph/) { get; } | Gibt den unmittelbar übergeordneten Absatz zurück. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar vorausgeht. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt einen[`Range`](../../aspose.words/range/)Objekt, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [Reflection](../../aspose.words.drawing/shapebase/reflection/) { get; } | Ruft die Reflexionsformatierung für die Form ab. |
| [RelativeHorizontalPosition](../../aspose.words.drawing/shapebase/relativehorizontalposition/) { get; set; } | Gibt an, relativ zu was die Form horizontal positioniert ist. |
| [RelativeHorizontalSize](../../aspose.words.drawing/shapebase/relativehorizontalsize/) { get; set; } | Ruft den Wert der relativen Größe der Form in horizontaler Richtung ab oder legt ihn fest. |
| [RelativeVerticalPosition](../../aspose.words.drawing/shapebase/relativeverticalposition/) { get; set; } | Gibt an, relativ zu welcher vertikalen Position die Form positioniert ist. |
| [RelativeVerticalSize](../../aspose.words.drawing/shapebase/relativeverticalsize/) { get; set; } | Ruft den Wert der relativen Größe der Form in vertikaler Richtung ab oder legt ihn fest. |
| [Right](../../aspose.words.drawing/shapebase/right/) { get; } | Ruft die Position der rechten Kante des umschließenden Blocks der Form ab. |
| [Rotation](../../aspose.words.drawing/shapebase/rotation/) { get; set; } | Definiert den Winkel (in Grad), um den eine Form gedreht wird. Ein positiver Wert entspricht einem Drehwinkel im Uhrzeigersinn. |
| [ScreenTip](../../aspose.words.drawing/shapebase/screentip/) { get; set; } | Definiert den Text, der angezeigt wird, wenn der Mauszeiger über die Form bewegt wird. |
| [ShadowFormat](../../aspose.words.drawing/shapebase/shadowformat/) { get; } | Ruft die Schattenformatierung für die Form ab. |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype/) { get; } | Ruft den Formtyp ab. |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints/) { get; } | Ruft die Größe der Form in Punkten ab. |
| [SoftEdge](../../aspose.words.drawing/shapebase/softedge/) { get; } | Ruft eine weiche Kantenformatierung für die Form ab. |
| [Target](../../aspose.words.drawing/shapebase/target/) { get; set; } | Ruft den Zielrahmen für den Form-Hyperlink ab oder legt ihn fest. |
| [Title](../../aspose.words.drawing/shapebase/title/) { get; set; } | Ruft den Titel (die Beschriftung) des aktuellen Formobjekts ab oder legt ihn fest. |
| [Top](../../aspose.words.drawing/shapebase/top/) { get; set; } | Ruft die Position der oberen Kante des umschließenden Blocks der Form ab oder legt sie fest. |
| [TopRelative](../../aspose.words.drawing/shapebase/toprelative/) { get; set; } | Ruft den Wert ab oder legt ihn fest, der die relative obere Position der Form in Prozent darstellt. |
| [VerticalAlignment](../../aspose.words.drawing/shapebase/verticalalignment/) { get; set; } | Gibt an, wie die Form vertikal positioniert wird. |
| [Width](../../aspose.words.drawing/shapebase/width/) { get; set; } | Ruft die Breite des umgebenden Blocks der Form ab oder legt sie fest. |
| [WidthRelative](../../aspose.words.drawing/shapebase/widthrelative/) { get; set; } | Ruft den Wert ab oder legt ihn fest, der den Prozentsatz der relativen Breite der Form darstellt. |
| [WrapSide](../../aspose.words.drawing/shapebase/wrapside/) { get; set; } | Gibt an, wie der Text um die Form gewickelt wird. |
| [WrapType](../../aspose.words.drawing/shapebase/wraptype/) { get; set; } | Definiert, ob die Form eingebettet oder schwebend ist. Bei schwebenden Formen definiert dies den Umbruchmodus für Text um die Form. |
| [ZOrder](../../aspose.words.drawing/shapebase/zorder/) { get; set; } | Bestimmt die Anzeigereihenfolge überlappender Formen. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Nimmt einen Besucher auf. |
| abstract [AcceptEnd](../../aspose.words/compositenode/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Ruft bei Implementierung in einer abgeleiteten Klasse die Methode VisitXXXEnd des angegebenen Dokumentbesuchers auf. |
| abstract [AcceptStart](../../aspose.words/compositenode/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Ruft bei Implementierung in einer abgeleiteten Klasse die Methode VisitXXXStart des angegebenen Dokumentbesuchers auf. |
| [AdjustWithEffects](../../aspose.words.drawing/shapebase/adjustwitheffects/)(*RectangleF*) | Fügt den Quellrechteckwerten den Effektumfang hinzu und gibt das endgültige Rechteck zurück. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Erstellt einen Navigator, der zum Durchlaufen und Lesen von Knoten verwendet werden kann. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Ruft den ersten Vorfahren des angegebenen[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ruft den ersten Vorgänger des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Gibt eine Live-Sammlung von untergeordneten Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bietet Unterstützung für die Iteration des For-Each-Stils über die untergeordneten Knoten dieses Knotens. |
| [GetShapeRenderer](../../aspose.words.drawing/shapebase/getshaperenderer/)() | Erstellt und gibt ein Objekt zurück, mit dem diese Form in ein Bild gerendert werden kann. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ruft den Text dieses Knotens und aller seiner untergeordneten Knoten ab. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knoten-Array zurück. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein. |
| [LocalToParent](../../aspose.words.drawing/shapebase/localtoparent/)(*PointF*) | Konvertiert einen Wert aus dem lokalen Koordinatenraum in den Koordinatenraum der übergeordneten Form. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Ruft den nächsten Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Fügt den angegebenen Knoten am Anfang der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Ruft den vorherigen Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Entfernt alle untergeordneten Knoten des aktuellen Knotens. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Entfernt den angegebenen untergeordneten Knoten. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Entfernt alle[`SmartTag`](../../aspose.words.markup/smarttag/) Nachkommenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Wählt den ersten[`Node`](../../aspose.words/node/) das dem XPath-Ausdruck entspricht. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exportiert den Inhalt des Knotens in eine Zeichenfolge im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in eine Zeichenfolge. |

## Bemerkungen

Dies ist eine abstrakte Klasse. Die beiden abgeleiteten Klassen, die Sie instantiieren können , sind[`Shape`](../shape/) Und[`GroupShape`](../groupshape/).

Eine Form ist ein Knoten im Dokumentbaum.

Wenn die Form ein untergeordnetes Element einer[`Paragraph`](../../aspose.words/paragraph/) Objekt, dann wird die Form als „oberste Ebene“ bezeichnet. Formen der obersten Ebene werden in Punkten gemessen und positioniert.

Eine Form kann auch als Kind einer[`GroupShape`](../groupshape/) Objekt, wenn mehrere shapes gruppiert sind. Untergeordnete Shapes einer Gruppenform werden im Koordinatenraum und units positioniert, die durch die[`CoordSize`](./coordsize/) Und[`CoordOrigin`](./coordorigin/) Eigenschaften der Form der Gruppe parent .

Eine Form kann inline mit Text oder schwebend positioniert werden. Die Positionierung erfolgt über[`WrapType`](./wraptype/) Eigentum.

Wenn eine Form schwebt, wird sie relativ zu etwas positioniert (z. B. dem aktuellen Absatz, dem Rand oder der Seite). Die relative Positionierung der Form wird mithilfe der[`RelativeHorizontalPosition`](./relativehorizontalposition/) Und[`RelativeVerticalPosition`](./relativeverticalposition/) Eigenschaften.

Eine schwebende Form kann explizit positioniert werden, indem man[`Left`](./left/) Und[`Top`](./top/) Eigenschaften oder relativ zu einem anderen Objekt ausgerichtet mit dem[`HorizontalAlignment`](./horizontalalignment/) und[`VerticalAlignment`](./verticalalignment/) Eigenschaften.

## Beispiele

Zeigt, wie ein schwebendes Bild in die Mitte einer Seite eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein schwebendes Bild ein, das hinter dem überlappenden Text angezeigt wird, und richten Sie es an der Seitenmitte aus.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

### Siehe auch

* class [CompositeNode](../../aspose.words/compositenode/)
* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
