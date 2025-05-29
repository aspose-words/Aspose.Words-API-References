---
title: DocumentPropertyCollection Class
linktitle: DocumentPropertyCollection
articleTitle: DocumentPropertyCollection
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Properties.DocumentPropertyCollection، وهي وجهتك المفضلة لإدارة خصائص المستندات المضمنة والمخصصة بكفاءة.
type: docs
weight: 5210
url: /ar/net/aspose.words.properties/documentpropertycollection/
---
## DocumentPropertyCollection class

الفئة الأساسية لـ[`BuiltInDocumentProperties`](../builtindocumentproperties/) و[`CustomDocumentProperties`](../customdocumentproperties/) المجموعات.

لمعرفة المزيد، قم بزيارة[العمل مع خصائص المستند](https://docs.aspose.com/words/net/work-with-document-properties/) مقالة توثيقية.

```csharp
public abstract class DocumentPropertyCollection : IEnumerable<DocumentProperty>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.properties/documentpropertycollection/count/) { get; } | يحصل على عدد العناصر في المجموعة. |
| [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | يعيد[`DocumentProperty`](../documentproperty/) الكائن حسب index. |
| virtual [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | يعيد[`DocumentProperty`](../documentproperty/) الكائن حسب اسم الخاصية. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Clear](../../aspose.words.properties/documentpropertycollection/clear/)() | يزيل جميع الخصائص من المجموعة. |
| [Contains](../../aspose.words.properties/documentpropertycollection/contains/)(*string*) | إرجاع`حقيقي` إذا كانت هناك خاصية بالاسم المحدد موجودة في المجموعة. |
| [GetEnumerator](../../aspose.words.properties/documentpropertycollection/getenumerator/)() | يعيد كائن عداد يمكن استخدامه للتكرار على جميع العناصر في المجموعة. |
| [IndexOf](../../aspose.words.properties/documentpropertycollection/indexof/)(*string*) | يحصل على فهرس الخاصية حسب الاسم. |
| [Remove](../../aspose.words.properties/documentpropertycollection/remove/)(*string*) | يزيل خاصية بالاسم المحدد من المجموعة. |
| [RemoveAt](../../aspose.words.properties/documentpropertycollection/removeat/)(*int*) | يزيل خاصية عند الفهرس المحدد. |

## ملاحظات

أسماء الخصائص لا تميز بين الأحرف الكبيرة والصغيرة.

يتم فرز الخصائص الموجودة في المجموعة أبجديًا حسب الاسم.

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

* class [BuiltInDocumentProperties](../builtindocumentproperties/)
* class [CustomDocumentProperties](../customdocumentproperties/)
* class [DocumentProperty](../documentproperty/)
* مساحة الاسم [Aspose.Words.Properties](../../aspose.words.properties/)
* المجسم [Aspose.Words](../../)
