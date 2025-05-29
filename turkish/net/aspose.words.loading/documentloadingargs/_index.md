---
title: DocumentLoadingArgs Class
linktitle: DocumentLoadingArgs
articleTitle: DocumentLoadingArgs
second_title: .NET için Aspose.Words
description: Verimli belge yükleme için Aspose.Words.Loading.DocumentLoadingArgs sınıfını keşfedin. Güçlü bildirim argümanlarıyla iş akışınızı geliştirin.
type: docs
weight: 4040
url: /tr/net/aspose.words.loading/documentloadingargs/
---
## DocumentLoadingArgs class

Bir argüman,[`Notify`](../idocumentloadingcallback/notify/) .

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yükleme Seçeneklerini Belirleyin](https://docs.aspose.com/words/net/specify-load-options/) belgeleme makalesi.

```csharp
public sealed class DocumentLoadingArgs
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [EstimatedProgress](../../aspose.words.loading/documentloadingargs/estimatedprogress/) { get; } | Genel tahmini ilerleme yüzdesi. |

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

* ad alanı [Aspose.Words.Loading](../../aspose.words.loading/)
* toplantı [Aspose.Words](../../)
