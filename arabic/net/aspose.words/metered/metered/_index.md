---
title: Metered.Metered
second_title: Aspose.Words لمراجع .NET API
description: Metered البناء. تهيئة مثيل جديد لهذه الفئة.
type: docs
weight: 10
url: /ar/net/aspose.words/metered/metered/
---
## Metered constructor

تهيئة مثيل جديد لهذه الفئة.

```csharp
public Metered()
```

### أمثلة

يوضح كيفية تفعيل الترخيص المقنن وتتبع الرصيد/الاستهلاك.

```csharp
// أنشئ ترخيصًا محدودًا جديدًا، ثم اطبع إحصائيات الاستخدام الخاصة به.
Metered metered = new Metered();
metered.SetMeteredKey("MyPublicKey", "MyPrivateKey");

Console.WriteLine($"Credit before operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

// قم بالتشغيل باستخدام Aspose.Words، ثم قم بطباعة الإحصائيات المقاسة لدينا مرة أخرى لمعرفة المبلغ الذي أنفقناه.
Document doc = new Document(MyDir + "Document.docx");
doc.Save(ArtifactsDir + "Metered.Usage.pdf");

// لا تقوم آلية الترخيص المقننة بإرسال بيانات الاستخدام لشراء الخادم في كل مرة،
// تحتاج إلى استخدام الانتظار.
System.Threading.Thread.Sleep(10000);

Console.WriteLine($"Credit after operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity after operation: {Metered.GetConsumptionQuantity()}");
```

### أنظر أيضا

* class [Metered](../)
* مساحة الاسم [Aspose.Words](../../metered/)
* المجسم [Aspose.Words](../../../)


