---
title: PageInfo.GetSizeInPixels
linktitle: GetSizeInPixels
articleTitle: GetSizeInPixels
second_title: Aspose.Words pour .NET
description: Découvrez la méthode PageInfo GetSizeInPixels pour calculer avec précision la taille de votre page en pixels en fonction du facteur de zoom et de la résolution pour un affichage optimal.
type: docs
weight: 90
url: /fr/net/aspose.words.rendering/pageinfo/getsizeinpixels/
---
## GetSizeInPixels(*float, float*) {#getsizeinpixels}

Calcule la taille de la page en pixels pour un facteur de zoom et une résolution spécifiés.

```csharp
public Size GetSizeInPixels(float scale, float dpi)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| scale | Single | Le facteur de zoom (1,0 est 100 %). |
| dpi | Single | La résolution (horizontale et verticale) pour convertir des points en pixels (points par pouce). |

### Return_Value

La taille de la page en pixels.

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

---

## GetSizeInPixels(*float, float, float*) {#getsizeinpixels_1}

Calcule la taille de la page en pixels pour un facteur de zoom et une résolution spécifiés.

```csharp
public Size GetSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| scale | Single | Le facteur de zoom (1,0 est 100 %). |
| horizontalDpi | Single | La résolution horizontale pour convertir des points en pixels (points par pouce). |
| verticalDpi | Single | La résolution verticale pour convertir des points en pixels (points par pouce). |

### Return_Value

La taille de la page en pixels.

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
