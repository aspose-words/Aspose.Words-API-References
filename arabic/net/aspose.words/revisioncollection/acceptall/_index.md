---
title: RevisionCollection.AcceptAll
linktitle: AcceptAll
articleTitle: AcceptAll
second_title: Aspose.Words لـ .NET
description: RevisionCollection AcceptAll طريقة. يقبل كافة المراجعات في هذه المجموعة في C#.
type: docs
weight: 40
url: /ar/net/aspose.words/revisioncollection/acceptall/
---
## RevisionCollection.AcceptAll method

يقبل كافة المراجعات في هذه المجموعة.

```csharp
public void AcceptAll()
```

## أمثلة

يوضح كيفية مقارنة المستندات.

```csharp
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);
builder.Writeln("This is the original document.");

Document docEdited = new Document();
builder = new DocumentBuilder(docEdited);
builder.Writeln("This is the edited document.");

// ستؤدي مقارنة المستندات مع المراجعات إلى حدوث استثناء.
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

// بعد المقارنة، سيحصل المستند الأصلي على مراجعة جديدة
// لكل عنصر مختلف في المستند المحرر.
foreach (Revision r in docOriginal.Revisions)
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

// سيؤدي قبول هذه المراجعات إلى تحويل المستند الأصلي إلى المستند المحرر.
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### أنظر أيضا

* class [RevisionCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
