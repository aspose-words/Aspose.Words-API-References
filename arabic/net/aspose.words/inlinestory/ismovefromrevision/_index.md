---
title: InlineStory.IsMoveFromRevision
linktitle: IsMoveFromRevision
articleTitle: IsMoveFromRevision
second_title: Aspose.Words لـ .NET
description: InlineStory IsMoveFromRevision ملكية. إرجاعحقيقي إذا تم نقل هذا الكائن حذفه في Microsoft Word أثناء تمكين تعقب التغييرات في C#.
type: docs
weight: 50
url: /ar/net/aspose.words/inlinestory/ismovefromrevision/
---
## InlineStory.IsMoveFromRevision property

إرجاع`حقيقي` إذا تم نقل هذا الكائن (حذفه) في Microsoft Word أثناء تمكين تعقب التغييرات.

```csharp
public bool IsMoveFromRevision { get; }
```

## أمثلة

يوضح كيفية عرض الخصائص المتعلقة بالمراجعة لعقد InlineStory.

```csharp
Document doc = new Document(MyDir + "Revision footnotes.docx");

// عندما نقوم بتحرير المستند أثناء وجود خيار "تتبع التغييرات" عبر المراجعة -> تتبع،
// قيد التشغيل في Microsoft Word، والتغييرات التي نطبقها تعتبر مراجعات.
// عند تحرير مستند باستخدام Aspose.Words، يمكننا البدء في تتبع المراجعات بواسطة
// استدعاء طريقة "StartTrackRevisions" للمستند وإيقاف التتبع باستخدام طريقة "StopTrackRevisions".
// يمكننا قبول المراجعات لاستيعابها في المستند
// أو ارفضها للتراجع عن التغيير المقترح وتجاهله.
Assert.IsTrue(doc.HasRevisions);

List<Footnote> footnotes = doc.GetChildNodes(NodeType.Footnote, true).Cast<Footnote>().ToList();

Assert.AreEqual(5, footnotes.Count);

// فيما يلي خمسة أنواع من المراجعات التي يمكنها وضع علامة على عقدة InlineStory.
// 1 - مراجعة "إدراج":
// تحدث هذه المراجعة عندما نقوم بإدراج نص أثناء تتبع التغييرات.
Assert.IsTrue(footnotes[2].IsInsertRevision);

// 2 - مراجعة "الانتقال من":
// عندما نقوم بتمييز النص في Microsoft Word، ثم نسحبه إلى مكان مختلف في المستند
// أثناء تتبع التغييرات، تظهر مراجعتان.
// مراجعة "النقل من" هي نسخة من النص في الأصل قبل نقله.
Assert.IsTrue(footnotes[4].IsMoveFromRevision);

// 3 - مراجعة "الانتقال إلى":
// المراجعة "الانتقال إلى" هي النص الذي نقلناه إلى موضعه الجديد في المستند.
// تظهر مراجعات "الانتقال من" و"الانتقال إلى" في أزواج لكل مراجعة نقل نقوم بتنفيذها.
// يؤدي قبول مراجعة النقل إلى حذف مراجعة "النقل من" ونصها،
// ويحتفظ بالنص من مراجعة "الانتقال إلى".
// يؤدي رفض مراجعة النقل إلى الاحتفاظ بمراجعة "الانتقال من" وحذف مراجعة "الانتقال إلى".
Assert.IsTrue(footnotes[1].IsMoveToRevision);

// 4 - مراجعة "الحذف":
// تحدث هذه المراجعة عندما نقوم بحذف النص أثناء تتبع التغييرات. عندما نقوم بحذف نص مثل هذا،
// سيبقى في المستند كمراجعة حتى نقبل المراجعة،
// مما سيؤدي إلى حذف النص نهائيًا، أو رفض المراجعة، مما سيبقي النص الذي حذفناه حيث كان.
Assert.IsTrue(footnotes[3].IsDeleteRevision);
```

### أنظر أيضا

* class [InlineStory](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
