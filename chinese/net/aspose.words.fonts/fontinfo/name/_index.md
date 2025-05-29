---
title: FontInfo.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words for .NET
description: 发现 FontInfo Name 属性以便轻松访问和使用字体名称来增强项目中的排版。
type: docs
weight: 60
url: /zh/net/aspose.words.fonts/fontinfo/name/
---
## FontInfo.Name property

获取字体的名称。

```csharp
public string Name { get; }
```

## 评论

不可能`无效的`. 可以是空字符串。

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
