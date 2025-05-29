---
title: Zip64Mode Enum
linktitle: Zip64Mode
articleTitle: Zip64Mode
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Saving.Zip64Mode для эффективного использования формата ZIP64 в файлах OOXML, что улучшает управление размером файлов и совместимость.
type: docs
weight: 6550
url: /ru/net/aspose.words.saving/zip64mode/
---
## Zip64Mode enumeration

Указывает, когда следует использовать расширения формата ZIP64 для файлов OOXML.

```csharp
public enum Zip64Mode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Never | `0` | Не используйте расширения формата ZIP64. |
| IfNecessary | `1` | При необходимости используйте расширения формата ZIP64. |
| Always | `2` | Всегда используйте расширения формата ZIP64. |

## Примечания

Файл OOXML представляет собой ZIP-архив, имеющий ограничение в 4 ГБ (2^32 байта) на размер несжатого файла, на размер сжатого файла и общий размер архива, а также ограничение в 65 535 (2^16-1) файлов в архиве. Расширения формата ZIP64 увеличивают ограничения до 2^64.

## Примеры

Показывает, как использовать расширения формата ZIP64.

```csharp
Random random = new Random();
DocumentBuilder builder = new DocumentBuilder();

for (int i = 0; i < 10000; i++)
{
    using (Bitmap bmp = new Bitmap(5, 5))
    using (Graphics g = Graphics.FromImage(bmp))
    {
        g.Clear(Color.FromArgb(random.Next(0, 254), random.Next(0, 254), random.Next(0, 254)));
        using (MemoryStream ms = new MemoryStream())
        {
            bmp.Save(ms, System.Drawing.Imaging.ImageFormat.Png);
            builder.InsertImage(ms.ToArray());
        }
    }
}

builder.Document.Save(ArtifactsDir + "OoxmlSaveOptions.Zip64ModeOption.docx", 
    new OoxmlSaveOptions { Zip64Mode = Zip64Mode.Always });
```

### Смотрите также

* property [Zip64Mode](../ooxmlsaveoptions/zip64mode/)
* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
