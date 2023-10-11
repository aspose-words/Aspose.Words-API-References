---
title: Document.StartTrackRevisions
second_title: Aspose.Words لمراجع .NET API
description: Document طريقة. يبدأ تلقائيًا بوضع علامة على كافة التغييرات الإضافية التي تجريها على المستند برمجيًا باعتبارها تغييرات مراجعة.
type: docs
weight: 730
url: /ar/net/aspose.words/document/starttrackrevisions/
---
## StartTrackRevisions(string, DateTime) {#starttrackrevisions_1}

يبدأ تلقائيًا بوضع علامة على كافة التغييرات الإضافية التي تجريها على المستند برمجيًا باعتبارها تغييرات مراجعة.

```csharp
public void StartTrackRevisions(string author, DateTime dateTime)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| author | String | الأحرف الأولى من اسم المؤلف لاستخدامها في المراجعات. |
| dateTime | DateTime | التاريخ والوقت المستخدم للمراجعات. |

### ملاحظات

إذا قمت باستدعاء هذه الطريقة ثم قمت بإجراء بعض التغييرات على المستند برمجيًا، فاحفظ المستند ثم افتح المستند لاحقًا في برنامج MS Word، وسترى هذه التغييرات كمراجعات.

يدعم Aspose.Words حاليًا تتبع عمليات إدراج وحذف العقدة فقط. لا يتم تسجيل تغييرات التنسيق كمراجعات.

يتم دعم التتبع التلقائي للتغييرات عند تعديل هذا المستند من خلال معالجة العقدة وكذلك عند الاستخدام[`DocumentBuilder`](../../documentbuilder/)

هذه الطريقة لا تغير[`TrackRevisions`](../trackrevisions/) الخيار ولا يستخدم value الخاص به لأغراض تتبع المراجعة.

### أمثلة

يوضح كيفية تتبع المراجعات أثناء تحرير مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تحرير المستند عادةً لا يُحتسب كمراجعة حتى نبدأ في تتبعه.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.That(doc.Revisions[0].DateTime, Is.EqualTo(DateTime.Now).Within(10).Milliseconds);

// إيقاف تتبع المراجعات حتى لا يتم احتساب أي تعديلات مستقبلية على أنها مراجعات.
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

// يمكننا قبول/رفض هذه المراجعات برمجيًا
// عن طريق استدعاء أساليب مثل Document.AcceptAllRevisions، أو أسلوب قبول كل مراجعة.
// في Microsoft Word، يمكننا معالجتها يدويًا عبر "المراجعة" -> "التغييرات".
doc.Save(ArtifactsDir + "Document.StartTrackRevisions.docx");
```

### أنظر أيضا

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)

---

## StartTrackRevisions(string) {#starttrackrevisions}

يبدأ تلقائيًا بوضع علامة على كافة التغييرات الإضافية التي تجريها على المستند برمجيًا باعتبارها تغييرات مراجعة.

```csharp
public void StartTrackRevisions(string author)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| author | String | الأحرف الأولى من اسم المؤلف لاستخدامها في المراجعات. |

### ملاحظات

إذا قمت باستدعاء هذه الطريقة ثم قمت بإجراء بعض التغييرات على المستند برمجيًا، فاحفظ المستند ثم افتح المستند لاحقًا في برنامج MS Word، وسترى هذه التغييرات كمراجعات.

يدعم Aspose.Words حاليًا تتبع عمليات إدراج وحذف العقدة فقط. لا يتم تسجيل تغييرات التنسيق كمراجعات.

يتم دعم التتبع التلقائي للتغييرات عند تعديل هذا المستند من خلال معالجة العقدة وكذلك عند الاستخدام[`DocumentBuilder`](../../documentbuilder/)

هذه الطريقة لا تغير[`TrackRevisions`](../trackrevisions/) الخيار ولا يستخدم value الخاص به لأغراض تتبع المراجعة.

### أمثلة

يوضح كيفية تتبع المراجعات أثناء تحرير مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تحرير المستند عادةً لا يُحتسب كمراجعة حتى نبدأ في تتبعه.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.That(doc.Revisions[0].DateTime, Is.EqualTo(DateTime.Now).Within(10).Milliseconds);

// إيقاف تتبع المراجعات حتى لا يتم احتساب أي تعديلات مستقبلية على أنها مراجعات.
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

// يمكننا قبول/رفض هذه المراجعات برمجيًا
// عن طريق استدعاء أساليب مثل Document.AcceptAllRevisions، أو أسلوب قبول كل مراجعة.
// في Microsoft Word، يمكننا معالجتها يدويًا عبر "المراجعة" -> "التغييرات".
doc.Save(ArtifactsDir + "Document.StartTrackRevisions.docx");
```

### أنظر أيضا

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


