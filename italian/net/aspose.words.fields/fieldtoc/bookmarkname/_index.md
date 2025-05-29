---
title: FieldToc.BookmarkName
linktitle: BookmarkName
articleTitle: BookmarkName
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldToc BookmarkName per gestire facilmente i segnalibri nei tuoi documenti, migliorando la creazione e l'organizzazione delle tabelle senza sforzi.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldtoc/bookmarkname/
---
## FieldToc.BookmarkName property

Ottiene o imposta il nome del segnalibro che contrassegna la parte del documento utilizzata per creare la tabella.

```csharp
public string BookmarkName { get; set; }
```

## Esempi

Mostra come inserire un indice e popolarlo con voci in base agli stili di intestazione.

```csharp
public void FieldToc()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");

    // Inserire un campo TOC, che compilerà tutte le intestazioni in un indice.
    // Per ogni titolo, questo campo creerà una riga con il testo in quello stile di titolo a sinistra,
    // e la pagina in cui appare l'intestazione sulla destra.
    FieldToc field = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Utilizzare la proprietà BookmarkName per elencare solo le intestazioni
    // che compaiono all'interno dei limiti di un segnalibro con il nome "MyBookmark".
    field.BookmarkName = "MyBookmark";

    // Il testo a cui è applicato uno stile di intestazione incorporato, ad esempio "Intestazione 1", verrà conteggiato come intestazione.
    // In questa proprietà possiamo nominare stili aggiuntivi da selezionare come titoli dall'indice e i relativi livelli di indice.
    field.CustomStyles = "Quote; 6; Intense Quote; 7";

    // Per impostazione predefinita, i livelli Stili/TOC sono separati nella proprietà CustomStyles da una virgola,
    // ma possiamo impostare un delimitatore personalizzato in questa proprietà.
    doc.FieldOptions.CustomTocStyleSeparator = ";";

    // Configurare il campo per escludere tutte le intestazioni con livelli di indice al di fuori di questo intervallo.
    field.HeadingLevelRange = "1-3";

    // L'indice non visualizzerà i numeri di pagina dei titoli i cui livelli rientrano in questo intervallo.
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

    // I numeri di pagina di queste due intestazioni saranno omessi perché rientrano nell'intervallo "2-5".
    InsertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
    InsertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

    // Questa voce non viene visualizzata perché "Titolo 4" è al di fuori dell'intervallo "1-3" impostato in precedenza.
    InsertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

    builder.EndBookmark("MyBookmark");
    builder.Writeln("Paragraph text.");

    // Questa voce non viene visualizzata perché è esterna al segnalibro specificato dall'indice.
    InsertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

    Assert.AreEqual(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.GetFieldCode());

    field.UpdatePageNumbers();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOC.docx");
}

/// <summary>
/// Inizia una nuova pagina e inserisci un paragrafo con uno stile specificato.
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
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
