---
title: HeaderFooter Class
linktitle: HeaderFooter
articleTitle: HeaderFooter
second_title: Aspose.Words für .NET
description: Aspose.Words.HeaderFooter klas. Stellt einen Container für den Kopf oder Fußzeilentext eines Abschnitts dar in C#.
type: docs
weight: 3100
url: /de/net/aspose.words/headerfooter/
---
## HeaderFooter class

Stellt einen Container für den Kopf- oder Fußzeilentext eines Abschnitts dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Kopf- und Fußzeilen](https://docs.aspose.com/words/net/working-with-headers-and-footers/) Dokumentationsartikel.

```csharp
public class HeaderFooter : Story
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [HeaderFooter](headerfooter/)(*[DocumentBase](../documentbase/), [HeaderFooterType](../headerfootertype/)*) | Erstellt eine neue Kopf- oder Fußzeile des angegebenen Typs. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ruft die Anzahl der unmittelbaren Kinder dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FirstParagraph](../../aspose.words/story/firstparagraph/) { get; } | Ruft den ersten Absatz in der Geschichte ab. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Gibt zurück`WAHR` wenn dieser Knoten untergeordnete Knoten hat. |
| [HeaderFooterType](../../aspose.words/headerfooter/headerfootertype/) { get; } | Ruft den Typ dieser Kopf-/Fußzeile ab. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Gibt zurück`WAHR` da dieser Knoten untergeordnete Knoten haben kann. |
| [IsHeader](../../aspose.words/headerfooter/isheader/) { get; } | True, wenn dies der Fall ist`HeaderFooter` Objekt ist ein Header. |
| [IsLinkedToPrevious](../../aspose.words/headerfooter/islinkedtoprevious/) { get; set; } | True, wenn diese Kopf- oder Fußzeile mit der entsprechenden Kopf- oder Fußzeile im vorherigen Abschnitt verknüpft ist. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [LastParagraph](../../aspose.words/story/lastparagraph/) { get; } | Ruft den letzten Absatz in der Geschichte ab. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words/headerfooter/nodetype/) { get; } | Gibt zurückHeaderFooter . |
| [Paragraphs](../../aspose.words/story/paragraphs/) { get; } | Ruft eine Sammlung von Absätzen ab, die unmittelbar untergeordnete Elemente der Geschichte sind. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft das unmittelbare übergeordnete Element dieses Knotens ab. |
| [ParentSection](../../aspose.words/headerfooter/parentsection/) { get; } | Ruft den übergeordneten Abschnitt dieser Story ab. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar vorangeht. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt a zurück[`Range`](../range/) Objekt, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [StoryType](../../aspose.words/story/storytype/) { get; } | Ruft den Typ dieser Geschichte ab. |
| [Tables](../../aspose.words/story/tables/) { get; } | Ruft eine Sammlung von Tabellen ab, die unmittelbar untergeordnete Elemente der Story sind. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words/headerfooter/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Akzeptiert einen Besucher. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../node/)*) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [AppendParagraph](../../aspose.words/story/appendparagraph/)(*string*) | Eine Verknüpfungsmethode, die eine erstellt[`Paragraph`](../paragraph/) Objekt mit optionalem Text und hängt ihn am Ende dieses Objekts an. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Erstellt einen Navigator, der zum Durchlaufen und Lesen von Knoten verwendet werden kann. |
| [DeleteShapes](../../aspose.words/story/deleteshapes/)() | Löscht alle Formen aus dem Text dieser Geschichte. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Ruft den ersten Vorfahren des angegebenen ab[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Gibt eine Live-Sammlung untergeordneter Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bietet Unterstützung für die Iteration jedes Stils über die untergeordneten Knoten dieses Knotens. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ruft den Text dieses Knotens und aller seiner untergeordneten Knoten ab. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knoten-Array zurück. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../node/), [Node](../node/)*) | Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../node/), [Node](../node/)*) | Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein. |
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

`HeaderFooter` enthalten kann[`Paragraph`](../paragraph/) Und[`Tisch`](../../aspose.words.tables/table/) untergeordnete Knoten.

`HeaderFooter` ist ein Knoten auf Abschnittsebene und kann nur ein untergeordnetes Element von sein[`Section`](../section/) . Es kann nur einen geben`HeaderFooter` von jedem[`HeaderFooterType`](./headerfootertype/) in einem[`Section`](../section/).

Wenn[`Section`](../section/) hat keine`HeaderFooter` eines bestimmten Typs oder der`HeaderFooter`keine untergeordneten Knoten hat, wird diese Kopf-/Fußzeile als mit der Kopf-/Fußzeile desselben Typs des vorherigen Abschnitts in Microsoft Word verknüpft betrachtet.

Wann`HeaderFooter` enthält mindestens eine[`Paragraph`](../paragraph/), wird es nicht mehr als mit dem vorherigen in Microsoft Word verknüpft betrachtet.

## Beispiele

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
    // Es gibt drei Arten von Fuß- und Kopfzeilentypen.
    // 1 – Die „erste“ Kopf-/Fußzeile, die nur auf der ersten Seite eines Abschnitts erscheint.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 – Die „primäre“ Kopf-/Fußzeile, die auf ungeraden Seiten erscheint.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 – Die „gerade“ Kopf-/Fußzeile, die auf geraden Seiten erscheint.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

Zeigt, wie eine Kopf- und Fußzeile erstellt wird.

```csharp
Document doc = new Document();

// Eine Überschrift erstellen und einen Absatz daran anhängen. Der Text in diesem Absatz
// wird oben auf jeder Seite dieses Abschnitts über dem Haupttext angezeigt.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Eine Fußzeile erstellen und einen Absatz daran anhängen. Der Text in diesem Absatz
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
