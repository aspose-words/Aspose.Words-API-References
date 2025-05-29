---
title: Document.StopTrackRevisions
linktitle: StopTrackRevisions
articleTitle: StopTrackRevisions
second_title: Aspose.Words لـ .NET
description: تعرف على كيفية استخدام طريقة StopTrackRevisions لمنع علامات التغيير التلقائية في المستندات، مما يعزز كفاءة التحرير ووضوح المستندات.
type: docs
weight: 770
url: /ar/net/aspose.words/document/stoptrackrevisions/
---
## Document.StopTrackRevisions method

يوقف وضع علامة تلقائية على تغييرات المستند باعتبارها مراجعات.

```csharp
public void StopTrackRevisions()
```

## أمثلة

يوضح كيفية تتبع المراجعات أثناء تحرير مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// عادةً لا يُعتبر تحرير المستند بمثابة مراجعة إلا بعد أن نبدأ في تتبعه.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.IsTrue((DateTime.Now - doc.Revisions[0].DateTime).Milliseconds <= 10);

//توقف عن تتبع المراجعات حتى لا يتم احتساب أي تعديلات مستقبلية كمراجعات.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

//إن إنشاء المراجعات يمنحها تاريخًا ووقتًا للعملية.
// يمكننا تعطيل ذلك عن طريق تمرير DateTime.MinValue عندما نبدأ في تتبع المراجعات.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// يمكننا قبول/رفض هذه المراجعات برمجيًا
// عن طريق استدعاء طرق مثل Document.AcceptAllRevisions، أو طريقة Accept الخاصة بكل مراجعة.
// في Microsoft Word، يمكننا معالجتها يدويًا عبر "مراجعة" -> "التغييرات".
doc.Save(ArtifactsDir + "Revision.StartTrackRevisions.docx");
```

### أنظر أيضا

* method [StartTrackRevisions](../starttrackrevisions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
