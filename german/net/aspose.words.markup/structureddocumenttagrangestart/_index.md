---
title: StructuredDocumentTagRangeStart
second_title: Aspose.Words für .NET-API-Referenz
description: Repräsentiert einen Beginn von reichte strukturiertes Dokument-Tag das Inhalte mit mehreren Abschnitten akzeptiert. Siehe auchStructuredDocumentTagRangeEnd./structureddocumenttagrangeend .
type: docs
weight: 3850
url: /de/net/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class

Repräsentiert einen Beginn von **reichte** strukturiertes Dokument-Tag, das Inhalte mit mehreren Abschnitten akzeptiert. Siehe auch[`StructuredDocumentTagRangeEnd`](../structureddocumenttagrangeend) .

```csharp
public class StructuredDocumentTagRangeStart : Node, IEnumerable<Node>, IStructuredDocumentTag
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [StructuredDocumentTagRangeStart](structureddocumenttagrangestart)(DocumentBase, SdtType) | Initialisiert eine neue Instanz von **Beginn des strukturierten Dokument-Tag-Bereichs** Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [ChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/childnodes) { get; } | Ruft alle Knoten zwischen diesem Startknoten des Bereichs und dem Endknoten des Bereichs ab. |
| [Color](../../aspose.words.markup/structureddocumenttagrangestart/color) { get; set; } | Ruft die Farbe des strukturierten Dokument-Tags ab oder legt sie fest. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| virtual [Document](../../aspose.words/node/document) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [Id](../../aspose.words.markup/structureddocumenttagrangestart/id) { get; } | Gibt eine eindeutige, schreibgeschützte, persistente numerische ID für dieses strukturierte Dokument-Tag an. |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | Gibt wahr zurück, wenn dieser Knoten andere Knoten enthalten kann. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttagrangestart/isshowingplaceholdertext) { get; set; } | Gibt an, ob der Inhalt dieses strukturierten Dokument-Tags so interpretiert werden soll, dass er Platzhaltertext enthält (im Gegensatz zu regulären Textinhalten innerhalb des strukturierten Dokument-Tags). |
| [LastChild](../../aspose.words.markup/structureddocumenttagrangestart/lastchild) { get; } | Ruft das letzte untergeordnete Element im stdContent-Bereich ab. |
| [Level](../../aspose.words.markup/structureddocumenttagrangestart/level) { get; } | Ruft die Ebene ab, auf der dieser strukturierte Dokument-Tag-Bereich in der Dokumentstruktur beginnt. |
| [LockContentControl](../../aspose.words.markup/structureddocumenttagrangestart/lockcontentcontrol) { get; set; } | Wenn diese Eigenschaft auf „true“ gesetzt ist, wird es einem Benutzer untersagt, dieses strukturierte Dokument-Tag zu löschen. |
| [LockContents](../../aspose.words.markup/structureddocumenttagrangestart/lockcontents) { get; set; } | Wenn diese Eigenschaft auf „true“ gesetzt ist, verhindert sie, dass ein Benutzer den Inhalt dieses strukturierten Dokument-Tags bearbeitet. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words.markup/structureddocumenttagrangestart/nodetype) { get; } |  |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [Placeholder](../../aspose.words.markup/structureddocumenttagrangestart/placeholder) { get; } | Ruft die ab[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock) Platzhaltertext enthält, der angezeigt werden soll, wenn dieser strukturierte Dokument-Tag-Laufinhalt leer ist, das zugeordnete gemappte XML-Element leer ist, wie über die angegebene [`XmlMapping`](./xmlmapping) Element oder die[`IsShowingPlaceholderText`](./isshowingplaceholdertext) Element ist wahr. |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttagrangestart/placeholdername) { get; set; } | Ruft den Namen der ab oder legt ihn fest[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock) mit Platzhaltertext. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Ruft den Knoten unmittelbar vor diesem Knoten ab. |
| [Range](../../aspose.words/node/range) { get; } | Gibt a zurück **Bereich** Objekt, das den Teil eines Dokuments darstellt, das in diesem Knoten enthalten ist. |
| [RangeEnd](../../aspose.words.markup/structureddocumenttagrangestart/rangeend) { get; } | Gibt das Ende des Bereichs an, wenn das StructuredDocumentTag ein Bereichs-Tag für strukturierte Dokumente ist. Gibt andernfalls null zurück. |
| [SdtType](../../aspose.words.markup/structureddocumenttagrangestart/sdttype) { get; } | Ruft den Typ dieses strukturierten Dokument-Tags ab. |
| [Tag](../../aspose.words.markup/structureddocumenttagrangestart/tag) { get; set; } | Gibt ein Tag an, das dem aktuellen strukturierten Dokument-Tag-Knoten zugeordnet ist. Darf nicht null sein. |
| [Title](../../aspose.words.markup/structureddocumenttagrangestart/title) { get; set; } | Gibt den Anzeigenamen an, der diesem strukturierten Dokument-Tag zugeordnet ist. Darf nicht null sein. |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttagrangestart/wordopenxml) { get; } | Ruft eine Zeichenfolge ab, die das XML darstellt, das im Knoten in der enthalten istFlatOpc format. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttagrangestart/xmlmapping) { get; } | Ruft ein Objekt ab, das die Zuordnung dieses strukturierten Dokument-Tag-Bereichs zu XML-Daten in einem benutzerdefinierten XML-Teil des aktuellen Dokuments darstellt. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttagrangestart/accept)(DocumentVisitor) |  |
| [AppendChild](../../aspose.words.markup/structureddocumenttagrangestart/appendchild)(Node) | Fügt den angegebenen Knoten am Ende des stdContent-Bereichs hinzu. |
| [Clone](../../aspose.words/node/clone)(bool) | Erstellt ein Duplikat des Knotens. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Ruft den ersten Vorfahren der angegebenen ab[`NodeType`](../../aspose.words/nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| [GetChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/getchildnodes)(NodeType, bool) | Gibt eine Live-Sammlung von untergeordneten Knoten zurück, die den angegebenen Typen entsprechen. |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagrangestart/getenumerator)() | Bietet Unterstützung für die Iteration für jeden Stil über die untergeordneten Knoten dieses Knotens. |
| virtual [GetText](../../aspose.words/node/gettext)() | Ruft den Text dieses Knotens und aller seiner Kinder ab. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Ruft den nächsten Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Ruft den vorherigen Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [Remove](../../aspose.words/node/remove)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words.markup/structureddocumenttagrangestart/removeallchildren)() | Entfernt alle Knoten zwischen diesem Startknoten des Bereichs und dem Endknoten des Bereichs. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttagrangestart/removeselfonly)() | Entfernt diesen Bereichsanfang und entsprechende Bereichsendknoten des strukturierten Dokument-Tags, , behält aber seinen Inhalt im Dokumentbaum. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exportiert den Inhalt des Knotens in einen String im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in einen String. |

### Bemerkungen

Kann direktes Kind von sein[`Body`](../../aspose.words/body) Knoten **nur** .

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

* class [Node](../../aspose.words/node)
* interface [IStructuredDocumentTag](../istructureddocumenttag)
* namensraum [Aspose.Words.Markup](../../aspose.words.markup)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
