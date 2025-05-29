---
title: FontInfo.EmbeddingLicensingRights
linktitle: EmbeddingLicensingRights
articleTitle: EmbeddingLicensingRights
second_title: Aspose.Words for .NET
description: 探索 FontInfo EmbeddingLicensingRights 属性，轻松访问和管理嵌入字体许可权，实现无缝设计集成。
type: docs
weight: 30
url: /zh/net/aspose.words.fonts/fontinfo/embeddinglicensingrights/
---
## FontInfo.EmbeddingLicensingRights property

获取嵌入字体许可权。

```csharp
public FontEmbeddingLicensingRights EmbeddingLicensingRights { get; }
```

## 评论

如果未嵌入字体，则该值可能为空。

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

* class [FontEmbeddingLicensingRights](../../fontembeddinglicensingrights/)
* class [FontInfo](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
