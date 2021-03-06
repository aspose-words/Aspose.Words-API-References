---
title: IsFormatRevision
second_title: Aspose.Words för .NET API Referens
description: Returnerar sant om formateringen av objektet ändrades i Microsoft Word medan ändringsspårning var aktiverad.
type: docs
weight: 90
url: /sv/net/aspose.words/paragraph/isformatrevision/
---
## Paragraph.IsFormatRevision property

Returnerar sant om formateringen av objektet ändrades i Microsoft Word medan ändringsspårning var aktiverad.

```csharp
public bool IsFormatRevision { get; }
```

### Exempel

Visar hur man kontrollerar om ett stycke är en formatversion.

```csharp
Document doc = new Document(MyDir + "Format revision.docx");

// Det här stycket är en "Format"-revision, som inträffar när vi ändrar formateringen av befintlig text
// medan du spårar revisioner i Microsoft Word via "Review" -> "Spåra ändringar".
Assert.True(doc.FirstSection.Body.FirstParagraph.IsFormatRevision);
```

### Se även

* class [Paragraph](../../paragraph)
* namnutrymme [Aspose.Words](../../paragraph)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
