---
title: RevisionGroupCollection Class
linktitle: RevisionGroupCollection
articleTitle: RevisionGroupCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.RevisionGroupCollection, die eine effiziente Verwaltung von Dokumentrevisionsgruppen für verbesserte Bearbeitung und Zusammenarbeit bietet.
type: docs
weight: 5530
url: /de/net/aspose.words/revisiongroupcollection/
---
## RevisionGroupCollection class

Eine Sammlung von[`RevisionGroup`](../revisiongroup/)Objekte, die Revisionsgruppen im Dokument darstellen.

Um mehr zu erfahren, besuchen Sie die[Änderungen in einem Dokument verfolgen](https://docs.aspose.com/words/net/track-changes-in-a-document/) Dokumentationsartikel.

```csharp
public sealed class RevisionGroupCollection : IEnumerable<RevisionGroup>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words/revisiongroupcollection/count/) { get; } | Gibt die Anzahl der Revisionsgruppen in der Sammlung zurück. |
| [Item](../../aspose.words/revisiongroupcollection/item/) { get; } | Gibt eine Revisionsgruppe am angegebenen Index zurück. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetEnumerator](../../aspose.words/revisiongroupcollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück. |

## Bemerkungen

Sie erstellen keine Instanzen dieser Klasse direkt. Verwenden Sie die[`Groups`](../revisioncollection/groups/) -Eigenschaft, um in einem Dokument vorhandene Revisionsgruppen abzurufen.

## Beispiele

Zeigt, wie man eine Gruppe von Revisionen in einem Dokument erhält.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

Zeigt, wie Informationen zu einer Gruppe von Revisionen in einem Dokument gedruckt werden.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Assert.AreEqual(7, doc.Revisions.Groups.Count);

foreach (RevisionGroup group in doc.Revisions.Groups)
{
    Console.WriteLine(
        $"Revision author: {group.Author}; Revision type: {group.RevisionType} \n\tRevision text: {group.Text}");
}
```

### Siehe auch

* class [RevisionGroup](../revisiongroup/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
