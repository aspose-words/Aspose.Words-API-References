---
title: PageInfo.HeightInPoints
linktitle: HeightInPoints
articleTitle: HeightInPoints
second_title: Aspose.Words pour .NET
description: PageInfo HeightInPoints propriété. Obtient la hauteur de la page en points en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.rendering/pageinfo/heightinpoints/
---
## PageInfo.HeightInPoints property

Obtient la hauteur de la page en points.

```csharp
public float HeightInPoints { get; }
```

## Exemples

Montre comment imprimer les informations sur la taille et l’orientation de chaque page d’un document Word.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// La première section comporte 2 pages. Nous attribuerons à chacun un bac à papier d'imprimante différent,
// dont le numéro correspondra à une sorte de source papier. Ces sources et leurs types varient
// en fonction du pilote d'imprimante installé.
PrinterSettings.PaperSourceCollection paperSources = new PrinterSettings().PaperSources;

doc.FirstSection.PageSetup.FirstPageTray = paperSources[0].RawKind;
doc.FirstSection.PageSetup.OtherPagesTray = paperSources[1].RawKind;

Console.WriteLine("Document \"{0}\" contains {1} pages.", doc.OriginalFileName, doc.PageCount);

float scale = 1.0f;
float dpi = 96;

for (int i = 0; i < doc.PageCount; i++)
{
    // Chaque page possède un objet PageInfo, dont l'index est le numéro de la page respective.
    PageInfo pageInfo = doc.GetPageInfo(i);

    // Imprime l'orientation et les dimensions de la page.
    Console.WriteLine($"Page {i + 1}:");
    Console.WriteLine($"\tOrientation:\t{(pageInfo.Landscape ? "Landscape" : "Portrait")}");
    Console.WriteLine($"\tPaper size:\t\t{pageInfo.PaperSize} ({pageInfo.WidthInPoints:F0}x{pageInfo.HeightInPoints:F0}pt)");
    Console.WriteLine($"\tSize in points:\t{pageInfo.SizeInPoints}");
    Console.WriteLine($"\tSize in pixels:\t{pageInfo.GetSizeInPixels(1.0f, 96)} at {scale * 100}% scale, {dpi} dpi");

    // Imprime les informations du bac source.
    Console.WriteLine($"\tTray:\t{pageInfo.PaperTray}");
    PaperSource source = pageInfo.GetSpecifiedPrinterPaperSource(paperSources, paperSources[0]);
    Console.WriteLine($"\tSuitable print source:\t{source.SourceName}, kind: {source.Kind}");
}
```

### Voir également

* class [PageInfo](../)
* espace de noms [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* Assemblée [Aspose.Words](../../../)
