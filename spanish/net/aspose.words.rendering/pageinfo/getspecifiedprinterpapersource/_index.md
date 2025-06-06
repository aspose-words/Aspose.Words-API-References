---
title: PageInfo.GetSpecifiedPrinterPaperSource
linktitle: GetSpecifiedPrinterPaperSource
articleTitle: GetSpecifiedPrinterPaperSource
second_title: Aspose.Words para .NET
description: Descubra el método GetSpecifiedPrinterPaperSource en PageInfo. Encuentre eficientemente el PaperSource ideal para una impresión de páginas fluida.
type: docs
weight: 100
url: /es/net/aspose.words.rendering/pageinfo/getspecifiedprinterpapersource/
---
## PageInfo.GetSpecifiedPrinterPaperSource method

Obtiene elPaperSource objeto adecuado para imprimir la página representada por este[`PageInfo`](../) .

```csharp
public PaperSource GetSpecifiedPrinterPaperSource(PaperSourceCollection paperSources, 
    PaperSource defaultPageSettingsPaperSource)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| paperSources | PaperSourceCollection | Fuentes de papel disponibles. |
| defaultPageSettingsPaperSource | PaperSource | Fuente de papel definida en la configuración predeterminada de la impresora. |

### Valor_devuelto

Un objeto que puede utilizar en el marco de impresión .NET para especificar la fuente del papel.

## Observaciones

Este método requiere .NET Framework 2.0 o posterior.

## Ejemplos

Muestra cómo imprimir información sobre el tamaño de página y la orientación de cada página de un documento de Word.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

La primera sección tiene dos páginas. Asignaremos una bandeja de papel de impresora diferente a cada una.
// cuyo número coincidirá con el tipo de fuente de papel. Estas fuentes y sus tipos varían.
// dependiendo del controlador de impresora instalado.
PrinterSettings.PaperSourceCollection paperSources = new PrinterSettings().PaperSources;

doc.FirstSection.PageSetup.FirstPageTray = paperSources[0].RawKind;
doc.FirstSection.PageSetup.OtherPagesTray = paperSources[1].RawKind;

Console.WriteLine("Document \"{0}\" contains {1} pages.", doc.OriginalFileName, doc.PageCount);

float scale = 1.0f;
float dpi = 96;

for (int i = 0; i < doc.PageCount; i++)
{
    // Cada página tiene un objeto PageInfo, cuyo índice es el número de la página respectiva.
    PageInfo pageInfo = doc.GetPageInfo(i);

    // Imprime la orientación y dimensiones de la página.
    Console.WriteLine($"Page {i + 1}:");
    Console.WriteLine($"\tOrientation:\t{(pageInfo.Landscape ? "Landscape" : "Portrait")}");
    Console.WriteLine($"\tPaper size:\t\t{pageInfo.PaperSize} ({pageInfo.WidthInPoints:F0}x{pageInfo.HeightInPoints:F0}pt)");
    Console.WriteLine($"\tSize in points:\t{pageInfo.SizeInPoints}");
    Console.WriteLine($"\tSize in pixels:\t{pageInfo.GetSizeInPixels(1.0f, 96)} at {scale * 100}% scale, {dpi} dpi");

    // Imprima la información de la bandeja de origen.
    Console.WriteLine($"\tTray:\t{pageInfo.PaperTray}");
    PaperSource source = pageInfo.GetSpecifiedPrinterPaperSource(paperSources, paperSources[0]);
    Console.WriteLine($"\tSuitable print source:\t{source.SourceName}, kind: {source.Kind}");
}
```

### Ver también

* class [PageInfo](../)
* espacio de nombres [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* asamblea [Aspose.Words](../../../)
