---
title: PageInfo.GetSpecifiedPrinterPaperSource
linktitle: GetSpecifiedPrinterPaperSource
articleTitle: GetSpecifiedPrinterPaperSource
second_title: Aspose.Words per .NET
description: Scopri il metodo GetSpecifiedPrinterPaperSource in PageInfo. Recupera in modo efficiente il PaperSource ideale per una stampa impeccabile.
type: docs
weight: 100
url: /it/net/aspose.words.rendering/pageinfo/getspecifiedprinterpapersource/
---
## PageInfo.GetSpecifiedPrinterPaperSource method

Ottiene ilPaperSource oggetto adatto per stampare la pagina rappresentata da questo[`PageInfo`](../) .

```csharp
public PaperSource GetSpecifiedPrinterPaperSource(PaperSourceCollection paperSources, 
    PaperSource defaultPageSettingsPaperSource)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| paperSources | PaperSourceCollection | Fonti cartacee disponibili. |
| defaultPageSettingsPaperSource | PaperSource | Origine carta definita nelle impostazioni predefinite della stampante. |

### Valore di ritorno

Un oggetto che è possibile utilizzare nel framework di stampa .NET per specificare l'origine della carta.

## Osservazioni

Questo metodo richiede .NET Framework 2.0 o versione successiva.

## Esempi

Mostra come stampare le informazioni relative alle dimensioni e all'orientamento della pagina per ogni pagina di un documento Word.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// La prima sezione è composta da 2 pagine. Assegneremo a ciascuna un vassoio carta diverso,
// il cui numero corrisponderà a un tipo di fonte cartacea. Queste fonti e i loro tipi varieranno
// a seconda del driver della stampante installato.
PrinterSettings.PaperSourceCollection paperSources = new PrinterSettings().PaperSources;

doc.FirstSection.PageSetup.FirstPageTray = paperSources[0].RawKind;
doc.FirstSection.PageSetup.OtherPagesTray = paperSources[1].RawKind;

Console.WriteLine("Document \"{0}\" contains {1} pages.", doc.OriginalFileName, doc.PageCount);

float scale = 1.0f;
float dpi = 96;

for (int i = 0; i < doc.PageCount; i++)
{
    // Ogni pagina ha un oggetto PageInfo, il cui indice è il numero della rispettiva pagina.
    PageInfo pageInfo = doc.GetPageInfo(i);

    // Stampa l'orientamento e le dimensioni della pagina.
    Console.WriteLine($"Page {i + 1}:");
    Console.WriteLine($"\tOrientation:\t{(pageInfo.Landscape ? "Landscape" : "Portrait")}");
    Console.WriteLine($"\tPaper size:\t\t{pageInfo.PaperSize} ({pageInfo.WidthInPoints:F0}x{pageInfo.HeightInPoints:F0}pt)");
    Console.WriteLine($"\tSize in points:\t{pageInfo.SizeInPoints}");
    Console.WriteLine($"\tSize in pixels:\t{pageInfo.GetSizeInPixels(1.0f, 96)} at {scale * 100}% scale, {dpi} dpi");

    // Stampa le informazioni sul vassoio di origine.
    Console.WriteLine($"\tTray:\t{pageInfo.PaperTray}");
    PaperSource source = pageInfo.GetSpecifiedPrinterPaperSource(paperSources, paperSources[0]);
    Console.WriteLine($"\tSuitable print source:\t{source.SourceName}, kind: {source.Kind}");
}
```

### Guarda anche

* class [PageInfo](../)
* spazio dei nomi [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* assemblea [Aspose.Words](../../../)
