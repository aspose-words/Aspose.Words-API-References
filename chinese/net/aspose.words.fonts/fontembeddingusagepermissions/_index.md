---
title: FontEmbeddingUsagePermissions Enum
linktitle: FontEmbeddingUsagePermissions
articleTitle: FontEmbeddingUsagePermissions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fonts.FontEmbeddingUsagePermissions 枚举，实现对字体嵌入权限的精确控制，从而增强文档管理。
type: docs
weight: 3320
url: /zh/net/aspose.words.fonts/fontembeddingusagepermissions/
---
## FontEmbeddingUsagePermissions enumeration

表示字体嵌入使用权限。

```csharp
public enum FontEmbeddingUsagePermissions
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Installable | `0` | 该字体可以嵌入，也可以永久安装以供远程系统使用，或供 其他用户使用。 |
| RestrictedLicense | `1` | 未经合法所有者明确许可，不得以任何方式修改、嵌入或交换字体。 |
| PrintAndPreview | `2` | 该字体可能被嵌入，并可能被临时加载到其他系统上以供查看或 打印文档。 |
| Editable | `3` | 该字体可能已嵌入，并且可能在其他系统上临时加载。 |

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
