---
title: HeaderFooter Class
linktitle: HeaderFooter
articleTitle: HeaderFooter
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.HeaderFooter, din lösning för att enkelt hantera sektionshuvuden och sidfot. Förbättra dokumentformateringen idag!
type: docs
weight: 3530
url: /sv/net/aspose.words/headerfooter/
---
## HeaderFooter class

Representerar en behållare för sidhuvud- eller sidfotstexten i ett avsnitt.

För att lära dig mer, besök[Arbeta med sidhuvuden och sidfot](https://docs.aspose.com/words/net/working-with-headers-and-footers/) dokumentationsartikel.

```csharp
public class HeaderFooter : Story
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [HeaderFooter](headerfooter/)(*[DocumentBase](../documentbase/), [HeaderFooterType](../headerfootertype/)*) | Skapar ett nytt sidhuvud eller en ny sidfot av den angivna typen. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Hämtar antalet omedelbara barn till denna nod. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Hämtar nodens första barn. |
| [FirstParagraph](../../aspose.words/story/firstparagraph/) { get; } | Hämtar det första stycket i berättelsen. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returer`sann` om den här noden har några undernoder. |
| [HeaderFooterType](../../aspose.words/headerfooter/headerfootertype/) { get; } | Hämtar typen av detta sidhuvud/sidfot. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returer`sann` eftersom denna nod kan ha underordnade noder. |
| [IsHeader](../../aspose.words/headerfooter/isheader/) { get; } | Sant om detta`HeaderFooter` objektet är en rubrik. |
| [IsLinkedToPrevious](../../aspose.words/headerfooter/islinkedtoprevious/) { get; set; } | Sant om detta sidhuvud eller sidfot är länkat till motsvarande sidhuvud eller sidfot i föregående avsnitt. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Hämtar nodens sista barn. |
| [LastParagraph](../../aspose.words/story/lastparagraph/) { get; } | Hämtar det sista stycket i berättelsen. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden som följer direkt efter denna nod. |
| override [NodeType](../../aspose.words/headerfooter/nodetype/) { get; } | ReturerHeaderFooter . |
| [Paragraphs](../../aspose.words/story/paragraphs/) { get; } | Hämtar en samling stycken som är direkta underordnade stycken till berättelsen. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [ParentSection](../../aspose.words/headerfooter/parentsection/) { get; } | Hämtar huvudavsnittet för den här artikeln. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden som omedelbart föregår denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en[`Range`](../range/)objekt som representerar den del av ett dokument som finns i denna nod. |
| [StoryType](../../aspose.words/story/storytype/) { get; } | Hämtar typen av den här berättelsen. |
| [Tables](../../aspose.words/story/tables/) { get; } | Hämtar en samling tabeller som är direkta underordnade tabeller till berättelsen. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words/headerfooter/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Tar emot en besökare. |
| override [AcceptEnd](../../aspose.words/headerfooter/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Accepterar en besökare för att besöka slutet av rubriken. |
| override [AcceptStart](../../aspose.words/headerfooter/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Accepterar en besökare för att besöka början av rubriken. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Lägger till den angivna noden i slutet av listan över underordnade noder för denna nod. |
| [AppendParagraph](../../aspose.words/story/appendparagraph/)(*string*) | En genvägsmetod som skapar en[`Paragraph`](../paragraph/) objekt med valfri text och lägger till den i slutet av detta objekt. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Skapar en duplikat av noden. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Skapar en navigator som kan användas för att korsa och läsa noder. |
| [DeleteShapes](../../aspose.words/story/deleteshapes/)() | Tar bort alla former från texten i den här berättelsen. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Hämtar den första förfadern till den angivna[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Hämtar den första förfadern till den angivna objekttypen. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Returnerar en N:te underordnad nod som matchar den angivna typen. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Returnerar en live-samling av underordnade noder som matchar den angivna typen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Ger stöd för iterationen för varje stil över de underordnade noderna till denna nod. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Hämtar texten för denna nod och alla dess underordnade noder. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Returnerar indexet för den angivna undernoden i undernodsmatrisen. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | Infogar den angivna noden omedelbart efter den angivna referensnoden. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | Infogar den angivna noden omedelbart före den angivna referensnoden. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Hämtar nästa nod enligt algoritmen för förbeställningsträdtraversering. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Lägger till den angivna noden i början av listan över underordnade noder för denna nod. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Hämtar föregående nod enligt algoritmen för trädtraversering i förbeställning. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Tar bort alla undernoder till den aktuella noden. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Tar bort den angivna undernoden. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tar bort alla[`SmartTag`](../../aspose.words.markup/smarttag/) underordnade noder till den aktuella noden. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Väljer en lista med noder som matchar XPath-uttrycket. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Väljer den första[`Node`](../node/) som matchar XPath-uttrycket. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exporterar nodens innehåll till en sträng i det angivna formatet. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporterar nodens innehåll till en sträng med de angivna sparalternativen. |

## Anmärkningar

`HeaderFooter` kan innehålla[`Paragraph`](../paragraph/) och[`Tabell`](../../aspose.words.tables/table/) underordnade noder.

`HeaderFooter` är en nod på sektionsnivå och kan bara vara underordnad[`Section`](../section/) . Det kan bara finnas en`HeaderFooter` av varje[`HeaderFooterType`](./headerfootertype/) i en[`Section`](../section/).

Om[`Section`](../section/) har inte en`HeaderFooter` av en specifik typ eller `HeaderFooter` inte har några underordnade noder anses denna sidhuvud/sidfot vara länkad till sidhuvudet/sidfoten av samma typ som föregående avsnitt i Microsoft Word.

När`HeaderFooter` innehåller minst en[`Paragraph`](../paragraph/), anses den inte längre vara länkad till föregående i Microsoft Word.

## Exempel

Visar hur man ersätter text i ett dokuments sidfot.

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

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

* class [Story](../story/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
