---
title: Metered.SetMeteredKey
second_title: Aspose.Words لمراجع .NET API
description: Metered طريقة. يعين المفتاح العام والخاص. إذا قمت بشراء ترخيص مقنن عند بدء التطبيق يجب استدعاء واجهة برمجة التطبيقات هذه عادةً وهذا يكفي. ومع ذلك إذا فشلت دائمًا في تحميل بيانات الاستهلاك وتجاوزت 24 ساعة فسيتم ضبط الترخيص على حالة التقييم لتجنب مثل هذه الحالة يجب عليك التحقق بانتظام من حالة الترخيص إذا كانت حالة التقييم فاتصل بواجهة برمجة التطبيقات هذه مرة أخرى.
type: docs
weight: 20
url: /ar/net/aspose.words/metered/setmeteredkey/
---
## Metered.SetMeteredKey method

يعين المفتاح العام والخاص. إذا قمت بشراء ترخيص مقنن، عند بدء التطبيق، يجب استدعاء واجهة برمجة التطبيقات هذه، عادةً، وهذا يكفي. ومع ذلك، إذا فشلت دائمًا في تحميل بيانات الاستهلاك وتجاوزت 24 ساعة، فسيتم ضبط الترخيص على حالة التقييم، لتجنب مثل هذه الحالة، يجب عليك التحقق بانتظام من حالة الترخيص، إذا كانت حالة التقييم، فاتصل بواجهة برمجة التطبيقات هذه مرة أخرى.

```csharp
public void SetMeteredKey(string publicKey, string privateKey)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| publicKey | String | المفتاح العمومي |
| privateKey | String | مفتاح سري |

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


