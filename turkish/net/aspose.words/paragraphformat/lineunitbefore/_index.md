---
title: ParagraphFormat.LineUnitBefore
linktitle: LineUnitBefore
articleTitle: LineUnitBefore
second_title: .NET için Aspose.Words
description: ParagraphFormat LineUnitBefore özelliğinin, paragraflar arasındaki boşlukları ayarlayarak belgenizin düzenini nasıl geliştirdiğini ve daha şık bir görünüm sağladığını keşfedin.
type: docs
weight: 230
url: /tr/net/aspose.words/paragraphformat/lineunitbefore/
---
## ParagraphFormat.LineUnitBefore property

Paragraflardan önceki boşluk miktarını (kılavuz çizgilerinde) alır veya ayarlar.

```csharp
public double LineUnitBefore { get; set; }
```

## Örnekler

Paragraf aralığının ve girintilerin nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;

// Aşağıda, yapılandırmalarının dolaylı olarak etkilediği özelliklerle birlikte beş farklı aralık seçeneği bulunmaktadır.
// 1 - Sol girinti:
Assert.AreEqual(format.LeftIndent, 0.0d);

format.CharacterUnitLeftIndent = 10.0;

Assert.AreEqual(format.LeftIndent, 120.0d);

// 2 - Sağ girinti:
Assert.AreEqual(format.RightIndent, 0.0d); 

format.CharacterUnitRightIndent = -5.5;

Assert.AreEqual(format.RightIndent, -66.0d);

// 3 - Asılı girinti:
Assert.AreEqual(format.FirstLineIndent, 0.0d);

format.CharacterUnitFirstLineIndent = 20.3;

Assert.AreEqual(format.FirstLineIndent, 243.59d, 0.1d);

// 4 - Paragraflardan önceki satır aralıkları:
Assert.AreEqual(format.SpaceBefore, 0.0d);

format.LineUnitBefore = 5.1;

Assert.AreEqual(format.SpaceBefore, 61.1d, 0.1d);

// 5 - Paragraflardan sonraki satır aralıkları:
Assert.AreEqual(format.SpaceAfter, 0.0d);

format.LineUnitAfter = 10.9;

Assert.AreEqual(format.SpaceAfter, 130.8d, 0.1d);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试" +
              "文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档");
```

### Ayrıca bakınız

* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
