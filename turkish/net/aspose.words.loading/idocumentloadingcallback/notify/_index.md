---
title: IDocumentLoadingCallback.Notify
linktitle: Notify
articleTitle: Notify
second_title: .NET için Aspose.Words
description: IDocumentLoadingCallback Notify yöntemi ile belge yükleme ilerlemesini zahmetsizce takip edin. Gerçek zamanlı güncellemelerle kullanıcı deneyimini geliştirin!
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

## Notlar

Bu arayüzün birincil kullanım amacı, uygulama kodunun ilerleme durumunu elde etmesini ve yükleme işlemini sonlandırmasını sağlamaktır.

Kürtaj için ilerleme geri çağrısından bir istisna atılmalı ve tüketici kodunda yakalanmalıdır.

## Örnekler

Belge yüklemesinin beklenen yükleme süresini aşması durumunda kullanıcıya nasıl bildirimde bulunulacağını gösterir.

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

        // Yükleme süresi sorununu çöz.
    }
}

/// <summary>
/// "MaxDuration" saniyesinden sonra belge yüklemeyi iptal et.
/// </summary>
public class LoadingProgressCallback : IDocumentLoadingCallback
{
    /// <summary>
    /// Merkez
    /// </summary>
    public LoadingProgressCallback()
    {
        mLoadingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Belge yüklenirken çağrılan geri çağırma yöntemi.
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
    /// Belgenin yüklenmeye başladığı tarih ve saat.
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
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
