---
title: HtmlFixedSaveOptions.SaveFontFaceCssSeparately
linktitle: SaveFontFaceCssSeparately
articleTitle: SaveFontFaceCssSeparately
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété SaveFontFaceCssSeparately optimise la gestion CSS de votre document en enregistrant les règles de police dans un fichier séparé pour des exportations plus propres.
type: docs
weight: 180
url: /fr/net/aspose.words.saving/htmlfixedsaveoptions/savefontfacecssseparately/
---
## HtmlFixedSaveOptions.SaveFontFaceCssSeparately property

L'indicateur indique si les règles CSS « @font-face » doivent être placées dans un fichier séparé « fontFaces.css » lorsqu'un document est enregistré avec une feuille de style externe (c'est-à-dire lorsque[`ExportEmbeddedCss`](../exportembeddedcss/) est`FAUX` ). La valeur par défaut est`FAUX` , toutes les règles CSS sont écrites dans un seul fichier « styles.css ».

```csharp
public bool SaveFontFaceCssSeparately { get; set; }
```

## Remarques

Définition de cette propriété sur`vrai` restaure l'ancien comportement (fichiers séparés) pour la compatibilité avec le code hérité.

## Exemples

Montre comment placer CSS dans un fichier séparé et ajouter un préfixe à tous ses noms de classe CSS.

```csharp
Document doc = new Document(MyDir + "Bookmarks.docx");

HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    CssClassNamesPrefix = "myprefix",
    SaveFontFaceCssSeparately = true
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix.html");

Assert.True(Regex.Match(outDocContents,
    "<div class=\"myprefixdiv myprefixpage\" style=\"width:595[.]3pt; height:841[.]9pt;\">" +
    "<div class=\"myprefixdiv\" style=\"left:85[.]05pt; top:36pt; clip:rect[(]0pt,510[.]25pt,74[.]95pt,-85.05pt[)];\">" +
    "<span class=\"myprefixspan myprefixtext001\" style=\"font-size:11pt; left:294[.]73pt; top:0[.]36pt; line-height:12[.]29pt;\">").Success);

outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix/styles.css");

Assert.True(Regex.Match(outDocContents,
    ".myprefixdiv { position:absolute; } " +
    ".myprefixspan { position:absolute; white-space:pre; color:#000000; font-size:12pt; }").Success);
```

### Voir également

* class [HtmlFixedSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
