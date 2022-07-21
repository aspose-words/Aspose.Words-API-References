---
title: Replacing
second_title: Aspose.Words für .NET-API-Referenz
description: Eine benutzerdefinierte Methode die während einer Ersetzungsoperation für jede gefundene Übereinstimmung aufgerufen wird kurz bevor eine Ersetzung vorgenommen wird.
type: docs
weight: 10
url: /de/net/aspose.words.replacing/ireplacingcallback/replacing/
---
## IReplacingCallback.Replacing method

Eine benutzerdefinierte Methode, die während einer Ersetzungsoperation für jede gefundene Übereinstimmung aufgerufen wird, kurz bevor eine Ersetzung vorgenommen wird.

```csharp
public ReplaceAction Replacing(ReplacingArgs args)
```

### Rückgabewert

A[`ReplaceAction`](../../replaceaction) Wert, der die Aktion angibt, die für die aktuelle Übereinstimmung ausgeführt werden soll.

### Beispiele

Zeigt, wie alle Vorkommen eines regulären Ausdrucksmusters durch eine andere Zeichenfolge ersetzt werden, während alle diese Ersetzungen nachverfolgt werden.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // Wir können ein "FindReplaceOptions"-Objekt verwenden, um den Suchen-und-Ersetzen-Prozess zu ändern.
    FindReplaceOptions options = new FindReplaceOptions();

    // Setzen Sie einen Rückruf, der alle Ersetzungen verfolgt, die die "Replace"-Methode vornimmt.
    TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
    options.ReplacingCallback = logger;

    doc.Range.Replace(new Regex("New York City|NYC"), "Washington", options);

    Assert.AreEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.GetText().Trim());

    Assert.AreEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node.", logger.GetLog().Trim());
}

/// <summary>
/// Verwaltet ein Protokoll über jede Textersetzung, die durch eine Suchen-und-Ersetzen-Operation durchgeführt wird
/// und notiert den Wert des ursprünglichen übereinstimmenden Textes.
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

Zeigt, wie der Inhalt eines gesamten Dokuments als Ersatz für eine Übereinstimmung in einem Suchen-und-Ersetzen-Vorgang eingefügt wird.

```csharp
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // Wir können ein "FindReplaceOptions"-Objekt verwenden, um den Suchen-und-Ersetzen-Prozess zu ändern.
    FindReplaceOptions options = new FindReplaceOptions();
    options.ReplacingCallback = new InsertDocumentAtReplaceHandler();

    mainDoc.Range.Replace(new Regex("\\[MY_DOCUMENT\\]"), "", options);
    mainDoc.Save(ArtifactsDir + "InsertDocument.InsertDocumentAtReplace.docx");

private class InsertDocumentAtReplaceHandler : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        Document subDoc = new Document(MyDir + "Document.docx");

        // Fügen Sie ein Dokument nach dem Absatz ein, der den übereinstimmenden Text enthält.
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        // Entfernen Sie den Absatz mit dem übereinstimmenden Text.
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
                // Den Knoten überspringen, wenn es der letzte leere Absatz in einem Abschnitt ist.
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

* enum [ReplaceAction](../../replaceaction)
* class [ReplacingArgs](../../replacingargs)
* interface [IReplacingCallback](../../ireplacingcallback)
* namensraum [Aspose.Words.Replacing](../../ireplacingcallback)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
