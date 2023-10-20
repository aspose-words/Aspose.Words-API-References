---
title: FontInfoCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words لـ .NET
description: FontInfoCollection Contains طريقة. يحدد ما إذا كانت المجموعة تحتوي على خط بالاسم المحدد في C#.
type: docs
weight: 60
url: /ar/net/aspose.words.fonts/fontinfocollection/contains/
---
## FontInfoCollection.Contains method

يحدد ما إذا كانت المجموعة تحتوي على خط بالاسم المحدد.

```csharp
public bool Contains(string name)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| name | String | اسم الخط الذي سيتم تحديد موقعه غير حساس لحالة الأحرف. |

### قيمة الإرجاع

`حقيقي` إذا تم العثور على العنصر في المجموعة؛ خلاف ذلك،`خطأ شنيع`.

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
