---
title: Metered.SetMeteredKey
linktitle: SetMeteredKey
articleTitle: SetMeteredKey
second_title: Aspose.Words لـ .NET
description: أدر ترخيصك المقنن بسهولة باستخدام طريقة SetMeteredKey. اضمن تحميل البيانات بسلاسة وتجنب حالات التقييم من خلال عمليات الفحص الدورية.
type: docs
weight: 30
url: /ar/net/aspose.words/metered/setmeteredkey/
---
## Metered.SetMeteredKey method

يحدد المفتاح العام والخاص المقاس. إذا قمت بشراء ترخيص مقاس، عند بدء التطبيق، يجب استدعاء واجهة برمجة التطبيقات هذه، وعادةً ما يكون هذا كافيًا. ومع ذلك، إذا فشل دائمًا في تحميل بيانات الاستهلاك وتجاوز 24 ساعة، فسيتم تعيين الترخيص على حالة التقييم، لتجنب مثل هذه الحالة، يجب عليك التحقق بانتظام من حالة الترخيص، إذا كانت حالة التقييم، فاتصل بهذه الواجهة مرة أخرى.

```csharp
public void SetMeteredKey(string publicKey, string privateKey)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| publicKey | String | المفتاح العام |
| privateKey | String | مفتاح خاص |

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
