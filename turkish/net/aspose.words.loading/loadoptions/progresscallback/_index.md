---
title: LoadOptions.ProgressCallback
linktitle: ProgressCallback
articleTitle: ProgressCallback
second_title: .NET için Aspose.Words
description: Belge yükleme ilerlemesini verimli bir şekilde izlemek için LoadOptions ProgressCallback özelliğini keşfedin. Uygulamanızın performansını ve kullanıcı deneyimini geliştirin!
type: docs
weight: 130
url: /tr/net/aspose.words.loading/loadoptions/progresscallback/
---
## LoadOptions.ProgressCallback property

Bir belge yüklenirken çağrılır ve yükleme ilerlemesiyle ilgili verileri kabul eder.

```csharp
public IDocumentLoadingCallback ProgressCallback { get; set; }
```

## Notlar

Docx ,FlatOpc ,Docm ,Dotm ,Dotx ,Markdown ,Rtf ,WordML ,Doc ,Dot ,Odt ,Ott desteklenen formatlar.

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

* interface [IDocumentLoadingCallback](../../idocumentloadingcallback/)
* class [LoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
