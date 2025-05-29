---
title: FieldOptions.IsBidiTextSupportedOnUpdate
linktitle: IsBidiTextSupportedOnUpdate
articleTitle: IsBidiTextSupportedOnUpdate
second_title: .NET için Aspose.Words
description: FieldOptions'da çift yönlü metin desteğinin etkin olup olmadığını keşfedin. Gelişmiş çok dilli işlevsellik için metin güncellemelerini kolayca yönetin.
type: docs
weight: 150
url: /tr/net/aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/
---
## FieldOptions.IsBidiTextSupportedOnUpdate property

Alan güncellemesi sırasında çift yönlü metnin tam olarak desteklenip desteklenmediğini gösteren değeri alır veya ayarlar.

```csharp
public bool IsBidiTextSupportedOnUpdate { get; set; }
```

## Notlar

Bu özellik şu şekilde ayarlandığında:`doğru`, güncelleme sırasında Sağdan Sola language (yani Arapça veya İbranice) uyumlu alan sonucunu üretmek için ek adımlar gerçekleştirilir.

Bu özellik şu şekilde ayarlandığında:`YANLIŞ` ve Sağdan Sola dil kullanıldığında, result alanının güncellendikten sonra doğruluğu garanti edilmez.

Varsayılan değer:`YANLIŞ`.

## Örnekler

Alan güncellemelerinin çift yönlü metni tam olarak desteklemesini sağlamak için FieldOptions'ın nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Sağdan sola metin içeren herhangi bir alan işleminin beklendiği gibi gerçekleştirildiğinden emin olun.
doc.FieldOptions.IsBidiTextSupportedOnUpdate = true;

// Sağdan sola metin içeren bir alan eklemek için bir belge oluşturucu kullanın.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "עֶשְׂרִים", "שְׁלוֹשִׁים", "אַרְבָּעִים", "חֲמִשִּׁים", "שִׁשִּׁים" }, 0);
comboBox.CalculateOnExit = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.Bidi.docx");
```

### Ayrıca bakınız

* class [FieldOptions](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
