---
title: Inline Class
linktitle: Inline
articleTitle: Inline
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Inline، المصممة لتنسيق الأحرف في العقد المضمنة. حسّن أسلوب مستندك دون الحاجة إلى عقد فرعية!
type: docs
weight: 3710
url: /ar/net/aspose.words/inline/
---
## Inline class

فئة أساسية للعقد ذات المستوى المضمن التي يمكن أن يكون لها تنسيق أحرف مرتبط بها، ولكن لا يمكن أن يكون لها عقد فرعية خاصة بها.

لمعرفة المزيد، قم بزيارة[المستويات المنطقية للعقد في المستند](https://docs.aspose.com/words/net/logical-levels-of-nodes-in-a-document/) مقالة توثيقية.

```csharp
public abstract class Inline : Node
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصص. |
| virtual [Document](../../aspose.words/node/document/) { get; } | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [Font](../../aspose.words/inline/font/) { get; } | يوفر الوصول إلى تنسيق الخط لهذا الكائن. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة قادرة على احتواء عقد أخرى. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | يعود صحيحًا إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | يعود صحيحًا إذا تم تغيير تنسيق الكائن في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | يعود صحيحًا إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (حذفه) في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | يحصل على نوع هذه العقدة. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الوالد المباشر لهذه العقدة. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | يسترد الأصل[`Paragraph`](../paragraph/) من هذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [Range](../../aspose.words/node/range/) { get; } | يعيد[`Range`](../range/)الكائن الذي يمثل الجزء من المستند الموجود في هذه العقدة. |

## طُرق

| اسم | وصف |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | يقبل زائرًا. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | ينشئ نسخة مكررة من العقدة. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | يحصل على السلف الأول للعنصر المحدد[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | يحصل على السلف الأول لنوع الكائن المحدد. |
| virtual [GetText](../../aspose.words/node/gettext/)() | يحصل على نص هذه العقدة وجميع أبنائها. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | يحصل على العقدة التالية وفقًا لخوارزمية عبور شجرة الترتيب المسبق. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | يحصل على العقدة السابقة وفقًا لخوارزمية عبور شجرة الترتيب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | يقوم بتصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

## ملاحظات

فئة مشتقة من`Inline` يمكن أن يكون طفلا[`Paragraph`](../paragraph/).

## أمثلة

يوضح كيفية تحديد نوع المراجعة لعقدة مضمنة.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// عندما نقوم بتحرير المستند أثناء وجود خيار "تعقب التغييرات"، الموجود عبر المراجعة -> التعقب،
// إذا تم تشغيله في Microsoft Word، فإن التغييرات التي نطبقها تعتبر بمثابة مراجعات.
// عند تحرير مستند باستخدام Aspose.Words، يمكننا البدء في تتبع المراجعات من خلال
// استدعاء طريقة "StartTrackRevisions" الخاصة بالمستند وإيقاف التتبع باستخدام طريقة "StopTrackRevisions".
// يمكننا إما قبول المراجعات لاستيعابها في المستند
// أو رفضهم لتغيير التغيير المقترح بشكل فعال.
Assert.AreEqual(6, doc.Revisions.Count);

// العقدة الأصلية للمراجعة هي التشغيل الذي يتعلق به. التشغيل هو عقدة مضمنة.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// فيما يلي خمسة أنواع من المراجعات التي يمكنها الإشارة إلى عقدة مضمنة.
// 1 - مراجعة "إدراج":
// يحدث هذا التعديل عندما نقوم بإدراج نص أثناء تتبع التغييرات.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - مراجعة "التنسيق":
// يحدث هذا التعديل عندما نقوم بتغيير تنسيق النص أثناء تتبع التغييرات.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - مراجعة "الانتقال من":
// عندما نقوم بتمييز النص في Microsoft Word، ثم نقوم بسحبه إلى مكان مختلف في المستند
// أثناء تتبع التغييرات، يظهر نسختان.
// إن النسخة المعدلة "نقل من" هي نسخة من النص الأصلي قبل نقله.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - مراجعة "الانتقال إلى":
// إن المراجعة "نقل إلى" هي النص الذي نقلناه إلى موضعه الجديد في المستند.
// تظهر مراجعات "الانتقال من" و"الانتقال إلى" في أزواج لكل مراجعة نقل نقوم بتنفيذها.
// يؤدي قبول مراجعة النقل إلى حذف مراجعة "النقل من" ونصها،
// ويحتفظ بالنص من المراجعة "نقل إلى".
// على العكس من ذلك، يؤدي رفض مراجعة النقل إلى الاحتفاظ بمراجعة "النقل من" وحذف مراجعة "النقل إلى".
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - مراجعة "حذف":
// يحدث هذا التعديل عند حذف نص أثناء تتبع التغييرات. عند حذف نص بهذه الطريقة،
// سوف تبقى في المستند كمراجعة حتى نقبل المراجعة،
// والذي سوف يقوم بحذف النص نهائيا، أو رفض المراجعة، مما سوف يبقي النص الذي قمنا بحذفه حيث كان.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### أنظر أيضا

* class [Node](../node/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
