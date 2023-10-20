---
title: BuiltInDocumentProperties.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words لـ .NET
description: BuiltInDocumentProperties Item ملكية. إرجاع أDocumentProperty كائن باسم الخاصية في C#.
type: docs
weight: 130
url: /ar/net/aspose.words.properties/builtindocumentproperties/item/
---
## BuiltInDocumentProperties indexer

إرجاع أ[`DocumentProperty`](../../documentproperty/) كائن باسم الخاصية.

```csharp
public override DocumentProperty this[string name] { get; }
```

| معامل | وصف |
| --- | --- |
| name | اسم الخاصية غير حساس لحالة الأحرف المراد استرداده. |

## ملاحظات

تتوافق أسماء سلسلة الخصائص مع أسماء الخصائص typed المتوفرة منها[`BuiltInDocumentProperties`](../).

إذا طلبت خاصية غير موجودة في المستند، ولكن تم التعرف على name الخاص بالخاصية كاسم مدمج صالح، فستتم إضافة اسم جديد[`DocumentProperty`](../../documentproperty/) يتم إنشاء وإضافته إلى المجموعة وإعادته. تم تعيين الخاصية التي تم إنشاؤها حديثًا كقيمة افتراضية (سلسلة فارغة، صفر،`خطأ شنيع` أو DateTime.MinValue اعتمادًا على نوع الخاص بالخاصية المضمنة).

إذا طلبت خاصية غير موجودة في المستند ولم يتم التعرف على name كاسم مضمن،`باطل` يتم إرجاع.

## أمثلة

يوضح كيفية العمل مع خصائص المستند المخصصة.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// يحتوي كل مستند على مجموعة من الخصائص المخصصة، والتي، مثل الخصائص المضمنة، هي أزواج قيمة المفتاح.
 // يحتوي المستند على قائمة ثابتة بالخصائص المضمنة. يقوم المستخدم بإنشاء كافة الخصائص المخصصة.
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
