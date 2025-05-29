---
title: FindReplaceOptions.ApplyParagraphFormat
linktitle: ApplyParagraphFormat
articleTitle: ApplyParagraphFormat
second_title: .NET için Aspose.Words
description: Belgelerinizde kusursuz paragraf biçimlendirmesi için FindReplaceOptions'daki ApplyParagraphFormat özelliğini keşfedin. İçeriğinizi zahmetsizce geliştirin!
type: docs
weight: 30
url: /tr/net/aspose.words.replacing/findreplaceoptions/applyparagraphformat/
---
## FindReplaceOptions.ApplyParagraphFormat property

Yeni içeriğe uygulanan paragraf biçimlendirmesi.

```csharp
public ParagraphFormat ApplyParagraphFormat { get; }
```

## Örnekler

Bul ve değiştir işleminin eşleşme bulduğu paragraflara biçimlendirmenin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Every paragraph that ends with a full stop like this one will be right aligned.");
builder.Writeln("This one will not!");
builder.Write("This one also will.");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(ParagraphAlignment.Left, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[2].ParagraphFormat.Alignment);

// Bul ve değiştir işlemini değiştirmek için "FindReplaceOptions" nesnesini kullanabiliriz.
FindReplaceOptions options = new FindReplaceOptions();

// Her paragrafı sağa hizalamak için "Hizalama" özelliğini "ParagraphAlignment.Right" olarak ayarlayın
// bul ve değiştir işleminin bulduğu eşleşmeyi içeren.
options.ApplyParagraphFormat.Alignment = ParagraphAlignment.Right;

// Paragraf sonundan hemen önce gelen tüm noktaları ünlem işaretiyle değiştirin.
int count = doc.Range.Replace(".&p", "!&p", options);

Assert.AreEqual(2, count);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[2].ParagraphFormat.Alignment);
Assert.AreEqual("Every paragraph that ends with a full stop like this one will be right aligned!\r" +
                "This one will not!\r" +
                "This one also will!", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [ParagraphFormat](../../../aspose.words/paragraphformat/)
* class [FindReplaceOptions](../)
* ad alanı [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* toplantı [Aspose.Words](../../../)
