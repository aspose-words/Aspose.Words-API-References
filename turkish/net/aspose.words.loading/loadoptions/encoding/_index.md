---
title: LoadOptions.Encoding
second_title: Aspose.Words for .NET API Referansı
description: LoadOptions mülk. Belgede kodlama belirtilmemişse bir HTML TXT veya CHM belgesini yüklemek için kullanılacak kodlamayı alır veya ayarlar. Olabilirhükümsüz . Varsayılanhükümsüz .
type: docs
weight: 50
url: /tr/net/aspose.words.loading/loadoptions/encoding/
---
## LoadOptions.Encoding property

Belgede kodlama belirtilmemişse bir HTML, TXT veya CHM belgesini yüklemek için kullanılacak kodlamayı alır veya ayarlar. Olabilir`hükümsüz` . Varsayılan:`hükümsüz` .

```csharp
public Encoding Encoding { get; set; }
```

### Notlar

Bu özellik yalnızca HTML, TXT veya CHM belgeleri yüklenirken kullanılır.

Belgede kodlama belirtilmemişse ve bu özellik`hükümsüz`ardından sistem to kodlamayı otomatik olarak algılamaya çalışacaktır.

### Örnekler

Bir belgenin açılacağı kodlamanın nasıl ayarlanacağını gösterir.

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
* ad alanı [Aspose.Words.Loading](../../loadoptions/)
* toplantı [Aspose.Words](../../../)


