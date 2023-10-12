---
title: FieldOptions.IsBidiTextSupportedOnUpdate
second_title: Aspose.Words for .NET API Referansı
description: FieldOptions mülk. Çift yönlü metnin alan güncellemesi sırasında tam olarak desteklenip desteklenmediğini belirten değeri alır veya ayarlar.
type: docs
weight: 150
url: /tr/net/aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/
---
## FieldOptions.IsBidiTextSupportedOnUpdate property

Çift yönlü metnin alan güncellemesi sırasında tam olarak desteklenip desteklenmediğini belirten değeri alır veya ayarlar.

```csharp
public bool IsBidiTextSupportedOnUpdate { get; set; }
```

### Notlar

Bu özellik olarak ayarlandığında`doğru`, güncellemesi sırasında Sağdan Sola language (yani Arapça veya İbranice) uyumlu alan sonucu üretmek için ek adımlar gerçekleştirilir.

Bu özellik olarak ayarlandığında`YANLIŞ` ve Sağdan Sola dili kullanıldığında, result alanının güncellendikten sonra doğruluğu garanti edilmez.

Varsayılan değer:`YANLIŞ`.

### Örnekler

Alan güncellemesinin çift yönlü metni tam olarak desteklediğinden emin olmak için FieldOptions'ın nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Sağdan sola metin içeren tüm saha işlemlerinin beklendiği gibi yapıldığından emin olun.
doc.FieldOptions.IsBidiTextSupportedOnUpdate = true;

// Sağdan sola metni içeren bir alan eklemek için belge oluşturucuyu kullanın.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "עֶשְׂרִים", "שְׁלוֹשִׁים", "אַרְבָּעִים", "חֲמִשִּׁים", "שִׁשִּׁים" }, 0);
comboBox.CalculateOnExit = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.Bidi.docx");
```

### Ayrıca bakınız

* class [FieldOptions](../)
* ad alanı [Aspose.Words.Fields](../../fieldoptions/)
* toplantı [Aspose.Words](../../../)


