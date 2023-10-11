---
title: Class StructuredDocumentTagRangeStart
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Markup.StructuredDocumentTagRangeStart klas. Stellt einen Anfang von dar reichte Strukturiertes DokumentTag das Inhalte mit mehreren Abschnitten akzeptiert. Siehe auchStructuredDocumentTagRangeEnd .
type: docs
weight: 4090
url: /de/net/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class

Stellt einen Anfang von dar **reichte** Strukturiertes Dokument-Tag, das Inhalte mit mehreren Abschnitten akzeptiert. Siehe auch[`StructuredDocumentTagRangeEnd`](../structureddocumenttagrangeend/) .

Um mehr zu erfahren, besuchen Sie die[Strukturierte Dokument-Tags oder Inhaltskontrolle](https://docs.aspose.com/words/net/working-with-content-control-sdt/) Dokumentationsartikel.

```csharp
public class StructuredDocumentTagRangeStart : Node, IEnumerable<Node>, IStructuredDocumentTag
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [StructuredDocumentTagRangeStart](structureddocumenttagrangestart/)(DocumentBase, SdtType) | Initialisiert eine neue Instanz von **Strukturierter Dokument-Tag-Bereichsanfang** Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [ChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/childnodes/) { get; } | Ruft alle Knoten zwischen diesem Bereichsanfangsknoten und dem Bereichsendknoten ab. |
| [Color](../../aspose.words.markup/structureddocumenttagrangestart/color/) { get; set; } | Ruft die Farbe des strukturierten Dokument-Tags ab oder legt diese fest. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [Id](../../aspose.words.markup/structureddocumenttagrangestart/id/) { get; } | Gibt eine eindeutige, schreibgeschützte, persistente numerische ID für dieses strukturierte Dokument-Tag an. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Gibt zurück`WAHR` ob dieser Knoten andere Knoten enthalten kann. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttagrangestart/isshowingplaceholdertext/) { get; set; } | Gibt an, ob der Inhalt dieses strukturierten Dokument-Tags so interpretiert werden soll, dass er Platzhaltertext enthält (im Gegensatz zu regulären Textinhalten innerhalb des strukturierten Dokument-Tags). |
| [LastChild](../../aspose.words.markup/structureddocumenttagrangestart/lastchild/) { get; } | Ruft das letzte untergeordnete Element im stdContent-Bereich ab. |
| [Level](../../aspose.words.markup/structureddocumenttagrangestart/level/) { get; } | Ruft die Ebene ab, auf der dieser Tagbereich des strukturierten Dokuments im Dokumentbaum beginnt. |
| [LockContentControl](../../aspose.words.markup/structureddocumenttagrangestart/lockcontentcontrol/) { get; set; } | Wenn eingestellt auf`WAHR` , diese Eigenschaft verhindert, dass ein Benutzer dieses strukturierte Dokument-Tag löscht. |
| [LockContents](../../aspose.words.markup/structureddocumenttagrangestart/lockcontents/) { get; set; } | Wenn eingestellt auf`WAHR` , diese Eigenschaft verhindert, dass ein Benutzer den Inhalt dieses strukturierten Dokument-Tags bearbeitet. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words.markup/structureddocumenttagrangestart/nodetype/) { get; } | Gibt zurückStructuredDocumentTagRangeStart . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft das unmittelbare übergeordnete Element dieses Knotens ab. |
| [Placeholder](../../aspose.words.markup/structureddocumenttagrangestart/placeholder/) { get; } | Ruft die ab[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)Enthält Platzhaltertext, der angezeigt werden soll, wenn der Inhalt dieses strukturierten Dokument-Tags leer ist und das zugehörige zugeordnete XML-Element leer ist, wie über angegeben [`XmlMapping`](./xmlmapping/) Element oder das[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) Element ist`WAHR` . |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttagrangestart/placeholdername/) { get; set; } | Ruft den Namen ab oder legt ihn fest[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) enthält Platzhaltertext. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar vorangeht. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt a zurück[`Range`](../../aspose.words/range/) Objekt, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [RangeEnd](../../aspose.words.markup/structureddocumenttagrangestart/rangeend/) { get; } | Gibt das Ende des Bereichs an, wenn der[`StructuredDocumentTag`](../structureddocumenttag/) ist ein strukturiertes Dokument-Tag mit Bereich. Andernfalls wird zurückgegeben`Null` . |
| [SdtType](../../aspose.words.markup/structureddocumenttagrangestart/sdttype/) { get; } | Ruft den Typ dieses strukturierten Dokument-Tags ab. |
| [Tag](../../aspose.words.markup/structureddocumenttagrangestart/tag/) { get; set; } | Gibt ein Tag an, das mit dem aktuellen Tag-Knoten des strukturierten Dokuments verknüpft ist. Kann nicht sein`Null` . |
| [Title](../../aspose.words.markup/structureddocumenttagrangestart/title/) { get; set; } | Gibt den Anzeigenamen an, der diesem strukturierten Dokument-Tag zugeordnet ist. Kann nicht sein`Null` . |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttagrangestart/wordopenxml/) { get; } | Ruft eine Zeichenfolge ab, die das im Knoten im enthaltene XML darstelltFlatOpc format. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttagrangestart/xmlmapping/) { get; } | Ruft ein Objekt ab, das die Zuordnung dieses strukturierten Dokument-Tag-Bereichs zu XML-Daten in einem benutzerdefinierten XML-Teil des aktuellen Dokuments darstellt. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttagrangestart/accept/)(DocumentVisitor) | Akzeptiert einen Besucher. |
| [AppendChild](../../aspose.words.markup/structureddocumenttagrangestart/appendchild/)(Node) | Fügt den angegebenen Knoten am Ende des stdContent-Bereichs hinzu. |
| [Clone](../../aspose.words/node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Ruft den ersten Vorfahren des angegebenen ab[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| [GetChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/getchildnodes/)(NodeType, bool) | Gibt eine Live-Sammlung untergeordneter Knoten zurück, die den angegebenen Typen entsprechen. |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagrangestart/getenumerator/)() | Bietet Unterstützung für die Iteration jedes Stils über die untergeordneten Knoten dieses Knotens. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Ruft den Text dieses Knotens und aller seiner untergeordneten Knoten ab. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ruft den nächsten Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ruft den vorherigen Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words.markup/structureddocumenttagrangestart/removeallchildren/)() | Entfernt alle Knoten zwischen diesem Bereichsanfangsknoten und dem Bereichsendknoten. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttagrangestart/removeselfonly/)() | Entfernt diesen Bereichsanfang und die entsprechenden Bereichsendknoten des strukturierten Dokument-Tags, , behält aber seinen Inhalt im Dokumentbaum. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exportiert den Inhalt des Knotens in einen String im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exportiert den Inhalt des Knotens mit den angegebenen Speicheroptionen in einen String. |

### Bemerkungen

Kann unmittelbares Kind von sein[`Body`](../../aspose.words/body/) Knoten **nur** .

### Beispiele

Zeigt, wie die Eigenschaften von strukturierten Dokument-Tags mit mehreren Abschnitten abgerufen werden.

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


