---
title: HeaderFooterCollection Class
linktitle: HeaderFooterCollection
articleTitle: HeaderFooterCollection
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.HeaderFooterCollection för enkel, maskinskriven åtkomst till Section Header Footer-noder, vilket effektiviserar dokumenthanteringen och förbättrar ditt arbetsflöde.
type: docs
weight: 3540
url: /sv/net/aspose.words/headerfootercollection/
---
## HeaderFooterCollection class

Ger maskinskriven åtkomst till[`HeaderFooter`](../headerfooter/) noder av en[`Section`](../section/) .

För att lära dig mer, besök[Arbeta med sidhuvuden och sidfot](https://docs.aspose.com/words/net/working-with-headers-and-footers/) dokumentationsartikel.

```csharp
public class HeaderFooterCollection : NodeCollection
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Hämtar antalet noder i samlingen. |
| [Item](../../aspose.words/headerfootercollection/item/) { get; } | Hämtar en[`HeaderFooter`](../headerfooter/) vid det givna indexet. (3 indexers) |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Lägger till en nod i slutet av samlingen. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Tar bort alla noder från den här samlingen och från dokumentet. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Avgör om en nod finns i samlingen. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Ger en enkel iteration i "foreach"-stil över samlingen av noder. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Returnerar det nollbaserade indexet för den angivna noden. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Infogar en nod i samlingen vid det angivna indexet. |
| [LinkToPrevious](../../aspose.words/headerfootercollection/linktoprevious/#linktoprevious_1)(*bool*) | Länkar eller avlänkar alla sidhuvuden och sidfötter till motsvarande sidhuvuden och sidfötter i föregående avsnitt. |
| [LinkToPrevious](../../aspose.words/headerfootercollection/linktoprevious/#linktoprevious)(*[HeaderFooterType](../headerfootertype/), bool*) | Länkar eller avlänkar det angivna sidhuvudet eller sidfoten till motsvarande sidhuvud eller sidfot i föregående avsnitt. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Tar bort noden från samlingen och från dokumentet. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Tar bort noden vid det angivna indexet från samlingen och från dokumentet. |
| [ToArray](../../aspose.words/headerfootercollection/toarray/#toarray)() | Kopierar alla`Sidhuvud/Sidfot` från kollektionen till en ny uppsättning av`Sidhuvud/Sidfot` s. (2 methods) |

## Anmärkningar

Det kan finnas maximalt en[`HeaderFooter`](../headerfooter/)

av varje[`HeaderFooterType`](../headerfootertype/) per [`Section`](../section/) .

[`HeaderFooter`](../headerfooter/) Objekt kan förekomma i valfri ordning i samlingen.

## Exempel

Visar hur man tar bort alla sidfot från ett dokument.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Gå igenom varje avsnitt och ta bort sidfot av alla slag.
foreach (Section section in doc.OfType<Section>())
{
    // Det finns tre typer av sidfot och sidhuvud.
    // 1 - Sidhuvudet/sidfoten "Första", som bara visas på första sidan i ett avsnitt.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 - Sidhuvudet/sidfoten "Primärt", som visas på udda sidor.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - Sidhuvudet/sidfoten "Jämnt", som visas på jämna sidor.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

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

* class [NodeCollection](../nodecollection/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
