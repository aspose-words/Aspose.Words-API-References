---
title: IDocumentLoadingCallback.Notify
second_title: Aspose.Words for .NET API Referansı
description: IDocumentLoadingCallback yöntem. Bu belge yükleme ilerlemesini bildirmek için çağrılır.
type: docs
weight: 10
url: /tr/net/aspose.words.loading/idocumentloadingcallback/notify/
---
## IDocumentLoadingCallback.Notify method

Bu, belge yükleme ilerlemesini bildirmek için çağrılır.

```csharp
public void Notify(DocumentLoadingArgs args)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| args | DocumentLoadingArgs | Olayın bir argümanı. |

### Notlar

Bu arabirimin birincil kullanımı, uygulama kodunun ilerleme durumunu almasına izin vermek ve yükleme işlemini iptal etmektir.

Kürtaj için ilerleme geri çağrısından bir istisna atılmalı ve tüketici kodunda yakalanmalıdır.

### Örnekler

Belge yüklemesi, beklenen yükleme süresini aştığında kullanıcıya nasıl bildirileceğini gösterir.

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

        // Yükleme süresi sorununu ele al.
    }
}

/// <summary>
/// "MaxDuration" saniyesinden sonra bir belge yüklemesini iptal edin.
/// </summary>
public class LoadingProgressCallback : IDocumentLoadingCallback
{
    /// <summary>
    /// Ktr.
    /// </summary>
    public LoadingProgressCallback()
    {
        mLoadingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Belge yükleme sırasında çağrılan geri arama yöntemi.
    /// </summary>
    /// <param name="args">Argümanlar yükleniyor.</param>
    public void Notify(DocumentLoadingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mLoadingStartedAt).TotalSeconds;

        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Belge yüklemenin başladığı tarih ve saat.
    /// </summary>
    private readonly DateTime mLoadingStartedAt;

    /// <summary>
    /// Saniye cinsinden izin verilen maksimum süre.
    /// </summary>
    private const double MaxDuration = 0.5;
}
```

### Ayrıca bakınız

* property [ProgressCallback](../../loadoptions/progresscallback/)
* class [DocumentLoadingArgs](../../documentloadingargs/)
* interface [IDocumentLoadingCallback](../)
* ad alanı [Aspose.Words.Loading](../../idocumentloadingcallback/)
* toplantı [Aspose.Words](../../../)


