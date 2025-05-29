---
title: FontInfoCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words لـ .NET
description: اكتشف ما إذا كانت مجموعة FontInfoCollection تتضمن خطًا معينًا بالاسم. أدر مجموعة خطوطك واحصل على الوصول إليها بسهولة باستخدام هذه الطريقة الأساسية.
type: docs
weight: 60
url: /ar/net/aspose.words.fonts/fontinfocollection/contains/
---
## FontInfoCollection.Contains method

يحدد ما إذا كانت المجموعة تحتوي على خط يحمل الاسم المحدد.

```csharp
public bool Contains(string name)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| name | String | اسم الخط الذي يجب تحديد موقعه دون مراعاة حالة الأحرف. |

### قيمة الإرجاع

`حقيقي`إذا تم العثور على العنصر في المجموعة؛ وإلا،`خطأ شنيع`.

## أمثلة

يعرض معلومات حول الخطوط الموجودة في المستند الفارغ.

```csharp
Document doc = new Document();

// يحتوي المستند الفارغ على ثلاثة خطوط افتراضية. كل خط في المستند
//سيكون هناك كائن FontInfo مطابق يحتوي على تفاصيل حول هذا الخط.
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
