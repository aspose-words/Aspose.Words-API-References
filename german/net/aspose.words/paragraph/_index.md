---
title: Paragraph Class
linktitle: Paragraph
articleTitle: Paragraph
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Paragraph, um Textabsätze mühelos zu verwalten und zu formatieren und so Ihre Dokumentverarbeitungsfunktionen zu verbessern.
type: docs
weight: 5120
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
| [Paragraph](paragraph/)(*[DocumentBase](../documentbase/)*) | Initialisiert eine neue Instanz des`Paragraph` Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BreakIsStyleSeparator](../../aspose.words/paragraph/breakisstyleseparator/) { get; } | Wahr, wenn dieser Absatzumbruch ein Stiltrennzeichen ist. Ein Stiltrennzeichen ermöglicht es, dass ein Absatz aus Teilen mit unterschiedlichen Absatzstilen besteht. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ruft die Anzahl der unmittelbar untergeordneten Elemente dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FrameFormat](../../aspose.words/paragraph/frameformat/) { get; } | Bietet Zugriff auf die Frame-Formatierungseigenschaften. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Rückgaben`WAHR` wenn dieser Knoten untergeordnete Knoten hat. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Rückgaben`WAHR` da dieser Knoten untergeordnete Knoten haben kann. |
| [IsDeleteRevision](../../aspose.words/paragraph/isdeleterevision/) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war. |
| [IsEndOfCell](../../aspose.words/paragraph/isendofcell/) { get; } | Wahr, wenn dieser Absatz der letzte Absatz in einem[`Cell`](../../aspose.words.tables/cell/) ; andernfalls false. |
| [IsEndOfDocument](../../aspose.words/paragraph/isendofdocument/) { get; } | Wahr, wenn dieser Absatz der letzte Absatz im letzten Abschnitt des Dokuments ist. |
| [IsEndOfHeaderFooter](../../aspose.words/paragraph/isendofheaderfooter/) { get; } | Wahr, wenn dieser Absatz der letzte Absatz in der[`HeaderFooter`](../headerfooter/) (Haupttextgeschichte) eines[`Section`](../section/) ; andernfalls false. |
| [IsEndOfSection](../../aspose.words/paragraph/isendofsection/) { get; } | Wahr, wenn dieser Absatz der letzte Absatz in der[`Body`](../body/) (Haupttextgeschichte) eines[`Section`](../section/) ; andernfalls false. |
| [IsFormatRevision](../../aspose.words/paragraph/isformatrevision/) { get; } | Gibt „true“ zurück, wenn die Formatierung des Objekts in Microsoft Word geändert wurde, während die Änderungsverfolgung aktiviert war. |
| [IsInCell](../../aspose.words/paragraph/isincell/) { get; } | Wahr, wenn dieser Absatz ein unmittelbares Kind von[`Cell`](../../aspose.words.tables/cell/) ; andernfalls false. |
| [IsInsertRevision](../../aspose.words/paragraph/isinsertrevision/) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war. |
| [IsListItem](../../aspose.words/paragraph/islistitem/) { get; } | Wahr, wenn der Absatz ein Element in einer Aufzählungs- oder nummerierten Liste in der Originalrevision ist. |
| [IsMoveFromRevision](../../aspose.words/paragraph/ismovefromrevision/) { get; } | Rückgaben`WAHR` wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsverfolgung aktiviert war. |
| [IsMoveToRevision](../../aspose.words/paragraph/ismovetorevision/) { get; } | Rückgaben`WAHR` wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung aktiviert war. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [ListFormat](../../aspose.words/paragraph/listformat/) { get; } | Bietet Zugriff auf die Listenformatierungseigenschaften des Absatzes. |
| [ListLabel](../../aspose.words/paragraph/listlabel/) { get; } | Erhält eine[`ListLabel`](./listlabel/)Objekt, das Zugriff auf den Listennummerierungswert und die Formatierung für diesen Absatz bietet. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words/paragraph/nodetype/) { get; } | RückgabenParagraph . |
| [ParagraphBreakFont](../../aspose.words/paragraph/paragraphbreakfont/) { get; } | Bietet Zugriff auf die Schriftformatierung des Absatzumbruchzeichens. |
| [ParagraphFormat](../../aspose.words/paragraph/paragraphformat/) { get; } | Bietet Zugriff auf die Absatzformatierungseigenschaften. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [ParentSection](../../aspose.words/paragraph/parentsection/) { get; } | Ruft das übergeordnete Element ab[`Section`](../section/) des Absatzes. |
| [ParentStory](../../aspose.words/paragraph/parentstory/) { get; } | Ruft die übergeordnete Story auf Abschnittsebene ab, die[`Body`](../body/) oder[`HeaderFooter`](../headerfooter/) . |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar vorausgeht. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt einen[`Range`](../range/)Objekt, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [Runs](../../aspose.words/paragraph/runs/) { get; } | Bietet Zugriff auf die eingegebene Sammlung von Textteilen innerhalb des Absatzes. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words/paragraph/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Nimmt einen Besucher auf. |
| override [AcceptEnd](../../aspose.words/paragraph/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Akzeptiert einen Besucher, der das Ende des Absatzes des Dokuments besucht. |
| override [AcceptStart](../../aspose.words/paragraph/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Akzeptiert einen Besucher, der den Anfang des Absatzes des Dokuments besucht. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_1)(*string*) | Fügt diesem Absatz ein Feld hinzu. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool*) | Fügt diesem Absatz ein Feld hinzu. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_2)(*string, string*) | Fügt diesem Absatz ein Feld hinzu. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Erstellt einen Navigator, der zum Durchlaufen und Lesen von Knoten verwendet werden kann. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Ruft den ersten Vorfahren des angegebenen[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ruft den ersten Vorgänger des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Gibt eine Live-Sammlung von untergeordneten Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEffectiveTabStops](../../aspose.words/paragraph/geteffectivetabstops/)() | Gibt ein Array aller Tabstopps zurück, die auf diesen Absatz angewendet wurden, einschließlich derer, die indirekt durch Stile oder Listen angewendet wurden. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bietet Unterstützung für die Iteration des For-Each-Stils über die untergeordneten Knoten dieses Knotens. |
| override [GetText](../../aspose.words/paragraph/gettext/)() | Ruft den Text dieses Absatzes einschließlich des Absatzendezeichens ab. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knoten-Array zurück. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_1)(*string, [Node](../node/), bool*) | Fügt ein Feld in diesen Absatz ein. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool, [Node](../node/), bool*) | Fügt ein Feld in diesen Absatz ein. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_2)(*string, string, [Node](../node/), bool*) | Fügt ein Feld in diesen Absatz ein. |
| [JoinRunsWithSameFormatting](../../aspose.words/paragraph/joinrunswithsameformatting/)() | Verbindet Textläufe mit gleicher Formatierung im Absatz. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Ruft den nächsten Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Fügt den angegebenen Knoten am Anfang der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Ruft den vorherigen Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Entfernt alle untergeordneten Knoten des aktuellen Knotens. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Entfernt den angegebenen untergeordneten Knoten. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Entfernt alle[`SmartTag`](../../aspose.words.markup/smarttag/) Nachkommenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Wählt den ersten[`Node`](../node/) das dem XPath-Ausdruck entspricht. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exportiert den Inhalt des Knotens in eine Zeichenfolge im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in eine Zeichenfolge. |

## Bemerkungen

`Paragraph` ist ein Knoten auf Blockebene und kann ein untergeordnetes Element von Klassen sein, die von abgeleitet sind.[`Story`](../story/) oder[`InlineStory`](../inlinestory/).

`Paragraph` kann eine beliebige Anzahl von Knoten und Lesezeichen auf Inline-Ebene enthalten.

Die vollständige Liste der untergeordneten Knoten, die innerhalb eines Absatzes auftreten können, besteht aus [`BookmarkStart`](../bookmarkstart/) ,[`BookmarkEnd`](../bookmarkend/) , [`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) , [`FieldEnd`](../../aspose.words.fields/fieldend/) ,[`FormField`](../../aspose.words.fields/formfield/) , [`Comment`](../comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) , [`Run`](../run/) ,[`SpecialChar`](../specialchar/) , [`Shape`](../../aspose.words.drawing/shape/) ,[`GroupShape`](../../aspose.words.drawing/groupshape/) , [`SmartTag`](../../aspose.words.markup/smarttag/).

Ein gültiger Absatz in Microsoft Word endet immer mit einem Absatzumbruchzeichen und ein minimal gültiger Absatz besteht nur aus einem Absatzumbruch. Die`Paragraph` Die Klasse fügt automatisch das entsprechende Absatzumbruchzeichen am Ende an und dieses Zeichen ist nicht Teil der untergeordneten Knoten der`Paragraph` , daher a`Paragraph` kann leer sein.

Schließen Sie das Ende des Absatzes nicht ein[`ParagraphBreak`](../controlchar/paragraphbreak/) oder Ende der Zelle[`Cell`](../controlchar/cell/) Zeichen im Text von des Absatzes, da dies den Absatz ungültig machen könnte, wenn das Dokument in Microsoft Word geöffnet wird.

## Beispiele

Zeigt, wie man ein Aspose.Words-Dokument manuell erstellt.

```csharp
Document doc = new Document();

// Ein leeres Dokument enthält einen Abschnitt, einen Hauptteil und einen Absatz.
// Rufen Sie die Methode „RemoveAllChildren“ auf, um alle diese Knoten zu entfernen.
// und am Ende einen Dokumentknoten ohne untergeordnete Elemente erhalten.
doc.RemoveAllChildren();

// Dieses Dokument hat jetzt keine zusammengesetzten untergeordneten Knoten, denen wir Inhalte hinzufügen können.
// Wenn wir es bearbeiten möchten, müssen wir seine Knotensammlung neu füllen.
// Erstellen Sie zuerst einen neuen Abschnitt und hängen Sie ihn dann als untergeordnetes Element an den Stammdokumentknoten an.
Section section = new Section(doc);
doc.AppendChild(section);

// Legen Sie einige Seiteneinrichtungseigenschaften für den Abschnitt fest.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Ein Abschnitt benötigt einen Hauptteil, der seinen gesamten Inhalt enthält und anzeigt
// auf der Seite zwischen Kopf- und Fußzeile des Abschnitts.
Body body = new Body(doc);
section.AppendChild(body);

// Erstellen Sie einen Absatz, legen Sie einige Formatierungseigenschaften fest und hängen Sie ihn dann als untergeordnetes Element an den Textkörper an.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Abschließend fügen Sie dem Dokument noch Inhalt hinzu. Erstellen Sie einen Lauf,
// Legen Sie das Erscheinungsbild und den Inhalt fest und hängen Sie es dann als untergeordnetes Element an den Absatz an.
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
