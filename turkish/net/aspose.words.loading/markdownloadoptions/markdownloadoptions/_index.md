---
title: MarkdownLoadOptions
linktitle: MarkdownLoadOptions
articleTitle: MarkdownLoadOptions
second_title: .NET için Aspose.Words
description: Gelişmiş belge işleme ve özelleştirme için MarkdownLoadOptions örneklerini kolayca başlatmak üzere MarkdownLoadOptions oluşturucusunu keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.loading/markdownloadoptions/markdownloadoptions/
---
## MarkdownLoadOptions constructor

Yeni bir örneğini başlatır[`MarkdownLoadOptions`](../) sınıf.

```csharp
public MarkdownLoadOptions()
```

## Notlar

Otomatik olarak ayarlar[`LoadFormat`](../../../aspose.words/loadformat/) ileMarkdown .

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
