---
title: ParagraphFormat.CharacterUnitFirstLineIndent
linktitle: CharacterUnitFirstLineIndent
articleTitle: CharacterUnitFirstLineIndent
second_title: Aspose.Words for .NET
description: Discover the ParagraphFormat CharacterUnitFirstLineIndent property to easily customize your document's first line or hanging indent for a polished look.
type: docs
weight: 70
url: /net/aspose.words/paragraphformat/characterunitfirstlineindent/
---
## ParagraphFormat.CharacterUnitFirstLineIndent property

Gets or sets the value (in characters) for the first-line or hanging indent.

Use positive values to set the first-line indent, and negative values to set the hanging indent.

```csharp
public double CharacterUnitFirstLineIndent { get; set; }
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
