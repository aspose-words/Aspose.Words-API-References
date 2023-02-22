---
title: Enum MetafileRenderingMode
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Saving.MetafileRenderingMode énumération. Spécifie comment Aspose.Words doit restituer les métafichiers WMF et EMF.
type: docs
weight: 5010
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
| VectorWithFallback | `0` | Aspose.Words essaie de restituer un métafichier sous forme de graphiques vectoriels. Si Aspose.Words ne peut pas restituer correctement certains des enregistrements de métafichier en graphiques vectoriels, Aspose.Words restitue ce métafichier en bitmap. |
| Vector | `1` | Aspose.Words rend un métafichier sous forme de graphiques vectoriels. |
| Bitmap | `2` | Aspose.Words appelle GDI+ pour restituer un métafichier en bitmap, puis enregistre le bitmap dans le document de sortie. |

### Exemples

Affiche l'ajout d'un retour au rendu bitmap et la modification du type d'avertissements concernant les enregistrements de métafichiers non pris en charge.

```csharp
{
    Document doc = new Document(MyDir + "WMF with image.docx");

    MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

    // Définissez la propriété "EmulateRasterOperations" sur "false" pour revenir au bitmap lorsque
    // il rencontre un métafichier, qui nécessitera des opérations raster pour s'afficher dans le PDF de sortie.
    metafileRenderingOptions.EmulateRasterOperations = false;

    // Définissez la propriété "RenderingMode" sur "VectorWithFallback" pour essayer de restituer chaque métafichier à l'aide de graphiques vectoriels.
    metafileRenderingOptions.RenderingMode = MetafileRenderingMode.VectorWithFallback;

    // Crée un objet "PdfSaveOptions" que nous pouvons passer à la méthode "Save" du document
    // pour modifier la façon dont cette méthode convertit le document en .PDF et applique la configuration
    // dans notre objet MetafileRenderingOptions à l'opération d'enregistrement.
    PdfSaveOptions saveOptions = new PdfSaveOptions();
    saveOptions.MetafileRenderingOptions = metafileRenderingOptions;

    HandleDocumentWarnings callback = new HandleDocumentWarnings();
    doc.WarningCallback = callback;

    doc.Save(ArtifactsDir + "PdfSaveOptions.HandleBinaryRasterWarnings.pdf", saveOptions);

    Assert.AreEqual(1, callback.Warnings.Count);
    Assert.AreEqual("'R2_XORPEN' binary raster operation is partly supported.",
        callback.Warnings[0].Description);
}

/// <summary>
/// Imprime et collecte les avertissements liés à la perte de mise en forme qui se produisent lors de l'enregistrement d'un document.
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


