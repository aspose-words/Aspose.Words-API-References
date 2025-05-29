---
title: HeaderFooterCollection Class
linktitle: HeaderFooterCollection
articleTitle: HeaderFooterCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.HeaderFooterCollection für einfachen, typisierten Zugriff auf Section HeaderFooter-Knoten, optimieren Sie die Dokumentenverwaltung und verbessern Sie Ihren Arbeitsablauf.
type: docs
weight: 3540
url: /de/net/aspose.words/headerfootercollection/
---
## HeaderFooterCollection class

Bietet typisierten Zugriff auf[`HeaderFooter`](../headerfooter/) Knoten eines[`Section`](../section/) .

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Kopf- und Fußzeilen](https://docs.aspose.com/words/net/working-with-headers-and-footers/) Dokumentationsartikel.

```csharp
public class HeaderFooterCollection : NodeCollection
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Ruft die Anzahl der Knoten in der Sammlung ab. |
| [Item](../../aspose.words/headerfootercollection/item/) { get; } | Ruft eine[`HeaderFooter`](../headerfooter/) am angegebenen Index. (3 indexers) |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Fügt am Ende der Sammlung einen Knoten hinzu. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Entfernt alle Knoten aus dieser Sammlung und aus dem Dokument. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Bestimmt, ob ein Knoten in der Sammlung vorhanden ist. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Bietet eine einfache Iteration im „foreach“-Stil über die Knotensammlung. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Gibt den nullbasierten Index des angegebenen Knotens zurück. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Fügt einen Knoten am angegebenen Index in die Sammlung ein. |
| [LinkToPrevious](../../aspose.words/headerfootercollection/linktoprevious/#linktoprevious_1)(*bool*) | Verknüpft oder trennt alle Kopf- und Fußzeilen mit den entsprechenden Kopf- und Fußzeilen im vorherigen Abschnitt. |
| [LinkToPrevious](../../aspose.words/headerfootercollection/linktoprevious/#linktoprevious)(*[HeaderFooterType](../headerfootertype/), bool*) | Verknüpft die angegebene Kopf- oder Fußzeile mit der entsprechenden Kopf- oder Fußzeile im vorherigen Abschnitt oder hebt die Verknüpfung auf. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Entfernt den Knoten aus der Sammlung und aus dem Dokument. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Entfernt den Knoten am angegebenen Index aus der Sammlung und aus dem Dokument. |
| [ToArray](../../aspose.words/headerfootercollection/toarray/#toarray)() | Kopiert alles`KopfzeileFußzeile` s aus der Sammlung zu einer neuen Reihe von`KopfzeileFußzeile` s. (2 methods) |

## Bemerkungen

Es kann maximal eine[`HeaderFooter`](../headerfooter/)

von jedem[`HeaderFooterType`](../headerfootertype/) pro [`Section`](../section/) .

[`HeaderFooter`](../headerfooter/) Objekte können in beliebiger Reihenfolge in der Sammlung vorkommen.

## Beispiele

Zeigt, wie alle Fußzeilen aus einem Dokument gelöscht werden.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Durchlaufen Sie jeden Abschnitt und entfernen Sie Fußzeilen aller Art.
foreach (Section section in doc.OfType<Section>())
{
    // Es gibt drei Arten von Fußzeilen- und Kopfzeilentypen.
    // 1 – Die „Erste“ Kopf-/Fußzeile, die nur auf der ersten Seite eines Abschnitts angezeigt wird.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 – Die „primäre“ Kopf-/Fußzeile, die auf ungeraden Seiten erscheint.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

        // 3 – Die Kopf-/Fußzeile „Gerade“, die auf geraden Seiten erscheint.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

Zeigt, wie eine Kopf- und eine Fußzeile erstellt wird.

```csharp
Document doc = new Document();

// Erstellen Sie eine Überschrift und fügen Sie einen Absatz hinzu. Der Text in diesem Absatz
// wird oben auf jeder Seite dieses Abschnitts über dem Haupttext angezeigt.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Erstellen Sie eine Fußzeile und fügen Sie einen Absatz hinzu. Der Text in diesem Absatz
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

* class [NodeCollection](../nodecollection/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
