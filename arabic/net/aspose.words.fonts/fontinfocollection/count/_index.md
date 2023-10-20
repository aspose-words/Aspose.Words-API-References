---
title: FontInfoCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words لـ .NET
description: FontInfoCollection Count ملكية. الحصول على عدد العناصر الموجودة في المجموعة في C#.
type: docs
weight: 10
url: /ar/net/aspose.words.fonts/fontinfocollection/count/
---
## FontInfoCollection.Count property

الحصول على عدد العناصر الموجودة في المجموعة.

```csharp
public int Count { get; }
```

## أمثلة

يعرض معلومات حول الخطوط الموجودة في المستند الفارغ.

```csharp
Document doc = new Document();

// يحتوي المستند الفارغ على 3 خطوط افتراضية. كل خط في الوثيقة
// سيكون له كائن FontInfo المطابق الذي يحتوي على تفاصيل حول هذا الخط.
Assert.AreEqual(3, doc.FontInfos.Count);

Assert.True(doc.FontInfos.Contains("Times New Roman"));
Assert.AreEqual(204, doc.FontInfos["Times New Roman"].Charset);

Assert.True(doc.FontInfos.Contains("Symbol"));
Assert.True(doc.FontInfos.Contains("Arial"));
```

### أنظر أيضا

* class [FontInfoCollection](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
