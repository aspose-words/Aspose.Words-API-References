---
title: CustomDocumentProperties Class
linktitle: CustomDocumentProperties
articleTitle: CustomDocumentProperties
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Properties.CustomDocumentProperties لإدارة خصائص المستندات المخصصة بسهولة. حسّن إدارة مستنداتك اليوم!
type: docs
weight: 5190
url: /ar/net/aspose.words.properties/customdocumentproperties/
---
## CustomDocumentProperties class

مجموعة من خصائص المستند المخصصة.

لمعرفة المزيد، قم بزيارة[العمل مع خصائص المستند](https://docs.aspose.com/words/net/work-with-document-properties/) مقالة توثيقية.

```csharp
public class CustomDocumentProperties : DocumentPropertyCollection
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
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add)(*string, bool*) | ينشئ خاصية مستند مخصصة جديدة لـBoolean نوع البيانات. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_3)(*string, DateTime*) | ينشئ خاصية مستند مخصصة جديدة لـDateTime نوع البيانات. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_1)(*string, double*) | ينشئ خاصية مستند مخصصة جديدة لـDouble نوع البيانات. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_2)(*string, int*) | ينشئ خاصية مستند مخصصة جديدة لـNumber نوع البيانات. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_4)(*string, string*) | ينشئ خاصية مستند مخصصة جديدة لـString نوع البيانات. |
| [AddLinkToContent](../../aspose.words.properties/customdocumentproperties/addlinktocontent/)(*string, string*) | ينشئ خاصية مستند مخصصة جديدة مرتبطة بالمحتوى. |
| [Clear](../../aspose.words.properties/documentpropertycollection/clear/)() | يزيل جميع الخصائص من المجموعة. |
| [Contains](../../aspose.words.properties/documentpropertycollection/contains/)(*string*) | إرجاع`حقيقي` إذا كانت هناك خاصية بالاسم المحدد موجودة في المجموعة. |
| [GetEnumerator](../../aspose.words.properties/documentpropertycollection/getenumerator/)() | يعيد كائن عداد يمكن استخدامه للتكرار على جميع العناصر في المجموعة. |
| [IndexOf](../../aspose.words.properties/documentpropertycollection/indexof/)(*string*) | يحصل على فهرس الخاصية حسب الاسم. |
| [Remove](../../aspose.words.properties/documentpropertycollection/remove/)(*string*) | يزيل خاصية بالاسم المحدد من المجموعة. |
| [RemoveAt](../../aspose.words.properties/documentpropertycollection/removeat/)(*int*) | يزيل خاصية عند الفهرس المحدد. |

## ملاحظات

كل[`DocumentProperty`](../documentproperty/) يمثل الكائن خاصية مخصصة لمستند الحاوية.

أسماء الخصائص لا تميز بين الأحرف الكبيرة والصغيرة.

يتم فرز الخصائص الموجودة في المجموعة أبجديًا حسب الاسم.

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

* class [Document](../../aspose.words/document/)
* property [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties/)
* property [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties/)
* class [DocumentPropertyCollection](../documentpropertycollection/)
* مساحة الاسم [Aspose.Words.Properties](../../aspose.words.properties/)
* المجسم [Aspose.Words](../../)
