---
title: HtmlLoadOptions.ConvertSvgToEmf
linktitle: ConvertSvgToEmf
articleTitle: ConvertSvgToEmf
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ConvertSvgToEmf de HtmlLoadOptions. Contrôlez facilement la conversion SVG en EMF pour une qualité d'image optimale. La valeur par défaut est « false » ; conservez les SVG intacts !
type: docs
weight: 30
url: /fr/net/aspose.words.loading/htmlloadoptions/convertsvgtoemf/
---
## HtmlLoadOptions.ConvertSvgToEmf property

Obtient ou définit une valeur indiquant s'il faut convertir les images SVG chargées au format EMF. La valeur par défaut est`FAUX` et, si possible, les images SVG chargées sont stockées telles quelles sans conversion.

```csharp
public bool ConvertSvgToEmf { get; set; }
```

## Remarques

Les versions récentes de MS Word prennent en charge les images SVG nativement. Si la version de MS Word spécifiée dans les options de chargement prend en charge le format SVG, Aspose.Words stockera les images SVG telles quelles, sans conversion. Si le format SVG n'est pas pris en charge, les images SVG chargées seront converties au format EMF.

Si, toutefois, cette option est définie sur`vrai` Aspose.Words convertira les images SVG chargées en EMF même si les images SVG sont prises en charge par la version spécifiée de MS Word.

## Exemples

Montre comment convertir des objets SVG dans un format différent lors de l'enregistrement de documents HTML.

```csharp
string html = 
    @"<html>
        <svg xmlns='http://www.w3.org/2000/svg' width='500' height='40' viewBox='0 0 500 40'>
            <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>
        </svg>
    </html>";

// Utilisez « ConvertSvgToEmf » pour rétablir le comportement hérité
// où toutes les images SVG chargées à partir d'un document HTML ont été converties en EMF.
// Les images SVG sont désormais chargées sans conversion
// si la version MS Word spécifiée dans les options de chargement prend en charge les images SVG de manière native.
HtmlLoadOptions loadOptions = new HtmlLoadOptions { ConvertSvgToEmf = true };

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), loadOptions);

// Ce document contient un élément <svg> sous forme de texte.
// Lorsque nous enregistrons le document au format HTML, nous pouvons passer un objet SaveOptions
// pour déterminer comment l'opération de sauvegarde gère cet objet.
// Définition de la propriété « MetafileFormat » sur « HtmlMetafileFormat.Png » pour la convertir en image PNG.
// En définissant la propriété « MetafileFormat » sur « HtmlMetafileFormat.Svg », vous la conservez en tant qu'objet SVG.
// Définition de la propriété « MetafileFormat » sur « HtmlMetafileFormat.EmfOrWmf » pour la convertir en métafichier.
HtmlSaveOptions options = new HtmlSaveOptions { MetafileFormat = htmlMetafileFormat };

doc.Save(ArtifactsDir + "HtmlSaveOptions.MetafileFormat.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.MetafileFormat.html");

switch (htmlMetafileFormat)
{
    case HtmlMetafileFormat.Png:
        Assert.True(outDocContents.Contains(
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<img src=\"HtmlSaveOptions.MetafileFormat.001.png\" width=\"500\" height=\"40\" alt=\"\" " +
                "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
            "</p>"));
        break;
    case HtmlMetafileFormat.Svg:
        Assert.True(outDocContents.Contains(
            "<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">" +
            "<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"499\" height=\"40\">"));
        break;
    case HtmlMetafileFormat.EmfOrWmf:
        Assert.True(outDocContents.Contains(
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<img src=\"HtmlSaveOptions.MetafileFormat.001.emf\" width=\"500\" height=\"40\" alt=\"\" " +
                "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
            "</p>"));
        break;
}
```

### Voir également

* class [HtmlLoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
