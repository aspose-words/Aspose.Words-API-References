---
title: Class PrinterSettingsContainer
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Rendering.PrinterSettingsContainer сорт. Представляет собой хранилище для некоторых параметровPrinterSettings объект.
type: docs
weight: 4580
url: /ru/net/aspose.words.rendering/printersettingscontainer/
---
## PrinterSettingsContainer class

Представляет собой хранилище для некоторых параметровPrinterSettings объект.

Чтобы узнать больше, посетите[Печать документа программно или с использованием диалоговых окон](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) статья документации.

```csharp
public class PrinterSettingsContainer
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [PrinterSettingsContainer](printersettingscontainer/)(PrinterSettings) | Создает контейнер дляPrinterSettings . |

## Характеристики

| Имя | Описание |
| --- | --- |
| [DefaultPageSettingsPaperSource](../../aspose.words.rendering/printersettingscontainer/defaultpagesettingspapersource/) { get; } | См.PaperSource изDefaultPageSettings . |
| [PaperSizes](../../aspose.words.rendering/printersettingscontainer/papersizes/) { get; } | См.PaperSizes . |
| [PaperSources](../../aspose.words.rendering/printersettingscontainer/papersources/) { get; } | См.PaperSources . |

### Примечания

Доступ к даннымPrinterSettings занимает много времени. `PrinterSettingsContainer` кэширует параметры изPrinterSettings , , чтобы печать работала быстрее.

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

* пространство имен [Aspose.Words.Rendering](../../aspose.words.rendering/)
* сборка [Aspose.Words](../../)


