---
title: IStructuredDocumentTag.IsRanged
second_title: Aspose.Words لمراجع .NET API
description: IStructuredDocumentTag طريقة. إرجاع صحيح إذا كان هذا المثيل عبارة عن علامة مستند منظمة ذات نطاق.
type: docs
weight: 140
url: /ar/net/aspose.words.markup/istructureddocumenttag/isranged/
---
## IStructuredDocumentTag.IsRanged method

إرجاع صحيح إذا كان هذا المثيل عبارة عن علامة مستند منظمة ذات نطاق.

```csharp
public bool IsRanged()
```

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

* interface [IStructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../istructureddocumenttag/)
* المجسم [Aspose.Words](../../../)


