---
title: PageInfo.GetSpecifiedPrinterPaperSource
linktitle: GetSpecifiedPrinterPaperSource
articleTitle: GetSpecifiedPrinterPaperSource
second_title: Aspose.Words pour .NET
description: Découvrez la méthode GetSpecifiedPrinterPaperSource dans PageInfo. Récupérez efficacement la source de papier idéale pour une impression fluide.
type: docs
weight: 100
url: /fr/net/aspose.words.rendering/pageinfo/getspecifiedprinterpapersource/
---
## PageInfo.GetSpecifiedPrinterPaperSource method

Obtient lePaperSource objet adapté à l'impression la page représentée par ceci[`PageInfo`](../) .

```csharp
public PaperSource GetSpecifiedPrinterPaperSource(PaperSourceCollection paperSources, 
    PaperSource defaultPageSettingsPaperSource)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| paperSources | PaperSourceCollection | Sources de papier disponibles. |
| defaultPageSettingsPaperSource | PaperSource | Source de papier définie dans les paramètres par défaut de l'imprimante. |

### Return_Value

Un objet que vous pouvez utiliser dans le framework d’impression .NET pour spécifier la source du papier.

## Remarques

Cette méthode nécessite .NET Framework 2.0 ou une version ultérieure.

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

* class [PageInfo](../)
* espace de noms [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* Assemblée [Aspose.Words](../../../)
