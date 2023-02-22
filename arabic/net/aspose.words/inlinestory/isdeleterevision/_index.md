---
title: InlineStory.IsDeleteRevision
second_title: Aspose.Words لمراجع .NET API
description: InlineStory ملكية. إرجاع صحيح إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات.
type: docs
weight: 30
url: /ar/net/aspose.words/inlinestory/isdeleterevision/
---
## InlineStory.IsDeleteRevision property

إرجاع صحيح إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات.

```csharp
public bool IsDeleteRevision { get; }
```

### أمثلة

يوضح كيفية عرض الخصائص المتعلقة بالمراجعة لعقد InlineStory.

```csharp
Document doc = new Document(MyDir + "Revision footnotes.docx");

// عندما نقوم بتحرير المستند أثناء وجود خيار "تتبع التغييرات" ، الموجود في مراجعة - >; تتبع ،
// قيد التشغيل في Microsoft Word ، التغييرات التي نطبقها تعد مراجعات.
// عند تحرير مستند باستخدام Aspose.Words ، يمكننا البدء في تتبع المراجعات بواسطة
// استدعاء طريقة "StartTrackRevisions" الخاصة بالمستند وإيقاف التتبع باستخدام طريقة "StopTrackRevisions".
// يمكننا إما قبول المراجعات لاستيعابها في المستند
// أو رفضها للتراجع عن التغيير المقترح وتجاهله.
Assert.IsTrue(doc.HasRevisions);

List<Footnote> footnotes = doc.GetChildNodes(NodeType.Footnote, true).Cast<Footnote>().ToList();

Assert.AreEqual(5, footnotes.Count);

// فيما يلي خمسة أنواع من المراجعات التي يمكنها وضع علامة على عقدة InlineStory.
// 1 - مراجعة "إدراج":
// تحدث هذه المراجعة عندما نقوم بإدخال نص أثناء تتبع التغييرات.
Assert.IsTrue(footnotes[2].IsInsertRevision);

// 2 - مراجعة "الانتقال من":
// عندما نقوم بتمييز النص في Microsoft Word ، ثم اسحبه إلى مكان مختلف في المستند
// أثناء تعقب التغييرات ، تظهر مراجعتان.
// مراجعة "الانتقال من" هي نسخة من النص في الأصل قبل نقله.
Assert.IsTrue(footnotes[4].IsMoveFromRevision);

// 3 - مراجعة "الانتقال إلى":
// مراجعة "الانتقال إلى" هي النص الذي نقلناه في موضعه الجديد في المستند.
تظهر المراجعات "الانتقال من" و "الانتقال إلى" في أزواج لكل مراجعة حركة نقوم بها.
// قبول مراجعة النقل يحذف مراجعة "الانتقال من" ونصها ،
// ويحافظ على النص من مراجعة "الانتقال إلى".
// رفض مراجعة الخطوة على العكس من ذلك يحافظ على "الانتقال من" المراجعة ويحذف مراجعة "الانتقال إلى".
Assert.IsTrue(footnotes[1].IsMoveToRevision);

// 4 - مراجعة "حذف":
// تحدث هذه المراجعة عندما نحذف النص أثناء تتبع التغييرات. عندما نحذف نصًا مثل هذا ،
// سيبقى في المستند كمراجعة حتى نقبل المراجعة ،
// التي ستحذف النص نهائيًا ، أو ترفض المراجعة ، مما سيبقي النص الذي حذفناه في مكانه.
Assert.IsTrue(footnotes[3].IsDeleteRevision);
```

### أنظر أيضا

* class [InlineStory](../)
* مساحة الاسم [Aspose.Words](../../inlinestory/)
* المجسم [Aspose.Words](../../../)


