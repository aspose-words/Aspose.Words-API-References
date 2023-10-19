---
title: List.HasSameTemplate
linktitle: HasSameTemplate
articleTitle: HasSameTemplate
second_title: Aspose.Words for .NET
description: List HasSameTemplate yöntem. Geçerli liste ile verilen liste aynı şablondan oluşturulmuşsa true değerini döndürür C#'da.
type: docs
weight: 120
url: /tr/net/aspose.words.lists/list/hassametemplate/
---
## List.HasSameTemplate method

Geçerli liste ile verilen liste aynı şablondan oluşturulmuşsa true değerini döndürür.

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
