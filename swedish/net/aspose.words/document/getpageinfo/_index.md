---
title: Document.GetPageInfo
linktitle: GetPageInfo
articleTitle: GetPageInfo
second_title: Aspose.Words för .NET
description: Upptäck GetPageInfo-metoden för att hämta viktig information om sidstorlek, orientering och rendering för optimerad utskrift och förbättrad dokumenthantering.
type: docs
weight: 650
url: /sv/net/aspose.words/document/getpageinfo/
---
## Document.GetPageInfo method

Hämtar sidstorlek, orientering och annan information om en sida som kan vara användbar för utskrift eller rendering.

```csharp
public PageInfo GetPageInfo(int pageIndex)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| pageIndex | Int32 | Det 0-baserade sidindexet. |

## Exempel

Visar hur man kontrollerar om sidan är i färg eller inte.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Kontrollera att dokumentets första sida inte är färgad.
Assert.IsFalse(doc.GetPageInfo(0).Colored);
```

### Se även

* class [PageInfo](../../../aspose.words.rendering/pageinfo/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
