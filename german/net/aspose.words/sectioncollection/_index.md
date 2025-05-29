---
title: SectionCollection Class
linktitle: SectionCollection
articleTitle: SectionCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.SectionCollection – Ihre Lösung für die effiziente Verwaltung von Dokumentabschnitten mit leistungsstarken Funktionen und Flexibilität.
type: docs
weight: 6570
url: /de/net/aspose.words/sectioncollection/
---
## SectionCollection class

Eine Sammlung von[`Section`](../section/) Objekte im Dokument.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Abschnitten](https://docs.aspose.com/words/net/working-with-sections/) Dokumentationsartikel.

```csharp
public class SectionCollection : NodeCollection
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Ruft die Anzahl der Knoten in der Sammlung ab. |
| [Item](../../aspose.words/sectioncollection/item/) { get; } | Ruft einen Abschnitt am angegebenen Index ab. (2 indexers) |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Fügt am Ende der Sammlung einen Knoten hinzu. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Entfernt alle Knoten aus dieser Sammlung und aus dem Dokument. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Bestimmt, ob ein Knoten in der Sammlung vorhanden ist. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Bietet eine einfache Iteration im „foreach“-Stil über die Knotensammlung. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Gibt den nullbasierten Index des angegebenen Knotens zurück. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Fügt einen Knoten am angegebenen Index in die Sammlung ein. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Entfernt den Knoten aus der Sammlung und aus dem Dokument. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Entfernt den Knoten am angegebenen Index aus der Sammlung und aus dem Dokument. |
| [ToArray](../../aspose.words/sectioncollection/toarray/#toarray_1)() | Kopiert alle Abschnitte aus der Sammlung in ein neues Abschnittsarray. (2 methods) |

## Bemerkungen

Ein Microsoft Word-Dokument kann mehrere Abschnitte enthalten. Um einen Abschnitt in Microsoft Word zu erstellen, wählen Sie den Befehl Einfügen/Umbruch und wählen Sie einen Umbruchtyp. Der Umbruch gibt an, ob der Abschnitt auf einer neuen Seite oder auf derselben Seite beginnt.

Das programmatische Einfügen und Entfernen von Abschnitten kann verwendet werden, um während des Seriendrucks erstellte Dokumente anzupassen. Wenn ein Dokument je nach Kriterien unterschiedliche Inhalte oder Teile des Inhalts enthalten muss, können Sie ein Masterdokument mit mehreren Abschnitten erstellen und einige Abschnitte vor oder nach dem Seriendruck löschen.

## Beispiele

Zeigt, wie Abschnitte in einem Dokument hinzugefügt und entfernt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

// Löschen Sie den ersten Abschnitt aus dem Dokument.
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// Fügen Sie eine Kopie des jetzigen ersten Abschnitts an das Ende des Dokuments an.
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

### Siehe auch

* class [NodeCollection](../nodecollection/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
