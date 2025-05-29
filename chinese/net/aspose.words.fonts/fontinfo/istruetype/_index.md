---
title: FontInfo.IsTrueType
linktitle: IsTrueType
articleTitle: IsTrueType
second_title: Aspose.Words for .NET
description: 探索 FontInfo 的 IsTrueType 属性，确保您的字体是 TrueType 或 OpenType，以获得卓越的品质 - 非常适合清晰且可扩展的设计。
type: docs
weight: 50
url: /zh/net/aspose.words.fonts/fontinfo/istruetype/
---
## FontInfo.IsTrueType property

表示此字体是 TrueType 或 OpenType 字体，而不是光栅字体或矢量字体。 默认值为`真的`.

```csharp
public bool IsTrueType { get; set; }
```

## 例子

显示如何打印文档中存在的字体的详细信息。

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
