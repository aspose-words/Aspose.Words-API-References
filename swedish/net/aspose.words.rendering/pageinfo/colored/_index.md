---
title: PageInfo.Colored
linktitle: Colored
articleTitle: Colored
second_title: Aspose.Words för .NET
description: Upptäck om din sida har innehåll i livfulla färger med egenskapen PageInfo Colored. Förbättra användarengagemang och förbättra den visuella attraktionskraften!
type: docs
weight: 10
url: /sv/net/aspose.words.rendering/pageinfo/colored/
---
## PageInfo.Colored property

Returer`sann` om sidan innehåller färgat innehåll.

```csharp
public bool Colored { get; }
```

## Exempel

Visar hur man kontrollerar om sidan är i färg eller inte.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Kontrollera att dokumentets första sida inte är färgad.
Assert.IsFalse(doc.GetPageInfo(0).Colored);
```

### Se även

* class [PageInfo](../)
* namnutrymme [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* hopsättning [Aspose.Words](../../../)
