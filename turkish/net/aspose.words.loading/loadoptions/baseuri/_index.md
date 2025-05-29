---
title: LoadOptions.BaseUri
linktitle: BaseUri
articleTitle: BaseUri
second_title: .NET için Aspose.Words
description: Belgelerinizdeki bağıl URI'leri kolayca mutlak olanlara dönüştürmek için LoadOptions BaseUri özelliğini keşfedin. URI yönetiminizi bugün geliştirin!
type: docs
weight: 20
url: /tr/net/aspose.words.loading/loadoptions/baseuri/
---
## LoadOptions.BaseUri property

Gerektiğinde belgede bulunan bağıl URI'leri mutlak URI'lere dönüştürmek için kullanılacak dizeyi alır veya ayarlar. `hükümsüz` veya boş dize. Varsayılan`hükümsüz` .

```csharp
public string BaseUri { get; set; }
```

## Notlar

Bu özellik, aşağıdaki durumlarda bağıl URI'leri mutlak URI'lere dönüştürmek için kullanılır:

1. Bir akıştan bir HTML belgesi yüklenirken ve belgede göreli URI'li resimler bulunuyorsa ve BASE HTML öğesinde belirtilen bir temel URI yoksa.
2. Bir belgeyi PDF ve diğer formatlara kaydederken, bağıl URI'ler kullanılarak bağlantılı görüntüleri almak için, böylece görüntüler çıktı belgesine kaydedilebilir.

## Örnekler

Bir akıştan gelen görselleri içeren bir HTML belgesinin temel URI kullanılarak nasıl açılacağını gösterir.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Yükleme sırasında temel klasörün URI'sini geçirin
    // böylece HTML belgesinde bağıl URI'leri olan tüm resimler bulunabilir.
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
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
