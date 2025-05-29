---
title: InlineStory.IsInsertRevision
linktitle: IsInsertRevision
articleTitle: IsInsertRevision
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية IsInsertRevision في InlineStory. تعرّف بسهولة على الكائنات المُدرجة في Word مع تفعيل ميزة تتبع التغييرات. حسّن إدارة مستنداتك اليوم!
type: docs
weight: 40
url: /ar/net/aspose.words/inlinestory/isinsertrevision/
---
## InlineStory.IsInsertRevision property

يعود صحيحًا إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تتبع التغييرات.

```csharp
public bool IsInsertRevision { get; }
```

## أمثلة

يوضح كيفية عرض خصائص مرتبطة بالمراجعة لعقد InlineStory.

```csharp
Document doc = new Document(MyDir + "Revision footnotes.docx");

// عندما نقوم بتحرير المستند أثناء وجود خيار "تعقب التغييرات"، الموجود عبر المراجعة -> التعقب،
// إذا تم تشغيله في Microsoft Word، فإن التغييرات التي نطبقها تعتبر بمثابة مراجعات.
// عند تحرير مستند باستخدام Aspose.Words، يمكننا البدء في تتبع المراجعات من خلال
// استدعاء طريقة "StartTrackRevisions" الخاصة بالمستند وإيقاف التتبع باستخدام طريقة "StopTrackRevisions".
// يمكننا إما قبول المراجعات لاستيعابها في المستند
// أو رفضهم للتراجع عن التغيير المقترح والتخلص منه.
Assert.IsTrue(doc.HasRevisions);

List<Footnote> footnotes = doc.GetChildNodes(NodeType.Footnote, true).Cast<Footnote>().ToList();

Assert.AreEqual(5, footnotes.Count);

// فيما يلي خمسة أنواع من المراجعات التي يمكنها الإشارة إلى عقدة InlineStory.
// 1 - مراجعة "إدراج":
// يحدث هذا التعديل عندما نقوم بإدراج نص أثناء تتبع التغييرات.
Assert.IsTrue(footnotes[2].IsInsertRevision);

// 2 - مراجعة "الانتقال من":
// عندما نقوم بتمييز النص في Microsoft Word، ثم نقوم بسحبه إلى مكان مختلف في المستند
// أثناء تتبع التغييرات، يظهر نسختان.
// إن النسخة المعدلة "نقل من" هي نسخة من النص الأصلي قبل نقله.
Assert.IsTrue(footnotes[4].IsMoveFromRevision);

// 3 - مراجعة "الانتقال إلى":
// إن المراجعة "نقل إلى" هي النص الذي نقلناه إلى موضعه الجديد في المستند.
// تظهر مراجعات "الانتقال من" و"الانتقال إلى" في أزواج لكل مراجعة نقل نقوم بتنفيذها.
// يؤدي قبول مراجعة النقل إلى حذف مراجعة "النقل من" ونصها،
// ويحتفظ بالنص من المراجعة "نقل إلى".
// على العكس من ذلك، يؤدي رفض مراجعة النقل إلى الاحتفاظ بمراجعة "النقل من" وحذف مراجعة "النقل إلى".
Assert.IsTrue(footnotes[1].IsMoveToRevision);

// 4 - مراجعة "حذف":
// يحدث هذا التعديل عند حذف نص أثناء تتبع التغييرات. عند حذف نص بهذه الطريقة،
// سوف تبقى في المستند كمراجعة حتى نقبل المراجعة،
// والذي سوف يقوم بحذف النص نهائيا، أو رفض المراجعة، مما سوف يبقي النص الذي قمنا بحذفه حيث كان.
Assert.IsTrue(footnotes[3].IsDeleteRevision);
```

### أنظر أيضا

* class [InlineStory](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
