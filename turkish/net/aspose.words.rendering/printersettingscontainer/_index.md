---
title: PrinterSettingsContainer Class
linktitle: PrinterSettingsContainer
articleTitle: PrinterSettingsContainer
second_title: .NET için Aspose.Words
description: PrinterSettings parametrelerinin etkili yönetimi için Aspose.Words.Rendering.PrinterSettingsContainer sınıfını keşfedin ve belge oluşturma deneyiminizi geliştirin.
type: docs
weight: 5310
url: /tr/net/aspose.words.rendering/printersettingscontainer/
---
## PrinterSettingsContainer class

Bazı parametreler için bir depolama alanını temsil ederPrinterSettings nesne.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Bir Belgeyi Programlama Yoluyla veya İletişim Kutularını Kullanarak Yazdırma](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) belgeleme makalesi.

```csharp
public class PrinterSettingsContainer
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [PrinterSettingsContainer](printersettingscontainer/)(*PrinterSettings*) | için bir kapsayıcı oluştururPrinterSettings . |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DefaultPageSettingsPaperSource](../../aspose.words.rendering/printersettingscontainer/defaultpagesettingspapersource/) { get; } | BakınızPaperSource ile ilgiliDefaultPageSettings . |
| [PaperSizes](../../aspose.words.rendering/printersettingscontainer/papersizes/) { get; } | BakınızPaperSizes . |
| [PaperSources](../../aspose.words.rendering/printersettingscontainer/papersources/) { get; } | BakınızPaperSources . |

## Notlar

Verilere erişimPrinterSettings uzun zaman alır. `PrinterSettingsContainer` parametreleri önbelleğe alırPrinterSettings , böylece yazdırma işlemi daha hızlı gerçekleşir.

## Örnekler

Yazıcınızın kağıt kaynaklarına ve boyutlarına nasıl erişeceğinizi ve bunları nasıl listeleyeceğinizi gösterir.

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

// "PaperSizes" özelliği, yazıcının kullanması gereken kağıt boyutlarının listesini içerir.
// Hem PrinterSource hem de PrinterSize bir "RawKind" özelliği içerir,
// PaperSourceKind enumunda listelenen bir kağıt türüne eşdeğerdir.
// Yazdırma sayfasının "RawKind" değeriyle aynı olan bir kağıt kaynağı varsa,
// yazıcı, sağlanan kağıt kaynağı ve boyutunu kullanarak sayfayı yazdıracaktır.
// Aksi takdirde yazıcı varsayılan olarak "DefaultPageSettingsPaperSource" özelliği tarafından belirtilen kaynağa dönecektir.
Console.WriteLine($"{container.PaperSizes.Count} paper sizes:");
foreach (System.Drawing.Printing.PaperSize paperSize in container.PaperSizes)
{
    Console.WriteLine($"\t{paperSize}, RawKind: {paperSize.RawKind}");
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Rendering](../../aspose.words.rendering/)
* toplantı [Aspose.Words](../../)
