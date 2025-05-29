---
title: AsposeWordsPrintDocument
linktitle: AsposeWordsPrintDocument
articleTitle: AsposeWordsPrintDocument
second_title: Aspose.Words pour .NET
description: Découvrez le constructeur Aspose.Words PrintDocument pour créer et gérer facilement l'impression de documents dans vos applications. Boostez votre productivité grâce à une intégration fluide !
type: docs
weight: 10
url: /fr/net/aspose.words.rendering/asposewordsprintdocument/asposewordsprintdocument/
---
## AsposeWordsPrintDocument constructor

Initialise une nouvelle instance de cette classe.

```csharp
public AsposeWordsPrintDocument(Document document)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| document | Document | Le document à imprimer. |

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

* class [Document](../../../aspose.words/document/)
* class [AsposeWordsPrintDocument](../)
* espace de noms [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* Assemblée [Aspose.Words](../../../)
