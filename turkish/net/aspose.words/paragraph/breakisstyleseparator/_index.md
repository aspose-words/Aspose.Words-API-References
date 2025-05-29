---
title: Paragraph.BreakIsStyleSeparator
linktitle: BreakIsStyleSeparator
articleTitle: BreakIsStyleSeparator
second_title: .NET için Aspose.Words
description: Paragraf Sonu IsStyleSeparator özelliğinin, daha fazla tasarım esnekliği için karışık paragraf stilleri kullanılmasına izin vererek belge biçimlendirmesini nasıl geliştirdiğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words/paragraph/breakisstyleseparator/
---
## Paragraph.BreakIsStyleSeparator property

Bu paragraf sonu bir Stil Ayırıcısıysa Doğru. Bir stil ayırıcısı, bir paragrafının farklı paragraf stillerine sahip parçalardan oluşmasına izin verir.

```csharp
public bool BreakIsStyleSeparator { get; }
```

## Örnekler

İçindekiler başlığıyla aynı satıra metin yazmanın ve İçindekiler'de görünmemesinin nasıl sağlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertTableOfContents("\\o \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// İçindekiler tablosunun giriş olarak seçeceği bir stilde bir paragraf ekleyin.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

// Bu iki dize de aynı paragrafta yer alır ve bu nedenle aynı İçindekiler girişinde gösterilir.
builder.Write("Heading 1. ");
builder.Write("Will appear in the TOC. ");

// Bir stil ayracı eklersek aynı paragrafa daha fazla metin yazabiliriz
// ve İçindekiler tablosunda görünmeden farklı bir stil kullanın.
// Ayırıcıdan sonra başlık tipi stili kullanırsak, bir belge metin satırından birden fazla İçindekiler girişi çizebiliriz.
builder.InsertStyleSeparator();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Quote;
builder.Write("Won't appear in the TOC. ");

Assert.True(doc.FirstSection.Body.FirstParagraph.BreakIsStyleSeparator);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Paragraph.BreakIsStyleSeparator.docx");
```

### Ayrıca bakınız

* class [Paragraph](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
