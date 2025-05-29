---
title: PrinterSettingsContainer Class
linktitle: PrinterSettingsContainer
articleTitle: PrinterSettingsContainer
second_title: Aspose.Words для .NET
description: Изучите класс Aspose.Words.Rendering.PrinterSettingsContainer для эффективного управления параметрами PrinterSettings, улучшая процесс рендеринга документов.
type: docs
weight: 5310
url: /ru/net/aspose.words.rendering/printersettingscontainer/
---
## PrinterSettingsContainer class

Представляет хранилище для некоторых параметровPrinterSettings объект.

Чтобы узнать больше, посетите[Печать документа программным способом или с использованием диалогов](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) документальная статья.

```csharp
public class PrinterSettingsContainer
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [PrinterSettingsContainer](printersettingscontainer/)(*PrinterSettings*) | Создает контейнер дляPrinterSettings . |

## Характеристики

| Имя | Описание |
| --- | --- |
| [DefaultPageSettingsPaperSource](../../aspose.words.rendering/printersettingscontainer/defaultpagesettingspapersource/) { get; } | СмотретьPaperSource изDefaultPageSettings . |
| [PaperSizes](../../aspose.words.rendering/printersettingscontainer/papersizes/) { get; } | СмотретьPaperSizes . |
| [PaperSources](../../aspose.words.rendering/printersettingscontainer/papersources/) { get; } | СмотретьPaperSources . |

## Примечания

Доступ к даннымPrinterSettings занимает много времени. `PrinterSettingsContainer` кэширует параметры изPrinterSettings , поэтому печать работает быстрее.

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

* пространство имен [Aspose.Words.Rendering](../../aspose.words.rendering/)
* сборка [Aspose.Words](../../)
