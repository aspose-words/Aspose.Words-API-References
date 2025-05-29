---
title: Metered.GetProductName
linktitle: GetProductName
articleTitle: GetProductName
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة Metered GetProductName لاسترداد أسماء المنتجات بسهولة، مما يعزز كفاءة تطبيقك وتجربة المستخدم.
type: docs
weight: 20
url: /ar/net/aspose.words/metered/getproductname/
---
## Metered.GetProductName method

إرجاع اسم المنتج

```csharp
public string GetProductName()
```

### قيمة الإرجاع

اسم المنتج

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
