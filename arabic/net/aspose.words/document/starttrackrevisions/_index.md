---
title: Document.StartTrackRevisions
linktitle: StartTrackRevisions
articleTitle: StartTrackRevisions
second_title: Aspose.Words لـ .NET
description: تتبع تغييرات المستندات بسهولة باستخدام طريقة StartTrackRevisions. حدّد تلقائيًا جميع التعديلات كمراجعات لضمان تعاون سلس ووضوح أكبر.
type: docs
weight: 760
url: /ar/net/aspose.words/document/starttrackrevisions/
---
## StartTrackRevisions(*string, DateTime*) {#starttrackrevisions_1}

يبدأ تلقائيًا بوضع علامة على جميع التغييرات الإضافية التي تقوم بها على المستند برمجيًا باعتبارها تغييرات مراجعة.

```csharp
public void StartTrackRevisions(string author, DateTime dateTime)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| author | String | الأحرف الأولى من اسم المؤلف لاستخدامها في المراجعات. |
| dateTime | DateTime | التاريخ والوقت المستخدم للمراجعة. |

## ملاحظات

إذا قمت باستدعاء هذه الطريقة ثم قمت بإجراء بعض التغييرات على المستند برمجيًا، ثم حفظ المستند ثم فتحه لاحقًا في MS Word، فسترى هذه التغييرات كإصدارات معدلة.

يدعم Aspose.Words حاليًا تتبع عمليات إدخال وحذف العقد فقط. لا تُسجل تغييرات التنسيق كمراجعات.

يتم دعم التتبع التلقائي للتغييرات عند تعديل هذه الوثيقة من خلال node manipulations وكذلك عند استخدام[`DocumentBuilder`](../../documentbuilder/)

هذه الطريقة لا تغير[`TrackRevisions`](../trackrevisions/) الخيار ولا يستخدم قيمته لأغراض تتبع المراجعة.

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

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## StartTrackRevisions(*string*) {#starttrackrevisions}

يبدأ تلقائيًا بوضع علامة على جميع التغييرات الإضافية التي تقوم بها على المستند برمجيًا باعتبارها تغييرات مراجعة.

```csharp
public void StartTrackRevisions(string author)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| author | String | الأحرف الأولى من اسم المؤلف لاستخدامها في المراجعات. |

## ملاحظات

إذا قمت باستدعاء هذه الطريقة ثم قمت بإجراء بعض التغييرات على المستند برمجيًا، ثم حفظ المستند ثم فتحه لاحقًا في MS Word، فسترى هذه التغييرات كإصدارات معدلة.

يدعم Aspose.Words حاليًا تتبع عمليات إدخال وحذف العقد فقط. لا تُسجل تغييرات التنسيق كمراجعات.

يتم دعم التتبع التلقائي للتغييرات عند تعديل هذه الوثيقة من خلال node manipulations وكذلك عند استخدام[`DocumentBuilder`](../../documentbuilder/)

هذه الطريقة لا تغير[`TrackRevisions`](../trackrevisions/) الخيار ولا يستخدم قيمته لأغراض تتبع المراجعة.

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

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
