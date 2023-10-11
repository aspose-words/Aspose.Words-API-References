---
title: StructuredDocumentTagCollection.GetByTitle
second_title: Aspose.Words لمراجع .NET API
description: StructuredDocumentTagCollection طريقة. إرجاع أول علامة مستند منظمة تمت مواجهتها في المجموعة بالعنوان المحدد.
type: docs
weight: 50
url: /ar/net/aspose.words.markup/structureddocumenttagcollection/getbytitle/
---
## StructuredDocumentTagCollection.GetByTitle method

إرجاع أول علامة مستند منظمة تمت مواجهتها في المجموعة بالعنوان المحدد.

```csharp
public IStructuredDocumentTag GetByTitle(string title)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| title | String | عنوان علامة المستند المنظمة. |

### ملاحظات

يُرجع قيمة فارغة إذا تعذر العثور على علامة المستند المنظمة ذات العنوان المحدد.

### أمثلة

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
* مساحة الاسم [Aspose.Words.Markup](../../structureddocumenttagcollection/)
* المجسم [Aspose.Words](../../../)


