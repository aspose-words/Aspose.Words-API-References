---
title: IDocumentLoadingCallback
second_title: Référence de l'API Aspose.Words pour .NET
description: Implémentez cette interface si vous souhaitez que votre propre méthode personnalisée soit appelée lors du chargement dun document.
type: docs
weight: 3430
url: /fr/net/aspose.words.loading/idocumentloadingcallback/
---
## IDocumentLoadingCallback interface

Implémentez cette interface si vous souhaitez que votre propre méthode personnalisée soit appelée lors du chargement d'un document.

```csharp
public interface IDocumentLoadingCallback
```

## Méthodes

| Nom | La description |
| --- | --- |
| [Notify](../../aspose.words.loading/idocumentloadingcallback/notify)(DocumentLoadingArgs) | Ceci est appelé pour notifier la progression du chargement du document. |

### Exemples

Montre comment avertir l'utilisateur si le chargement du document a dépassé le temps de chargement prévu.

```csharp
[Test]
public void ProgressCallback()
{
    LoadingProgressCallback progressCallback = new LoadingProgressCallback();

    LoadOptions loadOptions = new LoadOptions { ProgressCallback = progressCallback };

    try
    {
        Document doc = new Document(MyDir + "Big document.docx", loadOptions);
    }
    catch (OperationCanceledException exception)
    {
        Console.WriteLine(exception.Message);

        // Gère le problème de durée de chargement.
    }
}

/// <summary>
/// Annule le chargement d'un document après les secondes "MaxDuration".
/// </summary>
public class LoadingProgressCallback : IDocumentLoadingCallback
{
    /// <summary>
    /// Ctr.
    /// </summary>
    public LoadingProgressCallback()
    {
        mLoadingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Méthode de rappel appelée lors du chargement du document.
    /// </summary>
    /// <param name="args">Chargement des arguments.</param>
    public void Notify(DocumentLoadingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mLoadingStartedAt).TotalSeconds;

        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Date et heure de démarrage du chargement du document.
    /// </summary>
    private readonly DateTime mLoadingStartedAt;

    /// <summary>
    /// Durée maximale autorisée en sec.
    /// </summary>
    private const double MaxDuration = 0.5;
}
```

### Voir également

* espace de noms [Aspose.Words.Loading](../../aspose.words.loading)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
