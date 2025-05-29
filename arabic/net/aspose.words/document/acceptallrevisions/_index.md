---
title: Document.AcceptAllRevisions
linktitle: AcceptAllRevisions
articleTitle: AcceptAllRevisions
second_title: Aspose.Words لـ .NET
description: قم بتبسيط عملية التحرير الخاصة بك باستخدام طريقة AcceptAllRevisions، وقبول جميع التغييرات المتعقبة في مستندك بسهولة للحصول على نسخة نهائية مصقولة.
type: docs
weight: 540
url: /ar/net/aspose.words/document/acceptallrevisions/
---
## Document.AcceptAllRevisions method

يقبل جميع التغييرات المتعقبة في المستند.

```csharp
public void AcceptAllRevisions()
```

## ملاحظات

هذه الطريقة هي اختصار لـ[`AcceptAll`](../../revisioncollection/acceptall/).

## أمثلة

يوضح كيفية قبول كافة تغييرات التتبع في المستند.

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

// يمكننا تكرار كل مراجعة وقبولها/رفضها كجزء من مستندنا.
// إذا كنا نعلم أننا نرغب في قبول كل مراجعة، فيمكننا القيام بذلك بطريقة أكثر مباشرة عن طريق استدعاء هذه الطريقة.
doc.AcceptAllRevisions();

Assert.AreEqual(0, doc.Revisions.Count);
Assert.AreEqual("Hello world! Hello again! This is another revision.", doc.GetText().Trim());
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
