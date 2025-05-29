---
title: DocumentSavingArgs Class
linktitle: DocumentSavingArgs
articleTitle: DocumentSavingArgs
second_title: .NET için Aspose.Words
description: Uygulamalarınızda belge kaydetme olaylarını etkili bir şekilde yönetmek için gerekli olan Aspose.Words.Saving.DocumentSavingArgs sınıfını keşfedin.
type: docs
weight: 5700
url: /tr/net/aspose.words.saving/documentsavingargs/
---
## DocumentSavingArgs class

Bir argüman,[`Notify`](../idocumentsavingcallback/notify/) .

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Bir Belgeyi Kaydet](https://docs.aspose.com/words/net/save-a-document/) belgeleme makalesi.

```csharp
public sealed class DocumentSavingArgs
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [EstimatedProgress](../../aspose.words.saving/documentsavingargs/estimatedprogress/) { get; } | Genel tahmini ilerleme yüzdesi. |

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

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
