---
title: FontEmbeddingUsagePermissions Enum
linktitle: FontEmbeddingUsagePermissions
articleTitle: FontEmbeddingUsagePermissions
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Fonts.FontEmbeddingUsagePermissions, обеспечивающее точный контроль над разрешениями на встраивание шрифтов для улучшенного управления документами.
type: docs
weight: 3320
url: /ru/net/aspose.words.fonts/fontembeddingusagepermissions/
---
## FontEmbeddingUsagePermissions enumeration

Представляет разрешения на использование встроенного шрифта.

```csharp
public enum FontEmbeddingUsagePermissions
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Installable | `0` | Шрифт может быть встроенным и может быть установлен на постоянной основе для использования на удаленных системах или для использования другими пользователями. |
| RestrictedLicense | `1` | Шрифт не должен изменяться, внедряться или заменяться каким-либо образом без предварительного получения явного разрешения законного владельца. |
| PrintAndPreview | `2` | Шрифт может быть встроенным и может быть временно загружен в другие системы для просмотра или печати документа. |
| Editable | `3` | Шрифт может быть встроенным и может быть временно загружен в другие системы. |

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
