---
title: StructuredDocumentTagCollection Class
linktitle: StructuredDocumentTagCollection
articleTitle: StructuredDocumentTagCollection
second_title: Aspose.Words لـ .NET
description: استكشف فئة Aspose.Words.Markup.StructuredDocumentTagCollection لإدارة علامات المستندات المنظمة بكفاءة، مما يعزز قدرات معالجة المستندات لديك.
type: docs
weight: 4760
url: /ar/net/aspose.words.markup/structureddocumenttagcollection/
---
## StructuredDocumentTagCollection class

مجموعة من[`IStructuredDocumentTag`](../istructureddocumenttag/) الحالات التي تمثل علامات المستند المنظمة في النطاق المحدد.

لمعرفة المزيد، قم بزيارة[علامات المستند المنظم أو التحكم في المحتوى](https://docs.aspose.com/words/net/working-with-content-control-sdt/) مقالة توثيقية.

```csharp
public class StructuredDocumentTagCollection : IEnumerable<IStructuredDocumentTag>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.markup/structureddocumenttagcollection/count/) { get; } | يعيد عدد علامات المستند المنظمة في المجموعة. |
| [Item](../../aspose.words.markup/structureddocumenttagcollection/item/) { get; } | يعيد علامة المستند المنظمة في الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetById](../../aspose.words.markup/structureddocumenttagcollection/getbyid/)(*int*) | يعيد علامة المستند المنظمة حسب المعرف. |
| [GetByTag](../../aspose.words.markup/structureddocumenttagcollection/getbytag/)(*string*) | يعيد أول علامة مستند منظمة تم العثور عليها في المجموعة ذات العلامة المحددة. |
| [GetByTitle](../../aspose.words.markup/structureddocumenttagcollection/getbytitle/)(*string*) | يعيد أول علامة مستند منظمة تم العثور عليها في المجموعة بالعنوان المحدد. |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagcollection/getenumerator/)() | يعيد كائن المعداد. |
| [Remove](../../aspose.words.markup/structureddocumenttagcollection/remove/)(*int*) | يزيل علامة المستند المنظم بالمعرف المحدد. |
| [RemoveAt](../../aspose.words.markup/structureddocumenttagcollection/removeat/)(*int*) | يزيل علامة مستند منظمة في الفهرس المحدد. |

## أمثلة

يوضح كيفية الحصول على علامة مستند منظمة.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// احصل على علامة المستند المنظمة حسب المعرف.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsMultiSection);
Console.WriteLine(sdt.Title);

// احصل على علامة المستند المنظمة أو العلامة المحددة حسب العنوان.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### أنظر أيضا

* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup/)
* المجسم [Aspose.Words](../../)
