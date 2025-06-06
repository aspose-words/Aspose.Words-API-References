---
title: ReplacingArgs Class
linktitle: ReplacingArgs
articleTitle: ReplacingArgs
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Replacing.ReplacingArgs för effektiv anpassad textersättning i dina dokument. Förbättra ditt arbetsflöde idag!
type: docs
weight: 5390
url: /sv/net/aspose.words.replacing/replacingargs/
---
## ReplacingArgs class

Tillhandahåller data för en anpassad ersättningsåtgärd.

För att lära dig mer, besök[Sök och ersätt](https://docs.aspose.com/words/net/find-and-replace/) dokumentationsartikel.

```csharp
public class ReplacingArgs
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [GroupIndex](../../aspose.words.replacing/replacingargs/groupindex/) { get; set; } | Identifierar, med hjälp av index, en fångad grupp i[`Match`](./match/) som ska ersättas med[`Replacement`](./replacement/) sträng. |
| [GroupName](../../aspose.words.replacing/replacingargs/groupname/) { get; set; } | Identifierar, med namn, en fångad grupp i[`Match`](./match/) som ska ersättas med[`Replacement`](./replacement/) sträng. |
| [Match](../../aspose.words.replacing/replacingargs/match/) { get; } | DenMatch resultatet av en enda matchning av regular -uttrycket under en**Ersätta** . |
| [MatchNode](../../aspose.words.replacing/replacingargs/matchnode/) { get; } | Hämtar noden som innehåller början av matchningen. |
| [MatchOffset](../../aspose.words.replacing/replacingargs/matchoffset/) { get; } | Hämtar matchningens nollbaserade startposition från början av noden som innehåller matchningens början. |
| [Replacement](../../aspose.words.replacing/replacingargs/replacement/) { get; set; } | Hämtar eller ställer in ersättningssträngen. |

## Exempel

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

* interface [IReplacingCallback](../ireplacingcallback/)
* class [Range](../../aspose.words/range/)
* method [Replace](../../aspose.words/range/replace/)
* namnutrymme [Aspose.Words.Replacing](../../aspose.words.replacing/)
* hopsättning [Aspose.Words](../../)
