---
title: Range.Replace
second_title: Aspose.Words for .NET API Reference
description: Range method. Replaces all occurrences of a specified character string pattern with a replacement string in C#.
type: docs
weight: 90
url: /net/aspose.words/range/replace/
---
## Replace(string, string) {#replace}

Replaces all occurrences of a specified character string pattern with a replacement string.

```csharp
public int Replace(string pattern, string replacement)
```

| Parameter | Type | Description |
| --- | --- | --- |
| pattern | String | A string to be replaced. |
| replacement | String | A string to replace all occurrences of pattern. |

### Return Value

The number of replacements made.

## Remarks

The pattern will not be used as regular expression. Please use `Replace` if you need regular expressions.

Used case-insensitive comparison.

Method is able to process breaks in both pattern and replacement strings.

You should use special meta-characters if you need to work with breaks:

* **&amp;p** - paragraph break
* **&amp;b** - section break
* **&amp;m** - page break
* **&amp;l** - manual line break

Use method `Replace` to have more flexible customization.

## Examples

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// Inserts paragraph break after Numbers.
doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
```

Shows how to perform a find-and-replace text operation on the contents of a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Greetings, _FullName_!");

// Perform a find-and-replace operation on our document's contents and verify the number of replacements that took place.
int replacementCount = doc.Range.Replace("_FullName_", "John Doe");

Assert.AreEqual(1, replacementCount);
Assert.AreEqual("Greetings, John Doe!", doc.GetText().Trim());
```

Shows how to add formatting to paragraphs in which a find-and-replace operation has found matches.

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

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
FindReplaceOptions options = new FindReplaceOptions();

// Set the "Alignment" property to "ParagraphAlignment.Right" to right-align every paragraph
// that contains a match that the find-and-replace operation finds.
options.ApplyParagraphFormat.Alignment = ParagraphAlignment.Right;

// Replace every full stop that is right before a paragraph break with an exclamation point.
int count = doc.Range.Replace(".&p", "!&p", options);

Assert.AreEqual(2, count);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[2].ParagraphFormat.Alignment);
Assert.AreEqual("Every paragraph that ends with a full stop like this one will be right aligned!\r" +
                "This one will not!\r" +
                "This one also will!", doc.GetText().Trim());
```

### See Also

* class [Range](../)
* namespace [Aspose.Words](../../range/)
* assembly [Aspose.Words](../../../)

---

## Replace(Regex, string) {#replace_2}

Replaces all occurrences of a character pattern specified by a regular expression with another string.

```csharp
public int Replace(Regex pattern, string replacement)
```

| Parameter | Type | Description |
| --- | --- | --- |
| pattern | Regex | A regular expression pattern used to find matches. |
| replacement | String | A string to replace all occurrences of pattern. |

### Return Value

The number of replacements made.

## Remarks

Replaces the whole match captured by the regular expression.

Method is able to process breaks in both pattern and replacement strings.

You should use special meta-characters if you need to work with breaks:

* **&amp;p** - paragraph break
* **&amp;b** - section break
* **&amp;m** - page break
* **&amp;l** - manual line break

Use method `Replace` to have more flexible customization.

## Examples

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

// Replaces each number with paragraph break.
doc.Range.Replace(new Regex(@"\d+"), "&p");
```

Shows how to replace all occurrences of a regular expression pattern with other text.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("I decided to get the curtains in gray, ideal for the grey-accented room.");

doc.Range.Replace(new Regex("gr(a|e)y"), "lavender");

Assert.AreEqual("I decided to get the curtains in lavender, ideal for the lavender-accented room.", doc.GetText().Trim());
```

### See Also

* class [Range](../)
* namespace [Aspose.Words](../../range/)
* assembly [Aspose.Words](../../../)

---

## Replace(string, string, FindReplaceOptions) {#replace_1}

Replaces all occurrences of a specified character string pattern with a replacement string.

```csharp
public int Replace(string pattern, string replacement, FindReplaceOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| pattern | String | A string to be replaced. |
| replacement | String | A string to replace all occurrences of pattern. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) object to specify additional options. |

### Return Value

The number of replacements made.

## Remarks

The pattern will not be used as regular expression. Please use `Replace` if you need regular expressions.

Method is able to process breaks in both pattern and replacement strings.

You should use special meta-characters if you need to work with breaks:

* **&amp;p** - paragraph break
* **&amp;b** - section break
* **&amp;m** - page break
* **&amp;l** - manual line break
* **&amp;&amp;** - &amp; character

## Examples

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// Inserts paragraph break after Numbers.
doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
```

Shows how to replace text in a document's footer.

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

Shows how to toggle case sensitivity when performing a find-and-replace operation.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
FindReplaceOptions options = new FindReplaceOptions();

// Set the "MatchCase" flag to "true" to apply case sensitivity while finding strings to replace.
// Set the "MatchCase" flag to "false" to ignore character case while searching for text to replace.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

Shows how to toggle standalone word-only find-and-replace operations.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
FindReplaceOptions options = new FindReplaceOptions();

// Set the "FindWholeWordsOnly" flag to "true" to replace the found text if it is not a part of another word.
// Set the "FindWholeWordsOnly" flag to "false" to replace all text regardless of its surroundings.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

Shows how to replace all instances of String of text in a table and cell.

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

// Perform a find-and-replace operation on an entire table.
table.Range.Replace("Carrots", "Eggs", options);

// Perform a find-and-replace operation on the last cell of the last row of the table.
table.LastRow.LastCell.Range.Replace("50", "20", options);

Assert.AreEqual("Eggs\a50\a\a" +
                "Potatoes\a20\a\a", table.GetText().Trim());
```

### See Also

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Range](../)
* namespace [Aspose.Words](../../range/)
* assembly [Aspose.Words](../../../)

---

## Replace(Regex, string, FindReplaceOptions) {#replace_3}

Replaces all occurrences of a character pattern specified by a regular expression with another string.

```csharp
public int Replace(Regex pattern, string replacement, FindReplaceOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| pattern | Regex | A regular expression pattern used to find matches. |
| replacement | String | A string to replace all occurrences of pattern. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) object to specify additional options. |

### Return Value

The number of replacements made.

## Remarks

Replaces the whole match captured by the regular expression.

Method is able to process breaks in both pattern and replacement strings.

You should use special meta-characters if you need to work with breaks:

* **&amp;p** - paragraph break
* **&amp;b** - section break
* **&amp;m** - page break
* **&amp;l** - manual line break
* **&amp;&amp;** - &amp; character

## Examples

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

// Replaces each number with paragraph break.
doc.Range.Replace(new Regex(@"\d+"), "&p", new FindReplaceOptions());
```

Shows how to replace all occurrences of a regular expression pattern with another string, while tracking all such replacements.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
    FindReplaceOptions options = new FindReplaceOptions();

    // Set a callback that tracks any replacements that the "Replace" method will make.
    TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
    options.ReplacingCallback = logger;

    doc.Range.Replace(new Regex("New York City|NYC"), "Washington", options);

    Assert.AreEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.GetText().Trim());

    Assert.AreEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node.", logger.GetLog().Trim());
}

/// <summary>
/// Maintains a log of every text replacement done by a find-and-replace operation
/// and notes the original matched text's value.
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

Shows how to insert an entire document's contents as a replacement of a match in a find-and-replace operation.

```csharp
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
    FindReplaceOptions options = new FindReplaceOptions();
    options.ReplacingCallback = new InsertDocumentAtReplaceHandler();

    mainDoc.Range.Replace(new Regex("\\[MY_DOCUMENT\\]"), "", options);
    mainDoc.Save(ArtifactsDir + "InsertDocument.InsertDocumentAtReplace.docx");

private class InsertDocumentAtReplaceHandler : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        Document subDoc = new Document(MyDir + "Document.docx");

        // Insert a document after the paragraph containing the matched text.
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        // Remove the paragraph with the matched text.
        para.Remove();

        return ReplaceAction.Skip;
    }
}

/// <summary>
/// Inserts all the nodes of another document after a paragraph or table.
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
                // Skip the node if it is the last empty paragraph in a section.
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

### See Also

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Range](../)
* namespace [Aspose.Words](../../range/)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
