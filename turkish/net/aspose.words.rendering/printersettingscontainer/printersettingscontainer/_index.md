---
title: PrinterSettingsContainer
linktitle: PrinterSettingsContainer
articleTitle: PrinterSettingsContainer
second_title: .NET için Aspose.Words
description: PrinterSettingsContainer oluşturucusunu keşfedin, yazıcı ayarlarınızı kolayca ve verimli bir şekilde oluşturun ve yönetin. Yazdırma deneyiminizi bugün optimize edin!
type: docs
weight: 10
url: /tr/net/aspose.words.rendering/printersettingscontainer/printersettingscontainer/
---
## PrinterSettingsContainer constructor

için bir kapsayıcı oluştururPrinterSettings .

```csharp
public PrinterSettingsContainer(PrinterSettings settings)
```

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

* class [PrinterSettingsContainer](../)
* ad alanı [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* toplantı [Aspose.Words](../../../)
