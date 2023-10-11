---
title: LoadOptions.WarningCallback
second_title: Aspose.Words for .NET API Referansı
description: LoadOptions mülk. Yükleme işlemi sırasında veri veya biçimlendirme kalitesinin kaybına neden olabilecek bir sorun algılandığında çağrılır.
type: docs
weight: 170
url: /tr/net/aspose.words.loading/loadoptions/warningcallback/
---
## LoadOptions.WarningCallback property

Yükleme işlemi sırasında, veri veya biçimlendirme kalitesinin kaybına neden olabilecek bir sorun algılandığında çağrılır.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

### Örnekler

Belge yükleme sırasında oluşan uyarıların nasıl yazdırılacağını ve saklanacağını gösterir.

```csharp
public void LoadOptionsWarningCallback()
{
    // Yeni bir LoadOptions nesnesi oluşturun ve onun WarningCallback özelliğini ayarlayın
    // IWarningCallback uygulamamızın bir örneği olarak.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.WarningCallback = new DocumentLoadingWarningCallback();

    // Geri aramamız yükleme işlemi sırasında ortaya çıkan tüm uyarıları yazdıracaktır.
    Document doc = new Document(MyDir + "Document.docx", loadOptions);

    List<WarningInfo> warnings = ((DocumentLoadingWarningCallback)loadOptions.WarningCallback).GetWarnings();
    Assert.AreEqual(3, warnings.Count);
}

/// <summary>
/// Belge yükleme sırasında ortaya çıkan uyarıları ve ayrıntılarını yazdıran IWarningCallback.
/// </summary>
private class DocumentLoadingWarningCallback : IWarningCallback
{
    public void Warning(WarningInfo info)
    {
        Console.WriteLine($"Warning: {info.WarningType}");
        Console.WriteLine($"\tSource: {info.Source}");
        Console.WriteLine($"\tDescription: {info.Description}");
        mWarnings.Add(info);
    }

    public List<WarningInfo> GetWarnings()
    {
        return mWarnings;
    }

    private readonly List<WarningInfo> mWarnings = new List<WarningInfo>();
}
```

### Ayrıca bakınız

* interface [IWarningCallback](../../../aspose.words/iwarningcallback/)
* class [LoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../loadoptions/)
* toplantı [Aspose.Words](../../../)


