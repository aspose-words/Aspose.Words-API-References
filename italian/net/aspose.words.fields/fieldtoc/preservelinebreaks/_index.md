---
title: FieldToc.PreserveLineBreaks
second_title: Aspose.Words per .NET API Reference
description: FieldToc proprietà. Ottiene o imposta se conservare i caratteri di nuova riga allinterno delle voci della tabella.
type: docs
weight: 130
url: /it/net/aspose.words.fields/fieldtoc/preservelinebreaks/
---
## FieldToc.PreserveLineBreaks property

Ottiene o imposta se conservare i caratteri di nuova riga all'interno delle voci della tabella.

```csharp
public bool PreserveLineBreaks { get; set; }
```

### Esempi

Mostra come inserire un sommario e popolarlo con voci basate sugli stili di intestazione.

```csharp
public void FieldToc()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");

    // Inserisci un campo TOC, che compilerà tutte le intestazioni in un sommario.
    // Per ogni intestazione, questo campo creerà una riga con il testo in quello stile di intestazione a sinistra,
    // e la pagina in cui appare l'intestazione a destra.
    FieldToc field = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Utilizza la proprietà BookmarkName per elencare solo le intestazioni
    // che appaiono all'interno dei limiti di un segnalibro con il nome "MyBookmark".
    field.BookmarkName = "MyBookmark";

    // Il testo con uno stile di titolo integrato, ad esempio "Titolo 1", applicato ad esso verrà conteggiato come titolo.
    // Possiamo nominare stili aggiuntivi da raccogliere come intestazioni dal TOC in questa proprietà e i relativi livelli TOC.
    field.CustomStyles = "Quote; 6; Intense Quote; 7";

    // Per impostazione predefinita, i livelli Stili/TOC sono separati nella proprietà CustomStyles da una virgola,
    // ma possiamo impostare un delimitatore personalizzato in questa proprietà.
    doc.FieldOptions.CustomTocStyleSeparator = ";";

    // Configura il campo per escludere eventuali intestazioni con livelli di sommario esterni a questo intervallo.
    field.HeadingLevelRange = "1-3";

    // Il sommario non visualizzerà i numeri di pagina delle intestazioni i cui livelli di sommario rientrano in questo intervallo.
    field.PageNumberOmittingLevelRange = "2-5";

     // Imposta una stringa personalizzata che separerà ogni intestazione dal suo numero di pagina.
    field.EntrySeparator = "-";
    field.InsertHyperlinks = true;
    field.HideInWebLayout = false;
    field.PreserveLineBreaks = true;
    field.PreserveTabs = true;
    field.UseParagraphOutlineLevel = false;

    InsertNewPageWithHeading(builder, "First entry", "Heading 1");
    builder.Writeln("Paragraph text.");
    InsertNewPageWithHeading(builder, "Second entry", "Heading 1");
    InsertNewPageWithHeading(builder, "Third entry", "Quote");
    InsertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

    // Queste due intestazioni avranno i numeri di pagina omessi perché rientrano nell'intervallo "2-5".
    InsertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
    InsertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

    // Questa voce non viene visualizzata perché "Intestazione 4" non rientra nell'intervallo "1-3" impostato in precedenza.
    InsertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

    builder.EndBookmark("MyBookmark");
    builder.Writeln("Paragraph text.");

    // Questa voce non viene visualizzata perché è esterna al segnalibro specificato dal sommario.
    InsertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

    Assert.AreEqual(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.GetFieldCode());

    field.UpdatePageNumbers();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOC.docx");
}

/// <summary>
/// Inizia una nuova pagina e inserisce un paragrafo con lo stile specificato.
/// </summary>
public void InsertNewPageWithHeading(DocumentBuilder builder, string captionText, string styleName)
{
    builder.InsertBreak(BreakType.PageBreak);
    string originalStyle = builder.ParagraphFormat.StyleName;
    builder.ParagraphFormat.Style = builder.Document.Styles[styleName];
    builder.Writeln(captionText);
    builder.ParagraphFormat.Style = builder.Document.Styles[originalStyle];
}
```

### Guarda anche

* class [FieldToc](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldtoc/)
* assemblea [Aspose.Words](../../../)


