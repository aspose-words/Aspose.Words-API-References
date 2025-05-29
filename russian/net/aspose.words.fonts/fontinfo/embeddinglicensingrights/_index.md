---
title: FontInfo.EmbeddingLicensingRights
linktitle: EmbeddingLicensingRights
articleTitle: EmbeddingLicensingRights
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FontInfo EmbeddingLicensingRights, чтобы легко получать доступ и управлять правами лицензирования встроенных шрифтов для бесшовной интеграции дизайна.
type: docs
weight: 30
url: /ru/net/aspose.words.fonts/fontinfo/embeddinglicensingrights/
---
## FontInfo.EmbeddingLicensingRights property

Получает права лицензирования встроенного шрифта.

```csharp
public FontEmbeddingLicensingRights EmbeddingLicensingRights { get; }
```

## Примечания

Значение может быть нулевым, если шрифт не встроен.

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

* class [FontEmbeddingLicensingRights](../../fontembeddinglicensingrights/)
* class [FontInfo](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
