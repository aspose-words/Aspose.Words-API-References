---
title: Body Class
linktitle: Body
articleTitle: Body
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Body, Ihr unverzichtbares Tool zum mühelosen Verwalten von Abschnittstexten und zur Verbesserung der Effizienz der Dokumentverarbeitung.
type: docs
weight: 220
url: /de/net/aspose.words/body/
---
## Body class

Stellt einen Container für den Haupttext eines Abschnitts dar.

Um mehr zu erfahren, besuchen Sie die[Aspose.Words Dokumentobjektmodell (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) Dokumentationsartikel.

```csharp
public class Body : Story
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [Body](body/)(*[DocumentBase](../documentbase/)*) | Initialisiert eine neue Instanz des`Body` Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ruft die Anzahl der unmittelbar untergeordneten Elemente dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FirstParagraph](../../aspose.words/story/firstparagraph/) { get; } | Ruft den ersten Absatz der Geschichte ab. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Rückgaben`WAHR` wenn dieser Knoten untergeordnete Knoten hat. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Rückgaben`WAHR` da dieser Knoten untergeordnete Knoten haben kann. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [LastParagraph](../../aspose.words/story/lastparagraph/) { get; } | Ruft den letzten Absatz der Geschichte ab. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words/body/nodetype/) { get; } | RückgabenBody . |
| [Paragraphs](../../aspose.words/story/paragraphs/) { get; } | Ruft eine Sammlung von Absätzen ab, die unmittelbare untergeordnete Elemente der Story sind. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [ParentSection](../../aspose.words/body/parentsection/) { get; } | Ruft den übergeordneten Abschnitt dieser Story ab. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar vorausgeht. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt einen[`Range`](../range/)Objekt, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [StoryType](../../aspose.words/story/storytype/) { get; } | Ruft den Typ dieser Story ab. |
| [Tables](../../aspose.words/story/tables/) { get; } | Ruft eine Sammlung von Tabellen ab, die unmittelbare untergeordnete Elemente der Story sind. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words/body/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Nimmt einen Besucher auf. |
| override [AcceptEnd](../../aspose.words/body/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Akzeptiert einen Besucher zum Aufrufen des Endes des Dokumenttexts. |
| override [AcceptStart](../../aspose.words/body/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Akzeptiert einen Besucher, der den Anfang des Dokumenttexts besucht. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [AppendParagraph](../../aspose.words/story/appendparagraph/)(*string*) | Eine Abkürzungsmethode, die eine[`Paragraph`](../paragraph/) Objekt mit optionalem Text und hängt ihn an das Ende dieses Objekts an. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Erstellt einen Navigator, der zum Durchlaufen und Lesen von Knoten verwendet werden kann. |
| [DeleteShapes](../../aspose.words/story/deleteshapes/)() | Löscht alle Formen aus dem Text dieser Geschichte. |
| [EnsureMinimum](../../aspose.words/body/ensureminimum/)() | Wenn das letzte untergeordnete Element kein Absatz ist, wird ein leerer Absatz erstellt und angehängt. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Ruft den ersten Vorfahren des angegebenen[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ruft den ersten Vorgänger des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Gibt eine Live-Sammlung von untergeordneten Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bietet Unterstützung für die Iteration des For-Each-Stils über die untergeordneten Knoten dieses Knotens. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ruft den Text dieses Knotens und aller seiner untergeordneten Knoten ab. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knoten-Array zurück. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein. |
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

`Body` kann enthalten[`Paragraph`](../paragraph/) Und[`Tisch`](../../aspose.words.tables/table/) untergeordnete Knoten.

`Body` ist ein Knoten auf Abschnittsebene und kann nur ein untergeordnetes Element von[`Section`](../section/) . Es kann nur einen geben`Body` in einem[`Section`](../section/).

Eine minimal gültige`Body` muss mindestens eine enthalten[`Paragraph`](../paragraph/).

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

* class [Story](../story/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
