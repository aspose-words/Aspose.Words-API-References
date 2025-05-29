---
title: Zip64Mode Enum
linktitle: Zip64Mode
articleTitle: Zip64Mode
second_title: Aspose.Words for .NET
description: 发现 Aspose.Words.Saving.Zip64Mode 枚举，以便在 OOXML 文件中高效使用 ZIP64 格式，增强文件大小管理和兼容性。
type: docs
weight: 6550
url: /zh/net/aspose.words.saving/zip64mode/
---
## Zip64Mode enumeration

指定何时对 OOXML 文件使用 ZIP64 格式扩展名。

```csharp
public enum Zip64Mode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Never | `0` | 请勿使用 ZIP64 格式扩展名。 |
| IfNecessary | `1` | 如有必要，请使用 ZIP64 格式扩展。 |
| Always | `2` | 始终使用 ZIP64 格式扩展名。 |

## 评论

OOXML 文件是一个 ZIP 档案，其未压缩文件大小、 压缩文件大小和档案总大小的限制均为 4 GB（2^32 字节），并且档案中的文件数量限制为 65,535（2^16-1）。 ZIP64 格式扩展将限制增加到 2^64。

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

* property [Zip64Mode](../ooxmlsaveoptions/zip64mode/)
* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
