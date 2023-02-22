---
title: HtmlSaveOptions.TableWidthOutputMode
second_title: Aspose.Words per .NET API Reference
description: HtmlSaveOptions proprietà. Controlla come le larghezze di tabelle righe e celle vengono esportate in HTML MHTML o EPUB. Il valore predefinito èAll .
type: docs
weight: 460
url: /it/net/aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/
---
## HtmlSaveOptions.TableWidthOutputMode property

Controlla come le larghezze di tabelle, righe e celle vengono esportate in HTML, MHTML o EPUB. Il valore predefinito èAll .

```csharp
public HtmlElementSizeOutputMode TableWidthOutputMode { get; set; }
```

### Osservazioni

Nel formato HTML, gli elementi di tabella, riga e cella ( **&lt;tabella&gt;** , **&lt;tr&gt;** , **&lt;i&gt;** , **&lt;td&gt;**) può avere la larghezza specificata in unità relative (percentuali) o assolute. In un documento in Aspose.Words, tabelle, righe e celle possono avere la larghezza specificata utilizzando anche unità relative o assolute.

Quando converti un documento in HTML usando Aspose.Words, potresti voler controllare come le larghezze di tabelle, righe e celle vengono esportate per influenzare il modo in cui il documento risultante viene visualizzato nell'agente visivo (ad esempio un browser o un visualizzatore).

Utilizza questa proprietà come filtro per specificare quali valori di larghezza della tabella vengono esportati nel documento di destinazione. Ad esempio, se stai convertendo un documento in EPUB e intendi visualizzare il documento su un dispositivo di lettura mobile, probabilmente vorrai evitare esportare valori di larghezza assoluti. Per fare ciò è necessario specificare la modalità di outputRelativeOnly oNone in modo che lo spettatore sul dispositivo mobile possa disporre il tavolo per adattarlo alla larghezza dello schermo nel miglior modo possibile.

### Esempi

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

// Inserisce una tabella con un rientro positivo, che spingerà la tabella a destra.
table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = 36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

// Quando salviamo un documento in HTML, Aspose.Words conserverà solo i rientri negativi
// come quello che abbiamo applicato alla prima tabella se impostiamo il flag "AllowNegativeIndent".
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

* enum [HtmlElementSizeOutputMode](../../htmlelementsizeoutputmode/)
* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../htmlsaveoptions/)
* assemblea [Aspose.Words](../../../)


