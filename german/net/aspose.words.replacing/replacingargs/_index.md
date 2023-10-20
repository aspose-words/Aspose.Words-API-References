---
title: ReplacingArgs Class
linktitle: ReplacingArgs
articleTitle: ReplacingArgs
second_title: Aspose.Words für .NET
description: Aspose.Words.Replacing.ReplacingArgs klas. Stellt Daten für einen benutzerdefinierten Ersetzungsvorgang bereit in C#.
type: docs
weight: 4650
url: /de/net/aspose.words.replacing/replacingargs/
---
## ReplacingArgs class

Stellt Daten für einen benutzerdefinierten Ersetzungsvorgang bereit.

Um mehr zu erfahren, besuchen Sie die[Suchen und Ersetzen](https://docs.aspose.com/words/net/find-and-replace/) Dokumentationsartikel.

```csharp
public class ReplacingArgs
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [GroupIndex](../../aspose.words.replacing/replacingargs/groupindex/) { get; set; } | Identifiziert anhand des Index eine erfasste Gruppe im[`Match`](./match/) , das durch das ersetzt werden soll[`Replacement`](./replacement/) string. |
| [GroupName](../../aspose.words.replacing/replacingargs/groupname/) { get; set; } | Identifiziert anhand des Namens eine erfasste Gruppe im[`Match`](./match/) , das durch das ersetzt werden soll[`Replacement`](./replacement/) string. |
| [Match](../../aspose.words.replacing/replacingargs/match/) { get; } | DieMatch resultierend aus einer einzelnen regulären -Ausdrucksübereinstimmung während eines**Ersetzen** . |
| [MatchNode](../../aspose.words.replacing/replacingargs/matchnode/) { get; } | Ruft den Knoten ab, der den Anfang des Matches enthält. |
| [MatchOffset](../../aspose.words.replacing/replacingargs/matchoffset/) { get; } | Ruft die nullbasierte Startposition der Übereinstimmung ab dem Anfang des Knotens ab, der den Anfang der Übereinstimmung enthält. |
| [Replacement](../../aspose.words.replacing/replacingargs/replacement/) { get; set; } | Ruft die Ersatzzeichenfolge ab oder legt sie fest. |

## Beispiele

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

* interface [IReplacingCallback](../ireplacingcallback/)
* class [Range](../../aspose.words/range/)
* method [Replace](../../aspose.words/range/replace/)
* namensraum [Aspose.Words.Replacing](../../aspose.words.replacing/)
* Montage [Aspose.Words](../../)
