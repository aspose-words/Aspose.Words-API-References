---
title: HtmlMetafileFormat Enum
linktitle: HtmlMetafileFormat
articleTitle: HtmlMetafileFormat
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Saving.HtmlMetafileFormat pour un enregistrement fluide des métafichiers dans les documents HTML. Améliorez votre expérience de conversion de documents dès aujourd'hui !
type: docs
weight: 5840
url: /fr/net/aspose.words.saving/htmlmetafileformat/
---
## HtmlMetafileFormat enumeration

Indique le format dans lequel les métafichiers sont enregistrés dans les documents HTML.

```csharp
public enum HtmlMetafileFormat
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Png | `0` | Les métafichiers sont rendus en images PNG raster. |
| Svg | `1` | Les métafichiers sont convertis en images vectorielles SVG. |
| EmfOrWmf | `2` | Les métafichiers sont enregistrés tels quels, sans conversion. |

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

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
