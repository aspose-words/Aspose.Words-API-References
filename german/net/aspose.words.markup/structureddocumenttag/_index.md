---
title: Class StructuredDocumentTag
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Markup.StructuredDocumentTag klas. Stellt ein strukturiertes DokumentTag SDT oder Inhaltssteuerung in einem Dokument dar.
type: docs
weight: 4060
url: /de/net/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class

Stellt ein strukturiertes Dokument-Tag (SDT oder Inhaltssteuerung) in einem Dokument dar.

Um mehr zu erfahren, besuchen Sie die[Strukturierte Dokument-Tags oder Inhaltskontrolle](https://docs.aspose.com/words/net/working-with-content-control-sdt/) Dokumentationsartikel.

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
| [Appearance](../../aspose.words.markup/structureddocumenttag/appearance/) { get; set; } | Ruft das Erscheinungsbild eines strukturierten Dokument-Tags ab bzw. legt es fest. |
| [BuildingBlockCategory](../../aspose.words.markup/structureddocumenttag/buildingblockcategory/) { get; set; } | Gibt die Kategorie des Bausteins dafür an **SDT** node. Kann nicht sein`Null` . |
| [BuildingBlockGallery](../../aspose.words.markup/structureddocumenttag/buildingblockgallery/) { get; set; } | Gibt den Typ des Bausteins dafür an **SDT** . Kann nicht sein`Null` . |
| [CalendarType](../../aspose.words.markup/structureddocumenttag/calendartype/) { get; set; } | Gibt den Kalendertyp hierfür an **SDT** . Standard istDefault |
| [Checked](../../aspose.words.markup/structureddocumenttag/checked/) { get; set; } | Ruft den aktuellen Status des Kontrollkästchens ab bzw. legt diesen fest **SDT** . Der Standardwert für diese Eigenschaft ist`FALSCH` . |
| [Color](../../aspose.words.markup/structureddocumenttag/color/) { get; set; } | Ruft die Farbe des strukturierten Dokument-Tags ab oder legt diese fest. |
| [ContentsFont](../../aspose.words.markup/structureddocumenttag/contentsfont/) { get; } | Schriftartformatierung, die auf den eingegebenen Text angewendet wird **SDT** . |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ruft die Anzahl der unmittelbaren Kinder dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| [DateDisplayFormat](../../aspose.words.markup/structureddocumenttag/datedisplayformat/) { get; set; } | Zeichenfolge, die das Format darstellt, in dem Datumsangaben angezeigt werden. Kann nicht sein`Null` . Das Datum für Englisch (USA) ist „mm/tt/jjjj“. |
| [DateDisplayLocale](../../aspose.words.markup/structureddocumenttag/datedisplaylocale/) { get; set; } | Ermöglicht das Festlegen/Abrufen des Sprachformats für das hier angezeigte Datum **SDT** . |
| [DateStorageFormat](../../aspose.words.markup/structureddocumenttag/datestorageformat/) { get; set; } | Ruft das Format ab bzw. legt es fest, in dem das Datum für eine Datums-SDT gespeichert wird, wenn das **SDT**ist an einen XML-Knoten im Datenspeicher des Dokuments gebunden. Der Standardwert istDateTime |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [EndCharacterFont](../../aspose.words.markup/structureddocumenttag/endcharacterfont/) { get; } | Schriftartformatierung, die auf das letzte Zeichen des eingegebenen Textes angewendet wird **SDT** . |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FullDate](../../aspose.words.markup/structureddocumenttag/fulldate/) { get; set; } | Gibt das vollständige Datum und die Uhrzeit an, die zuletzt eingegeben wurden **SDT** . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Gibt zurück`WAHR` wenn dieser Knoten untergeordnete Knoten hat. |
| [Id](../../aspose.words.markup/structureddocumenttag/id/) { get; } | Gibt hierfür eine eindeutige, schreibgeschützte, persistente numerische ID an **SDT**. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Gibt zurück`WAHR` da dieser Knoten untergeordnete Knoten haben kann. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttag/isshowingplaceholdertext/) { get; set; } | Gibt an, ob der Inhalt davon **SDT**wird so interpretiert, dass es Platzhaltertext enthält (im Gegensatz zu regulären Textinhalten innerhalb des SDT). |
| [IsTemporary](../../aspose.words.markup/structureddocumenttag/istemporary/) { get; set; } | Gibt an, ob dies der Fall ist **SDT** wird aus dem WordProcessingML-Dokument entfernt, wenn dessen Inhalt geändert wird. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [Level](../../aspose.words.markup/structureddocumenttag/level/) { get; } | Ruft die Ebene ab, auf der dies geschieht **SDT** kommt im Dokumentenbaum vor. |
| [ListItems](../../aspose.words.markup/structureddocumenttag/listitems/) { get; } | Ruft ab[`SdtListItemCollection`](../sdtlistitemcollection/) damit verbunden **SDT** . |
| [LockContentControl](../../aspose.words.markup/structureddocumenttag/lockcontentcontrol/) { get; set; } | Wenn eingestellt auf`WAHR` , verhindert diese Eigenschaft, dass ein Benutzer dies löschen kann **SDT** . |
| [LockContents](../../aspose.words.markup/structureddocumenttag/lockcontents/) { get; set; } | Wenn eingestellt auf`WAHR` , verhindert diese Eigenschaft, dass ein Benutzer den Inhalt dieser Datei bearbeitet **SDT** . |
| [Multiline](../../aspose.words.markup/structureddocumenttag/multiline/) { get; set; } | Gibt an, ob dies der Fall ist **SDT** Ermöglicht mehrere Textzeilen. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words.markup/structureddocumenttag/nodetype/) { get; } | Gibt zurückStructuredDocumentTag . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft das unmittelbare übergeordnete Element dieses Knotens ab. |
| [Placeholder](../../aspose.words.markup/structureddocumenttag/placeholder/) { get; } | Ruft die ab[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)enthält Platzhaltertext, der angezeigt werden soll, wenn der Inhalt dieses SDT-Laufs leer ist, das zugehörige zugeordnete XML-Element ist leer, wie über angegeben[`XmlMapping`](./xmlmapping/) element oder die[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) Element ist`WAHR` . |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttag/placeholdername/) { get; set; } | Ruft den Namen ab oder legt ihn fest[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) enthält Platzhaltertext. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar vorangeht. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt a zurück[`Range`](../../aspose.words/range/) Objekt, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [SdtType](../../aspose.words.markup/structureddocumenttag/sdttype/) { get; } | Ruft den Typ davon ab **Strukturiertes Dokument-Tag** . |
| [Style](../../aspose.words.markup/structureddocumenttag/style/) { get; set; } | Ruft den Stil des strukturierten Dokument-Tags ab oder legt diesen fest. |
| [StyleName](../../aspose.words.markup/structureddocumenttag/stylename/) { get; set; } | Ruft den Namen des Stils ab, der auf das strukturierte Dokument-Tag angewendet wird, oder legt diesen fest. |
| [Tag](../../aspose.words.markup/structureddocumenttag/tag/) { get; set; } | Gibt ein Tag an, das dem aktuellen SDT-Knoten zugeordnet ist. Kann nicht sein`Null` . |
| [Title](../../aspose.words.markup/structureddocumenttag/title/) { get; set; } | Gibt den damit verbundenen Anzeigenamen an **SDT** . Kann nicht sein`Null` . |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttag/wordopenxml/) { get; } | Ruft eine Zeichenfolge ab, die das im Knoten im enthaltene XML darstelltFlatOpc format. |
| [WordOpenXMLMinimal](../../aspose.words.markup/structureddocumenttag/wordopenxmlminimal/) { get; } | Ruft eine Zeichenfolge ab, die das im Knoten im enthaltene XML darstelltFlatOpc format. Im Gegensatz zu[`WordOpenXML`](./wordopenxml/)-Eigenschaft generiert diese Methode ein reduziertes Dokument, das alle nicht inhaltsbezogenen Teile ausschließt. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttag/xmlmapping/) { get; } | Ruft ein Objekt ab, das die Zuordnung dieses strukturierten Dokument-Tags zu XML-Daten in einem benutzerdefinierten XML-Teil des aktuellen Dokuments darstellt. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttag/accept/)(DocumentVisitor) | Akzeptiert einen Besucher. |
| override [AcceptEnd](../../aspose.words.markup/structureddocumenttag/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words.markup/structureddocumenttag/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clear](../../aspose.words.markup/structureddocumenttag/clear/)() | Löscht den Inhalt dieses strukturierten Dokument-Tags und zeigt einen Platzhalter an, sofern dieser definiert ist. |
| [Clone](../../aspose.words/node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Erstellt einen Navigator, der zum Durchlaufen und Lesen von Knoten verwendet werden kann. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Ruft den ersten Vorfahren des angegebenen ab[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Gibt eine Live-Sammlung untergeordneter Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bietet Unterstützung für die Iteration jedes Stils über die untergeordneten Knoten dieses Knotens. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ruft den Text dieses Knotens und aller seiner untergeordneten Knoten ab. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knoten-Array zurück. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ruft den nächsten Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ruft den vorherigen Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Entfernt alle untergeordneten Knoten des aktuellen Knotens. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttag/removeselfonly/)() | Entfernt nur diesen SDT-Knoten selbst, behält aber seinen Inhalt im Dokumentbaum. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Entfernt alle[`SmartTag`](../smarttag/)Nachkommenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Wählt den ersten aus[`Node`](../../aspose.words/node/) das entspricht dem XPath-Ausdruck. |
| [SetCheckedSymbol](../../aspose.words.markup/structureddocumenttag/setcheckedsymbol/)(int, string) | Legt das Symbol fest, das zur Darstellung des aktivierten Status eines Kontrollkästchen-Inhaltssteuerelements verwendet wird. |
| [SetUncheckedSymbol](../../aspose.words.markup/structureddocumenttag/setuncheckedsymbol/)(int, string) | Legt das Symbol fest, das verwendet wird, um den deaktivierten Zustand eines Kontrollkästchen-Inhaltssteuerelements darzustellen. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exportiert den Inhalt des Knotens in einen String im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exportiert den Inhalt des Knotens mit den angegebenen Speicheroptionen in einen String. |

### Bemerkungen

Strukturierte Dokument-Tags (SDTs) ermöglichen die Einbettung kundenspezifischer Semantik sowie seines Verhaltens und Aussehens in ein Dokument.

In dieser Version stellt Aspose.Words eine Reihe öffentlicher Methoden und Eigenschaften bereit, um das Verhalten und den Inhalt von zu manipulieren`StructuredDocumentTag` . Die Zuordnung von SDT-Knoten zu benutzerdefinierten XML-Paketen innerhalb eines Dokuments kann mit using durchgeführt werden[`XmlMapping`](./xmlmapping/) Eigentum.

`StructuredDocumentTag` kann in einem Dokument an folgenden Stellen vorkommen:

* Blockebene – Zwischen Absätzen und Tabellen, als untergeordnetes Element von a[`Body`](../../aspose.words/body/) ,[`HeaderFooter`](../../aspose.words/headerfooter/) , [`Comment`](../../aspose.words/comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) oder ein[`Shape`](../../aspose.words.drawing/shape/) Knoten.
* Zeilenebene – Zwischen Zeilen in einer Tabelle, als untergeordnetes Element von a[`Table`](../../aspose.words.tables/table/) Knoten.
* Zellebene – Zwischen Zellen in einer Tabellenzeile, als untergeordnetes Element von a[`Row`](../../aspose.words.tables/row/) Knoten.
* Inline-Ebene – Unter Inline-Inhalten im Inneren, als untergeordnetes Element von a[`Paragraph`](../../aspose.words/paragraph/).
* In einem anderen verschachtelt`StructuredDocumentTag`.

### Beispiele

Zeigt, wie mit Stilen für Inhaltssteuerelemente gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nachfolgend finden Sie zwei Möglichkeiten, einen Stil aus dem Dokument auf ein strukturiertes Dokument-Tag anzuwenden.
// 1 – Ein Stilobjekt aus der Stilsammlung des Dokuments anwenden:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 – Einen Stil im Dokument namentlich referenzieren:
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Console.WriteLine(sdt.WordOpenXMLMinimal);

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### Siehe auch

* class [CompositeNode](../../aspose.words/compositenode/)
* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* namensraum [Aspose.Words.Markup](../../aspose.words.markup/)
* Montage [Aspose.Words](../../)


