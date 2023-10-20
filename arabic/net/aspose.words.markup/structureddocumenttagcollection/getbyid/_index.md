---
title: StructuredDocumentTagCollection.GetById
linktitle: GetById
articleTitle: GetById
second_title: Aspose.Words لـ .NET
description: StructuredDocumentTagCollection GetById طريقة. إرجاع علامة المستند المنظمة حسب المعرف في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.markup/structureddocumenttagcollection/getbyid/
---
## StructuredDocumentTagCollection.GetById method

إرجاع علامة المستند المنظمة حسب المعرف.

```csharp
public IStructuredDocumentTag GetById(int id)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| id | Int32 | معرف علامة الوثيقة المنظمة. |

## ملاحظات

يُرجع قيمة فارغة إذا تعذر العثور على علامة المستند المنظمة ذات المعرف المحدد.

## أمثلة

يوضح كيفية الحصول على علامة المستند المنظمة.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// احصل على علامة المستند المنظمة حسب المعرف.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsRanged());
Console.WriteLine(sdt.Title);

// احصل على علامة المستند المنظمة أو علامة النطاق حسب العنوان.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### أنظر أيضا

* interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* class [StructuredDocumentTagCollection](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
