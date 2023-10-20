---
title: Metered Class
linktitle: Metered
articleTitle: Metered
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Metered فصل. يوفر طرقًا لتعيين المفتاح المقنن في C#.
type: docs
weight: 4160
url: /ar/net/aspose.words/metered/
---
## Metered class

يوفر طرقًا لتعيين المفتاح المقنن.

لمعرفة المزيد، قم بزيارة[الترخيص والاشتراك](https://docs.aspose.com/words/net/licensing/) مقالة توثيقية.

```csharp
public class Metered
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [Metered](metered/)() | تهيئة مثيل جديد لهذه الفئة. |

## طُرق

| اسم | وصف |
| --- | --- |
| [SetMeteredKey](../../aspose.words/metered/setmeteredkey/)(*string, string*) | يعين المفتاح العام والخاص. إذا قمت بشراء ترخيص مقنن، عند بدء التطبيق، يجب استدعاء واجهة برمجة التطبيقات هذه، عادةً، وهذا يكفي. ومع ذلك، إذا فشلت دائمًا في تحميل بيانات الاستهلاك وتجاوزت 24 ساعة، فسيتم ضبط الترخيص على حالة التقييم، لتجنب مثل هذه الحالة، يجب عليك التحقق بانتظام من حالة الترخيص، إذا كانت حالة التقييم، فاتصل بواجهة برمجة التطبيقات هذه مرة أخرى. |
| static [GetConsumptionCredit](../../aspose.words/metered/getconsumptioncredit/)() | يحصل على رصيد الاستهلاك |
| static [GetConsumptionQuantity](../../aspose.words/metered/getconsumptionquantity/)() | الحصول على حجم ملف الاستهلاك |

## أمثلة

في هذا المثال، سيتم إجراء محاولة لتعيين المفتاح العام والخاص المحدود

```csharp
[C#]

Metered matered = new Metered();
matered.SetMeteredKey("PublicKey", "PrivateKey");


[Visual Basic]

Dim matered As Metered = New Metered
matered.SetMeteredKey("PublicKey", "PrivateKey")
```

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
