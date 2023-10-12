---
title: PrinterSettingsContainer.PaperSources
second_title: Aspose.Words for .NET API Referansı
description: PrinterSettingsContainer mülk. Bkz.PaperSources .
type: docs
weight: 40
url: /tr/net/aspose.words.rendering/printersettingscontainer/papersources/
---
## PrinterSettingsContainer.PaperSources property

Bkz.PaperSources .

```csharp
public PaperSourceCollection PaperSources { get; }
```

### Örnekler

Yazıcınızın kağıt kaynaklarına ve boyutlarına nasıl erişeceğinizi ve bunları listeleyeceğinizi gösterir.

```csharp
// "PrinterSettingsContainer" bir "PrinterSettings" nesnesi içerir,
// farklı yazıcı sürücüleri için benzersiz veriler içerir.
PrinterSettingsContainer container = new PrinterSettingsContainer(new PrinterSettings());

Console.WriteLine($"This printer contains {container.PaperSources.Count} printer paper sources:");
foreach (PaperSource paperSource in container.PaperSources)
{
    bool isDefault = container.DefaultPageSettingsPaperSource.SourceName == paperSource.SourceName;
    Console.WriteLine($"\t{paperSource.SourceName}, " +
                      $"RawKind: {paperSource.RawKind} {(isDefault ? "(Default)" : "")}");
}

// "PaperSizes" özelliği, yazıcının kullanması talimatını verecek kağıt boyutlarının listesini içerir.
// Hem PrinterSource hem de PrinterSize bir "RawKind" özelliği içerir,
// bu, PaperSourceKind numaralandırmasında listelenen kağıt türüne eşittir.
// Yazdırılan sayfayla aynı "RawKind" değerine sahip bir kağıt kaynağı varsa,
// yazıcı, sağlanan kağıt kaynağını ve boyutunu kullanarak sayfayı yazdıracaktır.
// Aksi takdirde, yazıcı varsayılan olarak "DefaultPageSettingsPaperSource" özelliği tarafından belirlenen kaynağı kullanacaktır.
Console.WriteLine($"{container.PaperSizes.Count} paper sizes:");
foreach (System.Drawing.Printing.PaperSize paperSize in container.PaperSizes)
{
    Console.WriteLine($"\t{paperSize}, RawKind: {paperSize.RawKind}");
}
```

### Ayrıca bakınız

* class [PrinterSettingsContainer](../)
* ad alanı [Aspose.Words.Rendering](../../printersettingscontainer/)
* toplantı [Aspose.Words](../../../)


