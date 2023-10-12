---
title: FontInfo.Name
second_title: Aspose.Words for .NET API 参考
description: FontInfo 财产. 获取字体名称
type: docs
weight: 50
url: /zh/net/aspose.words.fonts/fontinfo/name/
---
## FontInfo.Name property

获取字体名称。

```csharp
public string Name { get; }
```

### 评论

不可能是`无效的`。可以是空字符串。

### 例子

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
* 命名空间 [Aspose.Words.Fonts](../../fontinfo/)
* 部件 [Aspose.Words](../../../)


