---
title: MetafileRenderingOptions.RenderingMode
linktitle: RenderingMode
articleTitle: RenderingMode
second_title: Aspose.Words pour .NET
description: MetafileRenderingOptions RenderingMode propriété. Obtient ou définit une valeur déterminant la façon dont les images de métafichier doivent être rendues en C#.
type: docs
weight: 60
url: /fr/net/aspose.words.saving/metafilerenderingoptions/renderingmode/
---
## MetafileRenderingOptions.RenderingMode property

Obtient ou définit une valeur déterminant la façon dont les images de métafichier doivent être rendues.

```csharp
public MetafileRenderingMode RenderingMode { get; set; }
```

## Remarques

La valeur par défaut dépend du format de sauvegarde. Pour les images c'estBitmap . Pour les autres formats, c'estVectorWithFallback.

## Exemples

Affiche l'ajout d'une solution de secours au rendu bitmap et la modification du type d'avertissements concernant les enregistrements de métafichiers non pris en charge.

```csharp
public void HandleBinaryRasterWarnings()
{
    Document doc = new Document(MyDir + "WMF with image.docx");

    MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

    // Définissez la propriété "EmulateRasterOperations" sur "false" pour revenir au bitmap lorsque
    // il rencontre un métafichier, qui nécessitera le rendu des opérations raster dans le PDF de sortie.
    metafileRenderingOptions.EmulateRasterOperations = false;

    // Définissez la propriété "RenderingMode" sur "VectorWithFallback" pour essayer de restituer chaque métafichier à l'aide de graphiques vectoriels.
    metafileRenderingOptions.RenderingMode = MetafileRenderingMode.VectorWithFallback;

    // Crée un objet "PdfSaveOptions" que l'on peut passer à la méthode "Save" du document
    // pour modifier la façon dont cette méthode convertit le document en .PDF et applique la configuration
    // dans notre objet MetafileRenderingOptions à l'opération de sauvegarde.
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

* enum [MetafileRenderingMode](../../metafilerenderingmode/)
* class [MetafileRenderingOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
