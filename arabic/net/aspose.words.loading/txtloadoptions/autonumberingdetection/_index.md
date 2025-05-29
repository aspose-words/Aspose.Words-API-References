---
title: TxtLoadOptions.AutoNumberingDetection
linktitle: AutoNumberingDetection
articleTitle: AutoNumberingDetection
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية الكشف التلقائي للترقيم في TxtLoadOptions. فعّل أو عطّل الترقيم التلقائي بسهولة لتحميل المستندات بسلاسة. القيمة الافتراضية هي "صحيح".
type: docs
weight: 20
url: /ar/net/aspose.words.loading/txtloadoptions/autonumberingdetection/
---
## TxtLoadOptions.AutoNumberingDetection property

يحصل على قيمة منطقية أو يعينها للإشارة إلى أن الكشف التلقائي عن الترقيم سيتم إجراؤه أثناء تحميل مستند. القيمة الافتراضية هي`حقيقي` .

```csharp
public bool AutoNumberingDetection { get; set; }
```

## أمثلة

يوضح كيفية تعطيل اكتشاف الترقيم التلقائي.

```csharp
TxtLoadOptions options = new TxtLoadOptions { AutoNumberingDetection = false };
Document doc = new Document(MyDir + "Number detection.txt", options);
```

### أنظر أيضا

* class [TxtLoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
