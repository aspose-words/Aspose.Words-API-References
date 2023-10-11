---
title: AsposeWordsPrintDocument.ColorMode
second_title: Référence de l'API Aspose.Words pour .NET
description: AsposeWordsPrintDocument propriété. Obtient ou définit la façon dont les pages non colorées sont imprimées si le périphérique prend en charge limpression couleur.
type: docs
weight: 20
url: /fr/net/aspose.words.rendering/asposewordsprintdocument/colormode/
---
## AsposeWordsPrintDocument.ColorMode property

Obtient ou définit la façon dont les pages non colorées sont imprimées si le périphérique prend en charge l'impression couleur.

```csharp
public ColorPrintMode ColorMode { get; set; }
```

### Remarques

N'affecte pas l'impression des livrets.

### Exemples

Montre comment sélectionner une plage de pages et une imprimante avec laquelle imprimer le document, puis afficher un aperçu avant impression.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PrintPreviewDialog previewDlg = new PrintPreviewDialog();

// Appelez la méthode "Show" pour que le formulaire d'aperçu avant impression s'affiche en haut.
previewDlg.Show();

// Initialise la boîte de dialogue d'impression avec le nombre de pages du document.
PrintDialog printDlg = new PrintDialog();
printDlg.AllowSomePages = true;
printDlg.PrinterSettings.MinimumPage = 1;
printDlg.PrinterSettings.MaximumPage = doc.PageCount;
printDlg.PrinterSettings.FromPage = 1;
printDlg.PrinterSettings.ToPage = doc.PageCount;

if (printDlg.ShowDialog() != DialogResult.OK)
    return;

// Créer l'implémentation "Aspose.Words" du document d'impression .NET,
// puis transmettez les paramètres de l'imprimante depuis la boîte de dialogue.
AsposeWordsPrintDocument awPrintDoc = new AsposeWordsPrintDocument(doc);
awPrintDoc.PrinterSettings = printDlg.PrinterSettings;

// Spécifie le nouveau mode d'impression couleur.
awPrintDoc.ColorMode = ColorPrintMode.GrayscaleAuto;

// Utilisation de la méthode "CachePrinterSettings" pour réduire le temps du premier appel de la méthode "Print".
awPrintDoc.CachePrinterSettings();

// Appelez les méthodes "Hide", puis "InvalidatePreview" pour que l'aperçu avant impression s'affiche en haut.
previewDlg.Hide();
previewDlg.PrintPreviewControl.InvalidatePreview();

// Transmettez le document d'impression "Aspose.Words" à la boîte de dialogue Aperçu avant impression .NET.
previewDlg.Document = awPrintDoc;
previewDlg.ShowDialog();

awPrintDoc.Print();            
Console.WriteLine($"The numer of pages printed in color are {awPrintDoc.ColorPagesPrinted}.");
```

### Voir également

* enum [ColorPrintMode](../../colorprintmode/)
* class [AsposeWordsPrintDocument](../)
* espace de noms [Aspose.Words.Rendering](../../asposewordsprintdocument/)
* Assemblée [Aspose.Words](../../../)


