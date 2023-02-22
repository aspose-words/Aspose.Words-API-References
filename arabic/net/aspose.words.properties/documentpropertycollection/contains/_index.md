---
title: DocumentPropertyCollection.Contains
second_title: Aspose.Words لمراجع .NET API
description: DocumentPropertyCollection طريقة. إرجاع صحيح في حالة وجود خاصية بالاسم المحدد في المجموعة.
type: docs
weight: 40
url: /ar/net/aspose.words.properties/documentpropertycollection/contains/
---
## DocumentPropertyCollection.Contains method

إرجاع صحيح في حالة وجود خاصية بالاسم المحدد في المجموعة.

```csharp
public bool Contains(string name)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| name | String | الاسم غير المتحسس لحالة الأحرف للممتلكات. |

### قيمة الإرجاع

صحيح إذا كانت الخاصية موجودة في المجموعة ؛ خطأ خلاف ذلك.

### أمثلة

يوضح كيفية التعامل مع الخصائص المخصصة للمستند.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// خصائص المستند المخصصة هي أزواج ذات قيمة رئيسية يمكننا إضافتها إلى المستند.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// تقوم المجموعة بفرز الخصائص المخصصة بترتيب أبجدي.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// طباعة كل خاصية مخصصة في المستند.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// عرض قيمة خاصية مخصصة باستخدام حقل DOCPROPERTY.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// يمكننا العثور على هذه الخصائص المخصصة في Microsoft Word عبر "ملف" - >; "خصائص" >. "خصائص متقدمة" >. "العادة".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// فيما يلي ثلاث طرق أو إزالة الخصائص المخصصة من مستند.
// 1 - إزالة حسب الفهرس:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - إزالة بالاسم:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - إفراغ المجموعة بأكملها مرة واحدة:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### أنظر أيضا

* class [DocumentPropertyCollection](../)
* مساحة الاسم [Aspose.Words.Properties](../../documentpropertycollection/)
* المجسم [Aspose.Words](../../../)


