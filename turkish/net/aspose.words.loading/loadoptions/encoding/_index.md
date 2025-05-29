---
title: LoadOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: .NET için Aspose.Words
description: HTML TXT veya CHM belge kodlamasını kolayca yönetmek için LoadOptions Kodlama özelliğini keşfedin. En iyi performans için içerik yüklemenizi özelleştirin!
type: docs
weight: 50
url: /tr/net/aspose.words.loading/loadoptions/encoding/
---
## LoadOptions.Encoding property

Kodlama belirtilmemişse HTML, TXT veya CHM belgesini yüklemek için kullanılacak kodlamayı alır veya ayarlar belgenin içinde. Şu şekilde olabilir:`hükümsüz` Varsayılan değer:`hükümsüz` .

```csharp
public Encoding Encoding { get; set; }
```

## Notlar

Bu özellik yalnızca HTML, TXT veya CHM belgeleri yüklenirken kullanılır.

Belgenin içinde kodlama belirtilmemişse ve bu özellik`hükümsüz`daha sonra sistem kodlamayı otomatik olarak algılamaya çalışacaktır.

## Örnekler

Bir belgenin hangi kodlamayla açılacağını gösterir.

```csharp
LoadOptions loadOptions = new LoadOptions
{
    Encoding = Encoding.ASCII
};

// LoadOptions nesnesini geçirirken belgeyi yükleyin, ardından belgenin içeriğini doğrulayın.
Document doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.True(doc.ToString(SaveFormat.Text).Contains("This is a sample text in English."));
```

### Ayrıca bakınız

* class [LoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
