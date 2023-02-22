---
title: Class StructuredDocumentTag
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Markup.StructuredDocumentTag klas. Repräsentiert ein strukturiertes DokumentTag SDT oder Content Control in einem Dokument.
type: docs
weight: 3820
url: /de/net/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class

Repräsentiert ein strukturiertes Dokument-Tag (SDT oder Content Control) in einem Dokument.

```csharp
public class StructuredDocumentTag : CompositeNode, IStructuredDocumentTag
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [StructuredDocumentTag](structureddocumenttag/)(DocumentBase, SdtType, MarkupLevel) | Initialisiert eine neue Instanz von **Strukturiertes Dokument-Tag** Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Appearance](../../aspose.words.markup/structureddocumenttag/appearance/) { get; set; } | Erhält/legt das Erscheinungsbild eines strukturierten Dokument-Tags fest. |
| [BuildingBlockCategory](../../aspose.words.markup/structureddocumenttag/buildingblockcategory/) { get; set; } | Gibt die Kategorie des Bausteins dafür an **SDT** node. Darf nicht null sein. |
| [BuildingBlockGallery](../../aspose.words.markup/structureddocumenttag/buildingblockgallery/) { get; set; } | Gibt den Typ des Bausteins dafür an **SDT** . darf nicht null sein. |
| [CalendarType](../../aspose.words.markup/structureddocumenttag/calendartype/) { get; set; } | Gibt den Kalendertyp dafür an **SDT** . Standard istDefault |
| [Checked](../../aspose.words.markup/structureddocumenttag/checked/) { get; set; } | Ruft/Setzt den aktuellen Status der Checkbox **SDT** . Der Standardwert für diese Eigenschaft ist „false“. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Ruft alle unmittelbar untergeordneten Knoten dieses Knotens ab. |
| [Color](../../aspose.words.markup/structureddocumenttag/color/) { get; set; } | Ruft die Farbe des strukturierten Dokument-Tags ab oder legt sie fest. |
| [ContentsFont](../../aspose.words.markup/structureddocumenttag/contentsfont/) { get; } | Schriftartformatierung, die auf den eingegebenen Text angewendet wird **SDT** . |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ruft die Anzahl der unmittelbaren Kinder dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| [DateDisplayFormat](../../aspose.words.markup/structureddocumenttag/datedisplayformat/) { get; set; } | Zeichenfolge, die das Format darstellt, in dem Datumsangaben angezeigt werden. Darf nicht null sein. Die Daten für Englisch (US) sind "MM/TT/JJJJ". |
| [DateDisplayLocale](../../aspose.words.markup/structureddocumenttag/datedisplaylocale/) { get; set; } | Ermöglicht das Festlegen/Abrufen des Sprachformats für das darin angezeigte Datum **SDT** . |
| [DateStorageFormat](../../aspose.words.markup/structureddocumenttag/datestorageformat/) { get; set; } | Ruft/legt das Format ab, in dem das Datum für einen Datums-SDT gespeichert wird, wenn der **SDT** ist an einen XML-Knoten im Datenspeicher des Dokuments gebunden. Standardwert istDateTime |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [EndCharacterFont](../../aspose.words.markup/structureddocumenttag/endcharacterfont/) { get; } | Schriftartformatierung, die auf das letzte Zeichen des eingegebenen Textes angewendet wird **SDT** . |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FullDate](../../aspose.words.markup/structureddocumenttag/fulldate/) { get; set; } | Gibt das vollständige Datum und die letzte Uhrzeit an, die hierin eingegeben wurden **SDT** . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Gibt wahr zurück, wenn dieser Knoten untergeordnete Knoten hat. |
| [Id](../../aspose.words.markup/structureddocumenttag/id/) { get; } | Gibt eine eindeutige, schreibgeschützte, persistente numerische ID dafür an **SDT**. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Gibt wahr zurück, da dieser Knoten untergeordnete Knoten haben kann. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttag/isshowingplaceholdertext/) { get; set; } | Gibt an, ob der Inhalt dieser **SDT** soll so interpretiert werden, dass es Platzhaltertext enthält (im Gegensatz zu regulären Textinhalten innerhalb des SDT). |
| [IsTemporary](../../aspose.words.markup/structureddocumenttag/istemporary/) { get; set; } | Gibt an, ob dies **SDT** muss aus dem WordProcessingML-Dokument entfernt werden, wenn sein Inhalt geändert wird. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [Level](../../aspose.words.markup/structureddocumenttag/level/) { get; } | Ruft die Ebene ab, bei der dies der Fall ist **SDT** kommt im Dokumentbaum vor. |
| [ListItems](../../aspose.words.markup/structureddocumenttag/listitems/) { get; } | erhält[`SdtListItemCollection`](../sdtlistitemcollection/) damit verbunden **SDT** . |
| [LockContentControl](../../aspose.words.markup/structureddocumenttag/lockcontentcontrol/) { get; set; } | Wenn diese Eigenschaft auf „true“ gesetzt ist, verhindert sie, dass ein Benutzer dies löscht **SDT** . |
| [LockContents](../../aspose.words.markup/structureddocumenttag/lockcontents/) { get; set; } | Wenn diese Eigenschaft auf „true“ gesetzt ist, verbietet es einem Benutzer, den Inhalt von this zu bearbeiten **SDT** . |
| [Multiline](../../aspose.words.markup/structureddocumenttag/multiline/) { get; set; } | Gibt an, ob dies **SDT** erlaubt mehrere Textzeilen. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words.markup/structureddocumenttag/nodetype/) { get; } | gibt zurück **NodeType.StructuredDocumentTag** . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [Placeholder](../../aspose.words.markup/structureddocumenttag/placeholder/) { get; } | Ruft die ab[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) Platzhaltertext enthält, der angezeigt werden soll, wenn der Inhalt dieses SDT-Laufs leer ist, das zugeordnete zugeordnete XML-Element leer ist, wie über angegeben[`XmlMapping`](./xmlmapping/) element oder die[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) Element ist wahr. |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttag/placeholdername/) { get; set; } | Ruft den Namen der ab oder legt ihn fest[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) mit Platzhaltertext. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten unmittelbar vor diesem Knoten ab. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt a zurück **Bereich** Objekt, das den Teil eines Dokuments darstellt, das in diesem Knoten enthalten ist. |
| [SdtType](../../aspose.words.markup/structureddocumenttag/sdttype/) { get; } | Ruft diesen Typ ab **Strukturiertes Dokument-Tag** . |
| [Style](../../aspose.words.markup/structureddocumenttag/style/) { get; set; } | Ruft den Stil des strukturierten Dokument-Tags ab oder legt ihn fest. |
| [StyleName](../../aspose.words.markup/structureddocumenttag/stylename/) { get; set; } | Ruft den Namen des Stils ab, der auf das strukturierte Dokument-Tag angewendet wird, oder legt ihn fest. |
| [Tag](../../aspose.words.markup/structureddocumenttag/tag/) { get; set; } | Gibt ein Tag an, das dem aktuellen SDT-Knoten zugeordnet ist. Darf nicht null sein. |
| [Title](../../aspose.words.markup/structureddocumenttag/title/) { get; set; } | Gibt den zugehörigen Anzeigenamen an **SDT** . Darf nicht null sein. |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttag/wordopenxml/) { get; } | Ruft eine Zeichenfolge ab, die das XML darstellt, das im Knoten in der enthalten istFlatOpc format. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttag/xmlmapping/) { get; } | Ruft ein Objekt ab, das die Zuordnung dieses strukturierten Dokument-Tags zu XML-Daten in einem benutzerdefinierten XML-Teil des aktuellen Dokuments darstellt. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttag/accept/)(DocumentVisitor) | Akzeptiert einen Besucher. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [Clear](../../aspose.words.markup/structureddocumenttag/clear/)() | Löscht den Inhalt dieses strukturierten Dokument-Tags und zeigt einen Platzhalter an, falls definiert. |
| [Clone](../../aspose.words/node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Reserviert für Systemnutzung. IXPfadNavigierbar. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Ruft den ersten Vorfahren der angegebenen ab[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Gibt eine Live-Sammlung von untergeordneten Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bietet Unterstützung für die Iteration für jeden Stil über die untergeordneten Knoten dieses Knotens. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ruft den Text dieses Knotens und aller seiner Kinder ab. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knotenarray zurück. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ruft den nächsten Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Fügt den angegebenen Knoten am Anfang der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ruft den vorherigen Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Entfernt alle untergeordneten Knoten des aktuellen Knotens. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Entfernt den angegebenen untergeordneten Knoten. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttag/removeselfonly/)() | Entfernt nur diesen SDT-Knoten selbst, behält aber seinen Inhalt im Dokumentbaum. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Entfernt alle[`SmartTag`](../smarttag/) Nachkommenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Wählt eine Liste von Knoten aus, die mit dem XPath-Ausdruck übereinstimmen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Wählt den ersten Knoten aus, der mit dem XPath-Ausdruck übereinstimmt. |
| [SetCheckedSymbol](../../aspose.words.markup/structureddocumenttag/setcheckedsymbol/)(int, string) | Legt das Symbol fest, das zur Darstellung des aktivierten Zustands eines Kontrollkästchen-Inhaltssteuerelements verwendet wird. |
| [SetUncheckedSymbol](../../aspose.words.markup/structureddocumenttag/setuncheckedsymbol/)(int, string) | Legt das Symbol fest, das verwendet wird, um den deaktivierten Zustand eines Kontrollkästchen-Inhaltssteuerelements darzustellen. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exportiert den Inhalt des Knotens in einen String im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in einen String. |

### Bemerkungen

Strukturierte Dokument-Tags (SDTs) ermöglichen es, kundendefinierte Semantik sowie deren -Verhalten und -Erscheinungsbild in ein Dokument einzubetten.

In dieser Version bietet Aspose.Words eine Reihe von öffentlichen Methoden und Eigenschaften, um das Verhalten und den Inhalt von zu manipulieren`StructuredDocumentTag` . Die Zuordnung von SDT-Knoten zu benutzerdefinierten XML-Paketen innerhalb eines Dokuments kann mit durchgeführt werden[`XmlMapping`](./xmlmapping/) Eigentum.

`StructuredDocumentTag` kann in einem Dokument an folgenden Stellen vorkommen:

* Blockebene - Zwischen Absätzen und Tabellen, als untergeordnetes Element von a[`Body`](../../aspose.words/body/) ,[`HeaderFooter`](../../aspose.words/headerfooter/) , [`Comment`](../../aspose.words/comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) oder ein[`Shape`](../../aspose.words.drawing/shape/) Knoten.
* Zeilenebene - Zwischen Zeilen in einer Tabelle, als untergeordnetes Element von a[`Table`](../../aspose.words.tables/table/) Knoten.
* Zellenebene - Zwischen Zellen in einer Tabellenzeile, als untergeordnetes Element von a[`Row`](../../aspose.words.tables/row/) Knoten.
* Inline-Ebene - Unter Inline-Inhalten als untergeordnetes Element von a[`Paragraph`](../../aspose.words/paragraph/).
* Verschachtelt in einem anderen`StructuredDocumentTag`.

### Beispiele

Zeigt, wie Sie mit Stilen für Inhaltssteuerelemente arbeiten.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Im Folgenden finden Sie zwei Möglichkeiten, einen Stil aus dem Dokument auf ein strukturiertes Dokument-Tag anzuwenden.
// 1 - Wende ein Stilobjekt aus der Stilsammlung des Dokuments an:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Einen Stil im Dokument namentlich referenzieren:
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### Siehe auch

* class [CompositeNode](../../aspose.words/compositenode/)
* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* namensraum [Aspose.Words.Markup](../../aspose.words.markup/)
* Montage [Aspose.Words](../../)


