---
title: IDocumentLoadingCallback.Notify
second_title: Aspose.Words for .NET API Referansı
description: IDocumentLoadingCallback yöntem. Bu belge yükleme işleminin ilerlemesini bildirmek için çağrılır.
type: docs
weight: 10
url: /tr/net/aspose.words.loading/idocumentloadingcallback/notify/
---
## IDocumentLoadingCallback.Notify method

Bu, belge yükleme işleminin ilerlemesini bildirmek için çağrılır.

```csharp
public void Notify(DocumentLoadingArgs args)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| args | DocumentLoadingArgs | Olayın bir argümanı. |

### Notlar

Bu arayüzün birincil kullanımları, uygulama kodunun ilerleme durumunu elde etmesine ve yükleme işlemini iptal etmesine izin vermektir.

Kürtaj için Progress geri çağrısından bir istisna atılmalı ve tüketici koduna yakalanmalıdır.

### Örnekler

Belge yüklemesinin beklenen yükleme süresini aşması durumunda kullanıcıya nasıl bilgi verileceğini gösterir.

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

        // Yükleme süresi sorununu ele alın.
    }
}

/// <summary>
/// "MaxDuration" saniyeden sonra belge yüklemeyi iptal edin.
/// </summary>
public class LoadingProgressCallback : IDocumentLoadingCallback
{
    /// <summary>
    /// Kontrol Noktası
    /// </summary>
    public LoadingProgressCallback()
    {
        mLoadingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Doküman yüklenirken çağrılan geri çağırma yöntemi.
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
    /// Belge yüklemenin başlatıldığı tarih ve saat.
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


