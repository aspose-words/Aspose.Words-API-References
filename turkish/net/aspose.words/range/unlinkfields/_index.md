---
title: Range.UnlinkFields
linktitle: UnlinkFields
articleTitle: UnlinkFields
second_title: .NET için Aspose.Words
description: Belge aralığınızdaki alanların bağlantısını zahmetsizce kaldırmak, iş akışınızı ve belge yönetiminizi geliştirmek için Range UnlinkFields yöntemini keşfedin.
type: docs
weight: 120
url: /tr/net/aspose.words/range/unlinkfields/
---
## Range.UnlinkFields method

Bu aralıktaki alanların bağlantısını kaldırır.

```csharp
public void UnlinkFields()
```

## Notlar

Bu aralıktaki tüm alanları en son sonuçlarıyla değiştirir.

Tüm belgedeki alanların bağlantısını kaldırmak için şunu kullanın:`UnlinkFields`.

## Örnekler

Bir aralıktaki tüm alanların bağlantısının nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");

Section newSection = (Section)doc.Sections[0].Clone(true);
doc.Sections.Add(newSection);

doc.Sections[1].Range.UnlinkFields();
```

### Ayrıca bakınız

* class [Range](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
