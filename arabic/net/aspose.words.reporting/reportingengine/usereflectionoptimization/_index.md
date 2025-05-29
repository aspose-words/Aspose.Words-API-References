---
title: ReportingEngine.UseReflectionOptimization
linktitle: UseReflectionOptimization
articleTitle: UseReflectionOptimization
second_title: Aspose.Words لـ .NET
description: حسّن استدعاءات عناصر النوع المخصص باستخدام خاصية UseReflectionOptimization في ReportingEngine. حسّن الأداء من خلال إنشاء فئات ديناميكية لتحقيق كفاءة أعلى.
type: docs
weight: 60
url: /ar/net/aspose.words.reporting/reportingengine/usereflectionoptimization/
---
## ReportingEngine.UseReflectionOptimization property

يحصل على قيمة أو يعيّنها لتحديد ما إذا كانت استدعاءات عناصر النوع المخصص التي تُجرى عبر واجهة برمجة تطبيقات الانعكاس مُحسّنة باستخدام توليد الفئات الديناميكي أم لا. القيمة الافتراضية هي`حقيقي` .

```csharp
public static bool UseReflectionOptimization { get; set; }
```

## ملاحظات

هناك بعض السيناريوهات التي يُفضّل فيها تعطيل هذا التحسين. على سبيل المثال، إذا كنت تتعامل مع مجموعات صغيرة من عناصر البيانات باستمرار، فقد تكون تكلفة إنشاء الفئات الديناميكية أكبر من تكلفة استدعاءات واجهة برمجة التطبيقات للانعكاس المباشر. لا يؤثر هذا الخيار على نظام iOS عند عدم استخدام تحسين الانعكاس.

### أنظر أيضا

* class [ReportingEngine](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)
