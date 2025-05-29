---
title: RevisionGroup.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words für .NET
description: Erkunden Sie die Texteigenschaft „RevisionGroup“, um auf eingefügten, gelöschten oder verschobenen Text zuzugreifen und so die Formatierungserkenntnisse und die Bearbeitungseffizienz Ihres Dokuments zu verbessern.
type: docs
weight: 30
url: /de/net/aspose.words/revisiongroup/text/
---
## RevisionGroup.Text property

Gibt eingefügten/gelöschten/verschobenen Text oder eine Beschreibung der Formatänderung zurück.

```csharp
public string Text { get; }
```

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

* class [RevisionGroup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
