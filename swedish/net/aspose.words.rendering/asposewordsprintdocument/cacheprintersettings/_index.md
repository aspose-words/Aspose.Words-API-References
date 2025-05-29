---
title: AsposeWordsPrintDocument.CachePrinterSettings
linktitle: CachePrinterSettings
articleTitle: CachePrinterSettings
second_title: Aspose.Words för .NET
description: Förbättra utskriftseffektiviteten med Aspose.Words CachePrinterSettings-metod, som optimerar PrinterSettings för att minimera utskriftsfördröjningar och förbättra prestanda.
type: docs
weight: 40
url: /sv/net/aspose.words.rendering/asposewordsprintdocument/cacheprintersettings/
---
## AsposeWordsPrintDocument.CachePrinterSettings method

Läser och cachar vissa fält avPrinterSettings för att minska utskriftstiden.

```csharp
public void CachePrinterSettings()
```

## Anmärkningar

Den här metoden anropas innan utskriften startar om den inte har körts tidigare.

## Exempel

Visar hur man väljer ett sidintervall och en skrivare att skriva ut dokumentet med, och sedan visar en förhandsgranskning.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PrintPreviewDialog previewDlg = new PrintPreviewDialog();

// Anropa metoden "Visa" för att få förhandsgranskningsformuläret att visas överst.
previewDlg.Show();

// Initiera utskriftsdialogrutan med antalet sidor i dokumentet.
PrintDialog printDlg = new PrintDialog();
printDlg.AllowSomePages = true;
printDlg.PrinterSettings.MinimumPage = 1;
printDlg.PrinterSettings.MaximumPage = doc.PageCount;
printDlg.PrinterSettings.FromPage = 1;
printDlg.PrinterSettings.ToPage = doc.PageCount;

if (printDlg.ShowDialog() != DialogResult.OK)
    return;

// Skapa implementeringen "Aspose.Words" av .NET-utskriftsdokumentet,
// och skicka sedan skrivarinställningarna från dialogrutan.
AsposeWordsPrintDocument awPrintDoc = new AsposeWordsPrintDocument(doc);
awPrintDoc.PrinterSettings = printDlg.PrinterSettings;

// Ange det nya färgutskriftsläget.
awPrintDoc.ColorMode = ColorPrintMode.GrayscaleAuto;

// Använd metoden "CachePrinterSettings" för att minska tiden för det första anropet av metoden "Print".
awPrintDoc.CachePrinterSettings();

// Anropa metoderna "Dölj" och sedan "InvalidatePreview" för att få förhandsgranskningen att visas överst.
previewDlg.Hide();
previewDlg.PrintPreviewControl.InvalidatePreview();

// Skicka utskriftsdokumentet "Aspose.Words" till dialogrutan för förhandsgranskning i .NET.
previewDlg.Document = awPrintDoc;
previewDlg.ShowDialog();

awPrintDoc.Print();
Console.WriteLine($"The numer of pages printed in color are {awPrintDoc.ColorPagesPrinted}.");
```

### Se även

* class [AsposeWordsPrintDocument](../)
* namnutrymme [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* hopsättning [Aspose.Words](../../../)
