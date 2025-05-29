---
title: DocumentSavingArgs Class
linktitle: DocumentSavingArgs
articleTitle: DocumentSavingArgs
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Saving.DocumentSavingArgs, essentielle pour gérer efficacement les événements de sauvegarde de documents dans vos applications.
type: docs
weight: 5700
url: /fr/net/aspose.words.saving/documentsavingargs/
---
## DocumentSavingArgs class

Un argument passé dans[`Notify`](../idocumentsavingcallback/notify/) .

Pour en savoir plus, visitez le[Enregistrer un document](https://docs.aspose.com/words/net/save-a-document/) article de documentation.

```csharp
public sealed class DocumentSavingArgs
```

## Propriétés

| Nom | La description |
| --- | --- |
| [EstimatedProgress](../../aspose.words.saving/documentsavingargs/estimatedprogress/) { get; } | Pourcentage global estimé de progression. |

## Exemples

Montre comment gérer un document lors de son enregistrement au format HTML.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // Les formats suivants sont pris en charge : Html, Mhtml, Epub.
    HtmlSaveOptions saveOptions = new HtmlSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"HtmlSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// Rappel de progression de l'enregistrement. Annuler l'enregistrement d'un document après la durée maximale (en secondes).
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// Centre.
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Méthode de rappel appelée lors de l'enregistrement du document.
    /// </summary>
    /// <param name="args">Sauvegarde des arguments.</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Date et heure de début de l'enregistrement du document.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Durée maximale autorisée en sec.
    /// </summary>
    private const double MaxDuration = 0.1d;
}
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
