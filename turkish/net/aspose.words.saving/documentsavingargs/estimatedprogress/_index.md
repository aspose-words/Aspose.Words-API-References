---
title: EstimatedProgress
second_title: Aspose.Words for .NET API Referansı
description: Genel tahmini ilerleme yüzdesi.
type: docs
weight: 10
url: /tr/net/aspose.words.saving/documentsavingargs/estimatedprogress/
---
## DocumentSavingArgs.EstimatedProgress property

Genel tahmini ilerleme yüzdesi.

```csharp
public double EstimatedProgress { get; }
```

### Örnekler

Html'ye kaydederken bir belgenin nasıl yönetileceğini gösterir.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // Şu biçimler desteklenir: Html, Mhtml, Epub.
    HtmlSaveOptions saveOptions = new HtmlSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"HtmlSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// İlerleme geri araması kaydediliyor. "MaxDuration" saniyesinden sonra bir belge kaydetmeyi iptal edin.
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// Ktr.
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Belge kaydetme sırasında çağrılan geri arama yöntemi.
    /// </summary>
    /// <param name="args">Argümanları kaydetme.</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Belge kaydetmenin başladığı tarih ve saat.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Saniye cinsinden izin verilen maksimum süre.
    /// </summary>
    private const double MaxDuration = 0.1d;
}
```

docx'e kaydederken bir belgenin nasıl yönetileceğini gösterir.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // Şu formatlar desteklenir: Docx, FlatOpc, Docm, Dotm, Dotx.
    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"OoxmlSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// İlerleme geri araması kaydediliyor. "MaxDuration" saniyesinden sonra bir belge kaydetmeyi iptal edin.
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// Ktr.
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Belge kaydetme sırasında çağrılan geri arama yöntemi.
    /// </summary>
    /// <param name="args">Argümanları kaydetme.</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Belge kaydetmenin başladığı tarih ve saat.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Saniye cinsinden izin verilen maksimum süre.
    /// </summary>
    private const double MaxDuration = 0.01d;
}
```

xamlflow'a kaydederken bir belgenin nasıl yönetileceğini gösterir.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // Şu biçimler desteklenir: XamlFlow, XamlFlowPack.
    XamlFlowSaveOptions saveOptions = new XamlFlowSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"XamlFlowSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// İlerleme geri araması kaydediliyor. "MaxDuration" saniyesinden sonra bir belge kaydetmeyi iptal edin.
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// Ktr.
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Belge kaydetme sırasında çağrılan geri arama yöntemi.
    /// </summary>
    /// <param name="args">Argümanları kaydetme.</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Belge kaydetmenin başladığı tarih ve saat.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Saniye cinsinden izin verilen maksimum süre.
    /// </summary>
    private const double MaxDuration = 0.01d;
}
```

### Ayrıca bakınız

* class [DocumentSavingArgs](../)
* ad alanı [Aspose.Words.Saving](../../documentsavingargs/)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
