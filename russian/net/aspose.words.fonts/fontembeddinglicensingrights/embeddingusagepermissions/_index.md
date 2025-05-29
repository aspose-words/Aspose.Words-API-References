---
title: FontEmbeddingLicensingRights.EmbeddingUsagePermissions
linktitle: EmbeddingUsagePermissions
articleTitle: EmbeddingUsagePermissions
second_title: Aspose.Words для .NET
description: Раскройте творческий потенциал с помощью прав лицензирования внедрения шрифтов. Изучите разрешения на использование для бесшовной интеграции шрифтов в ваши проекты.
type: docs
weight: 20
url: /ru/net/aspose.words.fonts/fontembeddinglicensingrights/embeddingusagepermissions/
---
## FontEmbeddingLicensingRights.EmbeddingUsagePermissions property

Разрешения на использование.

```csharp
public FontEmbeddingUsagePermissions EmbeddingUsagePermissions { get; }
```

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

* enum [FontEmbeddingUsagePermissions](../../fontembeddingusagepermissions/)
* class [FontEmbeddingLicensingRights](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
