---
title: Class DocumentPropertyCollection
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Properties.DocumentPropertyCollection فصل. الفئة الأساسية لـBuiltInDocumentProperties وCustomDocumentProperties المجموعات.
type: docs
weight: 4480
url: /ar/net/aspose.words.properties/documentpropertycollection/
---
## DocumentPropertyCollection class

الفئة الأساسية لـ[`BuiltInDocumentProperties`](../builtindocumentproperties/) و[`CustomDocumentProperties`](../customdocumentproperties/) المجموعات.

لمعرفة المزيد، قم بزيارة[العمل مع خصائص الوثيقة](https://docs.aspose.com/words/net/work-with-document-properties/) مقالة توثيقية.

```csharp
public abstract class DocumentPropertyCollection : IEnumerable<DocumentProperty>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.properties/documentpropertycollection/count/) { get; } | الحصول على عدد العناصر الموجودة في المجموعة. |
| [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | إرجاع أ[`DocumentProperty`](../documentproperty/) كائن حسب الفهرس. |
| virtual [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | إرجاع أ[`DocumentProperty`](../documentproperty/) كائن باسم الخاصية. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Clear](../../aspose.words.properties/documentpropertycollection/clear/)() | إزالة كافة الخصائص من المجموعة. |
| [Contains](../../aspose.words.properties/documentpropertycollection/contains/)(string) | إرجاع`حقيقي` في حالة وجود خاصية بالاسم المحدد في المجموعة. |
| [GetEnumerator](../../aspose.words.properties/documentpropertycollection/getenumerator/)() | إرجاع كائن العداد الذي يمكن استخدامه للتكرار على كافة العناصر الموجودة في المجموعة. |
| [IndexOf](../../aspose.words.properties/documentpropertycollection/indexof/)(string) | الحصول على فهرس الخاصية بالاسم. |
| [Remove](../../aspose.words.properties/documentpropertycollection/remove/)(string) | إزالة خاصية بالاسم المحدد من المجموعة. |
| [RemoveAt](../../aspose.words.properties/documentpropertycollection/removeat/)(int) | إزالة خاصية في الفهرس المحدد. |

### ملاحظات

أسماء الخصائص غير حساسة لحالة الأحرف.

يتم فرز الخصائص الموجودة في المجموعة أبجديًا حسب الاسم.

### أمثلة

يوضح كيفية التعامل مع الخصائص المخصصة للمستند.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// خصائص المستند المخصصة هي أزواج ذات قيمة أساسية يمكننا إضافتها إلى المستند.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// تقوم المجموعة بفرز الخصائص المخصصة بالترتيب الأبجدي.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// اطبع كل خاصية مخصصة في المستند.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// اعرض قيمة الخاصية المخصصة باستخدام حقل DOCPROPERTY.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// يمكننا العثور على هذه الخصائص المخصصة في Microsoft Word عبر "ملف" -> "الخصائص" > "خصائص متقدمة" > "مخصص".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// فيما يلي ثلاث طرق لإزالة الخصائص المخصصة من المستند.
// 1 - الإزالة حسب الفهرس:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - الإزالة بالاسم:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - إفراغ المجموعة بأكملها مرة واحدة:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### أنظر أيضا

* class [BuiltInDocumentProperties](../builtindocumentproperties/)
* class [CustomDocumentProperties](../customdocumentproperties/)
* class [DocumentProperty](../documentproperty/)
* مساحة الاسم [Aspose.Words.Properties](../../aspose.words.properties/)
* المجسم [Aspose.Words](../../)


