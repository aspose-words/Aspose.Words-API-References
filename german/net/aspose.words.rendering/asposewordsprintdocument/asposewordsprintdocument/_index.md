---
title: AsposeWordsPrintDocument.AsposeWordsPrintDocument
second_title: Aspose.Words für .NET-API-Referenz
description: AsposeWordsPrintDocument constructeur. Initialisiert eine neue Instanz dieser Klasse.
type: docs
weight: 10
url: /de/net/aspose.words.rendering/asposewordsprintdocument/asposewordsprintdocument/
---
## AsposeWordsPrintDocument constructor

Initialisiert eine neue Instanz dieser Klasse.

```csharp
public AsposeWordsPrintDocument(Document document)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| document | Document | Das zu druckende Dokument. |

### Beispiele

Zeigt, wie Sie einen Seitenbereich und einen Drucker zum Drucken des Dokuments auswählen und dann eine Druckvorschau aufrufen.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PrintPreviewDialog previewDlg = new PrintPreviewDialog();

// Rufen Sie die Methode „Show“ auf, damit das Druckvorschauformular oben angezeigt wird.
previewDlg.Show();

// Druckdialog mit der Anzahl der Seiten im Dokument initialisieren.
PrintDialog printDlg = new PrintDialog();
printDlg.AllowSomePages = true;
printDlg.PrinterSettings.MinimumPage = 1;
printDlg.PrinterSettings.MaximumPage = doc.PageCount;
printDlg.PrinterSettings.FromPage = 1;
printDlg.PrinterSettings.ToPage = doc.PageCount;

if (printDlg.ShowDialog() != DialogResult.OK)
    return;

// Erstellen Sie die „Aspose.Words“-Implementierung des .NET-Druckdokuments,
// und übergeben Sie dann die Druckereinstellungen aus dem Dialog.
AsposeWordsPrintDocument awPrintDoc = new AsposeWordsPrintDocument(doc);
awPrintDoc.PrinterSettings = printDlg.PrinterSettings;

// Geben Sie den neuen Farbdruckmodus an.
awPrintDoc.ColorMode = ColorPrintMode.GrayscaleAuto;

// Verwenden Sie die Methode „CachePrinterSettings“, um die Zeit des ersten Aufrufs der Methode „Print“ zu verkürzen.
awPrintDoc.CachePrinterSettings();

// Rufen Sie die Methoden „Hide“ und dann „InvalidatePreview“ auf, damit die Druckvorschau oben angezeigt wird.
previewDlg.Hide();
previewDlg.PrintPreviewControl.InvalidatePreview();

// Übergeben Sie das Druckdokument „Aspose.Words“ an das .NET-Druckvorschau-Dialogfeld.
previewDlg.Document = awPrintDoc;
previewDlg.ShowDialog();

awPrintDoc.Print();            
Console.WriteLine($"The numer of pages printed in color are {awPrintDoc.ColorPagesPrinted}.");
```

### Siehe auch

* class [Document](../../../aspose.words/document/)
* class [AsposeWordsPrintDocument](../)
* namensraum [Aspose.Words.Rendering](../../asposewordsprintdocument/)
* Montage [Aspose.Words](../../../)


