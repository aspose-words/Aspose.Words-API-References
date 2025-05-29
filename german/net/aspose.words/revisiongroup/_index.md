---
title: RevisionGroup Class
linktitle: RevisionGroup
articleTitle: RevisionGroup
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.RevisionGroup, die für die effiziente Verwaltung und Organisation sequenzieller Revisionsobjekte zur optimierten Dokumentbearbeitung entwickelt wurde.
type: docs
weight: 5520
url: /de/net/aspose.words/revisiongroup/
---
## RevisionGroup class

Stellt eine Gruppe von sequentiellen[`Revision`](../revision/) Objekte.

Um mehr zu erfahren, besuchen Sie die[Änderungen in einem Dokument verfolgen](https://docs.aspose.com/words/net/track-changes-in-a-document/) Dokumentationsartikel.

```csharp
public class RevisionGroup
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Author](../../aspose.words/revisiongroup/author/) { get; } | Ruft den Autor dieser Revisionsgruppe ab. |
| [RevisionType](../../aspose.words/revisiongroup/revisiontype/) { get; } | Ruft den Typ der in dieser Gruppe enthaltenen Revisionen ab. |
| [Text](../../aspose.words/revisiongroup/text/) { get; } | Gibt eingefügten/gelöschten/verschobenen Text oder eine Beschreibung der Formatänderung zurück. |

## Beispiele

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
