---
title: CustomDocumentProperties Class
linktitle: CustomDocumentProperties
articleTitle: CustomDocumentProperties
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Properties.CustomDocumentProperties فصل. مجموعة من خصائص المستند المخصصة في C#.
type: docs
weight: 4460
url: /ar/net/aspose.words.properties/customdocumentproperties/
---
## CustomDocumentProperties class

مجموعة من خصائص المستند المخصصة.

لمعرفة المزيد، قم بزيارة[العمل مع خصائص الوثيقة](https://docs.aspose.com/words/net/work-with-document-properties/) مقالة توثيقية.

```csharp
public class CustomDocumentProperties : DocumentPropertyCollection
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
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add)(*string, bool*) | إنشاء خاصية مستند مخصصة جديدة لـBoolean نوع البيانات. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_3)(*string, DateTime*) | إنشاء خاصية مستند مخصصة جديدة لـDateTime نوع البيانات. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_1)(*string, double*) | إنشاء خاصية مستند مخصصة جديدة لـDouble نوع البيانات. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_2)(*string, int*) | إنشاء خاصية مستند مخصصة جديدة لـNumber نوع البيانات. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_4)(*string, string*) | إنشاء خاصية مستند مخصصة جديدة لـString نوع البيانات. |
| [AddLinkToContent](../../aspose.words.properties/customdocumentproperties/addlinktocontent/)(*string, string*) | إنشاء خاصية وثيقة مخصصة جديدة مرتبطة بالمحتوى. |
| [Clear](../../aspose.words.properties/documentpropertycollection/clear/)() | إزالة كافة الخصائص من المجموعة. |
| [Contains](../../aspose.words.properties/documentpropertycollection/contains/)(*string*) | إرجاع`حقيقي` في حالة وجود خاصية بالاسم المحدد في المجموعة. |
| [GetEnumerator](../../aspose.words.properties/documentpropertycollection/getenumerator/)() | إرجاع كائن العداد الذي يمكن استخدامه للتكرار على كافة العناصر الموجودة في المجموعة. |
| [IndexOf](../../aspose.words.properties/documentpropertycollection/indexof/)(*string*) | الحصول على فهرس الخاصية بالاسم. |
| [Remove](../../aspose.words.properties/documentpropertycollection/remove/)(*string*) | إزالة خاصية بالاسم المحدد من المجموعة. |
| [RemoveAt](../../aspose.words.properties/documentpropertycollection/removeat/)(*int*) | إزالة خاصية في الفهرس المحدد. |

## ملاحظات

كل[`DocumentProperty`](../documentproperty/) يمثل الكائن خاصية مخصصة لمستند الحاوية.

أسماء الخصائص غير حساسة لحالة الأحرف.

يتم فرز الخصائص الموجودة في المجموعة أبجديًا حسب الاسم.

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

* class [Document](../../aspose.words/document/)
* property [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties/)
* property [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties/)
* class [DocumentPropertyCollection](../documentpropertycollection/)
* مساحة الاسم [Aspose.Words.Properties](../../aspose.words.properties/)
* المجسم [Aspose.Words](../../)
