---
title: BuiltInDocumentProperties.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words لـ .NET
description: الوصول إلى كائنات DocumentProperty بسهولة باستخدام خاصية BuiltInDocumentProperties. سهّل إدارة مستنداتك اليوم!
type: docs
weight: 140
url: /ar/net/aspose.words.properties/builtindocumentproperties/item/
---
## BuiltInDocumentProperties indexer

يعيد[`DocumentProperty`](../../documentproperty/) الكائن حسب اسم الخاصية.

```csharp
public override DocumentProperty this[string name] { get; }
```

| معامل | وصف |
| --- | --- |
| name | الاسم غير الحساس لحالة الأحرف للخاصية التي سيتم استردادها. |

## ملاحظات

أسماء سلسلة الخصائص تتوافق مع أسماء خصائص typed المتوفرة من[`BuiltInDocumentProperties`](../).

إذا طلبت خاصية غير موجودة في المستند، ولكن تم التعرف على اسم الخاصية كاسم مدمج صالح، فسيتم إنشاء ملف جديد[`DocumentProperty`](../../documentproperty/) تم إنشاء وإضافته إلى المجموعة وإعادته. تم تعيين قيمة افتراضية للخاصية المُنشأة حديثًا (سلسلة فارغة، صفر،`خطأ شنيع` أو DateTime.MinValue اعتمادًا على type للخاصية المضمنة).

إذا طلبت خاصية غير موجودة في المستند ولم يتم التعرف على name كاسم مضمن،`باطل` تم إرجاعه.

## أمثلة

يوضح كيفية العمل مع خصائص المستند المخصصة.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// تحتوي كل مستند على مجموعة من الخصائص المخصصة، والتي، مثل الخصائص المضمنة، عبارة عن أزواج من القيمة الأساسية.
 // تحتوي الوثيقة على قائمة ثابتة من الخصائص المضمنة. يُنشئ المستخدم جميع الخصائص المخصصة.
Assert.AreEqual("Value of custom document property", doc.CustomDocumentProperties["CustomProperty"].ToString());

doc.CustomDocumentProperties.Add("CustomProperty2", "Value of custom document property #2");

Console.WriteLine("Custom Properties:");
foreach (var customDocumentProperty in doc.CustomDocumentProperties)
{
    Console.WriteLine(customDocumentProperty.Name);
    Console.WriteLine($"\tType:\t{customDocumentProperty.Type}");
    Console.WriteLine($"\tValue:\t\"{customDocumentProperty.Value}\"");
}
```

### أنظر أيضا

* class [DocumentProperty](../../documentproperty/)
* class [BuiltInDocumentProperties](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)
