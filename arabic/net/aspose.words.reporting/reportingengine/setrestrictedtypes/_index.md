---
title: ReportingEngine.SetRestrictedTypes
linktitle: SetRestrictedTypes
articleTitle: SetRestrictedTypes
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل طريقة SetRestrictedTypes في ReportingEngine على تعزيز الأمان من خلال تقييد وصول الأعضاء في بناء جملة القالب لتحسين تقارير البيانات.
type: docs
weight: 80
url: /ar/net/aspose.words.reporting/reportingengine/setrestrictedtypes/
---
## ReportingEngine.SetRestrictedTypes method

يحدد الأنواع، وأي الأعضاء، وكذلك أعضاء الأنواع المشتقة التي يجب ألا يتمكن engine من الوصول إليها من خلال بناء جملة القالب.

```csharp
public static void SetRestrictedTypes(params Type[] types)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| types | Type[] | الأنواع التي سيتم تقييدها. |

## ملاحظات

يجب تعيين الأنواع المقيدة قبل إنشاء التقرير لأول مرة. بعد`تقرير البناء` عند استدعاء الأمر، لا يمكن تعديل الأنواع المقيدة، ويُطرح استثناء عند محاولة القيام بذلك. أفضل مكان لتعيين الأنواع المقيدة هو بدء تشغيل التطبيق.

لاحظ أن عددًا كبيرًا من الأنواع المقيدة قد يؤثر على الأداء، لذا من الأفضل تقييد تلك الأنواع فقط، حيث يكون الوصول إلى أعضائها حساسًا حقًا.

رمياتArgumentException في الحالات التالية:

-*types* لا شيء.

- واحد من*types* العناصر هي`باطل`.

- واحد من*types* تمثل العناصر نوعًا غير مرئي، أي نوع غير عام أو نوع متداخل عام يحتوي على نوع خارجي غير عام.

- واحد من*types* العناصر تمثل نوع المصفوفة.

-*types* تحتوي على إدخالات مكررة.

## أمثلة

يوضح كيفية رفض الوصول إلى أعضاء الأنواع التي تعتبر غير آمنة.

```csharp
Document doc =
    DocumentHelper.CreateSimpleDocument(
        "<<var [typeVar = \"\".GetType().BaseType]>><<[typeVar]>>");

// لاحظ أنه لا يمكنك تعيين أنواع مقيدة أثناء أو بعد إنشاء تقرير.
ReportingEngine.SetRestrictedTypes(typeof(System.Type));
// لقد قمنا بتعيين خيار "AllowMissingMembers" لتجنب الاستثناءات أثناء بناء التقرير.
ReportingEngine engine = new ReportingEngine() { Options = ReportBuildOptions.AllowMissingMembers };
engine.BuildReport(doc, new object());

// نحصل على سلسلة فارغة لأننا لا نستطيع الوصول إلى طريقة GetType().
Assert.AreEqual(string.Empty, doc.GetText().Trim());
```

### أنظر أيضا

* class [ReportingEngine](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)
