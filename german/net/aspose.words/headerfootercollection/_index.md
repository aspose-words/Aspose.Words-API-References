---
title: Class HeaderFooterCollection
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.HeaderFooterCollection klas. Bietet getippten Zugriff aufHeaderFooter Knoten von a Abschnitt .
type: docs
weight: 2930
url: /de/net/aspose.words/headerfootercollection/
---
## HeaderFooterCollection class

Bietet getippten Zugriff auf[`HeaderFooter`](../headerfooter/) Knoten von a **Abschnitt** .

```csharp
public class HeaderFooterCollection : NodeCollection
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Ruft die Anzahl der Knoten in der Sammlung ab. |
| [Item](../../aspose.words/headerfootercollection/item/) { get; } | Ruft a **Kopfzeile Fußzeile** am angegebenen Index. (3 indexers) |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(Node) | Fügt am Ende der Sammlung einen Knoten hinzu. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Entfernt alle Knoten aus dieser Sammlung und aus dem Dokument. |
| [Contains](../../aspose.words/nodecollection/contains/)(Node) | Bestimmt, ob sich ein Knoten in der Sammlung befindet. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Bietet eine einfache Iteration im "foreach"-Stil über die Sammlung von Knoten. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(Node) | Gibt den nullbasierten Index des angegebenen Knotens zurück. |
| [Insert](../../aspose.words/nodecollection/insert/)(int, Node) | Fügt am angegebenen Index einen Knoten in die Sammlung ein. |
| [LinkToPrevious](../../aspose.words/headerfootercollection/linktoprevious/#linktoprevious_1)(bool) | Verknüpft alle Kopf- und Fußzeilen mit den entsprechenden Kopf- und Fußzeilen im vorherigen Abschnitt oder hebt die Verknüpfung auf. |
| [LinkToPrevious](../../aspose.words/headerfootercollection/linktoprevious/#linktoprevious)(HeaderFooterType, bool) | Verknüpft die angegebene Kopf- oder Fußzeile mit der entsprechenden Kopf- oder Fußzeile im vorherigen Abschnitt oder hebt die Verknüpfung auf. |
| [Remove](../../aspose.words/nodecollection/remove/)(Node) | Entfernt den Knoten aus der Sammlung und aus dem Dokument. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int) | Entfernt den Knoten am angegebenen Index aus der Sammlung und aus dem Dokument. |
| [ToArray](../../aspose.words/headerfootercollection/toarray/#toarray)() | Kopiert alle`KopfzeileFußzeile` s von der Sammlung zu einem neuen Array von`KopfzeileFußzeile` s. (2 methods) |

### Bemerkungen

Es kann maximal eins sein **Kopfzeile Fußzeile**

von jedem[`HeaderFooterType`](../headerfootertype/) pro  **Abschnitt** .

**Kopfzeile Fußzeile** Objekte können in beliebiger Reihenfolge in der Sammlung vorkommen.

### Beispiele

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

* class [NodeCollection](../nodecollection/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


