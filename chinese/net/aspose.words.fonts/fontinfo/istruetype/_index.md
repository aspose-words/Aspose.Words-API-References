---
title: FontInfo.IsTrueType
linktitle: IsTrueType
articleTitle: IsTrueType
second_title: 用于 .NET 的 Aspose.Words
description: FontInfo IsTrueType 财产. 指示此字体是 TrueType 或 OpenType 字体而不是光栅或矢量字体 默认为真的 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.fonts/fontinfo/istruetype/
---
## FontInfo.IsTrueType property

指示此字体是 TrueType 或 OpenType 字体，而不是光栅或矢量字体。 默认为`真的`.

```csharp
public bool IsTrueType { get; set; }
```

## 例子

演示如何打印文档中存在的字体的详细信息。

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// 打印文档中所有已使用和未使用的字体。
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

### 也可以看看

* class [FontInfo](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
