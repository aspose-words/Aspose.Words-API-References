---
title: HtmlSaveOptions.ExportPageMargins
linktitle: ExportPageMargins
articleTitle: ExportPageMargins
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété HtmlSaveOptions ExportPageMargins améliore vos exportations HTML, MHTML et EPUB en contrôlant les marges de page pour une présentation soignée.
type: docs
weight: 210
url: /fr/net/aspose.words.saving/htmlsaveoptions/exportpagemargins/
---
## HtmlSaveOptions.ExportPageMargins property

Spécifie si les marges de page sont exportées au format HTML, MHTML ou EPUB. La valeur par défaut est`FAUX` .

```csharp
public bool ExportPageMargins { get; set; }
```

## Remarques

Aspose.Words n'affiche pas la zone des marges de page par défaut. Si des éléments sont complètement ou partiellement coupés par le bord du document, la zone affichée peut être étendue avec cette option.

## Exemples

Montre comment afficher les objets hors limites dans les documents HTML de sortie.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utilisez un générateur pour insérer une forme sans habillage.
Shape shape = builder.InsertShape(ShapeType.Cube, 200, 200);

shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.WrapType = WrapType.None;

// Les valeurs de position de forme négatives peuvent placer la forme en dehors des limites de la page.
// Si nous exportons ceci en HTML, la forme apparaîtra tronquée.
shape.Left = -150;

// Lors de l'enregistrement du document au format HTML, nous pouvons passer un objet SaveOptions
// pour décider s'il faut ajuster la page pour afficher entièrement les objets hors limites.
// Si nous définissons l'indicateur « ExportPageMargins » sur « true », la forme sera entièrement visible dans le code HTML de sortie.
// Si nous définissons l'indicateur "ExportPageMargins" sur "false",
// notre document affichera la forme tronquée comme nous la verrions dans Microsoft Word.
HtmlSaveOptions options = new HtmlSaveOptions { ExportPageMargins = exportPageMargins };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportPageMargins.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportPageMargins.html");

if (exportPageMargins)
{
    Assert.True(outDocContents.Contains("<style type=\"text/css\">div.Section_1 { margin:70.85pt }</style>"));
    Assert.True(outDocContents.Contains("<div class=\"Section_1\"><p style=\"margin-top:0pt; margin-left:150pt; margin-bottom:0pt\">"));
}
else
{
    Assert.False(outDocContents.Contains("style type=\"text/css\">"));
    Assert.True(outDocContents.Contains("<div><p style=\"margin-top:0pt; margin-left:220.85pt; margin-bottom:0pt\">"));
}
```

### Voir également

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
