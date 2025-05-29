---
title: FontEmbeddingLicensingRights.BitmapEmbeddingOnly
linktitle: BitmapEmbeddingOnly
articleTitle: BitmapEmbeddingOnly
second_title: Aspose.Words for .NET
description: 发现 FontEmbeddingLicensingRights BitmapEmbeddingOnly 属性，该属性可确保独有的 Bitmap 嵌入限制，以增强设计控制。
type: docs
weight: 10
url: /zh/net/aspose.words.fonts/fontembeddinglicensingrights/bitmapembeddingonly/
---
## FontEmbeddingLicensingRights.BitmapEmbeddingOnly property

表示“仅位图嵌入”限制。

```csharp
public bool BitmapEmbeddingOnly { get; }
```

## 评论

置位此位时，只能嵌入字体中包含的位图，不能嵌入任何轮廓数据。 如果字体中没有可用的位图，则该字体被视为不可嵌入，嵌入 服务将失败。其他嵌入限制也适用。

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

* class [FontEmbeddingLicensingRights](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
