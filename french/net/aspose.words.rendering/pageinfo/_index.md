---
title: PageInfo Class
linktitle: PageInfo
articleTitle: PageInfo
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Rendering.PageInfo, qui fournit des détails essentiels sur chaque page de document, améliorant ainsi votre expérience de rendu de document.
type: docs
weight: 5300
url: /fr/net/aspose.words.rendering/pageinfo/
---
## PageInfo class

Représente des informations sur une page de document particulière.

Pour en savoir plus, visitez le[Rendu](https://docs.aspose.com/words/net/rendering/) article de documentation.

```csharp
public class PageInfo
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Colored](../../aspose.words.rendering/pageinfo/colored/) { get; } | Retours`vrai` si la page contient du contenu coloré. |
| [HeightInPoints](../../aspose.words.rendering/pageinfo/heightinpoints/) { get; } | Obtient la hauteur de la page en points. |
| [Landscape](../../aspose.words.rendering/pageinfo/landscape/) { get; } | Retours`vrai` si l'orientation de la page spécifiée dans le document pour cette page est paysage. |
| [PaperSize](../../aspose.words.rendering/pageinfo/papersize/) { get; } | Obtient la taille du papier sous forme d'énumération. |
| [PaperTray](../../aspose.words.rendering/pageinfo/papertray/) { get; } | Obtient le bac à papier (bin) pour cette page comme spécifié dans le document. La valeur est spécifique à l'implémentation (imprimante). |
| [SizeInPoints](../../aspose.words.rendering/pageinfo/sizeinpoints/) { get; } | Obtient la taille de la page en points. |
| [WidthInPoints](../../aspose.words.rendering/pageinfo/widthinpoints/) { get; } | Obtient la largeur de la page en points. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetDotNetPaperSize](../../aspose.words.rendering/pageinfo/getdotnetpapersize/)(*PaperSizeCollection*) | Obtient lePaperSize objet adapté à l'impression la page représentée par ceci`PageInfo` . |
| [GetSizeInPixels](../../aspose.words.rendering/pageinfo/getsizeinpixels/#getsizeinpixels)(*float, float*) | Calcule la taille de la page en pixels pour un facteur de zoom et une résolution spécifiés. |
| [GetSizeInPixels](../../aspose.words.rendering/pageinfo/getsizeinpixels/#getsizeinpixels_1)(*float, float, float*) | Calcule la taille de la page en pixels pour un facteur de zoom et une résolution spécifiés. |
| [GetSpecifiedPrinterPaperSource](../../aspose.words.rendering/pageinfo/getspecifiedprinterpapersource/)(*PaperSourceCollection, PaperSource*) | Obtient lePaperSource objet adapté à l'impression la page représentée par ceci`PageInfo` . |

## Remarques

La largeur et la hauteur de la page renvoyées par cet objet représentent la taille « finale » de la page, par exemple, elles sont déjà tournées vers la bonne orientation.

## Exemples

Montre comment imprimer les informations de taille et d'orientation de page pour chaque page d'un document Word.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// La première section comporte deux pages. Nous attribuerons un bac à papier différent à chacune d'elles.
// dont le numéro correspond à un type de source papier. Ces sources et leurs types varient.
// en fonction du pilote d'imprimante installé.
PrinterSettings.PaperSourceCollection paperSources = new PrinterSettings().PaperSources;

doc.FirstSection.PageSetup.FirstPageTray = paperSources[0].RawKind;
doc.FirstSection.PageSetup.OtherPagesTray = paperSources[1].RawKind;

Console.WriteLine("Document \"{0}\" contains {1} pages.", doc.OriginalFileName, doc.PageCount);

float scale = 1.0f;
float dpi = 96;

for (int i = 0; i < doc.PageCount; i++)
{
    // Chaque page possède un objet PageInfo, dont l'index est le numéro de la page correspondante.
    PageInfo pageInfo = doc.GetPageInfo(i);

    // Imprimez l'orientation et les dimensions de la page.
    Console.WriteLine($"Page {i + 1}:");
    Console.WriteLine($"\tOrientation:\t{(pageInfo.Landscape ? "Landscape" : "Portrait")}");
    Console.WriteLine($"\tPaper size:\t\t{pageInfo.PaperSize} ({pageInfo.WidthInPoints:F0}x{pageInfo.HeightInPoints:F0}pt)");
    Console.WriteLine($"\tSize in points:\t{pageInfo.SizeInPoints}");
    Console.WriteLine($"\tSize in pixels:\t{pageInfo.GetSizeInPixels(1.0f, 96)} at {scale * 100}% scale, {dpi} dpi");

    // Imprimez les informations du bac source.
    Console.WriteLine($"\tTray:\t{pageInfo.PaperTray}");
    PaperSource source = pageInfo.GetSpecifiedPrinterPaperSource(paperSources, paperSources[0]);
    Console.WriteLine($"\tSuitable print source:\t{source.SourceName}, kind: {source.Kind}");
}
```

### Voir également

* espace de noms [Aspose.Words.Rendering](../../aspose.words.rendering/)
* Assemblée [Aspose.Words](../../)
