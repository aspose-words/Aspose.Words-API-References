---
title: FontEmbeddingLicensingRights Class
linktitle: FontEmbeddingLicensingRights
articleTitle: FontEmbeddingLicensingRights
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fonts.FontEmbeddingLicensingRights, чтобы легко управлять правами на внедрение шрифтов и улучшить представление вашего документа.
type: docs
weight: 3310
url: /ru/net/aspose.words.fonts/fontembeddinglicensingrights/
---
## FontEmbeddingLicensingRights class

Представляет собой лицензионные права на внедрение шрифта.

```csharp
public class FontEmbeddingLicensingRights
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [BitmapEmbeddingOnly](../../aspose.words.fonts/fontembeddinglicensingrights/bitmapembeddingonly/) { get; } | Указывает на ограничение «Только встраивание растровых изображений». |
| [EmbeddingUsagePermissions](../../aspose.words.fonts/fontembeddinglicensingrights/embeddingusagepermissions/) { get; } | Разрешения на использование. |
| [NoSubsetting](../../aspose.words.fonts/fontembeddinglicensingrights/nosubsetting/) { get; } | Указывает на ограничение «Без подмножества». |

## Примечания

Чтобы узнать больше, посетите сайт the [Раздел спецификации OpenType](https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fstype) на портале типографии Microsoft.

## Примеры

Показывает, как получить информацию о лицензионных правах для встроенных шрифтов (FontInfo).

```csharp
Document doc = new Document(MyDir + "Embedded font rights.docx");

// Получить список шрифтов документа.
FontInfoCollection fontInfos = doc.FontInfos;
foreach (FontInfo fontInfo in fontInfos) 
{
    if (fontInfo.EmbeddingLicensingRights != null)
    {
        Console.WriteLine(fontInfo.EmbeddingLicensingRights.EmbeddingUsagePermissions);
        Console.WriteLine(fontInfo.EmbeddingLicensingRights.BitmapEmbeddingOnly);
        Console.WriteLine(fontInfo.EmbeddingLicensingRights.NoSubsetting);
    }
}
```

### Смотрите также

* пространство имен [Aspose.Words.Fonts](../../aspose.words.fonts/)
* сборка [Aspose.Words](../../)
