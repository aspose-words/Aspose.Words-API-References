---
title: ColorPrintMode Enum
linktitle: ColorPrintMode
articleTitle: ColorPrintMode
second_title: Aspose.Words för .NET
description: Upptäck enumerationen Aspose.Words.Rendering.ColorPrintMode för optimerad färgutskrift. Kontrollera hur sidor utan färg skrivs ut för förbättrad dokumentkvalitet.
type: docs
weight: 5270
url: /sv/net/aspose.words.rendering/colorprintmode/
---
## ColorPrintMode enumeration

Anger hur sidor utan färg skrivs ut om enheten stöder färgutskrift.

```csharp
public enum ColorPrintMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Normal | `0` | Alla sidor skrivs ut enligt skrivarens kapacitet och inställningar. |
| GrayscaleAuto | `1` | Om ofärgade sidor upptäcks skrivs de ut i gråskala. |

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

* namnutrymme [Aspose.Words.Rendering](../../aspose.words.rendering/)
* hopsättning [Aspose.Words](../../)
