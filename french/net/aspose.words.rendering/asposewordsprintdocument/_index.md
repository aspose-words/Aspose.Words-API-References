---
title: AsposeWordsPrintDocument Class
linktitle: AsposeWordsPrintDocument
articleTitle: AsposeWordsPrintDocument
second_title: Aspose.Words pour .NET
description: Simplifiez l'impression de vos documents avec Aspose.Words.Rendering. Notre classe AsposeWordsPrintDocument offre une intégration transparente avec les applications .NET.
type: docs
weight: 5260
url: /fr/net/aspose.words.rendering/asposewordsprintdocument/
---
## AsposeWordsPrintDocument class

Fournit une implémentation par défaut pour l'impression d'un[`Document`](../../aspose.words/document/)dans le framework d'impression .NET.

Pour en savoir plus, visitez le[Imprimer un document par programmation ou à l'aide de boîtes de dialogue](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) article de documentation.

```csharp
public class AsposeWordsPrintDocument : PrintDocument
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [AsposeWordsPrintDocument](asposewordsprintdocument/)(*[Document](../../aspose.words/document/)*) | Initialise une nouvelle instance de cette classe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [ColorMode](../../aspose.words.rendering/asposewordsprintdocument/colormode/) { get; set; } | Obtient ou définit la manière dont les pages non colorées sont imprimées si le périphérique prend en charge l'impression couleur. |
| [ColorPagesPrinted](../../aspose.words.rendering/asposewordsprintdocument/colorpagesprinted/) { get; } | Obtient le nombre de pages imprimées en couleur (c'est-à-dire avecColor défini sur vrai). |

## Méthodes

| Nom | La description |
| --- | --- |
| [CachePrinterSettings](../../aspose.words.rendering/asposewordsprintdocument/cacheprintersettings/)() | Lit et met en cache certains champs dePrinterSettings pour réduire le temps d'impression. |

## Remarques

`AsposeWordsPrintDocument` remplacementsPrintEventArgs) pour imprimer la plage de pages spécifiée dansPrinterSettings.

Un seul document Word peut être composé de plusieurs sections spécifiant des pages avec des tailles, des orientations et des bacs à papier différents.`AsposeWordsPrintDocument` remplace QueryPageSettingsEventArgs) pour sélectionner correctement le format du papier, l'orientation et la source du papier lors de l'impression d'un document Word.

Microsoft Word stocke les valeurs spécifiques à l'imprimante pour les bacs à papier dans un document Word. Par conséquent, l'impression se fera uniquement sur le même modèle d'imprimante que celui sélectionné lors de la spécification des bacs à papier. Si vous imprimez un document sur une autre imprimante, il est fort probable que le bac à papier par défaut soit utilisé, et non celui spécifié dans le document.

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

* espace de noms [Aspose.Words.Rendering](../../aspose.words.rendering/)
* Assemblée [Aspose.Words](../../)
