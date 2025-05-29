---
title: List.HasSameTemplate
linktitle: HasSameTemplate
articleTitle: HasSameTemplate
second_title: .NET için Aspose.Words
description: HasSameTemplate metodunu keşfedin, iki listenin aynı şablonu paylaşıp paylaşmadığını kolayca kontrol edin, veri yönetiminizde tutarlılığı ve verimliliği garantileyin.
type: docs
weight: 120
url: /tr/net/aspose.words.lists/list/hassametemplate/
---
## List.HasSameTemplate method

Mevcut liste ve verilen liste aynı şablondan oluşturulmuşsa doğru değerini döndürür.

```csharp
public bool HasSameTemplate(List other)
```

## Örnekler

Aynı ListDefId'ye sahip listelerin nasıl tanımlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Different lists.docx");

Assert.True(doc.Lists[0].HasSameTemplate(doc.Lists[1]));
Assert.False(doc.Lists[1].HasSameTemplate(doc.Lists[2]));
```

### Ayrıca bakınız

* class [List](../)
* ad alanı [Aspose.Words.Lists](../../../aspose.words.lists/)
* toplantı [Aspose.Words](../../../)
