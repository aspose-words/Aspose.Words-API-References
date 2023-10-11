---
title: StructuredDocumentTagCollection.Remove
second_title: Aspose.Words لمراجع .NET API
description: StructuredDocumentTagCollection طريقة. إزالة علامة المستند المنظمة بالمعرف المحدد.
type: docs
weight: 70
url: /ar/net/aspose.words.markup/structureddocumenttagcollection/remove/
---
## StructuredDocumentTagCollection.Remove method

إزالة علامة المستند المنظمة بالمعرف المحدد.

```csharp
public void Remove(int id)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| id | Int32 | معرف علامة الوثيقة المنظمة. |

### أمثلة

يوضح كيفية إزالة علامة المستند المنظمة.

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
// قم بإزالة علامة المستند المنظمة حسب المعرف.
structuredDocumentTags.Remove(1691867797);
// قم بإزالة علامة المستند المنظمة في الموضع 0.
structuredDocumentTags.RemoveAt(0);
Assert.AreEqual(3, structuredDocumentTags.Count);
```

### أنظر أيضا

* class [StructuredDocumentTagCollection](../)
* مساحة الاسم [Aspose.Words.Markup](../../structureddocumenttagcollection/)
* المجسم [Aspose.Words](../../../)


