---
title: Class PageInfo
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Rendering.PageInfo classe. Rappresenta informazioni su una particolare pagina del documento.
type: docs
weight: 4570
url: /it/net/aspose.words.rendering/pageinfo/
---
## PageInfo class

Rappresenta informazioni su una particolare pagina del documento.

Per saperne di più, visita il[Rendering](https://docs.aspose.com/words/net/rendering/) articolo di documentazione.

```csharp
public class PageInfo
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Colored](../../aspose.words.rendering/pageinfo/colored/) { get; } | Restituisce`VERO` se la pagina contiene contenuti colorati. |
| [HeightInPoints](../../aspose.words.rendering/pageinfo/heightinpoints/) { get; } | Ottiene l'altezza della pagina in punti. |
| [Landscape](../../aspose.words.rendering/pageinfo/landscape/) { get; } | Restituisce`VERO` se l'orientamento della pagina specificato nel documento per questa pagina è orizzontale. |
| [PaperSize](../../aspose.words.rendering/pageinfo/papersize/) { get; } | Ottiene la dimensione del foglio come enumerazione. |
| [PaperTray](../../aspose.words.rendering/pageinfo/papertray/) { get; } | Ottiene il vassoio della carta (contenitore) per questa pagina come specificato nel documento. Il valore è specifico dell'implementazione (stampante). |
| [SizeInPoints](../../aspose.words.rendering/pageinfo/sizeinpoints/) { get; } | Ottiene la dimensione della pagina in punti. |
| [WidthInPoints](../../aspose.words.rendering/pageinfo/widthinpoints/) { get; } | Ottiene la larghezza della pagina in punti. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetDotNetPaperSize](../../aspose.words.rendering/pageinfo/getdotnetpapersize/)(PaperSizeCollection) | Ottiene il filePaperSize oggetto adatto a stampare la pagina rappresentata da questo`PageInfo` . |
| [GetSizeInPixels](../../aspose.words.rendering/pageinfo/getsizeinpixels/#getsizeinpixels)(float, float) | Calcola la dimensione della pagina in pixel per un fattore di zoom e una risoluzione specificati. |
| [GetSizeInPixels](../../aspose.words.rendering/pageinfo/getsizeinpixels/#getsizeinpixels_1)(float, float, float) | Calcola la dimensione della pagina in pixel per un fattore di zoom e una risoluzione specificati. |
| [GetSpecifiedPrinterPaperSource](../../aspose.words.rendering/pageinfo/getspecifiedprinterpapersource/)(PaperSourceCollection, PaperSource) | Ottiene il filePaperSource oggetto adatto a stampare la pagina rappresentata da questo`PageInfo` . |

### Osservazioni

La larghezza e l'altezza della pagina restituite da questo oggetto rappresentano la dimensione "finale" della pagina, ad esempio sono già ruotate nell'orientamento corretto.

### Esempi

Mostra come stampare le informazioni sulle dimensioni e sull'orientamento della pagina per ogni pagina di un documento Word.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// La prima sezione ha 2 pagine. Assegneremo a ciascuno un vassoio carta diverso per la stampante,
// il cui numero corrisponderà a un tipo di origine cartacea. Queste fonti e i loro tipi varieranno
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

* spazio dei nomi [Aspose.Words.Rendering](../../aspose.words.rendering/)
* assemblea [Aspose.Words](../../)


