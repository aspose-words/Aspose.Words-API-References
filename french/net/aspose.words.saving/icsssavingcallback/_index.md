---
title: ICssSavingCallback Interface
linktitle: ICssSavingCallback
articleTitle: ICssSavingCallback
second_title: Aspose.Words pour .NET
description: Contrôlez l'enregistrement CSS dans Aspose.Words avec l'interface ICssSavingCallback. Personnalisez la sortie de votre document HTML pour un style et une flexibilité améliorés.
type: docs
weight: 5880
url: /fr/net/aspose.words.saving/icsssavingcallback/
---
## ICssSavingCallback interface

Implémentez cette interface si vous souhaitez contrôler la manière dont Aspose.Words enregistre le CSS (Cascading Style Sheet) lors de l'enregistrement d'un document au format HTML.

```csharp
public interface ICssSavingCallback
```

## Méthodes

| Nom | La description |
| --- | --- |
| [CssSaving](../../aspose.words.saving/icsssavingcallback/csssaving/)(*[CssSavingArgs](../csssavingargs/)*) | Appelé lorsque Aspose.Words enregistre une feuille de style CSS (Cascading Style Sheet). |

## Exemples

Montre comment travailler avec les feuilles de style CSS créées par une conversion HTML.

```csharp
public void ExternalCssFilenames()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Créez un objet « HtmlFixedSaveOptions », que nous pouvons transmettre à la méthode « Save » du document
    // pour modifier la façon dont nous convertissons le document en HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Définissez la propriété « CssStylesheetType » sur « CssStyleSheetType.External » pour
    // accompagner un document HTML enregistré avec un fichier de feuille de style CSS externe.
    options.CssStyleSheetType = CssStyleSheetType.External;

    // Vous trouverez ci-dessous deux manières de spécifier les répertoires et les noms de fichiers pour les feuilles de style CSS de sortie.
    // 1 - Utilisez la propriété « CssStyleSheetFileName » pour attribuer un nom de fichier à notre feuille de style :
    options.CssStyleSheetFileName = ArtifactsDir + "SavingCallback.ExternalCssFilenames.css";

    // 2 - Utilisez un rappel personnalisé pour nommer notre feuille de style :
    options.CssSavingCallback =
        new CustomCssSavingCallback(ArtifactsDir + "SavingCallback.ExternalCssFilenames.css", true, false);

    doc.Save(ArtifactsDir + "SavingCallback.ExternalCssFilenames.html", options);
}

/// <summary>
/// Définit un nom de fichier personnalisé, ainsi que d'autres paramètres pour une feuille de style CSS externe.
/// </summary>
private class CustomCssSavingCallback : ICssSavingCallback
{
    public CustomCssSavingCallback(string cssDocFilename, bool isExportNeeded, bool keepCssStreamOpen)
    {
        mCssTextFileName = cssDocFilename;
        mIsExportNeeded = isExportNeeded;
        mKeepCssStreamOpen = keepCssStreamOpen;
    }

    public void CssSaving(CssSavingArgs args)
    {
        // Nous pouvons accéder à l'intégralité du document source via la propriété "Document".
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        args.CssStream = new FileStream(mCssTextFileName, FileMode.Create);
        args.IsExportNeeded = mIsExportNeeded;
        args.KeepCssStreamOpen = mKeepCssStreamOpen;

        Assert.True(args.CssStream.CanWrite);
    }

    private readonly string mCssTextFileName;
    private readonly bool mIsExportNeeded;
    private readonly bool mKeepCssStreamOpen;
}
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
