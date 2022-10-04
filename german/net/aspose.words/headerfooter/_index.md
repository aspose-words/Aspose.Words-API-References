---
title: HeaderFooter
second_title: Aspose.Words für .NET-API-Referenz
description: Repräsentiert einen Container für den Kopf oder Fußzeilentext eines Abschnitts.
type: docs
weight: 2920
url: /de/net/aspose.words/headerfooter/
---
## HeaderFooter class

Repräsentiert einen Container für den Kopf- oder Fußzeilentext eines Abschnitts.

```csharp
public class HeaderFooter : Story
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [HeaderFooter](headerfooter/)(DocumentBase, HeaderFooterType) | Erstellt eine neue Kopf- oder Fußzeile des angegebenen Typs. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Ruft alle unmittelbar untergeordneten Knoten dieses Knotens ab. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ruft die Anzahl der unmittelbaren Kinder dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FirstParagraph](../../aspose.words/story/firstparagraph/) { get; } | Ruft den ersten Absatz in der Geschichte ab. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Gibt wahr zurück, wenn dieser Knoten untergeordnete Knoten hat. |
| [HeaderFooterType](../../aspose.words/headerfooter/headerfootertype/) { get; } | Ruft den Typ dieser Kopf-/Fußzeile ab. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Gibt wahr zurück, da dieser Knoten untergeordnete Knoten haben kann. |
| [IsHeader](../../aspose.words/headerfooter/isheader/) { get; } | Wahr, wenn dies der Fall ist **Kopfzeile Fußzeile** Objekt ist ein Header. |
| [IsLinkedToPrevious](../../aspose.words/headerfooter/islinkedtoprevious/) { get; set; } | Wahr, wenn diese Kopf- oder Fußzeile mit der entsprechenden Kopf- oder Fußzeile im vorherigen Abschnitt verknüpft ist. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [LastParagraph](../../aspose.words/story/lastparagraph/) { get; } | Ruft den letzten Absatz in der Story ab. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words/headerfooter/nodetype/) { get; } | gibt zurück **NodeType.HeaderFooter** . |
| [Paragraphs](../../aspose.words/story/paragraphs/) { get; } | Ruft eine Sammlung von Absätzen ab, die der Geschichte direkt untergeordnet sind. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [ParentSection](../../aspose.words/headerfooter/parentsection/) { get; } | Ruft den übergeordneten Abschnitt dieser Story ab. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten unmittelbar vor diesem Knoten ab. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt a zurück **Bereich** Objekt, das den Teil eines Dokuments darstellt, das in diesem Knoten enthalten ist. |
| [StoryType](../../aspose.words/story/storytype/) { get; } | Ruft den Typ dieser Geschichte ab. |
| [Tables](../../aspose.words/story/tables/) { get; } | Ruft eine Sammlung von Tabellen ab, die unmittelbar untergeordnete Elemente der Story sind. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words/headerfooter/accept/)(DocumentVisitor) | Akzeptiert einen Besucher. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [AppendParagraph](../../aspose.words/story/appendparagraph/)(string) | Eine Shortcut-Methode, die a erstellt[`Paragraph`](../paragraph/) Objekt mit optionalem Text und fügt ihn an das Ende dieses Objekts an. |
| [Clone](../../aspose.words/node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Reserviert für Systemnutzung. IXPfadNavigierbar. |
| [DeleteShapes](../../aspose.words/story/deleteshapes/)() | Löscht alle Formen aus dem Text dieser Geschichte. |
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

**Kopfzeile Fußzeile** enthalten kann **Absatz** und **Tisch** untergeordnete Knoten.

**Kopfzeile Fußzeile** ist ein Knoten auf Abschnittsebene und kann nur ein Kind von sein **Abschnitt** . Es kann nur einen geben **Kopfzeile Fußzeile** oder jeder[`HeaderFooterType`](./headerfootertype/) in einem **Abschnitt**.

Wenn **Abschnitt** hat kein **Kopfzeile Fußzeile** eines bestimmten Typs oder der **Kopfzeile Fußzeile** keine untergeordneten Knoten hat, wird diese Kopf-/Fußzeile als mit der Kopf-/Fußzeile desselben Typs des vorherigen Abschnitts in Microsoft Word verknüpft betrachtet.

Wann **Kopfzeile Fußzeile** enthält mindestens eine **Absatz**, wird es in Microsoft Word nicht mehr als mit dem vorherigen verknüpft betrachtet.

### Beispiele

Zeigt, wie Text in der Fußzeile eines Dokuments ersetzt wird.

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

Zeigt, wie alle Fußzeilen aus einem Dokument gelöscht werden.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Jeden Abschnitt durchlaufen und Fußzeilen aller Art entfernen.
foreach (Section section in doc.OfType<Section>())
{
    // Es gibt drei Arten von Fußzeilen- und Kopfzeilentypen.
    // 1 - Die "erste" Kopf-/Fußzeile, die nur auf der ersten Seite eines Abschnitts erscheint.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 - Die "primäre" Kopf-/Fußzeile, die auf ungeraden Seiten erscheint.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - Die "gerade" Kopf-/Fußzeile, die auf geraden Seiten erscheint.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

Zeigt, wie Sie eine Kopf- und eine Fußzeile erstellen.

```csharp
Document doc = new Document();

// Erstellen Sie eine Kopfzeile und hängen Sie einen Absatz daran an. Der Text in diesem Absatz
// erscheint oben auf jeder Seite dieses Abschnitts über dem Haupttext.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Erstellen Sie eine Fußzeile und hängen Sie einen Absatz daran an. Der Text in diesem Absatz
// wird unten auf jeder Seite dieses Abschnitts unter dem Haupttext angezeigt.
HeaderFooter footer = new HeaderFooter(doc, HeaderFooterType.FooterPrimary);
doc.FirstSection.HeadersFooters.Add(footer);

para = footer.AppendParagraph("My footer.");

Assert.False(footer.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

Assert.AreEqual(footer, para.ParentStory);
Assert.AreEqual(footer.ParentSection, para.ParentSection);
Assert.AreEqual(footer.ParentSection, header.ParentSection);

doc.Save(ArtifactsDir + "HeaderFooter.Create.docx");
```

### Siehe auch

* class [Story](../story/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
