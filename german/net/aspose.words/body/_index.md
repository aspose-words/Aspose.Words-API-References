---
title: Class Body
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Body klas. Stellt einen Container für den Haupttext eines Abschnitts dar.
type: docs
weight: 30
url: /de/net/aspose.words/body/
---
## Body class

Stellt einen Container für den Haupttext eines Abschnitts dar.

Um mehr zu erfahren, besuchen Sie die[Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) Dokumentationsartikel.

```csharp
public class Body : Story
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [Body](body/)(DocumentBase) | Initialisiert eine neue Instanz von`Body` Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ruft die Anzahl der unmittelbaren Kinder dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FirstParagraph](../../aspose.words/story/firstparagraph/) { get; } | Ruft den ersten Absatz in der Geschichte ab. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Gibt zurück`WAHR` wenn dieser Knoten untergeordnete Knoten hat. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Gibt zurück`WAHR` da dieser Knoten untergeordnete Knoten haben kann. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [LastParagraph](../../aspose.words/story/lastparagraph/) { get; } | Ruft den letzten Absatz in der Geschichte ab. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words/body/nodetype/) { get; } | Gibt zurückBody . |
| [Paragraphs](../../aspose.words/story/paragraphs/) { get; } | Ruft eine Sammlung von Absätzen ab, die unmittelbar untergeordnete Elemente der Geschichte sind. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft das unmittelbare übergeordnete Element dieses Knotens ab. |
| [ParentSection](../../aspose.words/body/parentsection/) { get; } | Ruft den übergeordneten Abschnitt dieser Story ab. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar vorangeht. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt a zurück[`Range`](../range/) Objekt, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [StoryType](../../aspose.words/story/storytype/) { get; } | Ruft den Typ dieser Geschichte ab. |
| [Tables](../../aspose.words/story/tables/) { get; } | Ruft eine Sammlung von Tabellen ab, die unmittelbar untergeordnete Elemente der Story sind. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words/body/accept/)(DocumentVisitor) | Akzeptiert einen Besucher. |
| override [AcceptEnd](../../aspose.words/body/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words/body/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [AppendParagraph](../../aspose.words/story/appendparagraph/)(string) | Eine Verknüpfungsmethode, die eine erstellt[`Paragraph`](../paragraph/) Objekt mit optionalem Text und hängt ihn am Ende dieses Objekts an. |
| [Clone](../../aspose.words/node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Erstellt einen Navigator, der zum Durchlaufen und Lesen von Knoten verwendet werden kann. |
| [DeleteShapes](../../aspose.words/story/deleteshapes/)() | Löscht alle Formen aus dem Text dieser Geschichte. |
| [EnsureMinimum](../../aspose.words/body/ensureminimum/)() | Wenn das letzte untergeordnete Element kein Absatz ist, wird ein leerer Absatz erstellt und angehängt. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Ruft den ersten Vorfahren des angegebenen ab[`NodeType`](../nodetype/) . |
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
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Entfernt alle[`SmartTag`](../../aspose.words.markup/smarttag/)Nachkommenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Wählt den ersten aus[`Node`](../node/) das entspricht dem XPath-Ausdruck. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exportiert den Inhalt des Knotens in einen String im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exportiert den Inhalt des Knotens mit den angegebenen Speicheroptionen in einen String. |

### Bemerkungen

`Body` enthalten kann[`Paragraph`](../paragraph/) Und[`Tisch`](../../aspose.words.tables/table/) untergeordnete Knoten.

`Body` ist ein Knoten auf Abschnittsebene und kann nur ein untergeordnetes Element von sein[`Section`](../section/) . Es kann nur einen geben`Body` in einem[`Section`](../section/).

Eine minimal gültige`Body` muss mindestens einen enthalten[`Paragraph`](../paragraph/).

### Beispiele

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

* class [Story](../story/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


