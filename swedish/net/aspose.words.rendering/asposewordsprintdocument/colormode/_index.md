---
title: AsposeWordsPrintDocument.ColorMode
second_title: Aspose.Words för .NET API Referens
description: AsposeWordsPrintDocument fast egendom. Hämtar eller ställer in hur ickefärgade sidor skrivs ut om enheten stöder färgutskrift.
type: docs
weight: 20
url: /sv/net/aspose.words.rendering/asposewordsprintdocument/colormode/
---
## AsposeWordsPrintDocument.ColorMode property

Hämtar eller ställer in hur icke-färgade sidor skrivs ut om enheten stöder färgutskrift.

```csharp
public ColorPrintMode ColorMode { get; set; }
```

### Anmärkningar

Påverkar inte utskrift av häften.

### Exempel

Visar hur du väljer ett sidintervall och en skrivare att skriva ut dokumentet med och sedan tar fram en förhandsgranskning.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PrintPreviewDialog previewDlg = new PrintPreviewDialog();

// Anropa "Visa"-metoden för att få förhandsgranskningsformuläret att visas överst.
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

// Skapa "Aspose.Words"-implementeringen av .NET-skrivdokumentet,
// och skicka sedan skrivarinställningarna från dialogrutan.
AsposeWordsPrintDocument awPrintDoc = new AsposeWordsPrintDocument(doc);
awPrintDoc.PrinterSettings = printDlg.PrinterSettings;

// Ange det nya färgutskriftsläget.
awPrintDoc.ColorMode = ColorPrintMode.GrayscaleAuto;

// Använd metoden "CachePrinterSettings" för att minska tiden för det första anropet av metoden "Skriv ut".
awPrintDoc.CachePrinterSettings();

// Anropa "Hide" och sedan "InvalidatePreview"-metoderna för att få förhandsgranskningen att visas överst.
previewDlg.Hide();
previewDlg.PrintPreviewControl.InvalidatePreview();

// Skicka "Aspose.Words" utskriftsdokumentet till .NET Print Preview-dialogrutan.
previewDlg.Document = awPrintDoc;
previewDlg.ShowDialog();

awPrintDoc.Print();            
Console.WriteLine($"The numer of pages printed in color are {awPrintDoc.ColorPagesPrinted}.");
```

### Se även

* enum [ColorPrintMode](../../colorprintmode/)
* class [AsposeWordsPrintDocument](../)
* namnutrymme [Aspose.Words.Rendering](../../asposewordsprintdocument/)
* hopsättning [Aspose.Words](../../../)


