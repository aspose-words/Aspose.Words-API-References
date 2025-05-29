---
title: IStructuredDocumentTag.RemoveSelfOnly
linktitle: RemoveSelfOnly
articleTitle: RemoveSelfOnly
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة IStructuredDocumentTag RemoveSelfOnly لإزالة عقدة SDT بسهولة مع الحفاظ على محتواها في شجرة المستندات الخاصة بك.
type: docs
weight: 180
url: /ar/net/aspose.words.markup/istructureddocumenttag/removeselfonly/
---
## IStructuredDocumentTag.RemoveSelfOnly method

يزيل عقدة SDT هذه فقط، لكنه يحتفظ بمحتوياتها داخل شجرة المستندات.

```csharp
public void RemoveSelfOnly()
```

## أمثلة

يوضح كيفية إزالة علامة المستند المنظمة، لكنه يحتفظ بالمحتوى بداخله.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

 // توفر هذه المجموعة واجهة موحدة للوصول إلى العلامات المنظمة المحددة وغير المحددة.
IEnumerable<IStructuredDocumentTag> sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(5, sdts.Count());

// هنا يمكننا الحصول على العقد الفرعية من الواجهة المشتركة للعلامات المنظمة المحددة وغير المحددة.
foreach (IStructuredDocumentTag sdt in sdts)
    if (sdt.GetChildNodes(NodeType.Any, false).Count > 0)
        sdt.RemoveSelfOnly();

sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(0, sdts.Count());
```

### أنظر أيضا

* interface [IStructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
