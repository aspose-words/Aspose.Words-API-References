---
title: IDocumentSavingCallback.Notify
linktitle: Notify
articleTitle: Notify
second_title: .NET için Aspose.Words
description: iDocumentSavingCallback Notify yöntemi ile belge kaydetme ilerlemesini takip edin. Uygulamanızın verimliliğini ve kullanıcı deneyimini bugün artırın!
type: docs
weight: 10
url: /tr/net/aspose.words.saving/idocumentsavingcallback/notify/
---
## IDocumentSavingCallback.Notify method

Bu, belge kaydetme ilerlemesini bildirmek için çağrılır.

```csharp
public void Notify(DocumentSavingArgs args)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| args | DocumentSavingArgs | Olayın bir argümanı. |

## Notlar

Bu arayüzün birincil kullanım amacı, uygulama kodunun ilerleme durumunu elde etmesini ve kaydetme işlemini iptal etmesini sağlamaktır.

Kürtaj için ilerleme geri çağrısından bir istisna atılmalı ve tüketici kodunda yakalanmalıdır.

## Örnekler

Bir belgeyi HTML'e kaydederken nasıl yöneteceğinizi gösterir.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // Aşağıdaki formatlar desteklenmektedir: Html, Mhtml, Epub.
    HtmlSaveOptions saveOptions = new HtmlSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"HtmlSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// İlerleme kaydetme geri araması. "MaxDuration" saniyesinden sonra belge kaydetmeyi iptal et.
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// Merkez
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Belge kaydedilirken çağrılan geri çağırma yöntemi.
    /// </summary>
    /// <param name="args">Argümanlar kaydediliyor.</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Belgenin kaydedilmeye başlandığı tarih ve saat.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Saniye cinsinden izin verilen maksimum süre.
    /// </summary>
    private const double MaxDuration = 0.1d;
}
```

Bir belgeyi docx olarak kaydederken nasıl yöneteceğinizi gösterir.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // Aşağıdaki formatlar desteklenmektedir: Docx, FlatOpc, Docm, Dotm, Dotx.
    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"OoxmlSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// İlerleme kaydetme geri araması. "MaxDuration" saniyesinden sonra belge kaydetmeyi iptal et.
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// Merkez
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Belge kaydedilirken çağrılan geri çağırma yöntemi.
    /// </summary>
    /// <param name="args">Argümanlar kaydediliyor.</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Belgenin kaydedilmeye başlandığı tarih ve saat.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Saniye cinsinden izin verilen maksimum süre.
    /// </summary>
    private const double MaxDuration = 0.01d;
}
```

Xamlflow'a kaydederken bir belgenin nasıl yönetileceğini gösterir.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // Aşağıdaki formatlar desteklenmektedir: XamlFlow, XamlFlowPack.
    XamlFlowSaveOptions saveOptions = new XamlFlowSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"XamlFlowSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// İlerleme kaydetme geri araması. "MaxDuration" saniyesinden sonra belge kaydetmeyi iptal et.
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// Merkez
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Belge kaydedilirken çağrılan geri çağırma yöntemi.
    /// </summary>
    /// <param name="args">Argümanlar kaydediliyor.</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Belgenin kaydedilmeye başlandığı tarih ve saat.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Saniye cinsinden izin verilen maksimum süre.
    /// </summary>
    private const double MaxDuration = 0.01d;
}
```

### Ayrıca bakınız

* class [DocumentSavingArgs](../../documentsavingargs/)
* interface [IDocumentSavingCallback](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
