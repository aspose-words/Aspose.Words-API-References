---
title: MailMergeOptions.UseNonMergeFields
linktitle: UseNonMergeFields
articleTitle: UseNonMergeFields
second_title: .NET için Aspose.Words
description: UseNonMergeFields özelliğiyle gelişmiş posta birleştirme yeteneklerinin kilidini açın. Gelişmiş belge özelleştirmesi için MERGEFIELD ve diğer alan türlerini sorunsuz bir şekilde entegre edin.
type: docs
weight: 130
url: /tr/net/aspose.words.lowcode/mailmergeoptions/usenonmergefields/
---
## MailMergeOptions.UseNonMergeFields property

Ne zaman`doğru` , MERGEFIELD alanlarına ek olarak, bazı diğer alan türlerinde ve ayrıca "{{fieldName}}" etiketlerinde posta birleştirmenin gerçekleştirildiğini belirtir.

```csharp
public bool UseNonMergeFields { get; set; }
```

## Notlar

Normalde, posta birleştirme yalnızca MERGEFIELD alanlarına yapılır, ancak birkaç müşterinin reporting 'si diğer alanları kullanarak oluşturulmuştu ve birçok belge bu şekilde oluşturulmuştu. Göçü basitleştirmek için (ve this yaklaşımı birkaç müşteri tarafından bağımsız olarak kullanıldığı için) diğer alanlara posta birleştirme yeteneği tanıtıldı.

Ne zaman`UseNonMergeFields` ayarlandı`doğru`, Aspose.Words aşağıdaki alanlarda posta birleştirme işlemini gerçekleştirecektir:

MERGEFIELD AlanAdı

MAKRO DÜĞME NOMACRO AlanAdı

EĞER 0 = 0 "{AlanAdı}" ""

Ayrıca, ne zaman`UseNonMergeFields` ayarlandı`doğru`, Aspose.Words, tags "{{fieldName}}" metnine posta birleştirme işlemi yapacaktır. Bunlar alan değil, sadece metin etiketleridir.

### Ayrıca bakınız

* class [MailMergeOptions](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)
