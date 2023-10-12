---
title: Interface IReplacingCallback
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Replacing.IReplacingCallback koppel. Implementieren Sie diese Schnittstelle wenn Sie Ihre eigene benutzerdefinierte Methode während eines Such und Ersetzungsvorgangs aufrufen möchten.
type: docs
weight: 4630
url: /de/net/aspose.words.replacing/ireplacingcallback/
---
## IReplacingCallback interface

Implementieren Sie diese Schnittstelle, wenn Sie Ihre eigene benutzerdefinierte Methode während eines Such- und Ersetzungsvorgangs aufrufen möchten.

```csharp
public interface IReplacingCallback
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Replacing](../../aspose.words.replacing/ireplacingcallback/replacing/)(ReplacingArgs) | Eine benutzerdefinierte Methode, die während eines Ersetzungsvorgangs für jede gefundene Übereinstimmung aufgerufen wird, kurz bevor ein Ersetzungsvorgang durchgeführt wird. |

### Beispiele

Zeigt, wie alle Vorkommen eines regulären Ausdrucksmusters durch eine andere Zeichenfolge ersetzt werden, während alle Ersetzungen verfolgt werden.

```csharp
public void ReplaceWithCallback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // Wir können ein „FindReplaceOptions“-Objekt verwenden, um den Such- und Ersetzungsprozess zu ändern.
    FindReplaceOptions options = new FindReplaceOptions();

    // Legen Sie einen Rückruf fest, der alle Ersetzungen verfolgt, die die Methode „Replace“ vornimmt.
    TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
    options.ReplacingCallback = logger;

    doc.Range.Replace(new Regex("New York City|NYC"), "Washington", options);

    Assert.AreEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.GetText().Trim());

    Assert.AreEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node.", logger.GetLog().Trim());
}

/// <summary>
/// Verwaltet ein Protokoll aller Textersetzungen, die durch einen Such- und Ersetzungsvorgang durchgeführt werden
/// und notiert den Wert des ursprünglich übereinstimmenden Texts.
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

Zeigt, wie die Reihenfolge verfolgt wird, in der ein Textersetzungsvorgang Knoten durchläuft.

```csharp
public void Order(bool differentFirstPageHeaderFooter)
        {
            Document doc = new Document(MyDir + "Header and footer types.docx");

            Section firstPageSection = doc.FirstSection;

            ReplaceLog logger = new ReplaceLog();
            FindReplaceOptions options = new FindReplaceOptions { ReplacingCallback = logger };

            // Die Verwendung einer anderen Kopf-/Fußzeile für die erste Seite wirkt sich auf die Suchreihenfolge aus.
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
        /// Zeichnet während einer Such- und Ersetzungsoperation den Inhalt jedes Knotens auf, der Text enthält, den die Operation „findet“.
        /// in dem Zustand, in dem es sich vor der Ersetzung befindet.
        /// Dies zeigt die Reihenfolge an, in der die Textersetzungsoperation Knoten durchläuft.
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

Zeigt, wie der Inhalt eines gesamten Dokuments als Ersatz für eine Übereinstimmung in einem Suchen-und-Ersetzen-Vorgang eingefügt wird.

```csharp
public void InsertDocumentAtReplace()
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // Wir können ein „FindReplaceOptions“-Objekt verwenden, um den Such- und Ersetzungsprozess zu ändern.
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

        // Ein Dokument nach dem Absatz einfügen, der den übereinstimmenden Text enthält.
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        // Den Absatz mit dem übereinstimmenden Text entfernen.
        para.Remove();

        return ReplaceAction.Skip;
    }
}

/// <summary>
/// Fügt alle Knoten eines anderen Dokuments nach einem Absatz oder einer Tabelle ein.
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
                // Den Knoten überspringen, wenn es sich um den letzten leeren Absatz in einem Abschnitt handelt.
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

### Siehe auch

* namensraum [Aspose.Words.Replacing](../../aspose.words.replacing/)
* Montage [Aspose.Words](../../)


