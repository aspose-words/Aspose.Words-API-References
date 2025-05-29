---
title: AsposeWordsPrintDocument.CachePrinterSettings
linktitle: CachePrinterSettings
articleTitle: CachePrinterSettings
second_title: Aspose.Words pour .NET
description: Améliorez l'efficacité de l'impression avec la méthode CachePrinterSettings d'Aspose.Words, qui optimise PrinterSettings pour minimiser les délais d'impression et améliorer les performances.
type: docs
weight: 40
url: /fr/net/aspose.words.rendering/asposewordsprintdocument/cacheprintersettings/
---
## AsposeWordsPrintDocument.CachePrinterSettings method

Lit et met en cache certains champs dePrinterSettings pour réduire le temps d'impression.

```csharp
public void CachePrinterSettings()
```

## Remarques

Cette méthode est appelée avant le début de l'impression si elle n'a pas été exécutée précédemment.

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
