---
title: MetafileRenderingOptions.ScaleWmfFontsToMetafileSize
second_title: Référence de l'API Aspose.Words pour .NET
description: MetafileRenderingOptions propriété. Obtient ou définit une valeur déterminant sil faut ou non mettre à léchelle les polices dans le métafichier WMF en fonction de la taille du métafichier sur la page.
type: docs
weight: 50
url: /fr/net/aspose.words.saving/metafilerenderingoptions/scalewmffontstometafilesize/
---
## MetafileRenderingOptions.ScaleWmfFontsToMetafileSize property

Obtient ou définit une valeur déterminant s'il faut ou non mettre à l'échelle les polices dans le métafichier WMF en fonction de la taille du métafichier sur la page.

```csharp
public bool ScaleWmfFontsToMetafileSize { get; set; }
```

### Remarques

Lorsque les métafichiers WMF sont affichés dans MS Word, les polices peuvent être mises à l'échelle en fonction de la taille réelle du métafichier sur la page.

Lorsque cette valeur est définie sur`vrai`, Aspose.Words émule la mise à l'échelle des polices en fonction de la taille du métafichier sur la page.

Lorsque cette valeur est définie sur`faux`, Aspose.Words affiche les polices lorsque le métafichier est rendu à sa taille par défaut.

Cette option est utilisée uniquement lorsque le métafichier est rendu sous forme de graphiques vectoriels.

La valeur par défaut est`vrai`.

### Exemples

Montre comment mettre à l'échelle les polices WMF en fonction de la taille du métafichier sur la page.

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// Crée un objet "PdfSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Définissez la propriété "ScaleWmfFontsToMetafileSize" sur "true" pour redimensionner les polices
// qui formate le texte dans les images WMF en fonction de la taille du métafichier sur la page.
// Définissez la propriété "ScaleWmfFontsToMetafileSize" sur "false" pour
// conserve l'échelle par défaut de ces polices.
saveOptions.MetafileRenderingOptions.ScaleWmfFontsToMetafileSize = scaleWmfFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.FontsScaledToMetafileSize.pdf", saveOptions);
```

### Voir également

* class [MetafileRenderingOptions](../)
* espace de noms [Aspose.Words.Saving](../../metafilerenderingoptions/)
* Assemblée [Aspose.Words](../../../)


