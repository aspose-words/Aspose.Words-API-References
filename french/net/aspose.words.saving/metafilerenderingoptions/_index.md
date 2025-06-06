---
title: MetafileRenderingOptions Class
linktitle: MetafileRenderingOptions
articleTitle: MetafileRenderingOptions
second_title: Aspose.Words pour .NET
description: Découvrez Aspose.Words.Saving.MetafileRenderingOptions pour un contrôle et une personnalisation améliorés du rendu des métafichiers dans vos documents. Optimisez votre flux de travail dès aujourd'hui !
type: docs
weight: 6080
url: /fr/net/aspose.words.saving/metafilerenderingoptions/
---
## MetafileRenderingOptions class

Permet de spécifier des options de rendu de métafichier supplémentaires.

Pour en savoir plus, visitez le[Gestion des métafichiers Windows](https://docs.aspose.com/words/net/handling-windows-metafiles/) article de documentation.

```csharp
public class MetafileRenderingOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [MetafileRenderingOptions](metafilerenderingoptions/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [EmfPlusDualRenderingMode](../../aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant comment les métafichiers EMF+ Dual doivent être rendus. |
| [EmulateRasterOperations](../../aspose.words.saving/metafilerenderingoptions/emulaterasteroperations/) { get; set; } | Obtient ou définit une valeur déterminant si les opérations raster doivent être émulées ou non. |
| [EmulateRenderingToSizeOnPage](../../aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/) { get; set; } | Obtient ou définit une valeur déterminant si le rendu du métafichier émule l'affichage du métafichier en fonction de la taille de la page ou l'affichage du métafichier dans sa taille par défaut. |
| [EmulateRenderingToSizeOnPageResolution](../../aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/) { get; set; } | Obtient ou définit la résolution en pixels par pouce pour l'émulation du rendu du métafichier à la taille de la page. |
| [RenderingMode](../../aspose.words.saving/metafilerenderingoptions/renderingmode/) { get; set; } | Obtient ou définit une valeur déterminant comment les images de métafichier doivent être rendues. |
| [UseEmfEmbeddedToWmf](../../aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/) { get; set; } | Obtient ou définit une valeur déterminant comment les métafichiers WMF avec des métafichiers EMF intégrés doivent être rendus. |
| [UseGdiRasterOperationsEmulation](../../aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser GDI+ pour l'émulation des opérations raster. |

## Exemples

Affiche un retour au rendu bitmap et un changement de type d'avertissements concernant les enregistrements de métafichiers non pris en charge.

```csharp
public void HandleBinaryRasterWarnings()
{
    Document doc = new Document(MyDir + "WMF with image.docx");

    MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

    // Définissez la propriété « EmulateRasterOperations » sur « false » pour revenir au bitmap lorsque
    // il rencontre un métafichier, qui nécessitera des opérations raster pour être rendu dans le PDF de sortie.
    metafileRenderingOptions.EmulateRasterOperations = false;

    // Définissez la propriété « RenderingMode » sur « VectorWithFallback » pour essayer de restituer chaque métafichier à l'aide de graphiques vectoriels.
    metafileRenderingOptions.RenderingMode = MetafileRenderingMode.VectorWithFallback;

    // Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
    // pour modifier la façon dont cette méthode convertit le document en .PDF et applique la configuration
    // dans notre objet MetafileRenderingOptions pour l'opération de sauvegarde.
    PdfSaveOptions saveOptions = new PdfSaveOptions();
    saveOptions.MetafileRenderingOptions = metafileRenderingOptions;

    HandleDocumentWarnings callback = new HandleDocumentWarnings();
    doc.WarningCallback = callback;

    doc.Save(ArtifactsDir + "PdfSaveOptions.HandleBinaryRasterWarnings.pdf", saveOptions);

    Assert.AreEqual(1, callback.Warnings.Count);
    Assert.AreEqual("'R2_XORPEN' binary raster operation is not supported.",
        callback.Warnings[0].Description);
}

/// <summary>
/// Imprime et collecte les avertissements liés à la perte de formatage qui se produisent lors de l'enregistrement d'un document.
/// </summary>
public class HandleDocumentWarnings : IWarningCallback
{
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.MinorFormattingLoss)
        {
            Console.WriteLine("Unsupported operation: " + info.Description);
            Warnings.Warning(info);
        }
    }

    public WarningInfoCollection Warnings = new WarningInfoCollection();
}
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
