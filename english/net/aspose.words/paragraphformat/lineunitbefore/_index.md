---
title: ParagraphFormat.LineUnitBefore
linktitle: LineUnitBefore
articleTitle: LineUnitBefore
second_title: Aspose.Words for .NET
description: Discover how the ParagraphFormat LineUnitBefore property enhances your document's layout by adjusting spacing before paragraphs for a polished look.
type: docs
weight: 230
url: /net/aspose.words/paragraphformat/lineunitbefore/
---
## ParagraphFormat.LineUnitBefore property

Gets or sets the amount of spacing (in gridlines) before the paragraphs.

```csharp
public double LineUnitBefore { get; set; }
```

## Examples

Shows how to change paragraph spacing and indents.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;

// Below are five different spacing options, along with the properties that their configuration indirectly affects.
// 1 -  Left indent:
Assert.That(0.0d, Is.EqualTo(format.LeftIndent));

format.CharacterUnitLeftIndent = 10.0;

Assert.That(120.0d, Is.EqualTo(format.LeftIndent));

// 2 -  Right indent:
Assert.That(0.0d, Is.EqualTo(format.RightIndent)); 

format.CharacterUnitRightIndent = -5.5;

Assert.That(-66.0d, Is.EqualTo(format.RightIndent));

// 3 -  Hanging indent:
Assert.That(0.0d, Is.EqualTo(format.FirstLineIndent));

format.CharacterUnitFirstLineIndent = 20.3;

Assert.That(243.59d, Is.EqualTo(format.FirstLineIndent).Within(0.1d));

// 4 -  Line spacing before paragraphs:
Assert.That(0.0d, Is.EqualTo(format.SpaceBefore));

format.LineUnitBefore = 5.1;

Assert.That(61.1d, Is.EqualTo(format.SpaceBefore).Within(0.1d));

// 5 -  Line spacing after paragraphs:
Assert.That(0.0d, Is.EqualTo(format.SpaceAfter));

format.LineUnitAfter = 10.9;

Assert.That(130.8d, Is.EqualTo(format.SpaceAfter).Within(0.1d));

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试" +
              "文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档");
```

### See Also

* class [ParagraphFormat](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
