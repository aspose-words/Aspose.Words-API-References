---
title: IStructuredDocumentTag.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words för .NET
description: IStructuredDocumentTag Title fast egendom. Anger det vänliga namnet som är associerat med dettaSDT . Kan inte vara null i C#.
type: docs
weight: 110
url: /sv/net/aspose.words.markup/istructureddocumenttag/title/
---
## IStructuredDocumentTag.Title property

Anger det vänliga namnet som är associerat med detta**SDT** . Kan inte vara null.

```csharp
public string Title { get; set; }
```

## Exempel

Visar hur man får strukturerad dokumenttagg.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// Hämta den strukturerade dokumenttaggen efter Id.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsRanged());
Console.WriteLine(sdt.Title);

// Hämta den strukturerade dokumenttaggen eller ranged taggen efter titel.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### Se även

* interface [IStructuredDocumentTag](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
