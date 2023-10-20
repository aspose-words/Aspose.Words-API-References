---
title: IPageSavingCallback Interface
linktitle: IPageSavingCallback
articleTitle: IPageSavingCallback
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.IPageSavingCallback arayüz. Bir belgeyi sabit sayfa formatlarında kaydederken Aspose.Wordsün ayrı sayfaları nasıl kaydettiğini kontrol etmek istiyorsanız bu arayüzü uygulayın C#'da.
type: docs
weight: 5180
url: /tr/net/aspose.words.saving/ipagesavingcallback/
---
## IPageSavingCallback interface

Bir belgeyi sabit sayfa formatlarında kaydederken Aspose.Words'ün ayrı sayfaları nasıl kaydettiğini kontrol etmek istiyorsanız bu arayüzü uygulayın.

```csharp
public interface IPageSavingCallback
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| [PageSaving](../../aspose.words.saving/ipagesavingcallback/pagesaving/)(*[PageSavingArgs](../pagesavingargs/)*) | Aspose.Words ayrı bir sayfayı sabit sayfa formatlarına kaydettiğinde çağrılır. |

## Örnekler

Bir belgeyi sayfa sayfa HTML'ye kaydetmek için geri aramanın nasıl kullanılacağını gösterir.

```csharp
public void PageFileNames()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Page 1.");
    builder.InsertBreak(BreakType.PageBreak);
    builder.Writeln("Page 2.");
    builder.InsertImage(ImageDir + "Logo.jpg");
    builder.InsertBreak(BreakType.PageBreak);
    builder.Writeln("Page 3.");

    // Belgenin "Save" yöntemine aktarabileceğimiz bir "HtmlFixedSaveOptions" nesnesi oluşturun
    // belgeyi HTML'ye nasıl dönüştüreceğimizi değiştirmek için.
    HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

    // Bu belgedeki her sayfayı yerel dosya sisteminde ayrı bir HTML dosyasına kaydedeceğiz.
    // Her çıktı HTML belgesini adlandırmamızı sağlayan bir geri çağırma ayarlayın.
    htmlFixedSaveOptions.PageSavingCallback = new CustomFileNamePageSavingCallback();

    doc.Save(ArtifactsDir + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

    string[] filePaths = Directory.GetFiles(ArtifactsDir).Where(
        s => s.StartsWith(ArtifactsDir + "SavingCallback.PageFileNames.Page_")).OrderBy(s => s).ToArray();

    Assert.AreEqual(3, filePaths.Length);
}

/// <summary>
/// Tüm sayfaları belirtilen dosya ve dizine kaydeder.
/// </summary>
private class CustomFileNamePageSavingCallback : IPageSavingCallback
{
    public void PageSaving(PageSavingArgs args)
    {
        string outFileName = $"{ArtifactsDir}SavingCallback.PageFileNames.Page_{args.PageIndex}.html";

        // Aşağıda Aspose.Words'ün belgenin her sayfasını nereye kaydedeceğini belirtmenin iki yolu verilmiştir.
        // 1 - Çıkış sayfası dosyası için bir dosya adı belirleyin:
        args.PageFileName = outFileName;

        // 2 - Çıkış sayfası dosyası için özel bir akış oluşturun:
        args.PageStream = new FileStream(outFileName, FileMode.Create);

        Assert.False(args.KeepPageStreamOpen);
    }
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
