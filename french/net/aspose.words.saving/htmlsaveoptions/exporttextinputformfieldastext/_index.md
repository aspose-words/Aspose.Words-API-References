---
title: HtmlSaveOptions.ExportTextInputFormFieldAsText
linktitle: ExportTextInputFormFieldAsText
articleTitle: ExportTextInputFormFieldAsText
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété HtmlSaveOptions ExportTextInputFormFieldAsText optimise les champs de saisie de texte pour un enregistrement HTML ou MHTML fluide. Améliorez votre processus d'exportation !
type: docs
weight: 260
url: /fr/net/aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext/
---
## HtmlSaveOptions.ExportTextInputFormFieldAsText property

Contrôle la manière dont les champs de formulaire de saisie de texte sont enregistrés au format HTML ou MHTML. La valeur par défaut est`FAUX` .

```csharp
public bool ExportTextInputFormFieldAsText { get; set; }
```

## Remarques

Lorsqu'il est réglé sur`vrai` , exporte les champs de formulaire de saisie de texte sous forme de texte normal. Lorsque`FAUX`, exporte les champs de formulaire de saisie de texte Word en tant qu'éléments INPUT en HTML.

Lors de l'exportation vers EPUB, les champs de saisie de texte sont toujours enregistrés sous forme de texte en raison des exigences de ce format.

## Exemples

Montre comment spécifier le dossier pour stocker les images liées après l'enregistrement au format .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Définissez une option pour exporter les champs de formulaire sous forme de texte brut au lieu d'éléments d'entrée HTML.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

### Voir également

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
