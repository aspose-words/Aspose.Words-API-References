---
title: Class HeaderFooter
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.HeaderFooter klass. Representerar en behållare för sidhuvudet eller sidfoten i ett avsnitt.
type: docs
weight: 3100
url: /sv/net/aspose.words/headerfooter/
---
## HeaderFooter class

Representerar en behållare för sidhuvudet eller sidfoten i ett avsnitt.

För att lära dig mer, besök[Arbeta med sidhuvuden och sidfötter](https://docs.aspose.com/words/net/working-with-headers-and-footers/) dokumentationsartikel.

```csharp
public class HeaderFooter : Story
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [HeaderFooter](headerfooter/)(DocumentBase, HeaderFooterType) | Skapar en ny sidhuvud eller sidfot av den angivna typen. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Hämtar antalet omedelbara barn till denna nod. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Får det första barnet i noden. |
| [FirstParagraph](../../aspose.words/story/firstparagraph/) { get; } | Får första stycket i berättelsen. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returnerar`Sann` om denna nod har några undernoder. |
| [HeaderFooterType](../../aspose.words/headerfooter/headerfootertype/) { get; } | Hämtar typen av denna sidhuvud/sidfot. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returnerar`Sann` eftersom denna nod kan ha underordnade noder. |
| [IsHeader](../../aspose.words/headerfooter/isheader/) { get; } | Sant om detta`HeaderFooter` objektet är en header. |
| [IsLinkedToPrevious](../../aspose.words/headerfooter/islinkedtoprevious/) { get; set; } | Sant om denna sidhuvud eller sidfot är länkad till motsvarande sidhuvud eller sidfot i föregående avsnitt. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Hämtar nodens sista underordnade. |
| [LastParagraph](../../aspose.words/story/lastparagraph/) { get; } | Hämtar det sista stycket i berättelsen. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden omedelbart efter denna nod. |
| override [NodeType](../../aspose.words/headerfooter/nodetype/) { get; } | ReturnerarHeaderFooter . |
| [Paragraphs](../../aspose.words/story/paragraphs/) { get; } | Får en samling stycken som är omedelbara barn till berättelsen. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [ParentSection](../../aspose.words/headerfooter/parentsection/) { get; } | Hämtar den överordnade delen av denna berättelse. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden omedelbart före denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en[`Range`](../range/) objekt som representerar den del av ett dokument som finns i denna nod. |
| [StoryType](../../aspose.words/story/storytype/) { get; } | Hämtar typen av denna berättelse. |
| [Tables](../../aspose.words/story/tables/) { get; } | Får en samling tabeller som är omedelbara barn till berättelsen. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words/headerfooter/accept/)(DocumentVisitor) | Accepterar en besökare. |
| override [AcceptEnd](../../aspose.words/headerfooter/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words/headerfooter/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [AppendParagraph](../../aspose.words/story/appendparagraph/)(string) | En genvägsmetod som skapar en[`Paragraph`](../paragraph/) objekt med valfri text och lägger till den i slutet av detta objekt. |
| [Clone](../../aspose.words/node/clone/)(bool) | Skapar en dubblett av noden. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Skapar navigator som kan användas för att korsa och läsa noder. |
| [DeleteShapes](../../aspose.words/story/deleteshapes/)() | Tar bort alla former från texten i denna berättelse. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Hämtar den första förfadern till den angivna[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Hämtar den första förfadern till den angivna objekttypen. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Returnerar en N:te underordnad nod som matchar den angivna typen. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Returnerar en aktiv samling av underordnade noder som matchar den angivna typen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Tillhandahåller stöd för varje stiliteration över undernoderna för denna nod. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Hämtar texten för denna nod och alla dess underordnade. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Returnerar indexet för den angivna undernoden i den underordnade nodmatrisen. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Hämtar nästa nod enligt algoritmen för förbeställningsträdet. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Hämtar föregående nod enligt algoritmen för förbeställningsträdet. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Tar bort alla undernoder för den aktuella noden. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tar bort alla[`SmartTag`](../../aspose.words.markup/smarttag/)underliggande noder till den aktuella noden. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Väljer en lista med noder som matchar XPath-uttrycket. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Väljer den första[`Node`](../node/) som matchar XPath-uttrycket. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporterar innehållet i noden till en sträng i angivet format. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |

### Anmärkningar

`HeaderFooter` kan innehålla[`Paragraph`](../paragraph/) och[`Tabell`](../../aspose.words.tables/table/) barnnoder.

`HeaderFooter` är en nod på sektionsnivå och kan bara vara ett barn till[`Section`](../section/) . Det kan bara finnas en`HeaderFooter` av varje[`HeaderFooterType`](./headerfootertype/) i en[`Section`](../section/).

Om[`Section`](../section/) har inte en`HeaderFooter` av en specifik typ eller the`HeaderFooter`har inga underordnade noder, anses denna sidhuvud/sidfot vara länkad till sidhuvudet/sidfoten av samma typ av föregående avsnitt i Microsoft Word.

När`HeaderFooter` innehåller minst en[`Paragraph`](../paragraph/), anses det inte längre vara länkat till tidigare i Microsoft Word.

### Exempel

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

Visar hur man tar bort alla sidfötter från ett dokument.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Iterera genom varje avsnitt och ta bort sidfötter av alla slag.
foreach (Section section in doc.OfType<Section>())
{
    // Det finns tre typer av sidfots- och sidhuvudstyper.
    // 1 - Den "Första" sidhuvudet/sidfoten, som bara visas på första sidan i ett avsnitt.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 - Den "Primära" sidhuvudet/sidfoten, som visas på udda sidor.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - "Jämn" sidhuvudet/sidfoten, som visas på jämna sidor.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

Visar hur man skapar ett sidhuvud och en sidfot.

```csharp
Document doc = new Document();

// Skapa en rubrik och lägg till ett stycke till den. Texten i det stycket
// kommer att visas överst på varje sida i det här avsnittet, ovanför huvudtexten.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Skapa en sidfot och lägg till ett stycke till den. Texten i det stycket
// kommer att visas längst ned på varje sida i det här avsnittet, under huvudtexten.
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


