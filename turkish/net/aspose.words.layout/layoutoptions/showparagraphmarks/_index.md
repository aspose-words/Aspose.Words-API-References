---
title: LayoutOptions.ShowParagraphMarks
second_title: Aspose.Words for .NET API Referansı
description: LayoutOptions mülk. Paragraf işaretlerinin oluşturulup oluşturulmayacağına ilişkin göstergeyi alır veya ayarlar. VarsayılanYANLIŞ .
type: docs
weight: 90
url: /tr/net/aspose.words.layout/layoutoptions/showparagraphmarks/
---
## LayoutOptions.ShowParagraphMarks property

Paragraf işaretlerinin oluşturulup oluşturulmayacağına ilişkin göstergeyi alır veya ayarlar. Varsayılan:`YANLIŞ` .

```csharp
public bool ShowParagraphMarks { get; set; }
```

### Örnekler

İşlenmiş bir çıktı belgesinde paragraf işaretlerinin nasıl gösterileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Birkaç paragraf ekleyin, ardından paragraf sonlarını göstermek için paragraf işaretlerini etkinleştirin
// belgeyi oluşturduğumuzda pilcrow (¶) sembolüyle.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

### Ayrıca bakınız

* class [LayoutOptions](../)
* ad alanı [Aspose.Words.Layout](../../layoutoptions/)
* toplantı [Aspose.Words](../../../)


