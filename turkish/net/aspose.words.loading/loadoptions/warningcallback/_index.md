---
title: LoadOptions.WarningCallback
linktitle: WarningCallback
articleTitle: WarningCallback
second_title: .NET için Aspose.Words
description: Veri kaybını önlemek ve biçimlendirme bütünlüğünü sağlamak için yükleme işlemleri sırasında sizi uyaran LoadOptions WarningCallback özelliğini keşfedin.
type: docs
weight: 180
url: /tr/net/aspose.words.loading/loadoptions/warningcallback/
---
## LoadOptions.WarningCallback property

Veri veya biçimlendirme sadakat kaybına yol açabilecek bir sorun algılandığında, yükleme işlemi sırasında çağrılır.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

## Örnekler

Belge yüklenirken oluşan uyarıların nasıl yazdırılacağını ve saklanacağını gösterir.

```csharp
public void LoadOptionsWarningCallback()
{
    // Yeni bir LoadOptions nesnesi oluşturun ve onun WarningCallback niteliğini ayarlayın
    // IWarningCallback uygulamamızın bir örneği olarak.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.WarningCallback = new DocumentLoadingWarningCallback();

    // Geri çağırmamız yükleme işlemi sırasında ortaya çıkan tüm uyarıları yazdıracaktır.
    Document doc = new Document(MyDir + "Document.docx", loadOptions);

    List<WarningInfo> warnings = ((DocumentLoadingWarningCallback)loadOptions.WarningCallback).GetWarnings();
    Assert.AreEqual(3, warnings.Count);
}

/// <summary>
/// Belge yüklenirken oluşan uyarıları ve ayrıntılarını yazdıran IWarningCallback.
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
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
