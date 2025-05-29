---
title: Metered.GetConsumptionCredit
linktitle: GetConsumptionCredit
articleTitle: GetConsumptionCredit
second_title: Aspose.Words لـ .NET
description: احصل على المدخرات باستخدام طريقة Metered GetConsumptionCredit - استرد أرصدة استهلاكك بكفاءة لإدارة الطاقة بشكل أكثر ذكاءً.
type: docs
weight: 40
url: /ar/net/aspose.words/metered/getconsumptioncredit/
---
## Metered.GetConsumptionCredit method

يحصل على رصيد الاستهلاك

```csharp
public static decimal GetConsumptionCredit()
```

### قيمة الإرجاع

كمية الاستهلاك

## أمثلة

يوضح كيفية تنشيط ترخيص مقيس وتتبع الائتمان/الاستهلاك.

```csharp
// قم بإنشاء ترخيص مقنن جديد، ثم اطبع إحصائيات الاستخدام الخاصة به.
Metered metered = new Metered();
metered.SetMeteredKey("MyPublicKey", "MyPrivateKey");

Console.WriteLine($"Is metered license accepted: {Metered.IsMeteredLicensed()}");
Console.WriteLine($"Product name: {metered.GetProductName()}");
Console.WriteLine($"Credit before operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

// قم بالعمل باستخدام Aspose.Words، ثم قم بطباعة إحصائياتنا المقاسة مرة أخرى لمعرفة المبلغ الذي أنفقناه.
Document doc = new Document(MyDir + "Document.docx");
doc.Save(ArtifactsDir + "Metered.Usage.pdf");

// لا تقوم آلية ترخيص Aspose Metered بإرسال بيانات الاستخدام إلى خادم الشراء في كل مرة،
//يجب عليك استخدام الانتظار.
System.Threading.Thread.Sleep(10000);

Console.WriteLine($"Credit after operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity after operation: {Metered.GetConsumptionQuantity()}");
```

### أنظر أيضا

* class [Metered](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
