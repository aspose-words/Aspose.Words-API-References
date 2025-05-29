---
title: CssSavingArgs Class
linktitle: CssSavingArgs
articleTitle: CssSavingArgs
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.CssSavingArgs, conçue pour améliorer le traitement de vos documents avec des données d'événement CssSaving personnalisables pour des résultats optimaux.
type: docs
weight: 5620
url: /fr/net/aspose.words.saving/csssavingargs/
---
## CssSavingArgs class

Fournit des données pour le[`CssSaving`](../icsssavingcallback/csssaving/) événement.

Pour en savoir plus, visitez le[Enregistrer un document](https://docs.aspose.com/words/net/save-a-document/) article de documentation.

```csharp
public class CssSavingArgs
```

## Propriétés

| Nom | La description |
| --- | --- |
| [CssStream](../../aspose.words.saving/csssavingargs/cssstream/) { get; set; } | Permet de spécifier le flux dans lequel les informations CSS seront enregistrées. |
| [Document](../../aspose.words.saving/csssavingargs/document/) { get; } | Obtient l'objet document en cours d'enregistrement. |
| [IsExportNeeded](../../aspose.words.saving/csssavingargs/isexportneeded/) { get; set; } | Permet de spécifier si le CSS sera exporté vers un fichier et intégré au document HTML. La valeur par défaut est`vrai` . Lorsque cette propriété est`FAUX` , les informations CSS ne seront pas enregistrées dans un fichier CSS et ne seront pas intégrées au document HTML. |
| [KeepCssStreamOpen](../../aspose.words.saving/csssavingargs/keepcssstreamopen/) { get; set; } | Spécifie si Aspose.Words doit garder le flux ouvert ou le fermer après avoir enregistré une information CSS. |

## Remarques

Par défaut, lorsque Aspose.Words enregistre un document au format HTML, il enregistre les informations CSS inline (en tant que valeur du**style** attribut sur chaque élément).

`CssSavingArgs` permet d'enregistrer les informations CSS dans un fichier en fournissant votre propre objet de flux.

Pour enregistrer le CSS dans le flux, utilisez le[`CssStream`](./cssstream/) propriété.

Pour supprimer l'enregistrement du CSS dans un fichier et l'intégration dans un document HTML, utilisez le[`IsExportNeeded`](./isexportneeded/) propriété.

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
