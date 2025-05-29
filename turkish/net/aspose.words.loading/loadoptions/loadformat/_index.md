---
title: LoadOptions.LoadFormat
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: .NET için Aspose.Words
description: Belge biçimlerini kolayca belirtmek için LoadOptions LoadFormat özelliğini keşfedin. Sorunsuz performans için varsayılan Otomatik ayarıyla yüklemeyi optimize edin.
type: docs
weight: 90
url: /tr/net/aspose.words.loading/loadoptions/loadformat/
---
## LoadOptions.LoadFormat property

Yüklenecek belgenin biçimini belirtir. VarsayılanAuto .

```csharp
public LoadFormat LoadFormat { get; set; }
```

## Notlar

Aşağıdakileri belirtmeniz önerilir:Auto değerini ve Aspose.Words'ün dosya biçimini otomatik olarak algılamasına izin verin. Yüklemek üzere olduğunuz belgenin biçimini biliyorsanız, format 'yi açıkça belirtebilirsiniz ve bu, biçimi otomatik olarak algılamayla ilişkili ek yük nedeniyle yükleme süresini biraz azaltacaktır. Açık bir yükleme biçimi belirtirseniz ve bunun yanlış olduğu ortaya çıkarsa, otomatik algılama çağrılacak ve dosyayı yüklemek için ikinci bir denemesi yapılacaktır.

## Örnekler

Bir HTML belgesini açarken temel URI'nin nasıl belirtileceğini gösterir.

```csharp
// Göreceli bir URI ile bağlantılı bir resim içeren bir .html belgesi yüklemek istediğimizi varsayalım
// görüntü farklı bir konumdayken. Bu durumda, bağıl URI'yi mutlak olana dönüştürmemiz gerekecektir.
 // HtmlLoadOptions nesnesini kullanarak bir temel URI sağlayabiliriz.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Giriş .html'deki resim bozulmuş olsa da, özel temel URI'miz bağlantıyı onarmamıza yardımcı oldu.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Bu çıktı belgesi eksik olan resmi gösterecektir.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### Ayrıca bakınız

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [LoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
