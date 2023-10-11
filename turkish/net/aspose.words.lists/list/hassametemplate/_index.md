---
title: List.HasSameTemplate
second_title: Aspose.Words for .NET API Referansı
description: List yöntem. Geçerli liste ile verilen liste aynı şablondan oluşturulmuşsa true değerini döndürür.
type: docs
weight: 120
url: /tr/net/aspose.words.lists/list/hassametemplate/
---
## List.HasSameTemplate method

Geçerli liste ile verilen liste aynı şablondan oluşturulmuşsa true değerini döndürür.

```csharp
public bool HasSameTemplate(List other)
```

### Örnekler

Aynı ListDefId'ye sahip listelerin nasıl tanımlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Different lists.docx");

Assert.True(doc.Lists[0].HasSameTemplate(doc.Lists[1]));
Assert.False(doc.Lists[1].HasSameTemplate(doc.Lists[2]));
```

### Ayrıca bakınız

* class [List](../)
* ad alanı [Aspose.Words.Lists](../../list/)
* toplantı [Aspose.Words](../../../)


