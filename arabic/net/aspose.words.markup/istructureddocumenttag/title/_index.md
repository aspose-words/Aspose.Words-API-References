---
title: IStructuredDocumentTag.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية عنوان IStructuredDocumentTag - حدّد اسمًا سهل الاستخدام لـ SDT وحسّن وضوح مستندك. تعرّف على المزيد الآن!
type: docs
weight: 140
url: /ar/net/aspose.words.markup/istructureddocumenttag/title/
---
## IStructuredDocumentTag.Title property

يحدد الاسم الودي المرتبط بهذا**SDT** . لا يمكن أن يكون فارغًا.

```csharp
public string Title { get; set; }
```

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

* interface [IStructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
