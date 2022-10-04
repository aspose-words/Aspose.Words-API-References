---
title: StartTrackRevisions
second_title: Aspose.Words لمراجع .NET API
description: يبدأ تلقائيًا في وضع علامة على جميع التغييرات الإضافية التي تجريها على المستند برمجيًا عند تغيير المراجعة.
type: docs
weight: 690
url: /ar/net/aspose.words/document/starttrackrevisions/
---
## StartTrackRevisions(string, DateTime) {#starttrackrevisions_1}

يبدأ تلقائيًا في وضع علامة على جميع التغييرات الإضافية التي تجريها على المستند برمجيًا عند تغيير المراجعة.

```csharp
public void StartTrackRevisions(string author, DateTime dateTime)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| author | String | الأحرف الأولى من المؤلف لاستخدامها في المراجعات. |
| dateTime | DateTime | التاريخ والوقت المراد استخدامهما للمراجعات. |

### ملاحظات

إذا قمت باستدعاء هذه الطريقة ثم قمت بإجراء بعض التغييرات على المستند برمجيًا ، احفظ المستند ثم فتحت المستند لاحقًا في MS Word ، فسترى هذه التغييرات كمراجعات.

يدعم Aspose.Words حاليًا تتبع عمليات إدراج العقدة وحذفها فقط. لم يتم تسجيل تغييرات التنسيق كمراجعات.

يتم دعم التتبع التلقائي للتغييرات عند تعديل هذا المستند من خلال معالجة العقدة وكذلك عند استخدام[`DocumentBuilder`](../../documentbuilder/)

هذه الطريقة لا تغير[`TrackRevisions`](../trackrevisions/) الخيار ولا يستخدم value لأغراض تتبع المراجعة.

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

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)

---

## StartTrackRevisions(string) {#starttrackrevisions}

يبدأ تلقائيًا في وضع علامة على جميع التغييرات الإضافية التي تجريها على المستند برمجيًا عند تغيير المراجعة.

```csharp
public void StartTrackRevisions(string author)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| author | String | الأحرف الأولى من المؤلف لاستخدامها في المراجعات. |

### ملاحظات

إذا قمت باستدعاء هذه الطريقة ثم قمت بإجراء بعض التغييرات على المستند برمجيًا ، احفظ المستند ثم فتحت المستند لاحقًا في MS Word ، فسترى هذه التغييرات كمراجعات.

يدعم Aspose.Words حاليًا تتبع عمليات إدراج العقدة وحذفها فقط. لم يتم تسجيل تغييرات التنسيق كمراجعات.

يتم دعم التتبع التلقائي للتغييرات عند تعديل هذا المستند من خلال معالجة العقدة وكذلك عند استخدام[`DocumentBuilder`](../../documentbuilder/)

هذه الطريقة لا تغير[`TrackRevisions`](../trackrevisions/) الخيار ولا يستخدم value لأغراض تتبع المراجعة.

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

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
