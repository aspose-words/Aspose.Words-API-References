---
title: Section.ClearContent
second_title: Aspose.Words för .NET API Referens
description: Section metod. Rensar avsnittet.
type: docs
weight: 110
url: /sv/net/aspose.words/section/clearcontent/
---
## Section.ClearContent method

Rensar avsnittet.

```csharp
public void ClearContent()
```

### Anmärkningar

Texten till[`Body`](../body/) rensas, finns bara ett tomt stycke kvar som representerar avsnittsbrytningen.

Texten i alla sidhuvuden och sidfötter rensas, men[`HeaderFooter`](../../headerfooter/) själva föremålen tas inte bort.

### Exempel

Visar hur man rensar innehållet i ett avsnitt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.GetText().Trim());
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Att köra "ClearContent"-metoden tar bort allt avsnittsinnehåll
// men lämna ett tomt stycke för att lägga till innehåll igen.
doc.FirstSection.ClearContent();

Assert.AreEqual(string.Empty, doc.GetText().Trim());
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);
```

### Se även

* class [Section](../)
* namnutrymme [Aspose.Words](../../section/)
* hopsättning [Aspose.Words](../../../)


