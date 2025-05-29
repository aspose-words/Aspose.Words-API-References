---
title: Range.Replace
linktitle: Replace
articleTitle: Replace
second_title: Aspose.Words för .NET
description: Ersätt enkelt alla förekomster av ett teckensträngmönster med metoden Range Replace. Förbättra din textbehandling med detta kraftfulla verktyg!
type: docs
weight: 100
url: /sv/net/aspose.words/range/replace/
---
## Replace(*string, string*) {#replace}

Ersätter alla förekomster av ett angivet teckensträngmönster med en ersättningssträng.

```csharp
public int Replace(string pattern, string replacement)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| pattern | String | En sträng som ska ersättas. |
| replacement | String | En sträng som ersätter alla förekomster av mönstret. |

### Returvärde

Antalet gjorda ersättningar.

## Anmärkningar

Mönstret kommer inte att användas som reguljärt uttryck. Vänligen använd`Replace` om du behöver reguljära uttryck.

Använde jämförelse utan skiftlägeskänslighet.

Metoden kan bearbeta avbrott i både mönster- och ersättningssträngar.

Du bör använda speciella metatecken om du behöver arbeta med brytningar:

* **&amp;p** - styckebrytning
* **&amp;b** - avsnittsbrytning
* **&amp;m** - sidbrytning
* **&amp;l** - manuell radbrytning

Användningsmetod`Replace` för att ha mer flexibel anpassning.

## Exempel

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// Infogar styckebrytning efter Numbers.
doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
```

Visar hur man utför en sök-och-ersätt-text-operation på innehållet i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Greetings, _FullName_!");

// Utför en sök-och-ersätt-operation på vårt dokuments innehåll och verifiera antalet ersättningar som har skett.
int replacementCount = doc.Range.Replace("_FullName_", "John Doe");

Assert.AreEqual(1, replacementCount);
Assert.AreEqual("Greetings, John Doe!", doc.GetText().Trim());
```

Visar hur man lägger till formatering i stycken där en sök-och-ersätt-åtgärd har hittat träffar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Every paragraph that ends with a full stop like this one will be right aligned.");
builder.Writeln("This one will not!");
builder.Write("This one also will.");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(ParagraphAlignment.Left, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[2].ParagraphFormat.Alignment);

// Vi kan använda ett "FindReplaceOptions"-objekt för att modifiera sök-och-ersätt-processen.
FindReplaceOptions options = new FindReplaceOptions();

// Ställ in egenskapen "Alignment" till "ParagraphAlignment.Right" för att högerjustera varje stycke
// som innehåller en matchning som sök-och-ersätt-operationen hittar.
options.ApplyParagraphFormat.Alignment = ParagraphAlignment.Right;

// Ersätt varje punkt som står precis före en styckebrytning med ett utropstecken.
int count = doc.Range.Replace(".&p", "!&p", options);

Assert.AreEqual(2, count);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[2].ParagraphFormat.Alignment);
Assert.AreEqual("Every paragraph that ends with a full stop like this one will be right aligned!\r" +
                "This one will not!\r" +
                "This one also will!", doc.GetText().Trim());
```

### Se även

* class [Range](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## Replace(*Regex, string*) {#replace_2}

Ersätter alla förekomster av ett teckenmönster som anges av ett reguljärt uttryck med en annan sträng.

```csharp
public int Replace(Regex pattern, string replacement)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| pattern | Regex | Ett reguljärt uttrycksmönster som används för att hitta matchningar. |
| replacement | String | En sträng som ersätter alla förekomster av mönstret. |

### Returvärde

Antalet gjorda ersättningar.

## Anmärkningar

Ersätter hela matchningen som registreras av det reguljära uttrycket.

Metoden kan bearbeta avbrott i både mönster- och ersättningssträngar.

Du bör använda speciella metatecken om du behöver arbeta med brytningar:

* **&amp;p** - styckebrytning
* **&amp;b** - avsnittsbrytning
* **&amp;m** - sidbrytning
* **&amp;l** - manuell radbrytning

Användningsmetod`Replace` för att ha mer flexibel anpassning.

## Exempel

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

// Ersätter varje nummer med styckebrytning.
doc.Range.Replace(new Regex(@"\d+"), "&p");
```

Visar hur man ersätter alla förekomster av ett reguljärt uttrycksmönster med annan text.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("I decided to get the curtains in gray, ideal for the grey-accented room.");

doc.Range.Replace(new Regex("gr(a|e)y"), "lavender");

Assert.AreEqual("I decided to get the curtains in lavender, ideal for the lavender-accented room.", doc.GetText().Trim());
```

### Se även

* class [Range](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## Replace(*string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_1}

Ersätter alla förekomster av ett angivet teckensträngmönster med en ersättningssträng.

```csharp
public int Replace(string pattern, string replacement, FindReplaceOptions options)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| pattern | String | En sträng som ska ersättas. |
| replacement | String | En sträng som ersätter alla förekomster av mönstret. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objekt för att ange ytterligare alternativ. |

### Returvärde

Antalet gjorda ersättningar.

## Anmärkningar

Mönstret kommer inte att användas som reguljärt uttryck. Vänligen använd`Replace` om du behöver reguljära uttryck.

Metoden kan bearbeta avbrott i både mönster- och ersättningssträngar.

Du bör använda speciella metatecken om du behöver arbeta med brytningar:

* **&amp;p** - styckebrytning
* **&amp;b** - avsnittsbrytning
* **&amp;m** - sidbrytning
* **&amp;l** - manuell radbrytning
* **&amp;&amp;** - &amp; karaktär

## Exempel

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// Infogar styckebrytning efter Numbers.
doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
```

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

Visar hur man växlar mellan skiftlägeskänslighet och versalkänslighet när man utför en sök-och-ersätt-åtgärd.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Vi kan använda ett "FindReplaceOptions"-objekt för att modifiera sök-och-ersätt-processen.
FindReplaceOptions options = new FindReplaceOptions();

// Sätt flaggan "MatchCase" till "true" för att tillämpa skiftlägeskänslighet när strängar söks efter att ersättas.
// Sätt flaggan "MatchCase" till "false" för att ignorera skiftläge vid sökning efter text att ersätta.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

Visar hur man växlar mellan fristående sök-och-ersätt-åtgärder som endast avser ord.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Vi kan använda ett "FindReplaceOptions"-objekt för att modifiera sök-och-ersätt-processen.
FindReplaceOptions options = new FindReplaceOptions();

// Sätt flaggan "FindWholeWordsOnly" till "true" för att ersätta den funna texten om den inte är en del av ett annat ord.
// Sätt flaggan "FindWholeWordsOnly" till "false" för att ersätta all text oavsett dess omgivning.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

Visar hur man ersätter alla förekomster av textsträngar i en tabell och cell.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Carrots");
builder.InsertCell();
builder.Write("50");
builder.EndRow();
builder.InsertCell();
builder.Write("Potatoes");
builder.InsertCell();
builder.Write("50");
builder.EndTable();

FindReplaceOptions options = new FindReplaceOptions();
options.MatchCase = true;
options.FindWholeWordsOnly = true;

// Utför en sök-och-ersätt-operation på en hel tabell.
table.Range.Replace("Carrots", "Eggs", options);

// Utför en sök-och-ersätt-operation på den sista cellen på den sista raden i tabellen.
table.LastRow.LastCell.Range.Replace("50", "20", options);

Assert.AreEqual("Eggs\a50\a\a" +
                "Potatoes\a20\a\a", table.GetText().Trim());
```

### Se även

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Range](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## Replace(*Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_3}

Ersätter alla förekomster av ett teckenmönster som anges av ett reguljärt uttryck med en annan sträng.

```csharp
public int Replace(Regex pattern, string replacement, FindReplaceOptions options)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| pattern | Regex | Ett reguljärt uttrycksmönster som används för att hitta matchningar. |
| replacement | String | En sträng som ersätter alla förekomster av mönstret. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objekt för att ange ytterligare alternativ. |

### Returvärde

Antalet gjorda ersättningar.

## Anmärkningar

Ersätter hela matchningen som registreras av det reguljära uttrycket.

Metoden kan bearbeta avbrott i både mönster- och ersättningssträngar.

Du bör använda speciella metatecken om du behöver arbeta med brytningar:

* **&amp;p** - styckebrytning
* **&amp;b** - avsnittsbrytning
* **&amp;m** - sidbrytning
* **&amp;l** - manuell radbrytning
* **&amp;&amp;** - &amp; karaktär

## Exempel

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

// Ersätter varje nummer med styckebrytning.
doc.Range.Replace(new Regex(@"\d+"), "&p", new FindReplaceOptions());
```

Visar hur man ersätter alla förekomster av ett reguljärt uttrycksmönster med en annan sträng, samtidigt som alla sådana ersättningar spåras.

```csharp
public void ReplaceWithCallback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // Vi kan använda ett "FindReplaceOptions"-objekt för att modifiera sök-och-ersätt-processen.
    FindReplaceOptions options = new FindReplaceOptions();

    // Ställ in en återanropning som spårar alla ersättningar som "Replace"-metoden gör.
    TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
    options.ReplacingCallback = logger;

    doc.Range.Replace(new Regex("New York City|NYC"), "Washington", options);

    Assert.AreEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.GetText().Trim());

    Assert.AreEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node.", logger.GetLog().Trim());
}

/// <summary>
/// Upprätthåller en logg över varje textersättning som görs av en sök-och-ersätt-operation
/// och noterar den ursprungliga matchande textens värde.
/// </summary>
private class TextFindAndReplacementLogger : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        mLog.AppendLine($"\"{args.Match.Value}\" converted to \"{args.Replacement}\" " +
                        $"{args.MatchOffset} characters into a {args.MatchNode.NodeType} node.");

        args.Replacement = $"(Old value:\"{args.Match.Value}\") {args.Replacement}";
        return ReplaceAction.Replace;
    }

    public string GetLog()
    {
        return mLog.ToString();
    }

    private readonly StringBuilder mLog = new StringBuilder();
}
```

Visar hur man infogar ett helt dokuments innehåll som en ersättning för en matchning i en sök-och-ersätt-åtgärd.

```csharp
public void InsertDocumentAtReplace()
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // Vi kan använda ett "FindReplaceOptions"-objekt för att modifiera sök-och-ersätt-processen.
    FindReplaceOptions options = new FindReplaceOptions();
    options.ReplacingCallback = new InsertDocumentAtReplaceHandler();

    mainDoc.Range.Replace(new Regex("\\[MY_DOCUMENT\\]"), "", options);
    mainDoc.Save(ArtifactsDir + "InsertDocument.InsertDocumentAtReplace.docx");

}

private class InsertDocumentAtReplaceHandler : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        Document subDoc = new Document(MyDir + "Document.docx");

        // Infoga ett dokument efter stycket som innehåller den matchande texten.
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        // Ta bort stycket med den matchande texten.
        para.Remove();

        return ReplaceAction.Skip;
    }
}

/// <summary>
/// Infogar alla noder i ett annat dokument efter ett stycke eller en tabell.
/// </summary>
private static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode dstStory = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        foreach (Section srcSection in docToInsert.Sections.OfType<Section>())
            foreach (Node srcNode in srcSection.Body)
            {
                // Hoppa över noden om det är det sista tomma stycket i ett avsnitt.
                if (srcNode.NodeType == NodeType.Paragraph)
                {
                    Paragraph para = (Paragraph)srcNode;
                    if (para.IsEndOfSection && !para.HasChildNodes)
                        continue;
                }

                Node newNode = importer.ImportNode(srcNode, true);

                dstStory.InsertAfter(newNode, insertionDestination);
                insertionDestination = newNode;
            }
    }
    else
    {
        throw new ArgumentException("The destination node must be either a paragraph or table.");
    }
}
```

### Se även

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Range](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
