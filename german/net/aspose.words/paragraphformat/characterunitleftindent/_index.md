---
title: ParagraphFormat.CharacterUnitLeftIndent
second_title: Aspose.Words für .NET-API-Referenz
description: ParagraphFormat eigendom. Ruft den Wert für den linken Einzug in Zeichen für die angegebenen Absätze ab oder legt diesen fest.
type: docs
weight: 80
url: /de/net/aspose.words/paragraphformat/characterunitleftindent/
---
## ParagraphFormat.CharacterUnitLeftIndent property

Ruft den Wert für den linken Einzug (in Zeichen) für die angegebenen Absätze ab oder legt diesen fest.

```csharp
public double CharacterUnitLeftIndent { get; set; }
```

### Beispiele

Zeigt, wie Absatzabstände und Einzüge geändert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;

// Nachfolgend finden Sie fünf verschiedene Abstandsoptionen sowie die Eigenschaften, die sich durch ihre Konfiguration indirekt auswirken.
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
* namensraum [Aspose.Words](../../paragraphformat/)
* Montage [Aspose.Words](../../../)


