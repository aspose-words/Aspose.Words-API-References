---
title: IStructuredDocumentTag.Title
second_title: Aspose.Words für .NET-API-Referenz
description: IStructuredDocumentTag eigendom. Gibt den damit verbundenen Anzeigenamen an SDT . Kann nicht null sein.
type: docs
weight: 110
url: /de/net/aspose.words.markup/istructureddocumenttag/title/
---
## IStructuredDocumentTag.Title property

Gibt den damit verbundenen Anzeigenamen an **SDT** . Kann nicht null sein.

```csharp
public string Title { get; set; }
```

### Beispiele

Zeigt, wie man ein strukturiertes Dokument-Tag erhält.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// Holen Sie sich das Tag des strukturierten Dokuments anhand der ID.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsRanged());
Console.WriteLine(sdt.Title);

// Holen Sie sich das strukturierte Dokument-Tag oder das Bereichs-Tag nach Titel.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### Siehe auch

* interface [IStructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../istructureddocumenttag/)
* Montage [Aspose.Words](../../../)


