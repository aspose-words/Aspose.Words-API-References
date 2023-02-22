---
title: Document.StopTrackRevisions
second_title: Aspose.Words لمراجع .NET API
description: Document طريقة. إيقاف وضع العلامات التلقائية على تغييرات المستند كمراجعات.
type: docs
weight: 700
url: /ar/net/aspose.words/document/stoptrackrevisions/
---
## Document.StopTrackRevisions method

إيقاف وضع العلامات التلقائية على تغييرات المستند كمراجعات.

```csharp
public void StopTrackRevisions()
```

### أمثلة

يوضح كيفية تعقب المراجعات أثناء تحرير مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تحرير المستند عادة لا يعتبر مراجعة حتى نبدأ في تعقبها.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.That(doc.Revisions[0].DateTime, Is.EqualTo(DateTime.Now).Within(10).Milliseconds);

// إيقاف تتبع المراجعات لعدم احتساب أي تعديلات مستقبلية كمراجعات.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

// إنشاء المراجعات يمنحهم تاريخ ووقت العملية.
// يمكننا تعطيل هذا عن طريق تمرير DateTime.MinValue عندما نبدأ في تتبع المراجعات.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// يمكننا قبول / رفض هذه المراجعات برمجيًا
// عن طريق استدعاء طرق مثل Document.AcceptAllRevisions ، أو طريقة قبول كل مراجعة.
// في Microsoft Word ، يمكننا معالجتها يدويًا عبر "مراجعة" - >; "التغييرات".
doc.Save(ArtifactsDir + "Document.StartTrackRevisions.docx");
```

### أنظر أيضا

* method [StartTrackRevisions](../starttrackrevisions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


