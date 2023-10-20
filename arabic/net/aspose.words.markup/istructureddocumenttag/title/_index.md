---
title: IStructuredDocumentTag.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words لـ .NET
description: IStructuredDocumentTag Title ملكية. يحدد الاسم المألوف المرتبط بهذاالمعاملة الخاصة والتفضيلية . لا يمكن أن يكون فارغًا في C#.
type: docs
weight: 110
url: /ar/net/aspose.words.markup/istructureddocumenttag/title/
---
## IStructuredDocumentTag.Title property

يحدد الاسم المألوف المرتبط بهذا**المعاملة الخاصة والتفضيلية** . لا يمكن أن يكون فارغًا.

```csharp
public string Title { get; set; }
```

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

* interface [IStructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
