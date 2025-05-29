---
title: IStructuredDocumentTag.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words för .NET
description: Upptäck egenskapen IStructuredDocumentTag Title – definiera ett användarvänligt namn för din SDT och förbättra dokumentets tydlighet. Läs mer nu!
type: docs
weight: 140
url: /sv/net/aspose.words.markup/istructureddocumenttag/title/
---
## IStructuredDocumentTag.Title property

Anger det användarvänliga namnet som är associerat med detta**SDT** . Kan inte vara null.

```csharp
public string Title { get; set; }
```

## Exempel

Visar hur man får taggar för strukturerade dokument.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// Hämta den strukturerade dokumenttaggen efter Id.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsMultiSection);
Console.WriteLine(sdt.Title);

// Hämta den strukturerade dokumenttaggen eller intervalltaggen efter titel.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### Se även

* interface [IStructuredDocumentTag](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
