---
title: IReplacingCallback
second_title: Aspose.Words för .NET API Referens
description: Implementera detta gränssnitt om du vill ha din egen anpassade metod anropad under en sök och ersättoperation.
type: docs
weight: 4370
url: /sv/net/aspose.words.replacing/ireplacingcallback/
---
## IReplacingCallback interface

Implementera detta gränssnitt om du vill ha din egen anpassade metod anropad under en sök- och ersätt-operation.

```csharp
public interface IReplacingCallback
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Replacing](../../aspose.words.replacing/ireplacingcallback/replacing/)(ReplacingArgs) | En användardefinierad metod som anropas under en ersättningsoperation för varje matchning som hittas precis innan en ersättning görs. |

### Exempel

Visar hur man ersätter alla förekomster av ett reguljärt uttrycksmönster med en annan sträng, samtidigt som alla sådana ersättningar spåras.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // Vi kan använda ett "FindReplaceOptions"-objekt för att ändra sök-och-ersätt-processen.
    FindReplaceOptions options = new FindReplaceOptions();

    // Ställ in en återuppringning som spårar alla ersättningar som "Ersätt"-metoden kommer att göra.
    TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
    options.ReplacingCallback = logger;

    doc.Range.Replace(new Regex("New York City|NYC"), "Washington", options);

    Assert.AreEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.GetText().Trim());

    Assert.AreEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node.", logger.GetLog().Trim());
}

/// <summary>
/// Upprätthåller en logg över varje textersättning som görs med en sök-och-ersätt-operation
/// och noterar den ursprungliga matchade textens värde.
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

Visar hur man spårar i vilken ordning en textersättningsoperation passerar noder.

```csharp
public void Order(bool differentFirstPageHeaderFooter)
        {
            Document doc = new Document(MyDir + "Header and footer types.docx");

            Section firstPageSection = doc.FirstSection;

            ReplaceLog logger = new ReplaceLog();
            FindReplaceOptions options = new FindReplaceOptions { ReplacingCallback = logger };

            // Att använda en annan sidhuvud/sidfot för den första sidan kommer att påverka sökordningen.
            firstPageSection.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;
            doc.Range.Replace(new Regex("(header|footer)"), "", options);

#if NET48 || NET5_0_OR_GREATER || JAVA
            if (differentFirstPageHeaderFooter)
                Assert.AreEqual("First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n", 
                    logger.Text.Replace("\r", ""));
            else
                Assert.AreEqual("Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n", 
                    logger.Text.Replace("\r", ""));
#elif __MOBILE__
            if (differentFirstPageHeaderFooter)
                Assert.AreEqual("First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n", logger.Text);
            else
                Assert.AreEqual("Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n", logger.Text);
#endif
        }

        /// <summary>
        /// Under en sök-och-ersätt-operation, registrerar innehållet i varje nod som har text som operationen "hittar",
        /// i det tillstånd den är i innan bytet sker.
        /// Detta kommer att visa i vilken ordning textersättningsoperationen korsar noder.
        /// </summary>
        private class ReplaceLog : IReplacingCallback
        {
            public ReplaceAction Replacing(ReplacingArgs args)
            {
                mTextBuilder.AppendLine(args.MatchNode.GetText());
                return ReplaceAction.Skip;
            }

            internal string Text => mTextBuilder.ToString();

            private readonly StringBuilder mTextBuilder = new StringBuilder();
        }
```

Visar hur man infogar ett helt dokuments innehåll som ersättning för en matchning i en sök-och-ersätt-operation.

```csharp
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // Vi kan använda ett "FindReplaceOptions"-objekt för att ändra sök-och-ersätt-processen.
    FindReplaceOptions options = new FindReplaceOptions();
    options.ReplacingCallback = new InsertDocumentAtReplaceHandler();

    mainDoc.Range.Replace(new Regex("\\[MY_DOCUMENT\\]"), "", options);
    mainDoc.Save(ArtifactsDir + "InsertDocument.InsertDocumentAtReplace.docx");

private class InsertDocumentAtReplaceHandler : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        Document subDoc = new Document(MyDir + "Document.docx");

        // Infoga ett dokument efter stycket som innehåller den matchade texten.
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        // Ta bort stycket med den matchade texten.
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

* namnutrymme [Aspose.Words.Replacing](../../aspose.words.replacing/)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
