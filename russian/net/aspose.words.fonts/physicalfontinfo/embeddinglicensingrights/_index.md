---
title: PhysicalFontInfo.EmbeddingLicensingRights
linktitle: EmbeddingLicensingRights
articleTitle: EmbeddingLicensingRights
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PhysicalFontInfo EmbeddingLicensingRights — разблокируйте основные права на встраивание шрифтов для бесшовной интеграции дизайна.
type: docs
weight: 10
url: /ru/net/aspose.words.fonts/physicalfontinfo/embeddinglicensingrights/
---
## PhysicalFontInfo.EmbeddingLicensingRights property

Внедрение лицензионных прав на шрифт.

```csharp
public FontEmbeddingLicensingRights EmbeddingLicensingRights { get; }
```

## Примеры

Показывает, как получить информацию о лицензионных правах для встроенных шрифтов (PhysicalFontInfo).

```csharp
FontSettings settings = FontSettings.DefaultInstance;
FontSourceBase source = settings.GetFontsSources()[0];

// Получить список доступных шрифтов.
IList<PhysicalFontInfo> fontInfos = source.GetAvailableFonts();
foreach (PhysicalFontInfo fontInfo in fontInfos)
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

* class [FontEmbeddingLicensingRights](../../fontembeddinglicensingrights/)
* class [PhysicalFontInfo](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
