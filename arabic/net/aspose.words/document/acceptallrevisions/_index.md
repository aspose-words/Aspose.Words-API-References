---
title: Document.AcceptAllRevisions
linktitle: AcceptAllRevisions
articleTitle: AcceptAllRevisions
second_title: Aspose.Words لـ .NET
description: Document AcceptAllRevisions طريقة. قبول كافة التغييرات المتعقبة في المستند في C#.
type: docs
weight: 520
url: /ar/net/aspose.words/document/acceptallrevisions/
---
## Document.AcceptAllRevisions method

قبول كافة التغييرات المتعقبة في المستند.

```csharp
public void AcceptAllRevisions()
```

## ملاحظات

هذه الطريقة هي اختصار ل[`AcceptAll`](../../revisioncollection/acceptall/).

## أمثلة

يوضح كيفية قبول جميع تغييرات التتبع في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتحرير المستند أثناء تتبع التغييرات لإنشاء بعض المراجعات.
doc.StartTrackRevisions("John Doe");
builder.Write("Hello world! ");
builder.Write("Hello again! "); 
builder.Write("This is another revision.");
doc.StopTrackRevisions();

Assert.AreEqual(3, doc.Revisions.Count);

// يمكننا تكرار كل مراجعة وقبولها/رفضها كجزء من وثيقتنا.
// إذا علمنا أننا نرغب في قبول كل مراجعة، فيمكننا القيام بذلك بشكل أكثر وضوحًا عن طريق استدعاء هذه الطريقة.
doc.AcceptAllRevisions();

Assert.AreEqual(0, doc.Revisions.Count);
Assert.AreEqual("Hello world! Hello again! This is another revision.", doc.GetText().Trim());
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
