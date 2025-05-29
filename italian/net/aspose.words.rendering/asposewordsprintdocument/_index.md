---
title: AsposeWordsPrintDocument Class
linktitle: AsposeWordsPrintDocument
articleTitle: AsposeWordsPrintDocument
second_title: Aspose.Words per .NET
description: Semplifica la stampa di documenti con Aspose.Words.Rendering. La nostra classe AsposeWordsPrintDocument offre una perfetta integrazione con le applicazioni .NET.
type: docs
weight: 5260
url: /it/net/aspose.words.rendering/asposewordsprintdocument/
---
## AsposeWordsPrintDocument class

Fornisce un'implementazione predefinita per la stampa di un[`Document`](../../aspose.words/document/)all'interno del framework di stampa .NET.

Per saperne di più, visita il[Stampa di un documento tramite programmazione o tramite finestre di dialogo](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) articolo di documentazione.

```csharp
public class AsposeWordsPrintDocument : PrintDocument
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [AsposeWordsPrintDocument](asposewordsprintdocument/)(*[Document](../../aspose.words/document/)*) | Inizializza una nuova istanza di questa classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [ColorMode](../../aspose.words.rendering/asposewordsprintdocument/colormode/) { get; set; } | Ottiene o imposta la modalità di stampa delle pagine non colorate se il dispositivo supporta la stampa a colori. |
| [ColorPagesPrinted](../../aspose.words.rendering/asposewordsprintdocument/colorpagesprinted/) { get; } | Ottiene il numero di pagine stampate a colori (ad esempio conColor impostato su vero). |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [CachePrinterSettings](../../aspose.words.rendering/asposewordsprintdocument/cacheprintersettings/)() | Legge e memorizza nella cache alcuni campi diPrinterSettings per ridurre i tempi di stampa. |

## Osservazioni

`AsposeWordsPrintDocument` sovrascritturePrintEventArgs) per stampare l'intervallo di pagine specificato inPrinterSettings.

Un singolo documento Word può essere costituito da più sezioni che specificano pagine con dimensioni, orientamenti e vassoi della carta diversi.`AsposeWordsPrintDocument` sovrascrive QueryPageSettingsEventArgs) per selezionare correttamente il formato della carta, l'orientamento e l'alimentazione della carta quando si stampa un documento Word.

Microsoft Word memorizza valori specifici per la stampante per i vassoi carta in un documento Word e, pertanto, la stampa solo sullo stesso modello di stampante selezionato al momento della specifica dei vassoi carta, comporterà la stampa dai vassoi corretti. Se si stampa un documento su una stampante diversa, molto probabilmente verrà utilizzato il vassoio carta predefinito, non quelli specificati nel documento.

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

* spazio dei nomi [Aspose.Words.Rendering](../../aspose.words.rendering/)
* assemblea [Aspose.Words](../../)
