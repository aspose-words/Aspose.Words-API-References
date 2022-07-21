---
title: Replace
second_title: Aspose.Words per .NET API Reference
description: Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa di sostituzione.
type: docs
weight: 80
url: /it/net/aspose.words/range/replace/
---
## Replace(string, string) {#replace}

Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa di sostituzione.

```csharp
public int Replace(string pattern, string replacement)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pattern | String | Una stringa da sostituire. |
| replacement | String | Una stringa per sostituire tutte le occorrenze di pattern. |

### Valore di ritorno

Il numero di sostituzioni effettuate.

### Osservazioni

Il modello non verrà utilizzato come espressione regolare. Utilizzare[`Replace`](../replace) se hai bisogno di espressioni regolari.

Usato confronto senza distinzione tra maiuscole e minuscole.

Il metodo è in grado di elaborare le interruzioni sia nel pattern che nelle stringhe di sostituzione.

Dovresti usare meta-caratteri speciali se devi lavorare con le interruzioni:

* **&amp;p** - interruzione di paragrafo
* **&amp;b** - interruzione di sezione
* **&amp;m** - interruzione di pagina
* **&amp;l** - interruzione di riga manuale

Usa metodo[`Replace`](../replace) per avere una personalizzazione più flessibile.

### Esempi

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// Inserisce un'interruzione di paragrafo dopo Numbers.
doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
```

Mostra come eseguire un'operazione di ricerca e sostituzione del testo sul contenuto di un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Greetings, _FullName_!");

// Esegui un'operazione di ricerca e sostituzione sul contenuto del nostro documento e verifica il numero di sostituzioni avvenute.
int replacementCount = doc.Range.Replace("_FullName_", "John Doe");

Assert.AreEqual(1, replacementCount);
Assert.AreEqual("Greetings, John Doe!", doc.GetText().Trim());
```

Mostra come aggiungere la formattazione ai paragrafi in cui un'operazione trova e sostituisci ha trovato corrispondenze.

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

// Possiamo usare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
FindReplaceOptions options = new FindReplaceOptions();

// Imposta la proprietà "Alignment" su "ParagraphAlignment.Right" per allineare a destra ogni paragrafo
// che contiene una corrispondenza trovata dall'operazione trova e sostituisci.
options.ApplyParagraphFormat.Alignment = ParagraphAlignment.Right;

// Sostituisci ogni punto fermo prima di un'interruzione di paragrafo con un punto esclamativo.
int count = doc.Range.Replace(".&p", "!&p", options);

Assert.AreEqual(2, count);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[2].ParagraphFormat.Alignment);
Assert.AreEqual("Every paragraph that ends with a full stop like this one will be right aligned!\r" +
                "This one will not!\r" +
                "This one also will!", doc.GetText().Trim());
```

### Guarda anche

* class [Range](../../range)
* spazio dei nomi [Aspose.Words](../../range)
* assemblea [Aspose.Words](../../../)

---

## Replace(Regex, string) {#replace_2}

Sostituisce tutte le occorrenze di una sequenza di caratteri specificata da un'espressione regolare con un'altra stringa.

```csharp
public int Replace(Regex pattern, string replacement)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pattern | Regex | Un modello di espressione regolare utilizzato per trovare corrispondenze. |
| replacement | String | Una stringa per sostituire tutte le occorrenze di pattern. |

### Valore di ritorno

Il numero di sostituzioni effettuate.

### Osservazioni

Sostituisce l'intera corrispondenza acquisita dall'espressione regolare.

Il metodo è in grado di elaborare le interruzioni sia nel pattern che nelle stringhe di sostituzione.

Dovresti usare meta-caratteri speciali se devi lavorare con le interruzioni:

* **&amp;p** - interruzione di paragrafo
* **&amp;b** - interruzione di sezione
* **&amp;m** - interruzione di pagina
* **&amp;l** - interruzione di riga manuale

Usa metodo[`Replace`](../replace) per avere una personalizzazione più flessibile.

### Esempi

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

// Sostituisce ogni numero con un'interruzione di paragrafo.
doc.Range.Replace(new Regex(@"\d+"), "&p");
```

Mostra come sostituire tutte le occorrenze di un modello di espressione regolare con altro testo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("I decided to get the curtains in gray, ideal for the grey-accented room.");

doc.Range.Replace(new Regex("gr(a|e)y"), "lavender");

Assert.AreEqual("I decided to get the curtains in lavender, ideal for the lavender-accented room.", doc.GetText().Trim());
```

### Guarda anche

* class [Range](../../range)
* spazio dei nomi [Aspose.Words](../../range)
* assemblea [Aspose.Words](../../../)

---

## Replace(string, string, FindReplaceOptions) {#replace_1}

Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa di sostituzione.

```csharp
public int Replace(string pattern, string replacement, FindReplaceOptions options)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pattern | String | Una stringa da sostituire. |
| replacement | String | Una stringa per sostituire tutte le occorrenze di pattern. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions) oggetto per specificare opzioni aggiuntive. |

### Valore di ritorno

Il numero di sostituzioni effettuate.

### Osservazioni

Il modello non verrà utilizzato come espressione regolare. Utilizzare[`Replace`](../replace) se hai bisogno di espressioni regolari.

Il metodo è in grado di elaborare le interruzioni sia nel pattern che nelle stringhe di sostituzione.

Dovresti usare meta-caratteri speciali se devi lavorare con le interruzioni:

* **&amp;p** - interruzione di paragrafo
* **&amp;b** - interruzione di sezione
* **&amp;m** - interruzione di pagina
* **&amp;l** - interruzione di riga manuale
* **&amp;&amp;** - &amp; carattere

### Esempi

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// Inserisce un'interruzione di paragrafo dopo Numbers.
doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
```

Mostra come sostituire il testo nel piè di pagina di un documento.

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

Mostra come attivare la distinzione tra maiuscole e minuscole durante l'esecuzione di un'operazione di ricerca e sostituzione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Possiamo usare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
FindReplaceOptions options = new FindReplaceOptions();

// Imposta il flag "MatchCase" su "true" per applicare la distinzione tra maiuscole e minuscole mentre trovi le stringhe da sostituire.
// Imposta il flag "MatchCase" su "false" per ignorare il carattere maiuscolo durante la ricerca del testo da sostituire.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

Mostra come attivare o disattivare le operazioni di ricerca e sostituzione di sole parole autonome.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Possiamo usare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
FindReplaceOptions options = new FindReplaceOptions();

// Imposta il flag "FindWholeWordsOnly" su "true" per sostituire il testo trovato se non fa parte di un'altra parola.
// Imposta il flag "FindWholeWordsOnly" su "false" per sostituire tutto il testo indipendentemente dall'ambiente circostante.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

Mostra come sostituire tutte le istanze di String of text in una tabella e in una cella.

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

// Esegue un'operazione di ricerca e sostituzione su un'intera tabella.
table.Range.Replace("Carrots", "Eggs", options);

// Esegue un'operazione di ricerca e sostituzione sull'ultima cella dell'ultima riga della tabella.
table.LastRow.LastCell.Range.Replace("50", "20", options);

Assert.AreEqual("Eggs\a50\a\a" +
                "Potatoes\a20\a\a", table.GetText().Trim());
```

### Guarda anche

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions)
* class [Range](../../range)
* spazio dei nomi [Aspose.Words](../../range)
* assemblea [Aspose.Words](../../../)

---

## Replace(Regex, string, FindReplaceOptions) {#replace_3}

Sostituisce tutte le occorrenze di una sequenza di caratteri specificata da un'espressione regolare con un'altra stringa.

```csharp
public int Replace(Regex pattern, string replacement, FindReplaceOptions options)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pattern | Regex | Un modello di espressione regolare utilizzato per trovare corrispondenze. |
| replacement | String | Una stringa per sostituire tutte le occorrenze di pattern. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions) oggetto per specificare opzioni aggiuntive. |

### Valore di ritorno

Il numero di sostituzioni effettuate.

### Osservazioni

Sostituisce l'intera corrispondenza acquisita dall'espressione regolare.

Il metodo è in grado di elaborare le interruzioni sia nel pattern che nelle stringhe di sostituzione.

Dovresti usare meta-caratteri speciali se devi lavorare con le interruzioni:

* **&amp;p** - interruzione di paragrafo
* **&amp;b** - interruzione di sezione
* **&amp;m** - interruzione di pagina
* **&amp;l** - interruzione di riga manuale
* **&amp;&amp;** - &amp; carattere

### Esempi

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

// Sostituisce ogni numero con un'interruzione di paragrafo.
doc.Range.Replace(new Regex(@"\d+"), "&p", new FindReplaceOptions());
```

Mostra come sostituire tutte le occorrenze di un modello di espressione regolare con un'altra stringa, tenendo traccia di tutte queste sostituzioni.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // Possiamo usare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
    FindReplaceOptions options = new FindReplaceOptions();

    // Imposta un callback che tenga traccia di tutte le sostituzioni che il metodo "Replace" effettuerà.
    TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
    options.ReplacingCallback = logger;

    doc.Range.Replace(new Regex("New York City|NYC"), "Washington", options);

    Assert.AreEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.GetText().Trim());

    Assert.AreEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node.", logger.GetLog().Trim());
}

/// <summary>
/// Mantiene un registro di ogni sostituzione di testo eseguita da un'operazione di ricerca e sostituzione
/// e annota il valore del testo corrispondente originale.
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

Mostra come inserire il contenuto di un intero documento in sostituzione di una corrispondenza in un'operazione di ricerca e sostituzione.

```csharp
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // Possiamo usare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
    FindReplaceOptions options = new FindReplaceOptions();
    options.ReplacingCallback = new InsertDocumentAtReplaceHandler();

    mainDoc.Range.Replace(new Regex("\\[MY_DOCUMENT\\]"), "", options);
    mainDoc.Save(ArtifactsDir + "InsertDocument.InsertDocumentAtReplace.docx");

private class InsertDocumentAtReplaceHandler : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        Document subDoc = new Document(MyDir + "Document.docx");

        // Inserisce un documento dopo il paragrafo contenente il testo corrispondente.
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        // Rimuovi il paragrafo con il testo corrispondente.
        para.Remove();

        return ReplaceAction.Skip;
    }
}

/// <summary>
/// Inserisce tutti i nodi di un altro documento dopo un paragrafo o una tabella.
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
                // Salta il nodo se è l'ultimo paragrafo vuoto in una sezione.
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

### Guarda anche

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions)
* class [Range](../../range)
* spazio dei nomi [Aspose.Words](../../range)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
