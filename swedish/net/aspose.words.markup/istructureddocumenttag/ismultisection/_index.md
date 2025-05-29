---
title: IStructuredDocumentTag.IsMultiSection
linktitle: IsMultiSection
articleTitle: IsMultiSection
second_title: Aspose.Words för .NET
description: Upptäck IStructuredDocumentTags IsMultiSection-egenskap, som identifierar om din tagg är en flersektionstagg med varierande intervall, vilket förbättrar dokumentorganisation och funktionalitet.
type: docs
weight: 40
url: /sv/net/aspose.words.markup/istructureddocumenttag/ismultisection/
---
## IStructuredDocumentTag.IsMultiSection property

Returnerar sant om den här instansen är en strukturerad dokumenttagg med varierande intervall (flera sektioner).

```csharp
public bool IsMultiSection { get; }
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
