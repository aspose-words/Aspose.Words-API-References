---
title: LoadOptions.BaseUri
second_title: Aspose.Words for .NET API Referansı
description: LoadOptions mülk. Gerektiğinde belgede bulunan göreli URIleri mutlak URIlere çözümlemek için kullanılacak dizeyi alır veya ayarlar. Olabilirhükümsüz veya boş dize. Varsayılanhükümsüz .
type: docs
weight: 20
url: /tr/net/aspose.words.loading/loadoptions/baseuri/
---
## LoadOptions.BaseUri property

Gerektiğinde belgede bulunan göreli URI'leri mutlak URI'lere çözümlemek için kullanılacak dizeyi alır veya ayarlar. Olabilir`hükümsüz` veya boş dize. Varsayılan:`hükümsüz` .

```csharp
public string BaseUri { get; set; }
```

### Notlar

Bu özellik, aşağıdaki durumlarda göreceli URI'leri mutlak olarak çözümlemek için kullanılır:

1. Bir akıştan bir HTML belgesi yüklerken ve belge göreli URI'leri olan görüntüler içeriyor ve BASE HTML öğesinde belirtilen bir temel URI'ye sahip değil.
2. Bir belgeyi PDF'ye ve diğer formatlara kaydederken, ilgili URIs kullanılarak bağlanan görüntüleri almak ve böylece görüntülerin çıktı belgesine kaydedilmesini sağlamak.

### Örnekler

Temel URI kullanarak bir akıştan görüntüler içeren bir HTML belgesinin nasıl açılacağını gösterir.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Temel klasörü yüklerken URI'yi iletin
    // böylece HTML belgesindeki ilgili URI'lere sahip tüm görseller bulunabilir.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // Belgenin ilk şeklinin geçerli bir resim içerdiğini doğrulayın.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

### Ayrıca bakınız

* class [LoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../loadoptions/)
* toplantı [Aspose.Words](../../../)


