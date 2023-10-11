---
title: PageInfo.GetDotNetPaperSize
second_title: Referencia de API de Aspose.Words para .NET
description: PageInfo método. Obtiene elPaperSize objeto adecuado para imprimir la página representada por estePageInfo .
type: docs
weight: 80
url: /es/net/aspose.words.rendering/pageinfo/getdotnetpapersize/
---
## PageInfo.GetDotNetPaperSize method

Obtiene elPaperSize objeto adecuado para imprimir la página representada por este[`PageInfo`](../) .

```csharp
public PaperSize GetDotNetPaperSize(PaperSizeCollection paperSizes)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| paperSizes | PaperSizeCollection | Tamaños de papel disponibles. |

### Valor_devuelto

Un objeto que puede utilizar en el marco de impresión .NET para especificar el tamaño del papel.

### Ejemplos

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
/// Selecciona el tamaño de papel, la orientación y la bandeja de papel adecuados al imprimir.
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
     /// Llamado antes de imprimir cada página.
    /// </summary>
    protected override void OnQueryPageSettings(QueryPageSettingsEventArgs e)
    {
        base.OnQueryPageSettings(e);

         // Un único documento de Microsoft Word puede tener varias secciones que especifican páginas con diferentes tamaños,
         // orientaciones y bandejas de papel. El marco de impresión .NET llama a este código antes
        // se imprime cada página, lo que nos da la oportunidad de especificar cómo imprimir la página actual.
        PageInfo pageInfo = mDocument.GetPageInfo(mCurrentPage - 1);
        e.PageSettings.PaperSize = pageInfo.GetDotNetPaperSize(PrinterSettings.PaperSizes);

        // Microsoft Word almacena el origen del papel (bandeja de la impresora) para cada sección como un valor específico de la impresora.
        // Para obtener el valor de bandeja correcto, deberá utilizar la propiedad "RawKind", que debería devolver su impresora.
        e.PageSettings.PaperSource.RawKind = pageInfo.PaperTray;
        e.PageSettings.Landscape = pageInfo.Landscape;
    }

    /// <summary>
     /// Llamado para que cada página se muestre para su impresión.
    /// </summary>
    protected override void OnPrintPage(PrintPageEventArgs e)
    {
        base.OnPrintPage(e);

        // El motor de renderizado Aspose.Words crea una página extraída del origen (x = 0, y = 0) del documento.
        // Habrá un margen estricto en la impresora, que representará cada página. Necesitamos compensar con ese duro margen.
        float hardOffsetX, hardOffsetY;

        // A continuación se muestran dos formas de establecer un margen estricto.
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


