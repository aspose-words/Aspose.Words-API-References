---
title: Paragraph Class
linktitle: Paragraph
articleTitle: Paragraph
second_title: Aspose.Words für .NET
description: Aspose.Words.Paragraph klas. Stellt einen Textabsatz dar in C#.
type: docs
weight: 4390
url: /de/net/aspose.words/paragraph/
---
## Paragraph class

Stellt einen Textabsatz dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Absätzen](https://docs.aspose.com/words/net/working-with-paragraphs/) Dokumentationsartikel.

```csharp
public class Paragraph : CompositeNode
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [Paragraph](paragraph/)(*[DocumentBase](../documentbase/)*) | Initialisiert eine neue Instanz von`Paragraph` Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BreakIsStyleSeparator](../../aspose.words/paragraph/breakisstyleseparator/) { get; } | True, wenn dieser Absatzumbruch ein Stiltrennzeichen ist. Ein Stiltrennzeichen ermöglicht, dass ein Absatz aus Teilen mit unterschiedlichen Absatzstilen bestehen kann. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ruft die Anzahl der unmittelbaren Kinder dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FrameFormat](../../aspose.words/paragraph/frameformat/) { get; } | Bietet Zugriff auf die Frame-Formatierungseigenschaften. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Gibt zurück`WAHR` wenn dieser Knoten untergeordnete Knoten hat. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Gibt zurück`WAHR` da dieser Knoten untergeordnete Knoten haben kann. |
| [IsDeleteRevision](../../aspose.words/paragraph/isdeleterevision/) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war. |
| [IsEndOfCell](../../aspose.words/paragraph/isendofcell/) { get; } | True, wenn dieser Absatz der letzte Absatz in a ist[`Cell`](../../aspose.words.tables/cell/) ; sonst falsch. |
| [IsEndOfDocument](../../aspose.words/paragraph/isendofdocument/) { get; } | True, wenn dieser Absatz der letzte Absatz im letzten Abschnitt des Dokuments ist. |
| [IsEndOfHeaderFooter](../../aspose.words/paragraph/isendofheaderfooter/) { get; } | True, wenn dieser Absatz der letzte Absatz im ist[`HeaderFooter`](../headerfooter/) (Haupttextgeschichte) von a[`Section`](../section/) ; sonst falsch. |
| [IsEndOfSection](../../aspose.words/paragraph/isendofsection/) { get; } | True, wenn dieser Absatz der letzte Absatz im ist[`Body`](../body/) (Haupttextgeschichte) von a[`Section`](../section/) ; sonst falsch. |
| [IsFormatRevision](../../aspose.words/paragraph/isformatrevision/) { get; } | Gibt „true“ zurück, wenn die Formatierung des Objekts in Microsoft Word geändert wurde, während die Änderungsverfolgung aktiviert war. |
| [IsInCell](../../aspose.words/paragraph/isincell/) { get; } | True, wenn dieser Absatz ein unmittelbares untergeordnetes Element von ist[`Cell`](../../aspose.words.tables/cell/) ; sonst falsch. |
| [IsInsertRevision](../../aspose.words/paragraph/isinsertrevision/) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war. |
| [IsListItem](../../aspose.words/paragraph/islistitem/) { get; } | True, wenn der Absatz ein Element in einer Liste mit Aufzählungszeichen oder Nummern in der Originalrevision ist. |
| [IsMoveFromRevision](../../aspose.words/paragraph/ismovefromrevision/) { get; } | Gibt zurück`WAHR` wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsverfolgung aktiviert war. |
| [IsMoveToRevision](../../aspose.words/paragraph/ismovetorevision/) { get; } | Gibt zurück`WAHR` wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung aktiviert war. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [ListFormat](../../aspose.words/paragraph/listformat/) { get; } | Bietet Zugriff auf die Listenformatierungseigenschaften des Absatzes. |
| [ListLabel](../../aspose.words/paragraph/listlabel/) { get; } | Ruft a ab[`ListLabel`](./listlabel/)Objekt, das Zugriff auf den Listennummerierungswert und die Formatierung für diesen Absatz bietet. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words/paragraph/nodetype/) { get; } | Gibt zurückParagraph . |
| [ParagraphBreakFont](../../aspose.words/paragraph/paragraphbreakfont/) { get; } | Bietet Zugriff auf die Schriftartformatierung des Absatzumbruchzeichens. |
| [ParagraphFormat](../../aspose.words/paragraph/paragraphformat/) { get; } | Bietet Zugriff auf die Absatzformatierungseigenschaften. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft das unmittelbare übergeordnete Element dieses Knotens ab. |
| [ParentSection](../../aspose.words/paragraph/parentsection/) { get; } | Ruft das übergeordnete Element ab[`Section`](../section/) des Absatzes. |
| [ParentStory](../../aspose.words/paragraph/parentstory/) { get; } | Ruft die übergeordnete Story auf Abschnittsebene ab, die sein kann[`Body`](../body/) oder[`HeaderFooter`](../headerfooter/) . |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar vorangeht. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt a zurück[`Range`](../range/) Objekt, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [Runs](../../aspose.words/paragraph/runs/) { get; } | Bietet Zugriff auf die eingegebene Sammlung von Textteilen im Absatz. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words/paragraph/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Akzeptiert einen Besucher. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../node/)*) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_1)(*string*) | Fügt ein Feld an diesen Absatz an. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool*) | Fügt ein Feld an diesen Absatz an. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_2)(*string, string*) | Fügt ein Feld an diesen Absatz an. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Erstellt einen Navigator, der zum Durchlaufen und Lesen von Knoten verwendet werden kann. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Ruft den ersten Vorfahren des angegebenen ab[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Gibt eine Live-Sammlung untergeordneter Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEffectiveTabStops](../../aspose.words/paragraph/geteffectivetabstops/)() | Gibt ein Array aller Tabstopps zurück, die auf diesen Absatz angewendet werden, einschließlich indirekter Tabstopps durch Stile oder Listen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bietet Unterstützung für die Iteration jedes Stils über die untergeordneten Knoten dieses Knotens. |
| override [GetText](../../aspose.words/paragraph/gettext/)() | Ruft den Text dieses Absatzes einschließlich des Absatzendezeichens ab. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knoten-Array zurück. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../node/), [Node](../node/)*) | Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../node/), [Node](../node/)*) | Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_1)(*string, [Node](../node/), bool*) | Fügt ein Feld in diesen Absatz ein. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool, [Node](../node/), bool*) | Fügt ein Feld in diesen Absatz ein. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_2)(*string, string, [Node](../node/), bool*) | Fügt ein Feld in diesen Absatz ein. |
| [JoinRunsWithSameFormatting](../../aspose.words/paragraph/joinrunswithsameformatting/)() | Joins werden mit der gleichen Formatierung im Absatz ausgeführt. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Ruft den nächsten Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../node/)*) | Fügt den angegebenen Knoten am Anfang der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Ruft den vorherigen Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Entfernt alle untergeordneten Knoten des aktuellen Knotens. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../node/)*) | Entfernt den angegebenen untergeordneten Knoten. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Entfernt alle[`SmartTag`](../../aspose.words.markup/smarttag/)Nachkommenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Wählt den ersten aus[`Node`](../node/) das entspricht dem XPath-Ausdruck. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exportiert den Inhalt des Knotens in einen String im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exportiert den Inhalt des Knotens mit den angegebenen Speicheroptionen in einen String. |

## Bemerkungen

`Paragraph` ist ein Knoten auf Blockebene und kann ein untergeordnetes Element von Klassen sein, die von abgeleitet sind.[`Story`](../story/) oder[`InlineStory`](../inlinestory/).

`Paragraph` kann eine beliebige Anzahl von Knoten und Lesezeichen auf Inline-Ebene enthalten.

Die vollständige Liste der untergeordneten Knoten, die innerhalb eines Absatzes vorkommen können, besteht aus [`BookmarkStart`](../bookmarkstart/) ,[`BookmarkEnd`](../bookmarkend/) , [`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) , [`FieldEnd`](../../aspose.words.fields/fieldend/) ,[`FormField`](../../aspose.words.fields/formfield/) , [`Comment`](../comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) , [`Run`](../run/) ,[`SpecialChar`](../specialchar/) , [`Shape`](../../aspose.words.drawing/shape/) ,[`GroupShape`](../../aspose.words.drawing/groupshape/) , [`SmartTag`](../../aspose.words.markup/smarttag/).

Ein gültiger Absatz in Microsoft Word endet immer mit einem Absatzumbruchzeichen und ein minimaler gültiger Absatz besteht nur aus einem Absatzumbruch. Der`Paragraph` Die Klasse hängt automatisch das entsprechende Absatzumbruchzeichen am Ende an und dieses Zeichen ist nicht Teil der untergeordneten Knoten der Klasse`Paragraph` , also a`Paragraph` kann leer sein.

Fügen Sie das Ende des Absatzes nicht ein[`ParagraphBreak`](../controlchar/paragraphbreak/) oder Ende der Zelle[`Cell`](../controlchar/cell/) Zeichen im Text von des Absatzes, da der Absatz dadurch möglicherweise ungültig wird, wenn das Dokument in Microsoft Word geöffnet wird.

## Beispiele

Zeigt, wie man ein Aspose.Words-Dokument manuell erstellt.

```csharp
Document doc = new Document();

// Ein leeres Dokument enthält einen Abschnitt, einen Hauptteil und einen Absatz.
// Rufen Sie die Methode „RemoveAllChildren“ auf, um alle diese Knoten zu entfernen.
// und erhalten am Ende einen Dokumentknoten ohne untergeordnete Elemente.
doc.RemoveAllChildren();

// Dieses Dokument hat jetzt keine zusammengesetzten untergeordneten Knoten, denen wir Inhalte hinzufügen können.
// Wenn wir es bearbeiten möchten, müssen wir seine Knotensammlung neu füllen.
// Erstellen Sie zunächst einen neuen Abschnitt und hängen Sie ihn dann als untergeordnetes Element an den Stammdokumentknoten an.
Section section = new Section(doc);
doc.AppendChild(section);

// Legen Sie einige Seiteneinrichtungseigenschaften für den Abschnitt fest.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Ein Abschnitt benötigt einen Hauptteil, der seinen gesamten Inhalt enthält und anzeigt
// auf der Seite zwischen Kopf- und Fußzeile des Abschnitts.
Body body = new Body(doc);
section.AppendChild(body);

// Einen Absatz erstellen, einige Formatierungseigenschaften festlegen und ihn dann als untergeordnetes Element an den Text anhängen.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Zum Schluss fügen Sie etwas Inhalt hinzu, um das Dokument zu erstellen. Erstellen Sie einen Lauf,
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
