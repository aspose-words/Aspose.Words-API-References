---
title: ParagraphFormat.LineUnitBefore
linktitle: LineUnitBefore
articleTitle: LineUnitBefore
second_title: 用于 .NET 的 Aspose.Words
description: ParagraphFormat LineUnitBefore 财产. 获取或设置段落之前的间距以网格线为单位 在 C#.
type: docs
weight: 230
url: /zh/net/aspose.words/paragraphformat/lineunitbefore/
---
## ParagraphFormat.LineUnitBefore property

获取或设置段落之前的间距（以网格线为单位）。

```csharp
public double LineUnitBefore { get; set; }
```

## 例子

演示如何更改段落间距和缩进。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;

// 下面是五个不同的间距选项，以及它们的配置间接影响的属性。
// 1 - 左缩进：
Assert.AreEqual(format.LeftIndent, 0.0d);

format.CharacterUnitLeftIndent = 10.0;

Assert.AreEqual(format.LeftIndent, 120.0d);

// 2 - 右缩进：
Assert.AreEqual(format.RightIndent, 0.0d); 

format.CharacterUnitRightIndent = -5.5;

Assert.AreEqual(format.RightIndent, -66.0d);

// 3 - 悬挂缩进：
Assert.AreEqual(format.FirstLineIndent, 0.0d);

format.CharacterUnitFirstLineIndent = 20.3;

Assert.AreEqual(format.FirstLineIndent, 243.59d, 0.1d);

// 4 - 段落前的行间距：
Assert.AreEqual(format.SpaceBefore, 0.0d);

format.LineUnitBefore = 5.1;

Assert.AreEqual(format.SpaceBefore, 61.1d, 0.1d);

// 5 - 段落后的行间距：
Assert.AreEqual(format.SpaceAfter, 0.0d);

format.LineUnitAfter = 10.9;

Assert.AreEqual(format.SpaceAfter, 130.8d, 0.1d);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试" +
              "文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档");
```

### 也可以看看

* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
