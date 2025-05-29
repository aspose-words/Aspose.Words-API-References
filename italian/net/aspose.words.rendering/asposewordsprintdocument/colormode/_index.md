---
title: AsposeWordsPrintDocument.ColorMode
linktitle: ColorMode
articleTitle: ColorMode
second_title: Aspose.Words per .NET
description: Scopri come ottimizzare la stampa con la proprietà ColorMode di AsposeWordsPrintDocument. Controlla l'output delle pagine non colorate per una stampa a colori migliorata!
type: docs
weight: 20
url: /it/net/aspose.words.rendering/asposewordsprintdocument/colormode/
---
## AsposeWordsPrintDocument.ColorMode property

Ottiene o imposta la modalità di stampa delle pagine non colorate se il dispositivo supporta la stampa a colori.

```csharp
public ColorPrintMode ColorMode { get; set; }
```

## Osservazioni

Non influisce sulla stampa del libretto.

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

* enum [ColorPrintMode](../../colorprintmode/)
* class [AsposeWordsPrintDocument](../)
* spazio dei nomi [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* assemblea [Aspose.Words](../../../)
