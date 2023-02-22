---
title: IDocumentLoadingCallback.Notify
second_title: Référence de l'API Aspose.Words pour .NET
description: IDocumentLoadingCallback méthode. Ceci est appelé pour notifier la progression du chargement du document.
type: docs
weight: 10
url: /fr/net/aspose.words.loading/idocumentloadingcallback/notify/
---
## IDocumentLoadingCallback.Notify method

Ceci est appelé pour notifier la progression du chargement du document.

```csharp
public void Notify(DocumentLoadingArgs args)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| args | DocumentLoadingArgs | Un argument de l'événement. |

### Remarques

Les principales utilisations de cette interface sont de permettre au code d'application d'obtenir l'état de progression et d'abandonner le processus de chargement.

Une exception doit être levée à partir du rappel de progression pour l'avortement et elle doit être capturée dans le code du consommateur.

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

* property [ProgressCallback](../../loadoptions/progresscallback/)
* class [DocumentLoadingArgs](../../documentloadingargs/)
* interface [IDocumentLoadingCallback](../)
* espace de noms [Aspose.Words.Loading](../../idocumentloadingcallback/)
* Assemblée [Aspose.Words](../../../)


