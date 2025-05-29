---
title: StructuredDocumentTagCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words لـ .NET
description: قم بإزالة علامات المستندات المنظمة المحددة بسهولة باستخدام طريقة StructuredDocumentTagCollection Remove لإدارة المستندات بشكل مبسط.
type: docs
weight: 70
url: /ar/net/aspose.words.markup/structureddocumenttagcollection/remove/
---
## StructuredDocumentTagCollection.Remove method

يزيل علامة المستند المنظم بالمعرف المحدد.

```csharp
public void Remove(int id)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| id | Int32 | معرف علامة المستند المنظم. |

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

* class [StructuredDocumentTagCollection](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
