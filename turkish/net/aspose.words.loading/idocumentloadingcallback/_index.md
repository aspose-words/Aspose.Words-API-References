---
title: IDocumentLoadingCallback Interface
linktitle: IDocumentLoadingCallback
articleTitle: IDocumentLoadingCallback
second_title: Aspose.Words for .NET
description: Aspose.Words.Loading.IDocumentLoadingCallback arayüz. Bir belgeyi yüklerken kendi özel yönteminizin çağrılmasını istiyorsanız bu arayüzü uygulayın C#'da.
type: docs
weight: 3630
url: /tr/net/aspose.words.loading/idocumentloadingcallback/
---
## IDocumentLoadingCallback interface

Bir belgeyi yüklerken kendi özel yönteminizin çağrılmasını istiyorsanız bu arayüzü uygulayın.

```csharp
public interface IDocumentLoadingCallback
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Notify](../../aspose.words.loading/idocumentloadingcallback/notify/)(*[DocumentLoadingArgs](../documentloadingargs/)*) | Bu, belge yükleme işleminin ilerlemesini bildirmek için çağrılır. |

## Örnekler

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

* ad alanı [Aspose.Words.Loading](../../aspose.words.loading/)
* toplantı [Aspose.Words](../../)
