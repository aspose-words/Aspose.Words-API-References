---
title: PrinterSettingsContainer.PaperSizes
second_title: Справочник по API Aspose.Words для .NET
description: PrinterSettingsContainer свойство. См.PaperSizes .
type: docs
weight: 30
url: /ru/net/aspose.words.rendering/printersettingscontainer/papersizes/
---
## PrinterSettingsContainer.PaperSizes property

См.PaperSizes .

```csharp
public PaperSizeCollection PaperSizes { get; }
```

### Примеры

Показывает, как получить доступ к источникам и форматам бумаги вашего принтера и составить их список.

```csharp
// Контейнер PrinterSettingsContainer содержит объект PrinterSettings,
// который содержит уникальные данные для разных драйверов принтера.
PrinterSettingsContainer container = new PrinterSettingsContainer(new PrinterSettings());

Console.WriteLine($"This printer contains {container.PaperSources.Count} printer paper sources:");
foreach (PaperSource paperSource in container.PaperSources)
{
    bool isDefault = container.DefaultPageSettingsPaperSource.SourceName == paperSource.SourceName;
    Console.WriteLine($"\t{paperSource.SourceName}, " +
                      $"RawKind: {paperSource.RawKind} {(isDefault ? "(Default)" : "")}");
}

// Свойство PaperSizes содержит список размеров бумаги, которые принтер должен использовать.
// И PrinterSource, и PrinterSize содержат свойство RawKind,
// что соответствует типу бумаги, указанному в перечислении PaperSourceKind.
// Если существует источник бумаги с тем же значением "RawKind", что и у печатаемой страницы,
// принтер напечатает страницу, используя указанный источник и размер бумаги.
// В противном случае принтер по умолчанию будет использовать источник, указанный в свойстве «DefaultPageSettingsPaperSource».
Console.WriteLine($"{container.PaperSizes.Count} paper sizes:");
foreach (System.Drawing.Printing.PaperSize paperSize in container.PaperSizes)
{
    Console.WriteLine($"\t{paperSize}, RawKind: {paperSize.RawKind}");
}
```

### Смотрите также

* class [PrinterSettingsContainer](../)
* пространство имен [Aspose.Words.Rendering](../../printersettingscontainer/)
* сборка [Aspose.Words](../../../)


