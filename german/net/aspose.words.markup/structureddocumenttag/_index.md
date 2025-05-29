---
title: StructuredDocumentTag Class
linktitle: StructuredDocumentTag
articleTitle: StructuredDocumentTag
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words.Markup.StructuredDocumentTag-Klasse für effiziente Inhaltskontrolle in Dokumenten. Verbessern Sie Ihr Dokumentenmanagement mit SDT-Funktionen!
type: docs
weight: 4750
url: /de/net/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class

Stellt ein strukturiertes Dokument-Tag (SDT oder Inhaltssteuerelement) in einem Dokument dar.

Um mehr zu erfahren, besuchen Sie die[Strukturierte Dokument-Tags oder Inhaltssteuerung](https://docs.aspose.com/words/net/working-with-content-control-sdt/) Dokumentationsartikel.

```csharp
public class StructuredDocumentTag : CompositeNode, IStructuredDocumentTag
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [StructuredDocumentTag](structureddocumenttag/)(*[DocumentBase](../../aspose.words/documentbase/), [SdtType](../sdttype/), [MarkupLevel](../markuplevel/)*) | Initialisiert eine neue Instanz des**Strukturiertes Dokument-Tag** Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Appearance](../../aspose.words.markup/structureddocumenttag/appearance/) { get; set; } | Ruft das Erscheinungsbild eines strukturierten Dokument-Tags ab/legt es fest. |
| [BuildingBlockCategory](../../aspose.words.markup/structureddocumenttag/buildingblockcategory/) { get; set; } | Gibt die Kategorie des Bausteins für dieses**SDT** node. Kann nicht`null` . |
| [BuildingBlockGallery](../../aspose.words.markup/structureddocumenttag/buildingblockgallery/) { get; set; } | Gibt den Typ des Bausteins für dieses**SDT** . Kann nicht sein`null` . |
| [CalendarType](../../aspose.words.markup/structureddocumenttag/calendartype/) { get; set; } | Gibt den Kalendertyp für dieses**SDT** . Standard istDefault |
| [Checked](../../aspose.words.markup/structureddocumenttag/checked/) { get; set; } | Ruft den aktuellen Status des Kontrollkästchens ab/setzt ihn**SDT** . Der Standardwert für diese Eigenschaft ist`FALSCH` . |
| [Color](../../aspose.words.markup/structureddocumenttag/color/) { get; set; } | Ruft die Farbe des strukturierten Dokument-Tags ab oder legt sie fest. |
| [ContentsFont](../../aspose.words.markup/structureddocumenttag/contentsfont/) { get; } | Schriftformatierung, die auf den eingegebenen Text angewendet wird**SDT** . |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ruft die Anzahl der unmittelbar untergeordneten Elemente dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| [DateDisplayFormat](../../aspose.words.markup/structureddocumenttag/datedisplayformat/) { get; set; } | Zeichenfolge, die das Format darstellt, in dem Datumsangaben angezeigt werden. |
| [DateDisplayLocale](../../aspose.words.markup/structureddocumenttag/datedisplaylocale/) { get; set; } | Ermöglicht das Festlegen/Abrufen des Sprachformats für das in diesem**SDT** . |
| [DateStorageFormat](../../aspose.words.markup/structureddocumenttag/datestorageformat/) { get; set; } | Ruft das Format ab, in dem das Datum für ein Datums-SDT gespeichert wird, wenn die**SDT** ist an einen XML-Knoten im Datenspeicher des Dokuments gebunden. Der Standardwert istDateTime |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [EndCharacterFont](../../aspose.words.markup/structureddocumenttag/endcharacterfont/) { get; } | Schriftformatierung, die auf das letzte Zeichen des eingegebenen Textes angewendet wird**SDT** . |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FullDate](../../aspose.words.markup/structureddocumenttag/fulldate/) { get; set; } | Gibt das vollständige Datum und die Uhrzeit der letzten Eingabe in dieses**SDT** . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Rückgaben`WAHR` wenn dieser Knoten untergeordnete Knoten hat. |
| [Id](../../aspose.words.markup/structureddocumenttag/id/) { get; } | Gibt eine eindeutige, schreibgeschützte, persistente numerische ID für dieses**SDT**. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Rückgaben`WAHR` da dieser Knoten untergeordnete Knoten haben kann. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttag/isshowingplaceholdertext/) { get; set; } | Gibt an, ob der Inhalt dieser**SDT** muss so interpretiert werden, dass es Platzhaltertext enthält (im Gegensatz zu regulärem Textinhalt innerhalb des SDT). |
| [IsTemporary](../../aspose.words.markup/structureddocumenttag/istemporary/) { get; set; } | Gibt an, ob diese**SDT** soll aus dem WordProcessingML-Dokument entfernt werden, wenn sein Inhalt geändert wird. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [Level](../../aspose.words.markup/structureddocumenttag/level/) { get; } | Ruft die Ebene ab, auf der dieses**SDT** tritt im Dokumentbaum auf. |
| [ListItems](../../aspose.words.markup/structureddocumenttag/listitems/) { get; } | Ruft ab[`SdtListItemCollection`](../sdtlistitemcollection/) damit verbunden**SDT** . |
| [LockContentControl](../../aspose.words.markup/structureddocumenttag/lockcontentcontrol/) { get; set; } | Wenn eingestellt auf`WAHR` , verhindert diese Eigenschaft, dass ein Benutzer diese**SDT** . |
| [LockContents](../../aspose.words.markup/structureddocumenttag/lockcontents/) { get; set; } | Wenn eingestellt auf`WAHR` , verhindert diese Eigenschaft, dass ein Benutzer den Inhalt dieser**SDT** . |
| [Multiline](../../aspose.words.markup/structureddocumenttag/multiline/) { get; set; } | Gibt an, ob diese**SDT** erlaubt mehrere Textzeilen. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words.markup/structureddocumenttag/nodetype/) { get; } | RückgabenStructuredDocumentTag . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [Placeholder](../../aspose.words.markup/structureddocumenttag/placeholder/) { get; } | Ruft die[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) Enthält Platzhaltertext, der angezeigt werden soll, wenn der Inhalt dieses SDT-Laufs leer ist, das zugehörige zugeordnete XML-Element leer ist, wie über die[`XmlMapping`](./xmlmapping/) element oder das[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) Element ist`WAHR` . |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttag/placeholdername/) { get; set; } | Ruft den Namen des[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) mit Platzhaltertext. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar vorausgeht. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt einen[`Range`](../../aspose.words/range/)Objekt, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [SdtType](../../aspose.words.markup/structureddocumenttag/sdttype/) { get; } | Ruft den Typ dieses**Strukturiertes Dokument-Tag** . |
| [Style](../../aspose.words.markup/structureddocumenttag/style/) { get; set; } | Ruft den Stil des strukturierten Dokument-Tags ab oder legt ihn fest. |
| [StyleName](../../aspose.words.markup/structureddocumenttag/stylename/) { get; set; } | Ruft den Namen des Stils ab, der auf das strukturierte Dokument-Tag angewendet wird, oder legt ihn fest. |
| [Tag](../../aspose.words.markup/structureddocumenttag/tag/) { get; set; } | Gibt ein Tag an, das mit dem aktuellen SDT-Knoten verknüpft ist. Kann nicht`null` . |
| [Title](../../aspose.words.markup/structureddocumenttag/title/) { get; set; } | Gibt den Anzeigenamen an, der mit diesem**SDT** . Kann nicht sein`null` . |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttag/wordopenxml/) { get; } | Ruft eine Zeichenfolge ab, die das XML darstellt, das im Knoten imFlatOpc format. |
| [WordOpenXMLMinimal](../../aspose.words.markup/structureddocumenttag/wordopenxmlminimal/) { get; } | Ruft eine Zeichenfolge ab, die das XML darstellt, das im Knoten imFlatOpc format. Im Gegensatz zu den[`WordOpenXML`](./wordopenxml/) Diese Methode generiert ein abgespecktes Dokument, das alle nicht inhaltsbezogenen Teile ausschließt. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttag/xmlmapping/) { get; } | Ruft ein Objekt ab, das die Zuordnung dieses strukturierten Dokumenttags zu XML-Daten in einem benutzerdefinierten XML-Teil des aktuellen Dokuments darstellt. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttag/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Nimmt einen Besucher auf. |
| override [AcceptEnd](../../aspose.words.markup/structureddocumenttag/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Akzeptiert einen Besucher für den Besuch des Endes des StructuredDocumentTag. |
| override [AcceptStart](../../aspose.words.markup/structureddocumenttag/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Akzeptiert einen Besucher für den Besuch des Anfangs des StructuredDocumentTag. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [Clear](../../aspose.words.markup/structureddocumenttag/clear/)() | Löscht den Inhalt dieses strukturierten Dokument-Tags und zeigt einen Platzhalter an, falls dieser definiert ist. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Erstellt einen Navigator, der zum Durchlaufen und Lesen von Knoten verwendet werden kann. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Ruft den ersten Vorfahren des angegebenen[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ruft den ersten Vorgänger des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Gibt eine Live-Sammlung von untergeordneten Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bietet Unterstützung für die Iteration des For-Each-Stils über die untergeordneten Knoten dieses Knotens. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ruft den Text dieses Knotens und aller seiner untergeordneten Knoten ab. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knoten-Array zurück. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Ruft den nächsten Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Fügt den angegebenen Knoten am Anfang der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Ruft den vorherigen Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Entfernt alle untergeordneten Knoten des aktuellen Knotens. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Entfernt den angegebenen untergeordneten Knoten. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttag/removeselfonly/)() | Entfernt nur diesen SDT-Knoten selbst, behält aber seinen Inhalt im Dokumentbaum. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Entfernt alle[`SmartTag`](../smarttag/) Nachkommenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Wählt den ersten[`Node`](../../aspose.words/node/) das dem XPath-Ausdruck entspricht. |
| [SetCheckedSymbol](../../aspose.words.markup/structureddocumenttag/setcheckedsymbol/)(*int, string*) | Legt das Symbol fest, das zur Darstellung des aktivierten Status eines Kontrollkästchen-Inhaltssteuerelements verwendet wird. |
| [SetUncheckedSymbol](../../aspose.words.markup/structureddocumenttag/setuncheckedsymbol/)(*int, string*) | Legt das Symbol fest, das zur Darstellung des deaktivierten Status eines Kontrollkästchen-Inhaltssteuerelements verwendet wird. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exportiert den Inhalt des Knotens in eine Zeichenfolge im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in eine Zeichenfolge. |

## Bemerkungen

Strukturierte Dokument-Tags (SDTs) ermöglichen die Einbettung kundendefinierter Semantik sowie des Verhaltens und Erscheinungsbilds in ein Dokument.

In dieser Version bietet Aspose.Words eine Reihe öffentlicher Methoden und Eigenschaften, um das Verhalten und den Inhalt von`StructuredDocumentTag` . Die Zuordnung von SDT-Knoten zu benutzerdefinierten XML-Paketen innerhalb eines Dokuments kann mithilfe von erfolgen.[`XmlMapping`](./xmlmapping/) Eigentum.

`StructuredDocumentTag` kann in einem Dokument an folgenden Stellen vorkommen:

* Blockebene - Zwischen Absätzen und Tabellen, als Kind eines[`Body`](../../aspose.words/body/) ,[`HeaderFooter`](../../aspose.words/headerfooter/) , [`Comment`](../../aspose.words/comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) oder ein[`Shape`](../../aspose.words.drawing/shape/) Knoten.
* Zeilenebene - Unter den Zeilen einer Tabelle, als Kind einer[`Table`](../../aspose.words.tables/table/) Knoten.
* Zellenebene - Unter den Zellen einer Tabellenzeile als Kind einer[`Row`](../../aspose.words.tables/row/) Knoten.
* Inline-Ebene - Unter Inline-Inhalten innerhalb, als Kind eines[`Paragraph`](../../aspose.words/paragraph/).
* Ineinander verschachtelt`StructuredDocumentTag`.

## Beispiele

Zeigt, wie mit Stilen für Inhaltssteuerelemente gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Unten finden Sie zwei Möglichkeiten, einen Stil aus dem Dokument auf ein strukturiertes Dokument-Tag anzuwenden.
// 1 – Wenden Sie ein Stilobjekt aus der Stilsammlung des Dokuments an:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Verweisen Sie im Dokument anhand des Namens auf einen Stil:
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
