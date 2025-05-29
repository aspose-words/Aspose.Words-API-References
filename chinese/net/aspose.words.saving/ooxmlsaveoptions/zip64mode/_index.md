---
title: OoxmlSaveOptions.Zip64Mode
linktitle: Zip64Mode
articleTitle: Zip64Mode
second_title: Aspose.Words for .NET
description: 探索 OoxmlSaveOptions Zip64Mode 属性，以 ZIP64 格式增强文档的输出效果。轻松优化大文件！
type: docs
weight: 80
url: /zh/net/aspose.words.saving/ooxmlsaveoptions/zip64mode/
---
## OoxmlSaveOptions.Zip64Mode property

指定是否对输出文档使用 ZIP64 格式扩展名。 默认值为Never.

```csharp
public Zip64Mode Zip64Mode { get; set; }
```

## 例子

展示如何使用 ZIP64 格式扩展。

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

### 也可以看看

* enum [Zip64Mode](../../zip64mode/)
* class [OoxmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
