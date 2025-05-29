---
title: FontEmbeddingLicensingRights.NoSubsetting
linktitle: NoSubsetting
articleTitle: NoSubsetting
second_title: Aspose.Words для .NET
description: Откройте для себя права лицензирования встраивания шрифтов без поднабора. Обеспечьте соответствие и защитите свои шрифты, одновременно улучшая свои дизайн-проекты.
type: docs
weight: 30
url: /ru/net/aspose.words.fonts/fontembeddinglicensingrights/nosubsetting/
---
## FontEmbeddingLicensingRights.NoSubsetting property

Указывает на ограничение «Без подмножества».

```csharp
public bool NoSubsetting { get; }
```

## Примечания

Когда этот флаг установлен, шрифт не должен быть подмножеством перед внедрением. Другие ограничения внедрения также применяются.

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

* class [FontEmbeddingLicensingRights](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
