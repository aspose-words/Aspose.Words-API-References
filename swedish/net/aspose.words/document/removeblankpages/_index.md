---
title: Document.RemoveBlankPages
linktitle: RemoveBlankPages
articleTitle: RemoveBlankPages
second_title: Aspose.Words för .NET
description: Förbättra dina dokument enkelt med metoden RemoveBlankPages, vilket eliminerar oönskade tomma sidor och ger en polerad och professionell finish.
type: docs
weight: 700
url: /sv/net/aspose.words/document/removeblankpages/
---
## Document.RemoveBlankPages method

Tar bort tomma sidor från dokumentet.

```csharp
public List<int> RemoveBlankPages()
```

### Returvärde

Listan med sidnummer har betraktats som tom och tagits bort.

## Anmärkningar

Det resulterande dokumentet kommer inte att innehålla sidor som anses vara tomma medan annat innehåll, inklusive numrering, sidhuvuden/sidfötter och övergripande layout, ska förbli oförändrat. Sidan anses vara tom när sidans brödtext inte har något synligt innehåll, till exempel, en tom tabell utan kantlinjer kommer att betraktas som osynlig och därför kommer sidan att detekteras som tom.

## Exempel

Visar hur man tar bort tomma sidor från dokumentet.

```csharp
Document doc = new Document(MyDir + "Blank pages.docx");
Assert.AreEqual(2, doc.PageCount);
doc.RemoveBlankPages();
doc.UpdatePageLayout();
Assert.AreEqual(1, doc.PageCount);
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
