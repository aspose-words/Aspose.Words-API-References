---
title: IStructuredDocumentTag.GetChildNodes
linktitle: GetChildNodes
articleTitle: GetChildNodes
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة IStructuredDocumentTag GetChildNodes، وقم بالوصول إلى مجموعة ديناميكية من العقد الفرعية المصممة خصيصًا لأنواعك المحددة لتحسين إدارة المستندات.
type: docs
weight: 170
url: /ar/net/aspose.words.markup/istructureddocumenttag/getchildnodes/
---
## IStructuredDocumentTag.GetChildNodes method

يعيد مجموعة حية من العقد الفرعية التي تطابق الأنواع المحددة.

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
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

* class [NodeCollection](../../../aspose.words/nodecollection/)
* enum [NodeType](../../../aspose.words/nodetype/)
* interface [IStructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
