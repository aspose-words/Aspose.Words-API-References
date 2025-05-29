---
title: HtmlSaveOptions.TableWidthOutputMode
linktitle: TableWidthOutputMode
articleTitle: TableWidthOutputMode
second_title: Aspose.Words per .NET
description: Ottimizza le tue esportazioni HTML con HtmlSaveOptions TableWidthOutputMode. Controlla la larghezza delle righe e delle celle della tabella per una formattazione MHTML ed EPUB impeccabile.
type: docs
weight: 480
url: /it/net/aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/
---
## HtmlSaveOptions.TableWidthOutputMode property

Controlla come le larghezze di tabelle, righe e celle vengono esportate in HTML, MHTML o EPUB. Il valore predefinito èAll .

```csharp
public HtmlElementSizeOutputMode TableWidthOutputMode { get; set; }
```

## Osservazioni

Nel formato HTML, elementi tabella, riga e cella (**&lt;tabella&gt;** ,**&lt;tr&gt;** ,**&lt;esimo&gt;** ,**&lt;td&gt;**) può avere la larghezza specificata in unità relative (percentuale) o in unità assolute. In un documento in Aspose, anche parole, tabelle, righe e celle possono avere la loro larghezza specificata utilizzando unità relative o assolute.

Quando si converte un documento in HTML utilizzando Aspose.Words, potrebbe essere necessario controllare il modo in cui vengono esportate le larghezze di tabelle, righe e celle per influenzare il modo in cui il documento risultante viene visualizzato nell'agente visivo (ad esempio un browser o un visualizzatore).

Utilizzare questa proprietà come filtro per specificare quali valori di larghezza delle tabelle esportare nel documento di destinazione. Ad esempio, se si converte un documento in EPUB e si intende visualizzarlo su un dispositivo di lettura mobile, probabilmente si desidera evitare di esportare valori di larghezza assoluti. Per fare ciò, è necessario specificare la modalità di output.RelativeOnly ONone in modo che chi visualizza la tabella sul dispositivo mobile possa adattarla il più possibile alla larghezza dello schermo.

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

* enum [HtmlElementSizeOutputMode](../../htmlelementsizeoutputmode/)
* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
