---
title: OoxmlSaveOptions.Zip64Mode
linktitle: Zip64Mode
articleTitle: Zip64Mode
second_title: Aspose.Words для .NET
description: Откройте для себя свойство OoxmlSaveOptions Zip64Mode, чтобы улучшить вывод вашего документа с помощью формата ZIP64. Оптимизируйте большие файлы без усилий!
type: docs
weight: 80
url: /ru/net/aspose.words.saving/ooxmlsaveoptions/zip64mode/
---
## OoxmlSaveOptions.Zip64Mode property

Указывает, следует ли использовать расширения формата ZIP64 для выходного документа. Значение по умолчанию:Never .

```csharp
public Zip64Mode Zip64Mode { get; set; }
```

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

* enum [Zip64Mode](../../zip64mode/)
* class [OoxmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
