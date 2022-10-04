---
title: Section
second_title: Aspose.Words für .NET-API-Referenz
description: Stellt einen einzelnen Abschnitt in einem Dokument dar.
type: docs
weight: 5440
url: /de/net/aspose.words/section/
---
## Section class

Stellt einen einzelnen Abschnitt in einem Dokument dar.

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
| [Body](../../aspose.words/section/body/) { get; } | Gibt die zurück **Körper** untergeordneter Knoten des Abschnitts. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Ruft alle unmittelbar untergeordneten Knoten dieses Knotens ab. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ruft die Anzahl der unmittelbaren Kinder dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Gibt wahr zurück, wenn dieser Knoten untergeordnete Knoten hat. |
| [HeadersFooters](../../aspose.words/section/headersfooters/) { get; } | Bietet Zugriff auf die Kopf- und Fußzeilenknoten des Abschnitts. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Gibt wahr zurück, da dieser Knoten untergeordnete Knoten haben kann. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words/section/nodetype/) { get; } | gibt zurück **NodeType.Section** . |
| [PageSetup](../../aspose.words/section/pagesetup/) { get; } | Gibt ein Objekt zurück, das Seiteneinrichtung und Abschnittseigenschaften darstellt. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten unmittelbar vor diesem Knoten ab. |
| [ProtectedForForms](../../aspose.words/section/protectedforforms/) { get; set; } | True, wenn der Abschnitt für Formulare geschützt ist. Wenn ein Abschnitt für Formulare geschützt ist, können Benutzer Text nur in Formularfeldern in Microsoft Word auswählen und ändern. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt a zurück **Bereich** Objekt, das den Teil eines Dokuments darstellt, das in diesem Knoten enthalten ist. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words/section/accept/)(DocumentVisitor) | Akzeptiert einen Besucher. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [AppendContent](../../aspose.words/section/appendcontent/)(Section) | Fügt eine Kopie des Inhalts des Quellabschnitts am Ende dieses Abschnitts ein. |
| [ClearContent](../../aspose.words/section/clearcontent/)() | Löscht den Abschnitt. |
| [ClearHeadersFooters](../../aspose.words/section/clearheadersfooters/)() | Löscht die Kopf- und Fußzeilen dieses Abschnitts. |
| [Clone](../../aspose.words/section/clone/#clone_1)() | Erstellt ein Duplikat dieses Abschnitts. |
| [Clone](../../aspose.words/node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Reserviert für Systemnutzung. IXPfadNavigierbar. |
| [DeleteHeaderFooterShapes](../../aspose.words/section/deleteheaderfootershapes/)() | Löscht alle Formen (Zeichnungsobjekte) aus den Kopf- und Fußzeilen dieses Abschnitts. |
| [EnsureMinimum](../../aspose.words/section/ensureminimum/)() | Stellt sicher, dass der Abschnitt einen Hauptteil mit einem Absatz hat. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Ruft den ersten Vorfahren der angegebenen ab[`NodeType`](../nodetype/) . |
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
| [PrependContent](../../aspose.words/section/prependcontent/)(Section) | Fügt eine Kopie des Inhalts des Quellabschnitts am Anfang dieses Abschnitts ein. |
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

**Abschnitt** kann einen haben[`Body`](./body/) und maximal eins[`HeaderFooter`](../headerfooter/) von jedem[`HeaderFooterType`](../headerfootertype/) . **Körper** und **Kopfzeile Fußzeile** nodes kann sich in beliebiger Reihenfolge darin befinden **Abschnitt**.

Ein gültiger Mindestabschnitt muss vorhanden sein **Körper** mit einer **Absatz**.

Jeder Abschnitt hat seine eigenen Eigenschaften, die Seitengröße, Ausrichtung, Ränder usw. angeben.

Mit können Sie eine Kopie eines Abschnitts erstellen[`Clone`](../node/clone/). Die Kopie kann in dasselbe oder ein anderes Dokument eingefügt werden.

Um einen ganzen Abschnitt einschließlich Abschnittsumbruch und Abschnittseigenschaften hinzuzufügen, einzufügen oder zu entfernen, verwenden Sie die Methoden von **Abschnitte** Objekt.

Um nur den Inhalt des Abschnitts zu kopieren und einzufügen, verwenden Sie nicht den Abschnitt break und die Abschnittseigenschaften **Inhalt anhängen** und **PrependContent**Methoden.

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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
