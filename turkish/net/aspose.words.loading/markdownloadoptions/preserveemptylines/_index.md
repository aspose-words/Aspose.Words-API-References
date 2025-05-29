---
title: MarkdownLoadOptions.PreserveEmptyLines
linktitle: PreserveEmptyLines
articleTitle: PreserveEmptyLines
second_title: .NET için Aspose.Words
description: MarkdownLoadOptions PreserveEmptyLines özelliğinin, okunabilirliği artırmak için boş satırları koruyarak Markdown belgenizin yüklenmesini nasıl iyileştirdiğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.loading/markdownloadoptions/preserveemptylines/
---
## MarkdownLoadOptions.PreserveEmptyLines property

Yükleme sırasında boş satırların korunup korunmayacağını belirten bir Boole değeri alır veya ayarlarMarkdown document. Varsayılan değer`YANLIŞ` .

Normalde, Markdown'daki blok düzeyindeki öğeler arasındaki boş satırlar yok sayılır. Belgenin başındaki ve sonundaki boş satırlar da yok sayılır. Bu seçenek bu tür boş satırların içe aktarılmasına izin verir.

```csharp
public bool PreserveEmptyLines { get; set; }
```

## Örnekler

Belge yüklenirken boş satırın nasıl korunacağını gösterir.

```csharp
string mdText = $"{Environment.NewLine}Line1{Environment.NewLine}{Environment.NewLine}Line2{Environment.NewLine}{Environment.NewLine}";
using (MemoryStream stream = new MemoryStream(Encoding.UTF8.GetBytes(mdText)))
{
    MarkdownLoadOptions loadOptions = new MarkdownLoadOptions() { PreserveEmptyLines = true };
    Document doc = new Document(stream, loadOptions);

    Assert.AreEqual("\rLine1\r\rLine2\r\f", doc.GetText());
}
```

### Ayrıca bakınız

* class [MarkdownLoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
