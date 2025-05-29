---
title: DocumentLoadingArgs.EstimatedProgress
linktitle: EstimatedProgress
articleTitle: EstimatedProgress
second_title: Aspose.Words pour .NET
description: Suivez les progrès sans effort avec la propriété EstimatedProgress de DocumentLoadingArgs, fournissant des mises à jour de pourcentage en temps réel pour une efficacité accrue.
type: docs
weight: 10
url: /fr/net/aspose.words.loading/documentloadingargs/estimatedprogress/
---
## DocumentLoadingArgs.EstimatedProgress property

Pourcentage global estimé de progression.

```csharp
public double EstimatedProgress { get; }
```

## Exemples

Montre comment avertir l'utilisateur si le chargement du document dépasse le temps de chargement prévu.

```csharp
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

        // Gérer le problème de durée de chargement.
    }
}

/// <summary>
/// Annuler le chargement d'un document après les secondes "MaxDuration".
/// </summary>
public class LoadingProgressCallback : IDocumentLoadingCallback
{
    /// <summary>
    /// Centre.
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
    /// Date et heure de début du chargement du document.
    /// </summary>
    private readonly DateTime mLoadingStartedAt;

    /// <summary>
    /// Durée maximale autorisée en sec.
    /// </summary>
    private const double MaxDuration = 0.5;
}
```

### Voir également

* class [DocumentLoadingArgs](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
