---
title: Class PrinterSettingsContainer
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Rendering.PrinterSettingsContainer sınıf. Bazı parametreler için bir depolamayı temsil ederPrinterSettings nesne.
type: docs
weight: 4320
url: /tr/net/aspose.words.rendering/printersettingscontainer/
---
## PrinterSettingsContainer class

Bazı parametreler için bir depolamayı temsil ederPrinterSettings nesne.

```csharp
public class PrinterSettingsContainer
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [PrinterSettingsContainer](printersettingscontainer/)(PrinterSettings) | Şunun için bir kapsayıcı oluşturur:PrinterSettings . |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DefaultPageSettingsPaperSource](../../aspose.words.rendering/printersettingscontainer/defaultpagesettingspapersource/) { get; } | Bkz.PaperSource nın-ninDefaultPageSettings . |
| [PaperSizes](../../aspose.words.rendering/printersettingscontainer/papersizes/) { get; } | Bkz.PaperSizes . |
| [PaperSources](../../aspose.words.rendering/printersettingscontainer/papersources/) { get; } | Bkz.PaperSources . |

### Notlar

Şunun verilerine erişim:PrinterSettings uzun zaman alır. `PrinterSettingsContainer` parametreleri önbelleğe alırPrinterSettings , böylece yazdırma daha hızlı çalışır.

### Örnekler

Yazıcınızın kağıt kaynaklarına ve boyutlarına nasıl erişileceğini ve bunların listeleneceğini gösterir.

```csharp
// "PrinterSettingsContainer", bir "PrinterSettings" nesnesi içeriyor,
// farklı yazıcı sürücüleri için benzersiz veriler içeren.
PrinterSettingsContainer container = new PrinterSettingsContainer(new PrinterSettings());

Console.WriteLine($"This printer contains {container.PaperSources.Count} printer paper sources:");
foreach (PaperSource paperSource in container.PaperSources)
{
    bool isDefault = container.DefaultPageSettingsPaperSource.SourceName == paperSource.SourceName;
    Console.WriteLine($"\t{paperSource.SourceName}, " +
                      $"RawKind: {paperSource.RawKind} {(isDefault ? "(Default)" : "")}");
}

// "PaperSizes" özelliği, yazıcıya kullanması talimatını verecek kağıt boyutlarının listesini içerir.
// Hem PrinterSource hem de PrinterSize bir "RawKind" özelliği içerir,
// bu, PaperSourceKind enum'da listelenen bir kağıt türüne eşittir.
// Yazdırılan sayfa ile aynı "RawKind" değerine sahip bir kağıt kaynağı varsa,
// yazıcı, sağlanan kağıt kaynağını ve boyutunu kullanarak sayfayı yazdıracaktır.
// Aksi takdirde, yazıcı varsayılan olarak "DefaultPageSettingsPaperSource" özelliği tarafından belirlenen kaynağa geçer.
Console.WriteLine($"{container.PaperSizes.Count} paper sizes:");
foreach (System.Drawing.Printing.PaperSize paperSize in container.PaperSizes)
{
    Console.WriteLine($"\t{paperSize}, RawKind: {paperSize.RawKind}");
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Rendering](../../aspose.words.rendering/)
* toplantı [Aspose.Words](../../)


