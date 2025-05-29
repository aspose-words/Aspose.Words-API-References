---
title: IDocumentSavingCallback.Notify
linktitle: Notify
articleTitle: Notify
second_title: Aspose.Words pour .NET
description: Suivez la progression de l'enregistrement de vos documents grâce à la méthode de notification iDocumentSavingCallback. Améliorez l'efficacité et l'expérience utilisateur de votre application dès aujourd'hui !
type: docs
weight: 10
url: /fr/net/aspose.words.saving/idocumentsavingcallback/notify/
---
## IDocumentSavingCallback.Notify method

Ceci est appelé pour notifier la progression de l'enregistrement du document.

```csharp
public void Notify(DocumentSavingArgs args)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| args | DocumentSavingArgs | Un argument de l'événement. |

## Remarques

Les principales utilisations de cette interface sont de permettre au code d'application d'obtenir l'état de progression et d'abandonner le processus de sauvegarde.

Une exception doit être levée à partir du rappel de progression pour l'avortement et elle doit être interceptée dans le code du consommateur.

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

Montre comment gérer un document lors de son enregistrement au format docx.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // Les formats suivants sont pris en charge : Docx, FlatOpc, Docm, Dotm, Dotx.
    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"OoxmlSaveOptions.ProgressCallback.{ext}", saveOptions));
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
    private const double MaxDuration = 0.01d;
}
```

Montre comment gérer un document lors de l'enregistrement dans xamlflow.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // Les formats suivants sont pris en charge : XamlFlow, XamlFlowPack.
    XamlFlowSaveOptions saveOptions = new XamlFlowSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"XamlFlowSaveOptions.ProgressCallback.{ext}", saveOptions));
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
    private const double MaxDuration = 0.01d;
}
```

### Voir également

* class [DocumentSavingArgs](../../documentsavingargs/)
* interface [IDocumentSavingCallback](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
