---
title: LayoutOptions.ShowParagraphMarks
linktitle: ShowParagraphMarks
articleTitle: ShowParagraphMarks
second_title: .NET için Aspose.Words
description: LayoutOptions ShowParagraphMarks özelliğinin paragraf işaretlerinin görünürlüğünü değiştirerek metin biçimlendirmesini nasıl geliştirdiğini keşfedin. Belgenizin netliğini bugün geliştirin!
type: docs
weight: 90
url: /tr/net/aspose.words.layout/layoutoptions/showparagraphmarks/
---
## LayoutOptions.ShowParagraphMarks property

Paragraf işaretlerinin işlenip işlenmediğine dair göstergeyi alır veya ayarlar. Varsayılan`YANLIŞ` .

```csharp
public bool ShowParagraphMarks { get; set; }
```

## Örnekler

İşlenmiş çıktı belgesinde paragraf işaretlerinin nasıl gösterileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Birkaç paragraf ekleyin, ardından paragraf sonlarını göstermek için paragraf işaretlerini etkinleştirin
// belgeyi oluştururken pilcrow (¶) sembolüyle.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

### Ayrıca bakınız

* class [LayoutOptions](../)
* ad alanı [Aspose.Words.Layout](../../../aspose.words.layout/)
* toplantı [Aspose.Words](../../../)
