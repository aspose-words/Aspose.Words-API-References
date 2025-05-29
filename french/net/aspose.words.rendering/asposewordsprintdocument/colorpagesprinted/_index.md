---
title: AsposeWordsPrintDocument.ColorPagesPrinted
linktitle: ColorPagesPrinted
articleTitle: ColorPagesPrinted
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ColorPagesPrinted d'Aspose.Words PrintDocument pour suivre efficacement le nombre de pages imprimées en couleurs vives. Optimisez vos données d'impression !
type: docs
weight: 30
url: /fr/net/aspose.words.rendering/asposewordsprintdocument/colorpagesprinted/
---
## AsposeWordsPrintDocument.ColorPagesPrinted property

Obtient le nombre de pages imprimées en couleur (c'est-à-dire avecColor défini sur vrai).

```csharp
public int ColorPagesPrinted { get; }
```

## Exemples

Montre comment sélectionner une plage de pages et une imprimante avec laquelle imprimer le document, puis afficher un aperçu avant impression.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PrintPreviewDialog previewDlg = new PrintPreviewDialog();

// Appelez la méthode « Afficher » pour afficher le formulaire d'aperçu avant impression en haut.
previewDlg.Show();

// Initialisez la boîte de dialogue d'impression avec le nombre de pages du document.
PrintDialog printDlg = new PrintDialog();
printDlg.AllowSomePages = true;
printDlg.PrinterSettings.MinimumPage = 1;
printDlg.PrinterSettings.MaximumPage = doc.PageCount;
printDlg.PrinterSettings.FromPage = 1;
printDlg.PrinterSettings.ToPage = doc.PageCount;

if (printDlg.ShowDialog() != DialogResult.OK)
    return;

// Créez l'implémentation « Aspose.Words » du document d'impression .NET,
// puis transmettez les paramètres de l'imprimante à partir de la boîte de dialogue.
AsposeWordsPrintDocument awPrintDoc = new AsposeWordsPrintDocument(doc);
awPrintDoc.PrinterSettings = printDlg.PrinterSettings;

// Spécifiez le nouveau mode d'impression couleur.
awPrintDoc.ColorMode = ColorPrintMode.GrayscaleAuto;

// Utilisez la méthode « CachePrinterSettings » pour réduire le temps du premier appel de la méthode « Print ».
awPrintDoc.CachePrinterSettings();

// Appelez les méthodes « Hide », puis « InvalidatePreview » pour afficher l'aperçu avant impression en haut.
previewDlg.Hide();
previewDlg.PrintPreviewControl.InvalidatePreview();

// Transmettez le document d'impression « Aspose.Words » à la boîte de dialogue Aperçu avant impression .NET.
previewDlg.Document = awPrintDoc;
previewDlg.ShowDialog();

awPrintDoc.Print();
Console.WriteLine($"The numer of pages printed in color are {awPrintDoc.ColorPagesPrinted}.");
```

### Voir également

* class [AsposeWordsPrintDocument](../)
* espace de noms [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* Assemblée [Aspose.Words](../../../)
