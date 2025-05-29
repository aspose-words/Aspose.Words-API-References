---
title: StructuredDocumentTagCollection.GetById
linktitle: GetById
articleTitle: GetById
second_title: Aspose.Words لـ .NET
description: استرجع علامات المستندات المنظمة بسهولة باستخدام طريقة GetById. تمتع بالوصول السريع إلى بياناتك وحسّن كفاءة إدارة مستنداتك.
type: docs
weight: 30
url: /ar/net/aspose.words.markup/structureddocumenttagcollection/getbyid/
---
## StructuredDocumentTagCollection.GetById method

يعيد علامة المستند المنظمة حسب المعرف.

```csharp
public IStructuredDocumentTag GetById(int id)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| id | Int32 | معرف علامة المستند المنظم. |

## ملاحظات

يتم إرجاع قيمة null إذا لم يتم العثور على علامة المستند المنظم بالمعرف المحدد.

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
