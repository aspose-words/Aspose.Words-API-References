---
title: AsposeWordsPrintDocument.ColorPagesPrinted
linktitle: ColorPagesPrinted
articleTitle: ColorPagesPrinted
second_title: Aspose.Words para .NET
description: Descubra la propiedad PrintDocument ColorPagesPrinted de Aspose.Words para controlar eficientemente el número de páginas impresas con colores vibrantes. ¡Optimice su información de impresión!
type: docs
weight: 30
url: /es/net/aspose.words.rendering/asposewordsprintdocument/colorpagesprinted/
---
## AsposeWordsPrintDocument.ColorPagesPrinted property

Obtiene el número de páginas impresas en color (es decir, conColor establecido en verdadero).

```csharp
public int ColorPagesPrinted { get; }
```

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

* class [AsposeWordsPrintDocument](../)
* espacio de nombres [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* asamblea [Aspose.Words](../../../)
