---
title: ParagraphFormat.CharacterUnitFirstLineIndent
linktitle: CharacterUnitFirstLineIndent
articleTitle: CharacterUnitFirstLineIndent
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ParagraphFormat CharacterUnitFirstLineIndent för att enkelt anpassa dokumentets första rad eller hängande indrag för ett elegant utseende.
type: docs
weight: 70
url: /sv/net/aspose.words/paragraphformat/characterunitfirstlineindent/
---
## ParagraphFormat.CharacterUnitFirstLineIndent property

Hämtar eller anger värdet (i tecken) för den första raden eller det hängande indraget.

Använd positiva värden för att ange indraget på första raden och negativa värden för att ange det hängande indraget.

```csharp
public double CharacterUnitFirstLineIndent { get; set; }
```

## Exempel

Visar hur man ändrar styckeavstånd och indrag.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;

// Nedan följer fem olika avståndsalternativ, tillsammans med de egenskaper som deras konfiguration indirekt påverkar.
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

* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
