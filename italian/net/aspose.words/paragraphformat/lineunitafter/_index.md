---
title: ParagraphFormat.LineUnitAfter
linktitle: LineUnitAfter
articleTitle: LineUnitAfter
second_title: Aspose.Words per .NET
description: Scopri la proprietà ParagraphFormat LineUnitAfter: controlla la spaziatura nelle linee della griglia per un layout di paragrafo migliorato e una migliore leggibilità del documento.
type: docs
weight: 220
url: /it/net/aspose.words/paragraphformat/lineunitafter/
---
## ParagraphFormat.LineUnitAfter property

Ottiene o imposta la quantità di spaziatura (nelle linee della griglia) dopo i paragrafi.

```csharp
public double LineUnitAfter { get; set; }
```

## Esempi

Mostra come modificare la spaziatura e i rientri dei paragrafi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;

// Di seguito sono riportate cinque diverse opzioni di spaziatura, insieme alle proprietà sulle quali la loro configurazione influisce indirettamente.
// 1 - Rientro sinistro:
Assert.AreEqual(format.LeftIndent, 0.0d);

format.CharacterUnitLeftIndent = 10.0;

Assert.AreEqual(format.LeftIndent, 120.0d);

// 2 - Rientro a destra:
Assert.AreEqual(format.RightIndent, 0.0d); 

format.CharacterUnitRightIndent = -5.5;

Assert.AreEqual(format.RightIndent, -66.0d);

// 3 - Rientro sporgente:
Assert.AreEqual(format.FirstLineIndent, 0.0d);

format.CharacterUnitFirstLineIndent = 20.3;

Assert.AreEqual(format.FirstLineIndent, 243.59d, 0.1d);

// 4 - Interlinea prima dei paragrafi:
Assert.AreEqual(format.SpaceBefore, 0.0d);

format.LineUnitBefore = 5.1;

Assert.AreEqual(format.SpaceBefore, 61.1d, 0.1d);

// 5 - Interlinea dopo i paragrafi:
Assert.AreEqual(format.SpaceAfter, 0.0d);

format.LineUnitAfter = 10.9;

Assert.AreEqual(format.SpaceAfter, 130.8d, 0.1d);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试" +
              "文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档");
```

### Guarda anche

* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
