---
title: FontEmbeddingLicensingRights Class
linktitle: FontEmbeddingLicensingRights
articleTitle: FontEmbeddingLicensingRights
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fonts.FontEmbeddingLicensingRights 类，轻松管理字体嵌入权限并增强文档的呈现效果。
type: docs
weight: 3310
url: /zh/net/aspose.words.fonts/fontembeddinglicensingrights/
---
## FontEmbeddingLicensingRights class

代表字体的嵌入许可权利。

```csharp
public class FontEmbeddingLicensingRights
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BitmapEmbeddingOnly](../../aspose.words.fonts/fontembeddinglicensingrights/bitmapembeddingonly/) { get; } | 表示“仅位图嵌入”限制。 |
| [EmbeddingUsagePermissions](../../aspose.words.fonts/fontembeddinglicensingrights/embeddingusagepermissions/) { get; } | 使用权限。 |
| [NoSubsetting](../../aspose.words.fonts/fontembeddinglicensingrights/nosubsetting/) { get; } | 表示“无子集”限制。 |

## 评论

要了解更多信息，请访问 [OpenType 规范部分](https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fstype) Microsoft Typography 门户上的 。

## 例子

展示如何获取嵌入字体（FontInfo）的许可权利信息。

```csharp
Document doc = new Document(MyDir + "Embedded font rights.docx");

// 获取文档字体列表。
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

### 也可以看看

* 命名空间 [Aspose.Words.Fonts](../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../)
