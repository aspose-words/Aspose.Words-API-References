---
title: FieldOptions.IsBidiTextSupportedOnUpdate
second_title: Aspose.Words for .NET API Referansı
description: FieldOptions mülk. Alan güncellemesi sırasında iki yönlü metnin tam olarak desteklenip desteklenmediğini gösteren değeri alır veya ayarlar.
type: docs
weight: 130
url: /tr/net/aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/
---
## FieldOptions.IsBidiTextSupportedOnUpdate property

Alan güncellemesi sırasında iki yönlü metnin tam olarak desteklenip desteklenmediğini gösteren değeri alır veya ayarlar.

```csharp
public bool IsBidiTextSupportedOnUpdate { get; set; }
```

### Notlar

Bu özellik olarak ayarlandığında **doğru**, güncelleme sırasında Sağdan Sola dil (yani Arapça veya İbranice) uyumlu alan sonucu üretmek için ek adımlar gerçekleştirilir.

Bu özellik olarak ayarlandığında **yanlış** ve Sağdan Sola dili kullanılır, update alanının güncellenmesinden sonra doğruluğu garanti edilmez.

Varsayılan değer **yanlış**.

### Örnekler

Alan güncellemesinin çift yönlü metni tam olarak desteklediğinden emin olmak için FieldOptions'ın nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Sağdan sola metin içeren herhangi bir alan işleminin beklendiği gibi yapıldığından emin olun. 
doc.FieldOptions.IsBidiTextSupportedOnUpdate = true;

// Sağdan sola metni içeren bir alan eklemek için bir belge oluşturucu kullanın.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "עֶשְׂרִים", "שְׁלוֹשִׁים", "אַרְבָּעִים", "חֲמִשִּׁים", "שִׁשִּׁים" }, 0);
comboBox.CalculateOnExit = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.Bidi.docx");
```

### Ayrıca bakınız

* class [FieldOptions](../)
* ad alanı [Aspose.Words.Fields](../../fieldoptions/)
* toplantı [Aspose.Words](../../../)


