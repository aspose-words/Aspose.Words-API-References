---
title: Enum PropertyType
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Properties.PropertyType تعداد. يحدد نوع البيانات لخاصية المستند .
type: docs
weight: 4250
url: /ar/net/aspose.words.properties/propertytype/
---
## PropertyType enumeration

يحدد نوع البيانات لخاصية المستند .

```csharp
public enum PropertyType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Boolean | `0` | الخاصية هي قيمة منطقية . |
| DateTime | `1` | الخاصية هي قيمة وقت للتاريخ . |
| Double | `2` | الخاصية هي رقم عائم . |
| Number | `3` | الخاصية هي رقم صحيح . |
| String | `4` | الخاصية هي قيمة سلسلة . |
| StringArray | `5` | الخاصية عبارة عن مصفوفة من السلاسل . |
| ObjectArray | `6` | الخاصية عبارة عن مصفوفة من الكائنات . |
| ByteArray | `7` | الخاصية عبارة عن مصفوفة من البايت. |
| Other | `8` | الخاصية هي نوع آخر . |

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

* class [DocumentProperty](../documentproperty/)
* property [Type](../documentproperty/type/)
* مساحة الاسم [Aspose.Words.Properties](../../aspose.words.properties/)
* المجسم [Aspose.Words](../../)


