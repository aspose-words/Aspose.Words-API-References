---
title: CharacterUnitFirstLineIndent
second_title: Aspose.Words för .NET API Referens
description: Hämtar eller ställer in värdet i tecken för första raden eller hängande indrag.
type: docs
weight: 60
url: /sv/net/aspose.words/paragraphformat/characterunitfirstlineindent/
---
## ParagraphFormat.CharacterUnitFirstLineIndent property

Hämtar eller ställer in värdet (i tecken) för första raden eller hängande indrag.

Använd positiva värden för att ställa in första radens indrag och negativa värden för att ställa in hängande indrag.

```csharp
public double CharacterUnitFirstLineIndent { get; set; }
```

### Exempel

Visar hur du ändrar styckeavstånd och indrag.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;

// Nedan finns fem olika mellanrumsalternativ, tillsammans med de egenskaper som deras konfiguration indirekt påverkar.
// 1 - Vänster indrag:
Assert.AreEqual(format.LeftIndent, 0.0d);

format.CharacterUnitLeftIndent = 10.0;

Assert.AreEqual(format.LeftIndent, 120.0d);

// 2 - Höger indrag:
Assert.AreEqual(format.RightIndent, 0.0d); 

format.CharacterUnitRightIndent = -5.5;

Assert.AreEqual(format.RightIndent, -66.0d);

// 3 - Hängande indrag:
Assert.AreEqual(format.FirstLineIndent, 0.0d);

format.CharacterUnitFirstLineIndent = 20.3;

Assert.AreEqual(format.FirstLineIndent, 243.59d, 0.1d);

// 4 - Radavstånd före stycken:
Assert.AreEqual(format.SpaceBefore, 0.0d);

format.LineUnitBefore = 5.1;

Assert.AreEqual(format.SpaceBefore, 61.1d, 0.1d);

// 5 - Radavstånd efter stycken:
Assert.AreEqual(format.SpaceAfter, 0.0d);

format.LineUnitAfter = 10.9;

Assert.AreEqual(format.SpaceAfter, 130.8d, 0.1d);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试" +
              "文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档");
```

### Se även

* class [ParagraphFormat](../../paragraphformat)
* namnutrymme [Aspose.Words](../../paragraphformat)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->