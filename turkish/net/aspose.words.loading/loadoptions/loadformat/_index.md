---
title: LoadOptions.LoadFormat
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: Aspose.Words for .NET
description: LoadOptions LoadFormat mülk. Yüklenecek belgenin biçimini belirtir. VarsayılanAuto  C#'da.
type: docs
weight: 90
url: /tr/net/aspose.words.loading/loadoptions/loadformat/
---
## LoadOptions.LoadFormat property

Yüklenecek belgenin biçimini belirtir. Varsayılan:Auto .

```csharp
public LoadFormat LoadFormat { get; set; }
```

## Notlar

belirtmeniz önerilir.Auto değerini girin ve Aspose.Words'ün dosya formatını otomatik olarak tespit etmesine izin verin . Yüklemek üzere olduğunuz belgenin formatını biliyorsanız, format 'yi açıkça belirleyebilirsiniz ve bu, formatın otomatik olarak algılanmasıyla ilişkili ek yük nedeniyle yükleme süresini biraz azaltır. Açık bir yükleme formatı belirtirseniz, o da açılacaktır. yanlış olduğu anlaşılırsa, otomatik algılama başlatılacak ve dosyayı yüklemek için Second denemesi yapılacaktır.

## Örnekler

Bir html belgesini açarken temel URI'nin nasıl belirtileceğini gösterir.

```csharp
// Göreli bir URI ile bağlantılı bir resim içeren bir .html belgesi yüklemek istediğimizi varsayalım
// resim farklı bir konumdayken. Bu durumda, göreceli URI'yi mutlak bir URI'ye dönüştürmemiz gerekecek.
 // HtmlLoadOptions nesnesini kullanarak bir temel URI sağlayabiliriz.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Görüntü .html girişinde bozuk olsa da, özel temel URI'miz bağlantıyı onarmamıza yardımcı oldu.
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
