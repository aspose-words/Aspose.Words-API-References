---
title: HtmlSaveOptions.CssStyleSheetFileName
linktitle: CssStyleSheetFileName
articleTitle: CssStyleSheetFileName
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété HtmlSaveOptions CssStyleSheetFileName personnalise vos exportations HTML avec un chemin de fichier CSS spécifié, améliorant ainsi le style de votre document.
type: docs
weight: 50
url: /fr/net/aspose.words.saving/htmlsaveoptions/cssstylesheetfilename/
---
## HtmlSaveOptions.CssStyleSheetFileName property

Spécifie le chemin et le nom du fichier de feuille de style en cascade (CSS) écrit lorsqu'un document est exporté au format HTML. La valeur par défaut est une chaîne vide.

```csharp
public string CssStyleSheetFileName { get; set; }
```

## Remarques

Cette propriété n'a d'effet que lors de l'enregistrement d'un document au format HTML et qu'une feuille de style CSS externe est demandée à l'aide de[`CssStyleSheetType`](../cssstylesheettype/).

Si cette propriété est vide, le fichier CSS sera enregistré dans le même dossier et avec le même nom que le document HTML mais avec l'extension ".css".

Si seul le chemin mais aucun nom de fichier est spécifié dans cette propriété, le fichier CSS sera enregistré dans le dossier specified et aura le même nom que le document HTML mais avec l'extension « .css ».

Si le dossier spécifié par cette propriété n'existe pas, il sera créé automatiquement avant l'enregistrement du fichier CSS .

Une autre façon de spécifier un dossier dans lequel le fichier CSS externe est enregistré est d'utiliser[`ResourceFolder`](../resourcefolder/) .

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

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
