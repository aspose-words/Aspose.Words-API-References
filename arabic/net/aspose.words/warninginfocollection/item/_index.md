---
title: WarningInfoCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words لـ .NET
description: يمكنك الوصول بسهولة إلى عناصر WarningInfoCollection المحددة من خلال الفهرس. سهّل إدارة بياناتك مع ميزة الخصائص البديهية لدينا!
type: docs
weight: 30
url: /ar/net/aspose.words/warninginfocollection/item/
---
## WarningInfoCollection indexer

يحصل على عنصر في الفهرس المحدد.

```csharp
public WarningInfo this[int index] { get; }
```

| معامل | وصف |
| --- | --- |
| index | مؤشر يعتمد على الصفر للعنصر. |

## أمثلة

يوضح كيفية الحصول على تحذيرات حول التنسيقات غير المدعومة.

```csharp
WarningInfoCollection warnings = new WarningInfoCollection();
Document doc = new Document(MyDir + "FB2 document.fb2", new LoadOptions { WarningCallback = warnings });

Assert.AreEqual("The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warnings[0].Description);
Assert.AreEqual(1, warnings.Count);
```

### أنظر أيضا

* class [WarningInfo](../../warninginfo/)
* class [WarningInfoCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
