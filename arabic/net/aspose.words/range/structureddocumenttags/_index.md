---
title: Range.StructuredDocumentTags
linktitle: StructuredDocumentTags
articleTitle: StructuredDocumentTags
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Range StructuredDocumentTags، التي توفر مجموعة شاملة من علامات المستندات المنظمة، مما يعزز تنظيم مستندك ووظائفه.
type: docs
weight: 50
url: /ar/net/aspose.words/range/structureddocumenttags/
---
## Range.StructuredDocumentTags property

يعيد`StructuredDocumentTags` مجموعة تمثل جميع علامات المستندات المنظمة في النطاق.

```csharp
public StructuredDocumentTagCollection StructuredDocumentTags { get; }
```

## أمثلة

يوضح كيفية إزالة علامة المستند المنظم.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

StructuredDocumentTagCollection structuredDocumentTags = doc.Range.StructuredDocumentTags;
IStructuredDocumentTag sdt;
for (int i = 0; i < structuredDocumentTags.Count; i++)
{
    sdt = structuredDocumentTags[i];
    Console.WriteLine(sdt.Title);
}

sdt = structuredDocumentTags.GetById(1691867797);
Assert.AreEqual(1691867797, sdt.Id);

Assert.AreEqual(5, structuredDocumentTags.Count);
// قم بإزالة علامة المستند المنظم حسب المعرف.
structuredDocumentTags.Remove(1691867797);
// قم بإزالة علامة المستند المنظم في الموضع 0.
structuredDocumentTags.RemoveAt(0);
Assert.AreEqual(3, structuredDocumentTags.Count);
```

### أنظر أيضا

* class [StructuredDocumentTagCollection](../../../aspose.words.markup/structureddocumenttagcollection/)
* class [Range](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
