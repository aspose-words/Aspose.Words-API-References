---
title: Class RevisionGroup
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.RevisionGroup klas. Stellt eine Gruppe von sequentiellen Elementen darRevision Objekte.
type: docs
weight: 4780
url: /de/net/aspose.words/revisiongroup/
---
## RevisionGroup class

Stellt eine Gruppe von sequentiellen Elementen dar[`Revision`](../revision/) Objekte.

Um mehr zu erfahren, besuchen Sie die[Verfolgen Sie Änderungen in einem Dokument](https://docs.aspose.com/words/net/track-changes-in-a-document/) Dokumentationsartikel.

```csharp
public class RevisionGroup
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Author](../../aspose.words/revisiongroup/author/) { get; } | Ruft den Autor dieser Revisionsgruppe ab. |
| [RevisionType](../../aspose.words/revisiongroup/revisiontype/) { get; } | Ruft den Typ der in dieser Gruppe enthaltenen Revisionen ab. |
| [Text](../../aspose.words/revisiongroup/text/) { get; } | Gibt eingefügten/gelöschten/verschobenen Text oder eine Beschreibung der Formatänderung zurück. |

### Beispiele

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

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


