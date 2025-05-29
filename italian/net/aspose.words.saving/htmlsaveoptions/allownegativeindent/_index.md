---
title: HtmlSaveOptions.AllowNegativeIndent
linktitle: AllowNegativeIndent
articleTitle: AllowNegativeIndent
second_title: Aspose.Words per .NET
description: Scopri la proprietà AllowNegativeIndent di HtmlSaveOptions per controllare i rientri dei paragrafi durante il salvataggio in HTML, MHTML o EPUB. Ottimizza la formattazione del tuo documento oggi stesso!
type: docs
weight: 20
url: /it/net/aspose.words.saving/htmlsaveoptions/allownegativeindent/
---
## HtmlSaveOptions.AllowNegativeIndent property

Specifica se i rientri negativi a sinistra e a destra dei paragrafi vengono normalizzati quando si salva in HTML, MHTML o EPUB. Il valore predefinito è`falso` .

```csharp
public bool AllowNegativeIndent { get; set; }
```

## Osservazioni

Se il rientro negativo non è consentito, il testo viene esportato come margine zero in HTML. Se il rientro negativo è consentito, un paragrafo potrebbe apparire parzialmente al di fuori della finestra del browser.

## Esempi

Mostra come preservare i rientri negativi nell'output .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce una tabella con un rientro negativo, che la spingerà a sinistra oltre il limite sinistro della pagina.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = -36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

builder.InsertBreak(BreakType.ParagraphBreak);

// Inserisce una tabella con un rientro positivo, che la sposterà verso destra.
table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = 36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

// Quando salviamo un documento in HTML, Aspose.Words conserverà solo i rientri negativi
// come quello che abbiamo applicato alla prima tabella se impostiamo il flag "AllowNegativeIndent"
// in un oggetto SaveOptions che passeremo a "true".
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    AllowNegativeIndent = allowNegativeIndent,
    TableWidthOutputMode = HtmlElementSizeOutputMode.RelativeOnly
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.NegativeIndent.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.NegativeIndent.html");

if (allowNegativeIndent)
{
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:-41.65pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
```

### Guarda anche

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
