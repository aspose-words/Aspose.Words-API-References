---
title: MetafileRenderingMode Enum
linktitle: MetafileRenderingMode
articleTitle: MetafileRenderingMode
second_title: Aspose.Words pour .NET
description: Découvrez comment Aspose.Words.Saving.MetafileRenderingMode améliore le rendu des métafichiers WMF et EMF pour une qualité et des performances optimales des documents.
type: docs
weight: 6070
url: /fr/net/aspose.words.saving/metafilerenderingmode/
---
## MetafileRenderingMode enumeration

Spécifie comment Aspose.Words doit restituer les métafichiers WMF et EMF.

```csharp
public enum MetafileRenderingMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| VectorWithFallback | `0` | Aspose.Words tente de restituer un métafichier sous forme d'images vectorielles. Si Aspose.Words ne parvient pas à restituer correctement certains enregistrements du métafichier sous forme d'images vectorielles, il restitue ce métafichier sous forme d'image bitmap. |
| Vector | `1` | Aspose.Words rend un métafichier sous forme de graphiques vectoriels. |
| Bitmap | `2` | Aspose.Words appelle GDI+ pour restituer un métafichier en bitmap, puis enregistre le bitmap dans le document de sortie. |

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
