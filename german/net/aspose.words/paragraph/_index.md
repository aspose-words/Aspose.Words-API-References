---
title: Class Paragraph
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Paragraph klas. Repräsentiert einen Textabsatz.
type: docs
weight: 4150
url: /de/net/aspose.words/paragraph/
---
## Paragraph class

Repräsentiert einen Textabsatz.

```csharp
public class Paragraph : CompositeNode
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [Paragraph](paragraph/)(DocumentBase) | Initialisiert eine neue Instanz von **Absatz** Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BreakIsStyleSeparator](../../aspose.words/paragraph/breakisstyleseparator/) { get; } | True, wenn dieser Absatzumbruch ein Stiltrennzeichen ist. Ein Stiltrenner ermöglicht es, dass ein Absatz aus Teilen mit unterschiedlichen Absatzstilen besteht. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Ruft alle unmittelbar untergeordneten Knoten dieses Knotens ab. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ruft die Anzahl der unmittelbaren Kinder dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FrameFormat](../../aspose.words/paragraph/frameformat/) { get; } | Bietet Zugriff auf die Absatzformatierungseigenschaften. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Gibt wahr zurück, wenn dieser Knoten untergeordnete Knoten hat. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Gibt wahr zurück, da dieser Knoten untergeordnete Knoten haben kann. |
| [IsDeleteRevision](../../aspose.words/paragraph/isdeleterevision/) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsnachverfolgung aktiviert war. |
| [IsEndOfCell](../../aspose.words/paragraph/isendofcell/) { get; } | True, wenn dieser Absatz der letzte Absatz in a ist[`Cell`](../../aspose.words.tables/cell/) ; andernfalls falsch. |
| [IsEndOfDocument](../../aspose.words/paragraph/isendofdocument/) { get; } | Wahr, wenn dieser Absatz der letzte Absatz im letzten Abschnitt des Dokuments ist. |
| [IsEndOfHeaderFooter](../../aspose.words/paragraph/isendofheaderfooter/) { get; } | True, wenn dieser Absatz der letzte Absatz in der ist **Kopfzeile Fußzeile** (Haupttextgeschichte) von a **Abschnitt** ; andernfalls falsch. |
| [IsEndOfSection](../../aspose.words/paragraph/isendofsection/) { get; } | True, wenn dieser Absatz der letzte Absatz in der ist **Körper** (Haupttextgeschichte) von a **Abschnitt** ; andernfalls falsch. |
| [IsFormatRevision](../../aspose.words/paragraph/isformatrevision/) { get; } | Gibt „true“ zurück, wenn die Formatierung des Objekts in Microsoft Word geändert wurde, während die Änderungsverfolgung aktiviert war. |
| [IsInCell](../../aspose.words/paragraph/isincell/) { get; } | Wahr, wenn dieser Absatz ein direktes Kind von ist[`Cell`](../../aspose.words.tables/cell/) ; andernfalls falsch. |
| [IsInsertRevision](../../aspose.words/paragraph/isinsertrevision/) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war. |
| [IsListItem](../../aspose.words/paragraph/islistitem/) { get; } | Wahr, wenn der Absatz ein Element in einer Aufzählung oder nummerierten Liste in der ursprünglichen Revision ist. |
| [IsMoveFromRevision](../../aspose.words/paragraph/ismovefromrevision/) { get; } | gibt zurück **Stimmt** wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsnachverfolgung aktiviert war. |
| [IsMoveToRevision](../../aspose.words/paragraph/ismovetorevision/) { get; } | gibt zurück **Stimmt** wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsnachverfolgung aktiviert war. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [ListFormat](../../aspose.words/paragraph/listformat/) { get; } | Bietet Zugriff auf die Listenformatierungseigenschaften des Absatzes. |
| [ListLabel](../../aspose.words/paragraph/listlabel/) { get; } | erhält a[`ListLabel`](./listlabel/) Objekt, das Zugriff auf den Listennummerierungswert und die Formatierung für diesen Absatz bereitstellt. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words/paragraph/nodetype/) { get; } | gibt zurück **Knotentyp.Absatz** . |
| [ParagraphBreakFont](../../aspose.words/paragraph/paragraphbreakfont/) { get; } | Bietet Zugriff auf die Schriftartformatierung des Absatzumbruchzeichens. |
| [ParagraphFormat](../../aspose.words/paragraph/paragraphformat/) { get; } | Bietet Zugriff auf die Absatzformatierungseigenschaften. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [ParentSection](../../aspose.words/paragraph/parentsection/) { get; } | Ruft das übergeordnete Element ab[`Section`](../section/) des Absatzes. |
| [ParentStory](../../aspose.words/paragraph/parentstory/) { get; } | Ruft die möglicherweise übergeordnete Story auf Abschnittsebene ab[`Body`](../body/) oder[`HeaderFooter`](../headerfooter/) . |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten unmittelbar vor diesem Knoten ab. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt a zurück **Bereich** Objekt, das den Teil eines Dokuments darstellt, das in diesem Knoten enthalten ist. |
| [Runs](../../aspose.words/paragraph/runs/) { get; } | Bietet Zugriff auf die getippte Sammlung von Textteilen innerhalb des Absatzes. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words/paragraph/accept/)(DocumentVisitor) | Akzeptiert einen Besucher. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_1)(string) | Fügt diesem Absatz ein Feld hinzu. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield)(FieldType, bool) | Fügt diesem Absatz ein Feld hinzu. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_2)(string, string) | Fügt diesem Absatz ein Feld hinzu. |
| [Clone](../../aspose.words/node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Reserviert für Systemnutzung. IXPfadNavigierbar. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Ruft den ersten Vorfahren der angegebenen ab[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Gibt eine Live-Sammlung von untergeordneten Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEffectiveTabStops](../../aspose.words/paragraph/geteffectivetabstops/)() | Gibt ein Array aller Tabstopps zurück, die auf diesen Absatz angewendet wurden, einschließlich der indirekten Anwendung durch Stile oder Listen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bietet Unterstützung für die Iteration für jeden Stil über die untergeordneten Knoten dieses Knotens. |
| override [GetText](../../aspose.words/paragraph/gettext/)() | Ruft den Text dieses Absatzes ab, einschließlich des Absatzendezeichens. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knotenarray zurück. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_1)(string, Node, bool) | Fügt ein Feld in diesen Absatz ein. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield)(FieldType, bool, Node, bool) | Fügt ein Feld in diesen Absatz ein. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_2)(string, string, Node, bool) | Fügt ein Feld in diesen Absatz ein. |
| [JoinRunsWithSameFormatting](../../aspose.words/paragraph/joinrunswithsameformatting/)() | Verbindet Läufe mit der gleichen Formatierung im Absatz. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ruft den nächsten Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Fügt den angegebenen Knoten am Anfang der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ruft den vorherigen Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Entfernt alle untergeordneten Knoten des aktuellen Knotens. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Entfernt den angegebenen untergeordneten Knoten. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Entfernt alle[`SmartTag`](../../aspose.words.markup/smarttag/) Nachkommenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Wählt eine Liste von Knoten aus, die mit dem XPath-Ausdruck übereinstimmen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Wählt den ersten Knoten aus, der mit dem XPath-Ausdruck übereinstimmt. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exportiert den Inhalt des Knotens in einen String im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in einen String. |

### Bemerkungen

`Paragraph` ist ein Knoten auf Blockebene und kann ein untergeordnetes Element von Klassen sein, die von abgeleitet sind[`Story`](../story/) oder[`InlineStory`](../inlinestory/).

`Paragraph` kann eine beliebige Anzahl von Knoten und Lesezeichen auf Inline-Ebene enthalten.

Die vollständige Liste der untergeordneten Knoten, die innerhalb eines Absatzes vorkommen können, besteht aus [`BookmarkStart`](../bookmarkstart/) ,[`BookmarkEnd`](../bookmarkend/) , [`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) , [`FieldEnd`](../../aspose.words.fields/fieldend/) ,[`FormField`](../../aspose.words.fields/formfield/) , [`Comment`](../comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) , [`Run`](../run/) ,[`SpecialChar`](../specialchar/) , [`Shape`](../../aspose.words.drawing/shape/) ,[`GroupShape`](../../aspose.words.drawing/groupshape/) , [`SmartTag`](../../aspose.words.markup/smarttag/).

Ein gültiger Absatz in Microsoft Word endet immer mit einem Absatzumbruchzeichen und ein minimal gültiger Absatz besteht nur aus einem Absatzumbruch. Das **Absatz** Die Klasse fügt automatisch das entsprechende Absatzumbruchzeichen am Ende hinzu und dieses Zeichen ist nicht Teil der untergeordneten Knoten der **Absatz** , also a **Absatz** kann leer sein.

Schließen Sie das Ende des Absatzes nicht ein[`ControlChar.ParagraphBreak`](../controlchar/paragraphbreak/) oder Zellenende[`ControlChar.Cell`](../controlchar/cell/) Zeichen innerhalb des Texts von des Absatzes, da dies den Absatz ungültig machen könnte, wenn das Dokument in Microsoft Word geöffnet wird.

### Beispiele

Zeigt, wie ein Aspose.Words-Dokument von Hand erstellt wird.

```csharp
Document doc = new Document();

// Ein leeres Dokument enthält einen Abschnitt, einen Hauptteil und einen Absatz.
// Rufen Sie die Methode "RemoveAllChildren" auf, um alle diese Knoten zu entfernen,
// und am Ende einen Dokumentknoten ohne Kinder haben.
doc.RemoveAllChildren();

// Dieses Dokument hat jetzt keine zusammengesetzten untergeordneten Knoten, denen wir Inhalte hinzufügen können.
// Wenn wir es bearbeiten möchten, müssen wir seine Knotensammlung neu füllen.
// Erstellen Sie zuerst einen neuen Abschnitt und hängen Sie ihn dann als untergeordnetes Element an den Stammdokumentknoten an.
Section section = new Section(doc);
doc.AppendChild(section);

// Legen Sie einige Seiteneinrichtungseigenschaften für den Abschnitt fest.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Ein Abschnitt benötigt einen Körper, der seinen gesamten Inhalt enthält und anzeigt
// auf der Seite zwischen Kopf- und Fußzeile des Abschnitts.
Body body = new Body(doc);
section.AppendChild(body);

// Erstellen Sie einen Absatz, legen Sie einige Formatierungseigenschaften fest und hängen Sie ihn dann als untergeordnetes Element an den Textkörper an.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Fügen Sie schließlich etwas Inhalt hinzu, um das Dokument zu erstellen. Erstellen Sie einen Lauf,
// Aussehen und Inhalt festlegen und dann als untergeordnetes Element an den Absatz anhängen.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Siehe auch

* class [CompositeNode](../compositenode/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


