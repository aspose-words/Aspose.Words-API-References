---
title: AsposeWordsPrintDocument.ColorPagesPrinted
linktitle: ColorPagesPrinted
articleTitle: ColorPagesPrinted
second_title: Aspose.Words per .NET
description: Scopri la proprietà PrintDocument ColorPagesPrinted di Aspose.Words per monitorare in modo efficiente il numero di pagine stampate a colori vivaci. Massimizza le tue informazioni di stampa!
type: docs
weight: 30
url: /it/net/aspose.words.rendering/asposewordsprintdocument/colorpagesprinted/
---
## AsposeWordsPrintDocument.ColorPagesPrinted property

Ottiene il numero di pagine stampate a colori (ad esempio conColor impostato su vero).

```csharp
public int ColorPagesPrinted { get; }
```

## Esempi

Mostra come selezionare un intervallo di pagine e una stampante con cui stampare il documento, per poi visualizzare un'anteprima di stampa.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PrintPreviewDialog previewDlg = new PrintPreviewDialog();

// Chiama il metodo "Show" per visualizzare in primo piano il modulo di anteprima di stampa.
previewDlg.Show();

// Inizializza la finestra di dialogo Stampa con il numero di pagine del documento.
PrintDialog printDlg = new PrintDialog();
printDlg.AllowSomePages = true;
printDlg.PrinterSettings.MinimumPage = 1;
printDlg.PrinterSettings.MaximumPage = doc.PageCount;
printDlg.PrinterSettings.FromPage = 1;
printDlg.PrinterSettings.ToPage = doc.PageCount;

if (printDlg.ShowDialog() != DialogResult.OK)
    return;

// Crea l'implementazione "Aspose.Words" del documento di stampa .NET,
// e quindi passare le impostazioni della stampante dalla finestra di dialogo.
AsposeWordsPrintDocument awPrintDoc = new AsposeWordsPrintDocument(doc);
awPrintDoc.PrinterSettings = printDlg.PrinterSettings;

// Specifica la nuova modalità di stampa a colori.
awPrintDoc.ColorMode = ColorPrintMode.GrayscaleAuto;

// Utilizzare il metodo "CachePrinterSettings" per ridurre il tempo della prima chiamata del metodo "Print".
awPrintDoc.CachePrinterSettings();

// Chiamare il metodo "Hide" e poi il metodo "InvalidatePreview" per visualizzare l'anteprima di stampa in primo piano.
previewDlg.Hide();
previewDlg.PrintPreviewControl.InvalidatePreview();

// Passare il documento di stampa "Aspose.Words" alla finestra di dialogo Anteprima di stampa .NET.
previewDlg.Document = awPrintDoc;
previewDlg.ShowDialog();

awPrintDoc.Print();
Console.WriteLine($"The numer of pages printed in color are {awPrintDoc.ColorPagesPrinted}.");
```

### Guarda anche

* class [AsposeWordsPrintDocument](../)
* spazio dei nomi [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* assemblea [Aspose.Words](../../../)
