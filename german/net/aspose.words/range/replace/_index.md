---
title: Replace
second_title: Aspose.Words für .NET-API-Referenz
description: Ersetzt alle Vorkommen eines angegebenen Zeichenfolgenmusters durch eine Ersatzzeichenfolge.
type: docs
weight: 80
url: /de/net/aspose.words/range/replace/
---
## Replace(string, string) {#replace}

Ersetzt alle Vorkommen eines angegebenen Zeichenfolgenmusters durch eine Ersatzzeichenfolge.

```csharp
public int Replace(string pattern, string replacement)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pattern | String | Eine Zeichenfolge, die ersetzt werden soll. |
| replacement | String | Eine Zeichenfolge zum Ersetzen aller Vorkommen von Muster. |

### Rückgabewert

Die Anzahl der vorgenommenen Ersetzungen.

### Bemerkungen

Das Muster wird nicht als regulärer Ausdruck verwendet. Bitte verwenden[`Replace`](./replace/) wenn Sie reguläre Ausdrücke benötigen.

Verwendeter Vergleich ohne Berücksichtigung der Groß-/Kleinschreibung.

Die Methode kann Unterbrechungen sowohl in Muster- als auch in Ersatzzeichenfolgen verarbeiten.

Sie sollten spezielle Metazeichen verwenden, wenn Sie mit Umbrüchen arbeiten müssen:

* **&amp;p** - Absatzumbruch
* **&amp;b** - Abschnitt Pause
* **&amp;m** - Seitenumbruch
* **&amp;l** - manueller Zeilenumbruch

Methode verwenden[`Replace`](./replace/) um eine flexiblere Anpassung zu haben.

### Beispiele

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// Fügt einen Absatzumbruch nach Zahlen ein.
doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
```

Zeigt, wie Sie einen Suchen-und-Ersetzen-Textvorgang für den Inhalt eines Dokuments ausführen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Greetings, _FullName_!");

// Führen Sie eine Suchen-und-Ersetzen-Operation für den Inhalt unseres Dokuments durch und überprüfen Sie die Anzahl der Ersetzungen, die stattgefunden haben.
int replacementCount = doc.Range.Replace("_FullName_", "John Doe");

Assert.AreEqual(1, replacementCount);
Assert.AreEqual("Greetings, John Doe!", doc.GetText().Trim());
```

Zeigt, wie Formatierungen zu Absätzen hinzugefügt werden, in denen ein Suchen-und-Ersetzen-Vorgang Übereinstimmungen gefunden hat.

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

// Wir können ein "FindReplaceOptions"-Objekt verwenden, um den Suchen-und-Ersetzen-Prozess zu ändern.
FindReplaceOptions options = new FindReplaceOptions();

// Setzen Sie die Eigenschaft "Alignment" auf "ParagraphAlignment.Right", um jeden Absatz rechtsbündig auszurichten
// die eine Übereinstimmung enthält, die die Suchen-und-Ersetzen-Operation findet.
options.ApplyParagraphFormat.Alignment = ParagraphAlignment.Right;

// Ersetze jeden Punkt direkt vor einem Absatzumbruch durch ein Ausrufezeichen.
int count = doc.Range.Replace(".&p", "!&p", options);

Assert.AreEqual(2, count);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[2].ParagraphFormat.Alignment);
Assert.AreEqual("Every paragraph that ends with a full stop like this one will be right aligned!\r" +
                "This one will not!\r" +
                "This one also will!", doc.GetText().Trim());
```

### Siehe auch

* class [Range](../)
* namensraum [Aspose.Words](../../range/)
* Montage [Aspose.Words](../../../)

---

## Replace(Regex, string) {#replace_2}

Ersetzt alle Vorkommen eines durch einen regulären Ausdruck angegebenen Zeichenmusters durch eine andere Zeichenfolge.

```csharp
public int Replace(Regex pattern, string replacement)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pattern | Regex | Ein reguläres Ausdrucksmuster, das verwendet wird, um Übereinstimmungen zu finden. |
| replacement | String | Eine Zeichenfolge zum Ersetzen aller Vorkommen von Muster. |

### Rückgabewert

Die Anzahl der vorgenommenen Ersetzungen.

### Bemerkungen

Ersetzt die gesamte vom regulären Ausdruck erfasste Übereinstimmung.

Die Methode kann Unterbrechungen sowohl in Muster- als auch in Ersatzzeichenfolgen verarbeiten.

Sie sollten spezielle Metazeichen verwenden, wenn Sie mit Umbrüchen arbeiten müssen:

* **&amp;p** - Absatzumbruch
* **&amp;b** - Abschnitt Pause
* **&amp;m** - Seitenumbruch
* **&amp;l** - manueller Zeilenumbruch

Methode verwenden[`Replace`](./replace/) um eine flexiblere Anpassung zu haben.

### Beispiele

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

// Ersetzt jede Zahl durch einen Absatzumbruch.
doc.Range.Replace(new Regex(@"\d+"), "&p");
```

Zeigt, wie alle Vorkommen eines regulären Ausdrucksmusters durch anderen Text ersetzt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("I decided to get the curtains in gray, ideal for the grey-accented room.");

doc.Range.Replace(new Regex("gr(a|e)y"), "lavender");

Assert.AreEqual("I decided to get the curtains in lavender, ideal for the lavender-accented room.", doc.GetText().Trim());
```

### Siehe auch

* class [Range](../)
* namensraum [Aspose.Words](../../range/)
* Montage [Aspose.Words](../../../)

---

## Replace(string, string, FindReplaceOptions) {#replace_1}

Ersetzt alle Vorkommen eines angegebenen Zeichenfolgenmusters durch eine Ersatzzeichenfolge.

```csharp
public int Replace(string pattern, string replacement, FindReplaceOptions options)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pattern | String | Eine Zeichenfolge, die ersetzt werden soll. |
| replacement | String | Eine Zeichenfolge zum Ersetzen aller Vorkommen von Muster. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) Objekt, um zusätzliche Optionen anzugeben. |

### Rückgabewert

Die Anzahl der vorgenommenen Ersetzungen.

### Bemerkungen

Das Muster wird nicht als regulärer Ausdruck verwendet. Bitte verwenden[`Replace`](./replace/) wenn Sie reguläre Ausdrücke benötigen.

Die Methode kann Unterbrechungen sowohl in Muster- als auch in Ersatzzeichenfolgen verarbeiten.

Sie sollten spezielle Metazeichen verwenden, wenn Sie mit Umbrüchen arbeiten müssen:

* **&amp;p** - Absatzumbruch
* **&amp;b** - Abschnitt Pause
* **&amp;m** - Seitenumbruch
* **&amp;l** - manueller Zeilenumbruch
* **&amp;&amp;** - &amp; Charakter

### Beispiele

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// Fügt einen Absatzumbruch nach Zahlen ein.
doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
```

Zeigt, wie Text in der Fußzeile eines Dokuments ersetzt wird.

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

Zeigt, wie die Groß-/Kleinschreibung beim Ausführen eines Suchen-und-Ersetzen-Vorgangs umgeschaltet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Wir können ein "FindReplaceOptions"-Objekt verwenden, um den Suchen-und-Ersetzen-Prozess zu ändern.
FindReplaceOptions options = new FindReplaceOptions();

// Setzen Sie das "MatchCase"-Flag auf "true", um die Groß-/Kleinschreibung beim Suchen von zu ersetzenden Zeichenfolgen anzuwenden.
// Setzen Sie das "MatchCase"-Flag auf "false", um die Groß-/Kleinschreibung bei der Suche nach zu ersetzendem Text zu ignorieren.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

Zeigt, wie Sie eigenständige Suchen-und-Ersetzen-Operationen nur für Wörter umschalten können.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Wir können ein "FindReplaceOptions"-Objekt verwenden, um den Suchen-und-Ersetzen-Prozess zu ändern.
FindReplaceOptions options = new FindReplaceOptions();

// Setzen Sie das Flag "FindWholeWordsOnly" auf "true", um den gefundenen Text zu ersetzen, wenn er nicht Teil eines anderen Worts ist.
// Setzen Sie das Flag "FindWholeWordsOnly" auf "false", um den gesamten Text unabhängig von seiner Umgebung zu ersetzen.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

Zeigt, wie alle Instanzen von String of text in einer Tabelle und Zelle ersetzt werden.

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

// Führen Sie eine Suchen-und-Ersetzen-Operation für eine ganze Tabelle durch.
table.Range.Replace("Carrots", "Eggs", options);

// Ausführen einer Suchen-und-Ersetzen-Operation für die letzte Zelle der letzten Zeile der Tabelle.
table.LastRow.LastCell.Range.Replace("50", "20", options);

Assert.AreEqual("Eggs\a50\a\a" +
                "Potatoes\a20\a\a", table.GetText().Trim());
```

### Siehe auch

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Range](../)
* namensraum [Aspose.Words](../../range/)
* Montage [Aspose.Words](../../../)

---

## Replace(Regex, string, FindReplaceOptions) {#replace_3}

Ersetzt alle Vorkommen eines durch einen regulären Ausdruck angegebenen Zeichenmusters durch eine andere Zeichenfolge.

```csharp
public int Replace(Regex pattern, string replacement, FindReplaceOptions options)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pattern | Regex | Ein reguläres Ausdrucksmuster, das verwendet wird, um Übereinstimmungen zu finden. |
| replacement | String | Eine Zeichenfolge zum Ersetzen aller Vorkommen von Muster. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) Objekt, um zusätzliche Optionen anzugeben. |

### Rückgabewert

Die Anzahl der vorgenommenen Ersetzungen.

### Bemerkungen

Ersetzt die gesamte vom regulären Ausdruck erfasste Übereinstimmung.

Die Methode kann Unterbrechungen sowohl in Muster- als auch in Ersatzzeichenfolgen verarbeiten.

Sie sollten spezielle Metazeichen verwenden, wenn Sie mit Umbrüchen arbeiten müssen:

* **&amp;p** - Absatzumbruch
* **&amp;b** - Abschnitt Pause
* **&amp;m** - Seitenumbruch
* **&amp;l** - manueller Zeilenumbruch
* **&amp;&amp;** - &amp; Charakter

### Beispiele

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

// Ersetzt jede Zahl durch einen Absatzumbruch.
doc.Range.Replace(new Regex(@"\d+"), "&p", new FindReplaceOptions());
```

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

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Range](../)
* namensraum [Aspose.Words](../../range/)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
