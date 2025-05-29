---
title: AsposeWordsPrintDocument Class
linktitle: AsposeWordsPrintDocument
articleTitle: AsposeWordsPrintDocument
second_title: Aspose.Words för .NET
description: Effektivisera dokumentutskrift med Aspose.Words.Rendering. Vår AsposeWordsPrintDocument-klass erbjuder sömlös integration för .NET-applikationer.
type: docs
weight: 5260
url: /sv/net/aspose.words.rendering/asposewordsprintdocument/
---
## AsposeWordsPrintDocument class

Tillhandahåller en standardimplementering för utskrift av en[`Document`](../../aspose.words/document/)inom .NET-utskriftsramverket.

För att lära dig mer, besök[Skriva ut ett dokument programmatiskt eller med hjälp av dialogrutor](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) dokumentationsartikel.

```csharp
public class AsposeWordsPrintDocument : PrintDocument
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [AsposeWordsPrintDocument](asposewordsprintdocument/)(*[Document](../../aspose.words/document/)*) | Initierar en ny instans av den här klassen. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [ColorMode](../../aspose.words.rendering/asposewordsprintdocument/colormode/) { get; set; } | Hämtar eller anger hur sidor utan färg skrivs ut om enheten stöder färgutskrift. |
| [ColorPagesPrinted](../../aspose.words.rendering/asposewordsprintdocument/colorpagesprinted/) { get; } | Hämtar antalet sidor som skrivits ut i färg (dvs. medColor sätt till sant). |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [CachePrinterSettings](../../aspose.words.rendering/asposewordsprintdocument/cacheprintersettings/)() | Läser och cachar vissa fält avPrinterSettings för att minska utskriftstiden. |

## Anmärkningar

`AsposeWordsPrintDocument` åsidosättningarPrintEventArgs) för att skriva ut det sidintervall som anges iPrinterSettings.

Ett enda Word-dokument kan bestå av flera avsnitt som anger sidor med olika storlekar, orientering och pappersfack.`AsposeWordsPrintDocument` overrides QueryPageSettingsEventArgs) för att korrekt välja pappersstorlek, orientation och papperskälla när du skriver ut ett Word-dokument.

Microsoft Word lagrar skrivarspecifika värden för pappersfack i ett Word-dokument och därför kommer utskrift från rätt fack att resultera i utskrift från samma skrivarmodell som den som valdes när användaren angav pappersfacken. Om du skriver ut ett dokument på en annan skrivare kommer standardpappersfacket troligtvis att användas, inte de fack som anges i dokumentet.

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
