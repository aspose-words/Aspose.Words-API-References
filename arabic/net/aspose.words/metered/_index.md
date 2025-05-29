---
title: Metered Class
linktitle: Metered
articleTitle: Metered
second_title: Aspose.Words لـ .NET
description: أطلق العنان لقوة فئة Aspose.Words.Metered! أدر مفتاحك المقياس بسهولة باستخدام أساليب فعّالة لمعالجة مستنداتك بسلاسة.
type: docs
weight: 4850
url: /ar/net/aspose.words/metered/
---
## Metered class

يوفر طرقًا لتعيين المفتاح المقاس.

```csharp
public class Metered
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [Metered](metered/)() | يقوم بتهيئة مثيل جديد لهذه الفئة. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetProductName](../../aspose.words/metered/getproductname/)() | إرجاع اسم المنتج |
| [SetMeteredKey](../../aspose.words/metered/setmeteredkey/)(*string, string*) | يحدد المفتاح العام والخاص المقاس. إذا قمت بشراء ترخيص مقاس، عند بدء التطبيق، يجب استدعاء واجهة برمجة التطبيقات هذه، وعادةً ما يكون هذا كافيًا. ومع ذلك، إذا فشل دائمًا في تحميل بيانات الاستهلاك وتجاوز 24 ساعة، فسيتم تعيين الترخيص على حالة التقييم، لتجنب مثل هذه الحالة، يجب عليك التحقق بانتظام من حالة الترخيص، إذا كانت حالة التقييم، فاتصل بهذه الواجهة مرة أخرى. |
| static [GetConsumptionCredit](../../aspose.words/metered/getconsumptioncredit/)() | يحصل على رصيد الاستهلاك |
| static [GetConsumptionQuantity](../../aspose.words/metered/getconsumptionquantity/)() | يحصل على حجم ملف الاستهلاك |
| static [IsMeteredLicensed](../../aspose.words/metered/ismeteredlicensed/)() | تحقق مما إذا كان القياس مرخصًا |

## أمثلة

في هذا المثال، سيتم إجراء محاولة لتعيين مفتاح عام وخاص مقيس

```csharp
[C#]

Metered matered = new Metered();
matered.SetMeteredKey("PublicKey", "PrivateKey");


[Visual Basic]

Dim matered As Metered = New Metered
matered.SetMeteredKey("PublicKey", "PrivateKey")
```

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
