---
title: DocumentPropertyCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words لـ .NET
description: اكتشف وجود خاصية في DocumentPropertyCollection باستخدام طريقة Contains الفعّالة. بسّط إدارة بياناتك اليوم!
type: docs
weight: 40
url: /ar/net/aspose.words.properties/documentpropertycollection/contains/
---
## DocumentPropertyCollection.Contains method

إرجاع`حقيقي` إذا كانت هناك خاصية بالاسم المحدد موجودة في المجموعة.

```csharp
public bool Contains(string name)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| name | String | اسم الخاصية غير حساس لحالة الأحرف. |

### قيمة الإرجاع

`حقيقي` إذا كانت الملكية موجودة في المجموعة؛`خطأ شنيع` خلاف ذلك.

## أمثلة

يوضح كيفية العمل مع خصائص المستند المخصصة.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// خصائص المستند المخصصة هي أزواج مفتاح-قيمة يمكننا إضافتها إلى المستند.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// تقوم المجموعة بفرز الخصائص المخصصة حسب الترتيب الأبجدي.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

//طباعة كل خاصية مخصصة في المستند.
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

// يمكننا العثور على هذه الخصائص المخصصة في Microsoft Word عبر "ملف" -> "خصائص" > "خصائص متقدمة" > "مخصص".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// فيما يلي ثلاث طرق لإزالة الخصائص المخصصة من المستند.
// 1 - الإزالة حسب الفهرس:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - إزالة حسب الاسم:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - إفراغ المجموعة بأكملها مرة واحدة:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### أنظر أيضا

* class [DocumentPropertyCollection](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)
