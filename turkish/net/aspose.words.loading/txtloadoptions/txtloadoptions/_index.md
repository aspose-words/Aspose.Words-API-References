---
title: TxtLoadOptions
linktitle: TxtLoadOptions
articleTitle: TxtLoadOptions
second_title: .NET için Aspose.Words
description: TxtLoadOptions kurucusunu keşfedin! Varsayılan değerlerle kolayca başlatın ve gelişmiş performans için veri yükleme sürecinizi kolaylaştırın.
type: docs
weight: 10
url: /tr/net/aspose.words.loading/txtloadoptions/txtloadoptions/
---
## TxtLoadOptions constructor

Bu sınıfın yeni bir örneğini varsayılan değerlerle başlatır.

```csharp
public TxtLoadOptions()
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
