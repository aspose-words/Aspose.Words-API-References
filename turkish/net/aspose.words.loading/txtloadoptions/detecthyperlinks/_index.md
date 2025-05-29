---
title: TxtLoadOptions.DetectHyperlinks
linktitle: DetectHyperlinks
articleTitle: DetectHyperlinks
second_title: .NET için Aspose.Words
description: TxtLoadOptions' DetectHyperlinks özelliğinin köprü metinlerini algılayarak ve veri doğruluğunu iyileştirerek metin işlemeyi nasıl geliştirdiğini keşfedin. Varsayılan değer false'tur.
type: docs
weight: 30
url: /tr/net/aspose.words.loading/txtloadoptions/detecthyperlinks/
---
## TxtLoadOptions.DetectHyperlinks property

Metindeki köprü metinlerini algılamayı belirtir. Varsayılan değer`YANLIŞ` .

```csharp
public bool DetectHyperlinks { get; set; }
```

## Örnekler

Köprü metinlerin nasıl okunacağını ve görüntüleneceğini gösterir.

```csharp
const string inputText = "Some links in TXT:\n" +
        "https://www.aspose.com/\n" +
        "https://docs.aspose.com/words/net/\n";

using (Stream stream = new MemoryStream())
{
    byte[] buf = Encoding.ASCII.GetBytes(inputText);
    stream.Write(buf, 0, buf.Length);

    // Bağlantılı dokümanı yükle.
    Document doc = new Document(stream, new TxtLoadOptions() { DetectHyperlinks = true });

    // Köprü metinlerini yazdır.
    foreach (Field field in doc.Range.Fields)
        Console.WriteLine(field.Result);

    Assert.AreEqual(doc.Range.Fields[0].Result.Trim(), "https://www.aspose.com/");
    Assert.AreEqual(doc.Range.Fields[1].Result.Trim(), "https://docs.aspose.com/words/net/");
}
```

### Ayrıca bakınız

* class [TxtLoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
