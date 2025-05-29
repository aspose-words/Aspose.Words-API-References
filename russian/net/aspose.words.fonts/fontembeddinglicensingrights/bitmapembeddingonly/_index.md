---
title: FontEmbeddingLicensingRights.BitmapEmbeddingOnly
linktitle: BitmapEmbeddingOnly
articleTitle: BitmapEmbeddingOnly
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FontEmbeddingLicensingRights BitmapEmbeddingOnly, которое обеспечивает эксклюзивные ограничения на встраивание растровых изображений для расширенного управления дизайном.
type: docs
weight: 10
url: /ru/net/aspose.words.fonts/fontembeddinglicensingrights/bitmapembeddingonly/
---
## FontEmbeddingLicensingRights.BitmapEmbeddingOnly property

Указывает на ограничение «Только встраивание растровых изображений».

```csharp
public bool BitmapEmbeddingOnly { get; }
```

## Примечания

Когда этот бит установлен, могут быть внедрены только битовые карты, содержащиеся в шрифте. Никакие контурные данные не могут быть внедрены. Если в шрифте нет доступных битовых карт, то шрифт считается невстраиваемым и службы встраивания завершатся ошибкой. Также применяются другие ограничения встраивания.

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
