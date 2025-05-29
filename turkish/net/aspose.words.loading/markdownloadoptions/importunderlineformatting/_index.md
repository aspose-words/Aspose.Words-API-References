---
title: MarkdownLoadOptions.ImportUnderlineFormatting
linktitle: ImportUnderlineFormatting
articleTitle: ImportUnderlineFormatting
second_title: .NET için Aspose.Words
description: MarkdownLoadOptions ImportUnderlineFormatting özelliğini keşfedin. Basit bir boolean ayarıyla alt çizgi metin biçimlendirmesini kontrol edin. Markdown deneyiminizi geliştirin!
type: docs
weight: 20
url: /tr/net/aspose.words.loading/markdownloadoptions/importunderlineformatting/
---
## MarkdownLoadOptions.ImportUnderlineFormatting property

İki artı karakterden oluşan bir diziyi "++" alt çizgi metin biçimlendirmesi olarak tanımayı belirten bir Boole değeri alır veya ayarlar. Varsayılan değer`YANLIŞ` .

```csharp
public bool ImportUnderlineFormatting { get; set; }
```

## Örnekler

Altı çizili metin biçimlendirmesinde artı karakterleri "++"nın nasıl tanınacağını gösterir.

```csharp
using (MemoryStream stream = new MemoryStream(Encoding.ASCII.GetBytes("++12 and B++")))
{
    MarkdownLoadOptions loadOptions = new MarkdownLoadOptions() { ImportUnderlineFormatting = true };
    Document doc = new Document(stream, loadOptions);

    Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
    Assert.AreEqual(Underline.Single, para.Runs[0].Font.Underline);

    loadOptions = new MarkdownLoadOptions() { ImportUnderlineFormatting = false };
    doc = new Document(stream, loadOptions);

    para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
    Assert.AreEqual(Underline.None, para.Runs[0].Font.Underline);
}
```

### Ayrıca bakınız

* class [MarkdownLoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
