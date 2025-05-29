---
title: Section.ClearContent
linktitle: ClearContent
articleTitle: ClearContent
second_title: Aspose.Words för .NET
description: Rensa enkelt sektioner med ClearContent-metoden. Förbättra ditt arbetsflöde och effektivisera innehållshanteringen idag!
type: docs
weight: 110
url: /sv/net/aspose.words/section/clearcontent/
---
## Section.ClearContent method

Rensar sektionen.

```csharp
public void ClearContent()
```

## Anmärkningar

Texten till[`Body`](../body/) rensas, återstår bara ett tomt stycke som representerar avsnittsbrytningen.

Texten i alla sidhuvuden och sidfot rensas, men[`HeaderFooter`](../../headerfooter/) själva föremålen tas inte bort.

## Exempel

Visar hur man rensar innehållet i ett avsnitt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.GetText().Trim());
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Att köra metoden "ClearContent" tar bort allt innehåll i avsnittet
// men lämna ett tomt stycke för att lägga till innehåll igen.
doc.FirstSection.ClearContent();

Assert.AreEqual(string.Empty, doc.GetText().Trim());
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);
```

### Se även

* class [Section](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
