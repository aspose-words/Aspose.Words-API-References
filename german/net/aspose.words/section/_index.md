---
title: Class Section
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Section klas. Stellt einen einzelnen Abschnitt in einem Dokument dar.
type: docs
weight: 5730
url: /de/net/aspose.words/section/
---
## Section class

Stellt einen einzelnen Abschnitt in einem Dokument dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Abschnitten](https://docs.aspose.com/words/net/working-with-sections/) Dokumentationsartikel.

```csharp
public sealed class Section : CompositeNode
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [Section](section/)(DocumentBase) | Initialisiert eine neue Instanz der Section-Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Body](../../aspose.words/section/body/) { get; } | Gibt die zurück[`Body`](../body/) Unterknoten des Abschnitts. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ruft die Anzahl der unmittelbaren Kinder dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Gibt zurück`WAHR` wenn dieser Knoten untergeordnete Knoten hat. |
| [HeadersFooters](../../aspose.words/section/headersfooters/) { get; } | Bietet Zugriff auf die Kopf- und Fußzeilenknoten des Abschnitts. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Gibt zurück`WAHR` da dieser Knoten untergeordnete Knoten haben kann. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words/section/nodetype/) { get; } | Gibt zurückSection . |
| [PageSetup](../../aspose.words/section/pagesetup/) { get; } | Gibt ein Objekt zurück, das die Seiteneinrichtung und Abschnittseigenschaften darstellt. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft das unmittelbare übergeordnete Element dieses Knotens ab. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar vorangeht. |
| [ProtectedForForms](../../aspose.words/section/protectedforforms/) { get; set; } | True, wenn der Abschnitt für Formulare geschützt ist. Wenn ein Abschnitt für Formulare geschützt ist, können Benutzer Text nur in Formularfeldern in Microsoft Word auswählen und ändern. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt a zurück[`Range`](../range/) Objekt, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words/section/accept/)(DocumentVisitor) | Akzeptiert einen Besucher. |
| override [AcceptEnd](../../aspose.words/section/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words/section/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [AppendContent](../../aspose.words/section/appendcontent/)(Section) | Fügt am Ende dieses Abschnitts eine Kopie des Inhalts des Quellabschnitts ein. |
| [ClearContent](../../aspose.words/section/clearcontent/)() | Löscht den Abschnitt. |
| [ClearHeadersFooters](../../aspose.words/section/clearheadersfooters/)() | Löscht die Kopf- und Fußzeilen dieses Abschnitts. |
| [Clone](../../aspose.words/section/clone/#clone_1)() | Erstellt ein Duplikat dieses Abschnitts. |
| [Clone](../../aspose.words/node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Erstellt einen Navigator, der zum Durchlaufen und Lesen von Knoten verwendet werden kann. |
| [DeleteHeaderFooterShapes](../../aspose.words/section/deleteheaderfootershapes/)() | Löscht alle Formen (Zeichenobjekte) aus den Kopf- und Fußzeilen dieses Abschnitts. |
| [EnsureMinimum](../../aspose.words/section/ensureminimum/)() | Stellt sicher, dass der Abschnitt vorhanden ist[`Body`](./body/) mit einer[`Paragraph`](../paragraph/) . |
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
| [PrependContent](../../aspose.words/section/prependcontent/)(Section) | Fügt eine Kopie des Inhalts des Quellabschnitts am Anfang dieses Abschnitts ein. |
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

`Section` kann eins haben[`Body`](../body/) und maximal eins[`HeaderFooter`](../headerfooter/) von jedem[`HeaderFooterType`](../headerfootertype/) .[`Body`](../body/) Und[`HeaderFooter`](../headerfooter/) nodes kann in beliebiger Reihenfolge darin sein`Section`.

Es muss ein minimaler gültiger Abschnitt vorhanden sein[`Body`](../body/) mit einer[`Paragraph`](../paragraph/).

Jeder Abschnitt verfügt über einen eigenen Satz von Eigenschaften, die Seitengröße, Ausrichtung, Ränder usw. festlegen.

Mit können Sie eine Kopie eines Abschnitts erstellen[`Clone`](../node/clone/). Die Kopie kann in dasselbe oder ein anderes Dokument eingefügt werden.

Um einen ganzen Abschnitt einschließlich Abschnittswechsel und Abschnittseigenschaften hinzuzufügen, einzufügen oder zu entfernen, verwenden Sie Methoden von[`Sections`](../document/sections/) Objekt.

Um nur den Inhalt des Abschnitts zu kopieren und einzufügen, mit Ausnahme des Abschnitts break und der Abschnittseigenschaften, verwenden Sie[`AppendContent`](./appendcontent/) Und[`PrependContent`](./prependcontent/) Methoden.

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

* class [CompositeNode](../compositenode/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


