---
title: AsposeWordsPrintDocument Class
linktitle: AsposeWordsPrintDocument
articleTitle: AsposeWordsPrintDocument
second_title: Aspose.Words para .NET
description: Optimice la impresión de documentos con Aspose.Words.Rendering. Nuestra clase AsposeWordsPrintDocument ofrece una integración perfecta con aplicaciones .NET.
type: docs
weight: 5260
url: /es/net/aspose.words.rendering/asposewordsprintdocument/
---
## AsposeWordsPrintDocument class

Proporciona una implementación predeterminada para la impresión de un[`Document`](../../aspose.words/document/)dentro del marco de impresión .NET.

Para obtener más información, visite el[Imprimir un documento mediante programación o mediante cuadros de diálogo](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) Artículo de documentación.

```csharp
public class AsposeWordsPrintDocument : PrintDocument
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [AsposeWordsPrintDocument](asposewordsprintdocument/)(*[Document](../../aspose.words/document/)*) | Inicializa una nueva instancia de esta clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [ColorMode](../../aspose.words.rendering/asposewordsprintdocument/colormode/) { get; set; } | Obtiene o establece cómo se imprimen las páginas sin color si el dispositivo admite la impresión en color. |
| [ColorPagesPrinted](../../aspose.words.rendering/asposewordsprintdocument/colorpagesprinted/) { get; } | Obtiene el número de páginas impresas en color (es decir, conColor establecido en verdadero). |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [CachePrinterSettings](../../aspose.words.rendering/asposewordsprintdocument/cacheprintersettings/)() | Lee y almacena en caché algunos campos dePrinterSettings para reducir el tiempo de impresión. |

## Observaciones

`AsposeWordsPrintDocument` anulacionesPrintEventArgs) para imprimir el rango de páginas que se especifica enPrinterSettings.

Un solo documento de Word puede constar de varias secciones que especifican páginas con diferentes tamaños, orientación y bandejas de papel.`AsposeWordsPrintDocument` anulaciones QueryPageSettingsEventArgs) para seleccionar correctamente el tamaño del papel, la orientación y la fuente del papel al imprimir un documento de Word.

Microsoft Word almacena valores específicos de impresora para las bandejas de papel en un documento de Word y, por lo tanto, al imprimir solo en el mismo modelo de impresora que el seleccionado al especificar las bandejas de papel, se imprimirá desde las bandejas correctas. Si imprime un documento en una impresora diferente, lo más probable es que se utilice la bandeja de papel predeterminada, no las bandejas especificadas en el documento.

## Ejemplos

Muestra cómo seleccionar un rango de páginas y una impresora para imprimir el documento y luego mostrar una vista previa de impresión.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PrintPreviewDialog previewDlg = new PrintPreviewDialog();

// Llame al método "Mostrar" para que el formulario de vista previa de impresión se muestre en la parte superior.
previewDlg.Show();

// Inicializa el cuadro de diálogo de impresión con el número de páginas del documento.
PrintDialog printDlg = new PrintDialog();
printDlg.AllowSomePages = true;
printDlg.PrinterSettings.MinimumPage = 1;
printDlg.PrinterSettings.MaximumPage = doc.PageCount;
printDlg.PrinterSettings.FromPage = 1;
printDlg.PrinterSettings.ToPage = doc.PageCount;

if (printDlg.ShowDialog() != DialogResult.OK)
    return;

// Cree la implementación "Aspose.Words" del documento de impresión .NET,
// y luego pase la configuración de la impresora desde el cuadro de diálogo.
AsposeWordsPrintDocument awPrintDoc = new AsposeWordsPrintDocument(doc);
awPrintDoc.PrinterSettings = printDlg.PrinterSettings;

// Especifique el nuevo modo de impresión en color.
awPrintDoc.ColorMode = ColorPrintMode.GrayscaleAuto;

// Utilice el método "CachePrinterSettings" para reducir el tiempo de la primera llamada al método "Print".
awPrintDoc.CachePrinterSettings();

// Llame a los métodos "Ocultar" y luego a "InvalidatePreview" para que la vista previa de impresión se muestre en la parte superior.
previewDlg.Hide();
previewDlg.PrintPreviewControl.InvalidatePreview();

// Pase el documento de impresión "Aspose.Words" al cuadro de diálogo Vista previa de impresión de .NET.
previewDlg.Document = awPrintDoc;
previewDlg.ShowDialog();

awPrintDoc.Print();
Console.WriteLine($"The numer of pages printed in color are {awPrintDoc.ColorPagesPrinted}.");
```

### Ver también

* espacio de nombres [Aspose.Words.Rendering](../../aspose.words.rendering/)
* asamblea [Aspose.Words](../../)
