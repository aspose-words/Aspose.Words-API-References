---
title: LoadOptions.LoadFormat
second_title: Aspose.Words for .NET API Referansı
description: LoadOptions mülk. Yüklenecek belgenin biçimini belirtir. VarsayılanAuto .
type: docs
weight: 90
url: /tr/net/aspose.words.loading/loadoptions/loadformat/
---
## LoadOptions.LoadFormat property

Yüklenecek belgenin biçimini belirtir. VarsayılanAuto .

```csharp
public LoadFormat LoadFormat { get; set; }
```

### Notlar

belirtmeniz önerilir.Autodeğerini belirleyin ve Aspose.Words'ün dosya biçimini otomatik olarak algılamasına izin verin. Yüklemek üzere olduğunuz belgenin biçimini biliyorsanız, biçim 'yi açıkça belirtebilirsiniz ve bu, biçimin otomatik olarak algılanmasıyla ilişkili ek yük nedeniyle yükleme süresini biraz azaltacaktır. Açık bir yükleme biçimi belirtirseniz, dosya dönecektir. yanlışsa, otomatik algılama başlatılacak ve dosyayı ikinci yükleme girişiminde bulunulacaktır.

### Örnekler

Bir html belgesini açarken bir temel URI'nin nasıl belirtileceğini gösterir.

```csharp
// Göreli bir URI ile bağlantılı bir resim içeren bir .html belgesi yüklemek istediğimizi varsayalım.
// görüntü farklı bir konumdayken. Bu durumda, göreli URI'yi mutlak bir URI'ye çözmemiz gerekecek.
 // Bir HtmlLoadOptions nesnesi kullanarak bir temel URI sağlayabiliriz.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// .html girişinde görüntü bozukken, özel temel URI'miz bağlantıyı onarmamıza yardımcı oldu.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Bu çıktı belgesi, eksik olan resmi gösterecektir.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### Ayrıca bakınız

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [LoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../loadoptions/)
* toplantı [Aspose.Words](../../../)


