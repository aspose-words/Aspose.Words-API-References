---
title: Document.UnlinkFields
linktitle: UnlinkFields
articleTitle: UnlinkFields
second_title: .NET için Aspose.Words
description: Düzenleme iş akışınızı geliştirerek, tüm belgenizdeki alanların bağlantısını etkili bir şekilde kaldırmak için UnlinkFields yöntemini nasıl kullanacağınızı öğrenin.
type: docs
weight: 780
url: /tr/net/aspose.words/document/unlinkfields/
---
## Document.UnlinkFields method

Tüm belgedeki alanların bağlantısını kaldırır.

```csharp
public void UnlinkFields()
```

## Notlar

Belgenin tamamındaki tüm alanları en son sonuçlarıyla değiştirir.

Belgenin belirli bir bölümündeki alanların bağlantısını kaldırmak için şunu kullanın:[`UnlinkFields`](../../range/unlinkfields/).

## Örnekler

Belgedeki tüm alanların bağlantısının nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");

doc.UnlinkFields();
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
