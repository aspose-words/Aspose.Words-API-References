---
title: PrinterSettingsContainer.DefaultPageSettingsPaperSource
linktitle: DefaultPageSettingsPaperSource
articleTitle: DefaultPageSettingsPaperSource
second_title: Aspose.Words для .NET
description: Откройте для себя свойство DefaultPageSettingsPaperSource для PrinterSettingsContainer. Оптимизируйте печать с помощью настраиваемых параметров источника бумаги!
type: docs
weight: 20
url: /ru/net/aspose.words.rendering/printersettingscontainer/defaultpagesettingspapersource/
---
## PrinterSettingsContainer.DefaultPageSettingsPaperSource property

СмотретьPaperSource изDefaultPageSettings .

```csharp
public PaperSource DefaultPageSettingsPaperSource { get; }
```

## Примеры

Показывает, как получить доступ и просмотреть список источников и размеров бумаги вашего принтера.

```csharp
// "PrinterSettingsContainer" содержит объект "PrinterSettings",
// который содержит уникальные данные для разных драйверов принтера.
PrinterSettingsContainer container = new PrinterSettingsContainer(new PrinterSettings());

Console.WriteLine($"This printer contains {container.PaperSources.Count} printer paper sources:");
foreach (PaperSource paperSource in container.PaperSources)
{
    bool isDefault = container.DefaultPageSettingsPaperSource.SourceName == paperSource.SourceName;
    Console.WriteLine($"\t{paperSource.SourceName}, " +
                      $"RawKind: {paperSource.RawKind} {(isDefault ? "(Default)" : "")}");
}

// Свойство «PaperSizes» содержит список размеров бумаги, которые следует использовать принтеру.
// PrinterSource и PrinterSize содержат свойство "RawKind",
// что соответствует типу бумаги, указанному в перечислении PaperSourceKind.
// Если есть источник бумаги с тем же значением «RawKind», что и у печатной страницы,
// принтер напечатает страницу, используя указанный источник бумаги и размер.
// В противном случае принтер по умолчанию будет использовать источник, указанный свойством «DefaultPageSettingsPaperSource».
Console.WriteLine($"{container.PaperSizes.Count} paper sizes:");
foreach (System.Drawing.Printing.PaperSize paperSize in container.PaperSizes)
{
    Console.WriteLine($"\t{paperSize}, RawKind: {paperSize.RawKind}");
}
```

### Смотрите также

* class [PrinterSettingsContainer](../)
* пространство имен [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* сборка [Aspose.Words](../../../)
