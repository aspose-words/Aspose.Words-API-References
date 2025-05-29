---
title: StructuredDocumentTagCollection.GetByTitle
linktitle: GetByTitle
articleTitle: GetByTitle
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة GetByTitle في StructuredDocumentTagCollection، والتي تسترجع بكفاءة علامة المستند الأولى حسب العنوان لإدارة البيانات بشكل مبسط.
type: docs
weight: 50
url: /ar/net/aspose.words.markup/structureddocumenttagcollection/getbytitle/
---
## StructuredDocumentTagCollection.GetByTitle method

يعيد أول علامة مستند منظمة تم العثور عليها في المجموعة بالعنوان المحدد.

```csharp
public IStructuredDocumentTag GetByTitle(string title)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| title | String | عنوان علامة المستند المنظم. |

## ملاحظات

يتم إرجاع قيمة null إذا لم يتم العثور على علامة المستند المنظم بالعنوان المحدد.

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

* interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* class [StructuredDocumentTagCollection](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
