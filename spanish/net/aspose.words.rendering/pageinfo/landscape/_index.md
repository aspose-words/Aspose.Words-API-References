---
title: PageInfo.Landscape
second_title: Referencia de API de Aspose.Words para .NET
description: PageInfo propiedad. Devuelve verdadero si la orientación de la página especificada en el documento para esta página es horizontal.
type: docs
weight: 20
url: /es/net/aspose.words.rendering/pageinfo/landscape/
---
## PageInfo.Landscape property

Devuelve verdadero si la orientación de la página especificada en el documento para esta página es horizontal.

```csharp
public bool Landscape { get; }
```

### Ejemplos

Muestra cómo imprimir información sobre el tamaño y la orientación de la página para cada página de un documento de Word.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// La primera sección tiene 2 páginas. Asignaremos una bandeja de papel de impresora diferente a cada uno,
// cuyo número coincidirá con un tipo de fuente de papel. Estas fuentes y sus tipos variarán
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

    // Imprime la orientación y las dimensiones de la página.
    Console.WriteLine($"Page {i + 1}:");
    Console.WriteLine($"\tOrientation:\t{(pageInfo.Landscape ? "Landscape" : "Portrait")}");
    Console.WriteLine($"\tPaper size:\t\t{pageInfo.PaperSize} ({pageInfo.WidthInPoints:F0}x{pageInfo.HeightInPoints:F0}pt)");
    Console.WriteLine($"\tSize in points:\t{pageInfo.SizeInPoints}");
    Console.WriteLine($"\tSize in pixels:\t{pageInfo.GetSizeInPixels(1.0f, 96)} at {scale * 100}% scale, {dpi} dpi");

    // Imprimir la información de la bandeja de origen.
    Console.WriteLine($"\tTray:\t{pageInfo.PaperTray}");
    PaperSource source = pageInfo.GetSpecifiedPrinterPaperSource(paperSources, paperSources[0]);
    Console.WriteLine($"\tSuitable print source:\t{source.SourceName}, kind: {source.Kind}");
}
```

Muestra cómo personalizar la impresión de documentos de Aspose.Words.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

    MyPrintDocument printDoc = new MyPrintDocument(doc);
    printDoc.PrinterSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;
    printDoc.PrinterSettings.FromPage = 1;
    printDoc.PrinterSettings.ToPage = 1;

    printDoc.Print();
}

/// <summary>
/// Selecciona un tamaño de papel, una orientación y una bandeja de papel apropiados al imprimir.
/// </summary>
public class MyPrintDocument : PrintDocument
{
    public MyPrintDocument(Document document)
    {
        mDocument = document;
    }

    /// <summary>
    /// Inicializa el rango de páginas a imprimir según la selección del usuario.
    /// </summary>
    protected override void OnBeginPrint(PrintEventArgs e)
    {
        base.OnBeginPrint(e);

        switch (PrinterSettings.PrintRange)
        {
            case System.Drawing.Printing.PrintRange.AllPages:
                mCurrentPage = 1;
                mPageTo = mDocument.PageCount;
                break;
            case System.Drawing.Printing.PrintRange.SomePages:
                mCurrentPage = PrinterSettings.FromPage;
                mPageTo = PrinterSettings.ToPage;
                break;
            default:
                throw new InvalidOperationException("Unsupported print range.");
        }
    }

    /// <summary>
    /// Se llama antes de que se imprima cada página. 
    /// </summary>
    protected override void OnQueryPageSettings(QueryPageSettingsEventArgs e)
    {
        base.OnQueryPageSettings(e);

        // Un solo documento de Microsoft Word puede tener múltiples secciones que especifican páginas con diferentes tamaños, 
        // orientaciones y bandejas de papel. El framework de impresión .NET llama a este código antes 
        // se imprime cada página, lo que nos da la oportunidad de especificar cómo imprimir la página actual.
        PageInfo pageInfo = mDocument.GetPageInfo(mCurrentPage - 1);
        e.PageSettings.PaperSize = pageInfo.GetDotNetPaperSize(PrinterSettings.PaperSizes);

        // Microsoft Word almacena el origen del papel (bandeja de la impresora) para cada sección como un valor específico de la impresora.
        // Para obtener el valor correcto de la bandeja, deberá utilizar la propiedad "RawKind", que debe devolver su impresora.
        e.PageSettings.PaperSource.RawKind = pageInfo.PaperTray;
        e.PageSettings.Landscape = pageInfo.Landscape;
    }

    /// <summary>
    /// Llamado para que cada página la renderice para su impresión. 
    /// </summary>
    protected override void OnPrintPage(PrintPageEventArgs e)
    {
        base.OnPrintPage(e);

        // El motor de renderizado Aspose.Words crea una página dibujada desde el origen (x = 0, y = 0) del papel.
        // Habrá un margen duro en la impresora, que representará cada página. Necesitamos compensar por ese margen duro.
        float hardOffsetX, hardOffsetY;

        // A continuación se muestran dos formas de establecer un margen rígido.
        if (e.PageSettings != null && e.PageSettings.HardMarginX != 0 && e.PageSettings.HardMarginY != 0)
        {
            // 1 - A través de la propiedad "PageSettings".
            hardOffsetX = e.PageSettings.HardMarginX;
            hardOffsetY = e.PageSettings.HardMarginY;
        }
        else
        {
            // 2 - Usando nuestros propios valores, si la propiedad "PageSettings" no está disponible.
            hardOffsetX = 20;
            hardOffsetY = 20;
        }

        mDocument.RenderToScale(mCurrentPage, e.Graphics, -hardOffsetX, -hardOffsetY, 1.0f);

        mCurrentPage++;
        e.HasMorePages = mCurrentPage <= mPageTo;
    }

    private readonly Document mDocument;
    private int mCurrentPage;
    private int mPageTo;
}
```

### Ver también

* class [PageInfo](../)
* espacio de nombres [Aspose.Words.Rendering](../../pageinfo/)
* asamblea [Aspose.Words](../../../)


