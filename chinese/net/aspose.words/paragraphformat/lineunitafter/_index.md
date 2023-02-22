---
title: ParagraphFormat.LineUnitAfter
second_title: Aspose.Words for .NET API 参考
description: ParagraphFormat 财产. 获取或设置段落后的间距量以网格线为单位
type: docs
weight: 210
url: /zh/net/aspose.words/paragraphformat/lineunitafter/
---
## ParagraphFormat.LineUnitAfter property

获取或设置段落后的间距量（以网格线为单位）。

```csharp
public double LineUnitAfter { get; set; }
```

### 例子

显示如何更改段落间距和缩进。

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

// 4 - 段落前的行距：
Assert.AreEqual(format.SpaceBefore, 0.0d);

format.LineUnitBefore = 5.1;

Assert.AreEqual(format.SpaceBefore, 61.1d, 0.1d);

// 5 - 段落后的行距：
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
* 命名空间 [Aspose.Words](../../paragraphformat/)
* 部件 [Aspose.Words](../../../)


