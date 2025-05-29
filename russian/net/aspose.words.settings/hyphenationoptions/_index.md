---
title: HyphenationOptions Class
linktitle: HyphenationOptions
articleTitle: HyphenationOptions
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Settings.HyphenationOptions, чтобы легко настраивать параметры переносов для ваших документов и улучшать представление текста.
type: docs
weight: 6620
url: /ru/net/aspose.words.settings/hyphenationoptions/
---
## HyphenationOptions class

Позволяет настраивать параметры переноса слов в документе.

Чтобы узнать больше, посетите[Работа с переносами](https://docs.aspose.com/words/net/working-with-hyphenation/) документальная статья.

```csharp
public class HyphenationOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [HyphenationOptions](hyphenationoptions/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AutoHyphenation](../../aspose.words.settings/hyphenationoptions/autohyphenation/) { get; set; } | Возвращает или задает значение, определяющее, включена ли автоматическая расстановка переносов для документа. Значение по умолчанию для этого свойства:`ЛОЖЬ` . |
| [ConsecutiveHyphenLimit](../../aspose.words.settings/hyphenationoptions/consecutivehyphenlimit/) { get; set; } | Возвращает или задает максимальное количество последовательных строк, которые могут заканчиваться дефисами. Значение по умолчанию для этого свойства — 0. |
| [HyphenateCaps](../../aspose.words.settings/hyphenationoptions/hyphenatecaps/) { get; set; } | Возвращает или задает значение, определяющее, переносятся ли слова, написанные заглавными буквами. Значение по умолчанию для этого свойства:`истинный` . |
| [HyphenationZone](../../aspose.words.settings/hyphenationoptions/hyphenationzone/) { get; set; } | Возвращает или задает расстояние в 1/20 пункта от правого поля, в пределах которого не требуется переносить слова. Значение по умолчанию для этого свойства — 360 (0,25 дюйма). |

## Примеры

Показывает, как настроить автоматическую расстановку переносов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.HyphenationOptions.AutoHyphenation = true;
doc.HyphenationOptions.ConsecutiveHyphenLimit = 2;
doc.HyphenationOptions.HyphenationZone = 720;
doc.HyphenationOptions.HyphenateCaps = true;

doc.Save(ArtifactsDir + "Document.HyphenationOptions.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Settings](../../aspose.words.settings/)
* сборка [Aspose.Words](../../)
