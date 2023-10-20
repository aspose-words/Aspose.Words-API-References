---
title: ColorPrintMode Enum
linktitle: ColorPrintMode
articleTitle: ColorPrintMode
second_title: Aspose.Words para .NET
description: Aspose.Words.Rendering.ColorPrintMode enumeración. Especifica cómo se imprimen las páginas sin color si el dispositivo admite la impresión en color en C#.
type: docs
weight: 4540
url: /es/net/aspose.words.rendering/colorprintmode/
---
## ColorPrintMode enumeration

Especifica cómo se imprimen las páginas sin color si el dispositivo admite la impresión en color.

```csharp
public enum ColorPrintMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Normal | `0` | Todas las páginas se imprimen de acuerdo con las capacidades y configuraciones de la impresora. |
| GrayscaleAuto | `1` | Las páginas sin color, si se detectan, se imprimen en escala de grises. |

## Ejemplos

Muestra cómo seleccionar un rango de páginas y una impresora para imprimir el documento y luego abrir una vista previa de impresión.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PrintPreviewDialog previewDlg = new PrintPreviewDialog();

// Llame al método "Mostrar" para que el formulario de vista previa de impresión se muestre en la parte superior.
previewDlg.Show();

// Inicializa el cuadro de diálogo Imprimir con el número de páginas del documento.
PrintDialog printDlg = new PrintDialog();
printDlg.AllowSomePages = true;
printDlg.PrinterSettings.MinimumPage = 1;
printDlg.PrinterSettings.MaximumPage = doc.PageCount;
printDlg.PrinterSettings.FromPage = 1;
printDlg.PrinterSettings.ToPage = doc.PageCount;

if (printDlg.ShowDialog() != DialogResult.OK)
    return;

// Crea la implementación "Aspose.Words" del documento de impresión .NET,
// y luego pasar la configuración de la impresora desde el cuadro de diálogo.
AsposeWordsPrintDocument awPrintDoc = new AsposeWordsPrintDocument(doc);
awPrintDoc.PrinterSettings = printDlg.PrinterSettings;

// Especifique el nuevo modo de impresión en color.
awPrintDoc.ColorMode = ColorPrintMode.GrayscaleAuto;

// Utilice el método "CachePrinterSettings" para reducir el tiempo de la primera llamada del método "Imprimir".
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
