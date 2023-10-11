---
title: TxtLoadOptions.AutoNumberingDetection
second_title: Aspose.Words لمراجع .NET API
description: TxtLoadOptions ملكية. الحصول على قيمة منطقية أو تعيينها تشير إلى أنه سيتم إجراء اكتشاف الترقيم التلقائي أثناء تحميل مستند. القيمة الافتراضية هيحقيقي .
type: docs
weight: 20
url: /ar/net/aspose.words.loading/txtloadoptions/autonumberingdetection/
---
## TxtLoadOptions.AutoNumberingDetection property

الحصول على قيمة منطقية أو تعيينها تشير إلى أنه سيتم إجراء اكتشاف الترقيم التلقائي أثناء تحميل مستند. القيمة الافتراضية هي`حقيقي` .

```csharp
public bool AutoNumberingDetection { get; set; }
```

### أمثلة

يوضح كيفية تعطيل الكشف التلقائي عن الترقيم.

```csharp
TxtLoadOptions options = new TxtLoadOptions { AutoNumberingDetection = false };
Document doc = new Document(MyDir + "Number detection.txt", options);
```

### أنظر أيضا

* class [TxtLoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../txtloadoptions/)
* المجسم [Aspose.Words](../../../)


