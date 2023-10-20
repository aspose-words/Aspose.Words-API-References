---
title: IStructuredDocumentTag.IsRanged
linktitle: IsRanged
articleTitle: IsRanged
second_title: Aspose.Words för .NET
description: IStructuredDocumentTag IsRanged metod. Returnerar sant om denna instans är en strukturerad dokumenttagg med intervall i C#.
type: docs
weight: 140
url: /sv/net/aspose.words.markup/istructureddocumenttag/isranged/
---
## IStructuredDocumentTag.IsRanged method

Returnerar sant om denna instans är en strukturerad dokumenttagg med intervall.

```csharp
public bool IsRanged()
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
