---
title: IStructuredDocumentTag.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words für .NET
description: Entdecken Sie die Titeleigenschaft von IStructuredDocumentTag – definieren Sie einen benutzerfreundlichen Namen für Ihr SDT und verbessern Sie die Dokumentübersicht. Jetzt mehr erfahren!
type: docs
weight: 140
url: /de/net/aspose.words.markup/istructureddocumenttag/title/
---
## IStructuredDocumentTag.Title property

Gibt den Anzeigenamen an, der mit diesem**SDT** . Darf nicht null sein.

```csharp
public string Title { get; set; }
```

## Beispiele

Zeigt, wie man strukturierte Dokument-Tags erhält.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// Holen Sie sich das strukturierte Dokument-Tag nach ID.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsMultiSection);
Console.WriteLine(sdt.Title);

// Holen Sie sich das strukturierte Dokument-Tag oder das Bereichs-Tag nach Titel.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### Siehe auch

* interface [IStructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
