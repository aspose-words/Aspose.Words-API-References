---
title: HtmlSaveOptions.ExportXhtmlTransitional
linktitle: ExportXhtmlTransitional
articleTitle: ExportXhtmlTransitional
second_title: Aspose.Words pour .NET
description: HtmlSaveOptions ExportXhtmlTransitional propriété. Spécifie sil faut écrire la déclaration DOCTYPE lors de lenregistrement au format HTML ou MHTML. Quandvrai  écrit une déclaration DOCTYPE dans le document avant lélément racine. La valeur par défaut estFAUX. Lors de lenregistrement au format EPUB ou HTML5 Html5  la déclaration DOCTYPE est toujours écrite en C#.
type: docs
weight: 280
url: /fr/net/aspose.words.saving/htmlsaveoptions/exportxhtmltransitional/
---
## HtmlSaveOptions.ExportXhtmlTransitional property

Spécifie s'il faut écrire la déclaration DOCTYPE lors de l'enregistrement au format HTML ou MHTML. Quand`vrai` , écrit une déclaration DOCTYPE dans le document avant l'élément racine. La valeur par défaut est`FAUX`. Lors de l'enregistrement au format EPUB ou HTML5 (Html5 ) la déclaration DOCTYPE est toujours écrite.

```csharp
public bool ExportXhtmlTransitional { get; set; }
```

## Remarques

Aspose.Words écrit toujours du HTML bien formé quel que soit ce paramètre.

Quand`vrai`, le début du document de sortie HTML ressemblera à ceci :

Aspose.Words vise à générer du XHTML conformément à la spécification XHTML 1.0 Transitional, , mais la sortie ne sera pas toujours validée par rapport à la DTD. Certaines structures à l'intérieur d'un document Microsoft Word sont difficiles, voire impossibles, à mapper à un document qui sera validé par rapport au schéma XHTML. Par exemple, XHTML n'autorise pas les listes imbriquées (UL ne peut pas être imbriquée dans un autre élément UL), mais dans les documents Microsoft Word, les listes à plusieurs niveaux se produisent assez souvent.

```csharp
<?xml version="1.0" encoding="utf-8" standalone="no" ?>
<!DOCTYPE html 
      PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//FR"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="fr" lang="fr">
```

## Exemples

Montre comment afficher un en-tête DOCTYPE lors de la conversion de documents vers la norme de transition Xhtml 1.0.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    HtmlVersion = HtmlVersion.Xhtml,
    ExportXhtmlTransitional = showDoctypeDeclaration,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html", options);

// Notre document ne contiendra un en-tête de déclaration DOCTYPE que si nous avons mis le flag "ExportXhtmlTransitional" à "true".
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html");

if (showDoctypeDeclaration)
    Assert.True(outDocContents.Contains(
        "<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>\r\n" +
        "<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Transitional//FR\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">\r\n" +
        "<html xmlns=\"http://www.w3.org/1999/xhtml\">"));
else
    Assert.True(outDocContents.Contains("<html>"));
```

### Voir également

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
