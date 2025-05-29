---
title: IStructuredDocumentTag.IsMultiSection
linktitle: IsMultiSection
articleTitle: IsMultiSection
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية IsMultiSection في IStructuredDocumentTag، والتي تحدد ما إذا كانت علامتك عبارة عن قسم متعدد النطاقات، مما يعزز تنظيم المستند ووظائفه.
type: docs
weight: 40
url: /ar/net/aspose.words.markup/istructureddocumenttag/ismultisection/
---
## IStructuredDocumentTag.IsMultiSection property

يعود صحيحًا إذا كانت هذه المثيل عبارة عن علامة مستند منظمة (متعددة الأقسام).

```csharp
public bool IsMultiSection { get; }
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
