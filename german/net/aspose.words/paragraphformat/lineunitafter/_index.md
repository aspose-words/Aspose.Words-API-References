---
title: ParagraphFormat.LineUnitAfter
linktitle: LineUnitAfter
articleTitle: LineUnitAfter
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „PargraphFormat LineUnitAfter“ – steuern Sie den Abstand in Gitternetzlinien für ein verbessertes Absatzlayout und eine verbesserte Lesbarkeit des Dokuments.
type: docs
weight: 220
url: /de/net/aspose.words/paragraphformat/lineunitafter/
---
## ParagraphFormat.LineUnitAfter property

Ruft den Abstand (in Gitternetzlinien) nach den Absätzen ab oder legt ihn fest.

```csharp
public double LineUnitAfter { get; set; }
```

## Beispiele

Zeigt, wie Absatzabstände und Einzüge geändert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;

// Nachfolgend finden Sie fünf verschiedene Abstandsoptionen sowie die Eigenschaften, auf die sich ihre Konfiguration indirekt auswirkt.
// 1 - Linker Einzug:
Assert.AreEqual(format.LeftIndent, 0.0d);

format.CharacterUnitLeftIndent = 10.0;

Assert.AreEqual(format.LeftIndent, 120.0d);

// 2 - Rechter Einzug:
Assert.AreEqual(format.RightIndent, 0.0d); 

format.CharacterUnitRightIndent = -5.5;

Assert.AreEqual(format.RightIndent, -66.0d);

// 3 - Hängender Einzug:
Assert.AreEqual(format.FirstLineIndent, 0.0d);

format.CharacterUnitFirstLineIndent = 20.3;

Assert.AreEqual(format.FirstLineIndent, 243.59d, 0.1d);

// 4 - Zeilenabstand vor Absätzen:
Assert.AreEqual(format.SpaceBefore, 0.0d);

format.LineUnitBefore = 5.1;

Assert.AreEqual(format.SpaceBefore, 61.1d, 0.1d);

// 5 - Zeilenabstand nach Absätzen:
Assert.AreEqual(format.SpaceAfter, 0.0d);

format.LineUnitAfter = 10.9;

Assert.AreEqual(format.SpaceAfter, 130.8d, 0.1d);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试" +
              "文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档");
```

### Siehe auch

* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
