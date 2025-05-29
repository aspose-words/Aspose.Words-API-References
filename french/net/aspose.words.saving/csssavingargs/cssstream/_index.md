---
title: CssSavingArgs.CssStream
linktitle: CssStream
articleTitle: CssStream
second_title: Aspose.Words pour .NET
description: Optimisez votre stockage CSS avec la propriété CssSavingArgs CssStream, permettant une sauvegarde transparente des données CSS dans votre flux préféré.
type: docs
weight: 10
url: /fr/net/aspose.words.saving/csssavingargs/cssstream/
---
## CssSavingArgs.CssStream property

Permet de spécifier le flux dans lequel les informations CSS seront enregistrées.

```csharp
public Stream CssStream { get; set; }
```

## Remarques

Cette propriété vous permet d'enregistrer des informations CSS dans un flux.

La valeur par défaut est`nul`Cette propriété ne supprime pas l'enregistrement des informations CSS dans un fichier ni leur intégration dans un document HTML. Pour supprimer l'exportation des informations CSS, utilisez l'option[`IsExportNeeded`](../isexportneeded/) propriété.

En utilisant[`ICssSavingCallback`](../../icsssavingcallback/) Vous ne pouvez pas remplacer CSS par . Ce format est uniquement destiné à l'enregistrement CSS dans un flux.

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

* class [CssSavingArgs](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
