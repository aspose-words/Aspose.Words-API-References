---
title: PrinterSettingsContainer Class
linktitle: PrinterSettingsContainer
articleTitle: PrinterSettingsContainer
second_title: Aspose.Words for .NET
description: Aspose.Words.Rendering.PrinterSettingsContainer sınıf. Bazı parametreler için bir depolama alanını temsil ederPrinterSettings nesne C#'da.
type: docs
weight: 4580
url: /tr/net/aspose.words.rendering/printersettingscontainer/
---
## PrinterSettingsContainer class

Bazı parametreler için bir depolama alanını temsil ederPrinterSettings nesne.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Bir Belgeyi Programlı Olarak Yazdırma veya İletişim Kutularını Kullanma](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) dokümantasyon makalesi.

```csharp
public class PrinterSettingsContainer
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [PrinterSettingsContainer](printersettingscontainer/)(*PrinterSettings*) | Şunun için bir kapsayıcı oluşturur:PrinterSettings . |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DefaultPageSettingsPaperSource](../../aspose.words.rendering/printersettingscontainer/defaultpagesettingspapersource/) { get; } | Bkz.PaperSource ile ilgiliDefaultPageSettings . |
| [PaperSizes](../../aspose.words.rendering/printersettingscontainer/papersizes/) { get; } | Bkz.PaperSizes . |
| [PaperSources](../../aspose.words.rendering/printersettingscontainer/papersources/) { get; } | Bkz.PaperSources . |

## Notlar

Verilerine erişimPrinterSettings uzun zaman alır. `PrinterSettingsContainer` parametreleri önbelleğe alırPrinterSettings , böylece yazdırma daha hızlı çalışır.

## Örnekler

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

* ad alanı [Aspose.Words.Rendering](../../aspose.words.rendering/)
* toplantı [Aspose.Words](../../)
