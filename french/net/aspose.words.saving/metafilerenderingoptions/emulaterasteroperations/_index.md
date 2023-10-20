---
title: MetafileRenderingOptions.EmulateRasterOperations
linktitle: EmulateRasterOperations
articleTitle: EmulateRasterOperations
second_title: Aspose.Words pour .NET
description: MetafileRenderingOptions EmulateRasterOperations propriété. Obtient ou définit une valeur déterminant si les opérations raster doivent être émulées ou non en C#.
type: docs
weight: 30
url: /fr/net/aspose.words.saving/metafilerenderingoptions/emulaterasteroperations/
---
## MetafileRenderingOptions.EmulateRasterOperations property

Obtient ou définit une valeur déterminant si les opérations raster doivent être émulées ou non.

```csharp
public bool EmulateRasterOperations { get; set; }
```

## Remarques

Des opérations raster spécifiques pourraient être utilisées dans les métafichiers. Ils ne peuvent pas être rendus directement en graphiques vectoriels. Les opérations d'émulation raster nécessitent une rastérisation partielle des graphiques vectoriels résultants, ce qui peut affecter les performances de rendu du métafichier .

Lorsque cette valeur est fixée à`vrai`, Aspose.Words émule les opérations raster. La sortie résultante peut-être partiellement pixellisée et les performances peuvent être plus lentes.

Lorsque cette valeur est fixée à`FAUX`, Aspose.Words n'émule pas les opérations raster. Lorsqu'Aspose.Words rencontre une opération raster dans un métafichier, il revient au rendu du métafichier dans un bitmap en utilisant le système d'exploitation .

Cette option est utilisée uniquement lorsque le métafichier est rendu sous forme de graphiques vectoriels.

La valeur par défaut est`vrai`.

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

* class [MetafileRenderingOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
