---
title: EstimatedProgress
second_title: Referencia de API de Aspose.Words para .NET
description: Progreso porcentual estimado general.
type: docs
weight: 10
url: /es/net/aspose.words.saving/documentsavingargs/estimatedprogress/
---
## DocumentSavingArgs.EstimatedProgress property

Progreso porcentual estimado general.

```csharp
public double EstimatedProgress { get; }
```

### Ejemplos

Muestra cómo administrar un documento mientras se guarda en html.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // Se admiten los siguientes formatos: Html, Mhtml, Epub.
    HtmlSaveOptions saveOptions = new HtmlSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"HtmlSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// Guardando devolución de llamada de progreso. Cancele el guardado de un documento después de los segundos "MaxDuration".
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// Centro
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Método de devolución de llamada que llamó durante el guardado del documento.
    /// </summary>
    /// <param name="args">Guardando argumentos.</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Fecha y hora en que se inicia el guardado del documento.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Duración máxima permitida en seg.
    /// </summary>
    private const double MaxDuration = 0.1d;
}
```

Muestra cómo administrar un documento mientras se guarda en docx.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // Se admiten los siguientes formatos: Docx, FlatOpc, Docm, Dotm, Dotx.
    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"OoxmlSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// Guardando devolución de llamada de progreso. Cancele el guardado de un documento después de los segundos "MaxDuration".
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// Centro
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Método de devolución de llamada que llamó durante el guardado del documento.
    /// </summary>
    /// <param name="args">Guardando argumentos.</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Fecha y hora en que se inicia el guardado del documento.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Duración máxima permitida en seg.
    /// </summary>
    private const double MaxDuration = 0.01d;
}
```

Muestra cómo administrar un documento mientras se guarda en xamlflow.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // Se admiten los siguientes formatos: XamlFlow, XamlFlowPack.
    XamlFlowSaveOptions saveOptions = new XamlFlowSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"XamlFlowSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// Guardando devolución de llamada de progreso. Cancele el guardado de un documento después de los segundos "MaxDuration".
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// Centro
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Método de devolución de llamada que llamó durante el guardado del documento.
    /// </summary>
    /// <param name="args">Guardando argumentos.</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Fecha y hora en que se inicia el guardado del documento.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Duración máxima permitida en seg.
    /// </summary>
    private const double MaxDuration = 0.01d;
}
```

### Ver también

* class [DocumentSavingArgs](../../documentsavingargs)
* espacio de nombres [Aspose.Words.Saving](../../documentsavingargs)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
