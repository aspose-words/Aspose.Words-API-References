---
title: List.HasSameTemplate
linktitle: HasSameTemplate
articleTitle: HasSameTemplate
second_title: Aspose.Words för .NET
description: Upptäck HasSameTemplate-metoden, kontrollera enkelt om två listor delar samma mall, vilket säkerställer konsekvens och effektivitet i din datahantering.
type: docs
weight: 120
url: /sv/net/aspose.words.lists/list/hassametemplate/
---
## List.HasSameTemplate method

Returnerar sant om den aktuella listan och den givna listan skapas från samma mall.

```csharp
public bool HasSameTemplate(List other)
```

## Exempel

Visar hur man definierar listor med samma ListDefId.

```csharp
Document doc = new Document(MyDir + "Different lists.docx");

Assert.True(doc.Lists[0].HasSameTemplate(doc.Lists[1]));
Assert.False(doc.Lists[1].HasSameTemplate(doc.Lists[2]));
```

### Se även

* class [List](../)
* namnutrymme [Aspose.Words.Lists](../../../aspose.words.lists/)
* hopsättning [Aspose.Words](../../../)
