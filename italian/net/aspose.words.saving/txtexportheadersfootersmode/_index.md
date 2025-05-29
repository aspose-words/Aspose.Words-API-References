---
title: TxtExportHeadersFootersMode Enum
linktitle: TxtExportHeadersFootersMode
articleTitle: TxtExportHeadersFootersMode
second_title: Aspose.Words per .NET
description: Scopri come l'enum TxtExportHeadersFootersMode di Aspose.Words migliora le esportazioni di testo normale personalizzando la gestione di intestazioni e piè di pagina per risultati ottimali.
type: docs
weight: 6440
url: /it/net/aspose.words.saving/txtexportheadersfootersmode/
---
## TxtExportHeadersFootersMode enumeration

Specifica il modo in cui intestazioni e piè di pagina vengono esportati in formato di testo normale.

```csharp
public enum TxtExportHeadersFootersMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Non vengono esportate intestazioni e piè di pagina. |
| PrimaryOnly | `1` | All'inizio e alla fine di ogni sezione vengono esportate solo le intestazioni e i piè di pagina principali. |
| AllAtEnd | `2` | Tutte le intestazioni e i piè di pagina vengono posizionati dopo tutti i corpi delle sezioni, alla fine di un documento. |

## Esempi

Mostra come specificare come esportare intestazioni e piè di pagina in formato testo normale.

```csharp
Document doc = new Document();

// Inserisce intestazioni/piè di pagina pari e principali nel documento.
// Le intestazioni e i piè di pagina primari sovrascriveranno le intestazioni e i piè di pagina pari.
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.HeaderEven));
doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderEven].AppendParagraph("Even header");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.FooterEven));
doc.FirstSection.HeadersFooters[HeaderFooterType.FooterEven].AppendParagraph("Even footer");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.HeaderPrimary));
doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].AppendParagraph("Primary header");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.FooterPrimary));
doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].AppendParagraph("Primary footer");

// Inserire pagine per visualizzare queste intestazioni e piè di pagina.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak); 
builder.Write("Page 3");

// Creiamo un oggetto "TxtSaveOptions", che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui salviamo il documento in testo normale.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// Imposta la proprietà "ExportHeadersFootersMode" su "TxtExportHeadersFootersMode.None"
// per non esportare intestazioni/piè di pagina.
// Imposta la proprietà "ExportHeadersFootersMode" su "TxtExportHeadersFootersMode.PrimaryOnly"
// per esportare solo intestazioni/piè di pagina primari.
// Imposta la proprietà "ExportHeadersFootersMode" su "TxtExportHeadersFootersMode.AllAtEnd"
// per posizionare tutte le intestazioni e i piè di pagina di tutte le sezioni alla fine del documento.
saveOptions.ExportHeadersFootersMode = txtExportHeadersFootersMode;

doc.Save(ArtifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt", saveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt");

string newLine = Environment.NewLine;
switch (txtExportHeadersFootersMode)
{
    case TxtExportHeadersFootersMode.AllAtEnd:
        Assert.AreEqual($"Page 1{newLine}" +
                        $"Page 2{newLine}" +
                        $"Page 3{newLine}" +
                        $"Even header{newLine}{newLine}" +
                        $"Primary header{newLine}{newLine}" +
                        $"Even footer{newLine}{newLine}" +
                        $"Primary footer{newLine}{newLine}", docText);
        break;
    case TxtExportHeadersFootersMode.PrimaryOnly:
        Assert.AreEqual($"Primary header{newLine}" +
                        $"Page 1{newLine}" +
                        $"Page 2{newLine}" +
                        $"Page 3{newLine}" +
                        $"Primary footer{newLine}", docText);
        break;
    case TxtExportHeadersFootersMode.None:
        Assert.AreEqual($"Page 1{newLine}" +
                        $"Page 2{newLine}" +
                        $"Page 3{newLine}", docText);
        break;
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
