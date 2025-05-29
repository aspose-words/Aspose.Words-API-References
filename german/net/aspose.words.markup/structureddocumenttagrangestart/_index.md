---
title: StructuredDocumentTagRangeStart Class
linktitle: StructuredDocumentTagRangeStart
articleTitle: StructuredDocumentTagRangeStart
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Markup.StructuredDocumentTagRangeStart, die eine nahtlose Verwaltung mehrteiliger Inhalte in strukturierten Dokumenten ermöglicht.
type: docs
weight: 4780
url: /de/net/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class

Stellt einen Anfang von**reichte** strukturiertes Dokument-Tag, das Inhalte mit mehreren Abschnitten akzeptiert. Siehe auch[`StructuredDocumentTagRangeEnd`](../structureddocumenttagrangeend/) .

Um mehr zu erfahren, besuchen Sie die[Strukturierte Dokument-Tags oder Inhaltssteuerung](https://docs.aspose.com/words/net/working-with-content-control-sdt/) Dokumentationsartikel.

```csharp
public class StructuredDocumentTagRangeStart : Node, IEnumerable<Node>, IStructuredDocumentTag
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [StructuredDocumentTagRangeStart](structureddocumenttagrangestart/)(*[DocumentBase](../../aspose.words/documentbase/), [SdtType](../sdttype/)*) | Initialisiert eine neue Instanz des**Tagbereichsanfang für strukturierte Dokumente** Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Appearance](../../aspose.words.markup/structureddocumenttagrangestart/appearance/) { get; set; } | Ruft das Erscheinungsbild des strukturierten Dokumenttags ab oder legt es fest. |
| [Color](../../aspose.words.markup/structureddocumenttagrangestart/color/) { get; set; } | Ruft die Farbe des strukturierten Dokument-Tags ab oder legt sie fest. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [Id](../../aspose.words.markup/structureddocumenttagrangestart/id/) { get; } | Gibt eine eindeutige, schreibgeschützte, dauerhafte numerische ID für dieses strukturierte Dokument-Tag an. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Rückgaben`WAHR` wenn dieser Knoten andere Knoten enthalten kann. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttagrangestart/isshowingplaceholdertext/) { get; set; } | Gibt an, ob der Inhalt dieses strukturierten Dokument-Tags so interpretiert werden soll, dass er Platzhaltertext enthält (im Gegensatz zu regulärem Textinhalt innerhalb des strukturierten Dokument-Tags). |
| [LastChild](../../aspose.words.markup/structureddocumenttagrangestart/lastchild/) { get; } | Ruft das letzte untergeordnete Element im stdContent-Bereich ab. |
| [Level](../../aspose.words.markup/structureddocumenttagrangestart/level/) { get; } | Ruft die Ebene ab, auf der dieser strukturierte Dokument-Tagbereichsanfang im Dokumentbaum auftritt. |
| [LockContentControl](../../aspose.words.markup/structureddocumenttagrangestart/lockcontentcontrol/) { get; set; } | Wenn eingestellt auf`WAHR` , diese Eigenschaft verhindert, dass ein Benutzer dieses strukturierte Dokument-Tag löscht. |
| [LockContents](../../aspose.words.markup/structureddocumenttagrangestart/lockcontents/) { get; set; } | Wenn eingestellt auf`WAHR` , diese Eigenschaft verhindert, dass ein Benutzer den Inhalt dieses strukturierten Dokument-Tags bearbeitet. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words.markup/structureddocumenttagrangestart/nodetype/) { get; } | RückgabenStructuredDocumentTagRangeStart . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [Placeholder](../../aspose.words.markup/structureddocumenttagrangestart/placeholder/) { get; } | Ruft die[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)Enthält Platzhaltertext, der angezeigt werden soll, wenn der Inhalt dieses strukturierten Dokument-Tags leer ist und das zugeordnete zugeordnete XML-Element leer ist, wie angegeben über[`XmlMapping`](./xmlmapping/) Element oder das[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) Element ist`WAHR` . |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttagrangestart/placeholdername/) { get; set; } | Ruft den Namen des[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) mit Platzhaltertext. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar vorausgeht. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt einen[`Range`](../../aspose.words/range/)Objekt, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [RangeEnd](../../aspose.words.markup/structureddocumenttagrangestart/rangeend/) { get; } | Gibt das Ende des Bereichs an, wenn der[`StructuredDocumentTag`](../structureddocumenttag/) ist ein strukturiertes Dokument-Tag. Andernfalls wird zurückgegeben`null` . |
| [SdtType](../../aspose.words.markup/structureddocumenttagrangestart/sdttype/) { get; } | Ruft den Typ dieses strukturierten Dokument-Tags ab. |
| [Tag](../../aspose.words.markup/structureddocumenttagrangestart/tag/) { get; set; } | Gibt ein Tag an, das mit dem aktuellen Tag-Knoten des strukturierten Dokuments verknüpft ist. Kann nicht`null` . |
| [Title](../../aspose.words.markup/structureddocumenttagrangestart/title/) { get; set; } | Gibt den Anzeigenamen an, der mit diesem strukturierten Dokument-Tag verknüpft ist. Kann nicht`null` . |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttagrangestart/wordopenxml/) { get; } | Ruft eine Zeichenfolge ab, die das XML darstellt, das im Knoten imFlatOpc format. |
| [WordOpenXMLMinimal](../../aspose.words.markup/structureddocumenttagrangestart/wordopenxmlminimal/) { get; } | Ruft eine Zeichenfolge ab, die das XML darstellt, das im Knoten imFlatOpc format. Im Gegensatz zu den[`WordOpenXML`](./wordopenxml/) Diese Methode generiert ein abgespecktes Dokument, das alle nicht inhaltsbezogenen Teile ausschließt. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttagrangestart/xmlmapping/) { get; } | Ruft ein Objekt ab, das die Zuordnung dieses strukturierten Dokument-Tag-Bereichs zu XML-Daten in einem benutzerdefinierten XML-Teil des aktuellen Dokuments darstellt. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttagrangestart/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Nimmt einen Besucher auf. |
| [AppendChild](../../aspose.words.markup/structureddocumenttagrangestart/appendchild/)(*[Node](../../aspose.words/node/)*) | Fügt den angegebenen Knoten am Ende des stdContent-Bereichs hinzu. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Erstellt ein Duplikat des Knotens. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Ruft den ersten Vorfahren des angegebenen[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ruft den ersten Vorgänger des angegebenen Objekttyps ab. |
| [GetChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Gibt eine Live-Sammlung von untergeordneten Knoten zurück, die den angegebenen Typen entsprechen. |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagrangestart/getenumerator/)() | Bietet Unterstützung für die Iteration des For-Each-Stils über die untergeordneten Knoten dieses Knotens. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Ruft den Text dieses Knotens und aller seiner untergeordneten Knoten ab. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Ruft den nächsten Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Ruft den vorherigen Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words.markup/structureddocumenttagrangestart/removeallchildren/)() | Entfernt alle Knoten zwischen diesem Bereichsstartknoten und dem Bereichsendknoten. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttagrangestart/removeselfonly/)() | Entfernt diesen Bereichsanfang und die entsprechenden Bereichsendknoten des strukturierten Dokumenttags, behält aber seinen Inhalt im Dokumentbaum. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exportiert den Inhalt des Knotens in eine Zeichenfolge im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in eine Zeichenfolge. |

## Bemerkungen

Kann unmittelbares Kind von sein[`Body`](../../aspose.words/body/) Knoten**nur** .

## Beispiele

Zeigt, wie die Eigenschaften von aus mehreren Abschnitten strukturierten Dokument-Tags abgerufen werden.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");

StructuredDocumentTagRangeStart rangeStartTag =
    doc.GetChildNodes(NodeType.StructuredDocumentTagRangeStart, true)[0] as StructuredDocumentTagRangeStart;
StructuredDocumentTagRangeEnd rangeEndTag =
    doc.GetChildNodes(NodeType.StructuredDocumentTagRangeEnd, true)[0] as StructuredDocumentTagRangeEnd;

Console.WriteLine("StructuredDocumentTagRangeStart values:");
Console.WriteLine($"\t|Id: {rangeStartTag.Id}");
Console.WriteLine($"\t|Title: {rangeStartTag.Title}");
Console.WriteLine($"\t|PlaceholderName: {rangeStartTag.PlaceholderName}");
Console.WriteLine($"\t|IsShowingPlaceholderText: {rangeStartTag.IsShowingPlaceholderText}");
Console.WriteLine($"\t|LockContentControl: {rangeStartTag.LockContentControl}");
Console.WriteLine($"\t|LockContents: {rangeStartTag.LockContents}");
Console.WriteLine($"\t|Level: {rangeStartTag.Level}");
Console.WriteLine($"\t|NodeType: {rangeStartTag.NodeType}");
Console.WriteLine($"\t|RangeEnd: {rangeStartTag.RangeEnd}");
Console.WriteLine($"\t|Color: {rangeStartTag.Color.ToArgb()}");
Console.WriteLine($"\t|SdtType: {rangeStartTag.SdtType}");
Console.WriteLine($"\t|FlatOpcContent: {rangeStartTag.WordOpenXML}");
Console.WriteLine($"\t|Tag: {rangeStartTag.Tag}\n");

Console.WriteLine("StructuredDocumentTagRangeEnd values:");
Console.WriteLine($"\t|Id: {rangeEndTag.Id}");
Console.WriteLine($"\t|NodeType: {rangeEndTag.NodeType}");
```

### Siehe auch

* class [Node](../../aspose.words/node/)
* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* namensraum [Aspose.Words.Markup](../../aspose.words.markup/)
* Montage [Aspose.Words](../../)
