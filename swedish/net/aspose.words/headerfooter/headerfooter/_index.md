---
title: HeaderFooter
linktitle: HeaderFooter
articleTitle: HeaderFooter
second_title: Aspose.Words för .NET
description: Designa enkelt snygga sidhuvuden och sidfot med vår intuitiva konstruktor. Anpassa din webbplats utseende för en unik och professionell touch!
type: docs
weight: 10
url: /sv/net/aspose.words/headerfooter/headerfooter/
---
## HeaderFooter constructor

Skapar ett nytt sidhuvud eller en ny sidfot av den angivna typen.

```csharp
public HeaderFooter(DocumentBase doc, HeaderFooterType headerFooterType)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | DocumentBase | Ägardokumentet. |
| headerFooterType | HeaderFooterType | En[`HeaderFooterType`](../headerfootertype/)värde som anger typen av sidhuvud eller sidfot. |

## Anmärkningar

När[`HeaderFooter`](../) skapas, tillhör den det angivna dokumentet, men är ännu inte en del av dokumentet och[`ParentNode`](../../node/parentnode/) är`null`.

Att lägga till[`HeaderFooter`](../)till en[`Section`](../../section/) använda[`InsertAfter`](../../compositenode/insertafter/) ,[`InsertBefore`](../../compositenode/insertbefore/) , eller[`HeadersFooters`](../../section/headersfooters/) egenskaper och metoder[`Add`](../../nodecollection/add/) ,[`Insert`](../../nodecollection/insert/).

## Exempel

Visar hur man skapar ett sidhuvud och en sidfot.

```csharp
Document doc = new Document();

// Skapa en rubrik och lägg till ett stycke i den. Texten i det stycket
// kommer att visas högst upp på varje sida i det här avsnittet, ovanför huvudtexten.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Skapa en sidfot och lägg till ett stycke i den. Texten i det stycket
// kommer att visas längst ner på varje sida i det här avsnittet, under huvudtexten.
HeaderFooter footer = new HeaderFooter(doc, HeaderFooterType.FooterPrimary);
doc.FirstSection.HeadersFooters.Add(footer);

para = footer.AppendParagraph("My footer.");

Assert.False(footer.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

Assert.AreEqual(footer, para.ParentStory);
Assert.AreEqual(footer.ParentSection, para.ParentSection);
Assert.AreEqual(footer.ParentSection, header.ParentSection);

doc.Save(ArtifactsDir + "HeaderFooter.Create.docx");
```

### Se även

* class [DocumentBase](../../documentbase/)
* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooter](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
