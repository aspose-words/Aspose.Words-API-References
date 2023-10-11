---
title: Class Inline
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Inline فصل. الفئة الأساسية للعقد ذات المستوى المضمّن التي يمكن أن يكون لها تنسيق أحرف مرتبط بها ولكن لا يمكن أن تحتوي على عقد فرعية خاصة بها.
type: docs
weight: 3260
url: /ar/net/aspose.words/inline/
---
## Inline class

الفئة الأساسية للعقد ذات المستوى المضمّن التي يمكن أن يكون لها تنسيق أحرف مرتبط بها، ولكن لا يمكن أن تحتوي على عقد فرعية خاصة بها.

لمعرفة المزيد، قم بزيارة[المستويات المنطقية للعقد في المستند](https://docs.aspose.com/words/net/logical-levels-of-nodes-in-a-document/) مقالة توثيقية.

```csharp
public abstract class Inline : Node
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصصة. |
| virtual [Document](../../aspose.words/node/document/) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة. |
| [Font](../../aspose.words/inline/font/) { get; } | يوفر الوصول إلى تنسيق الخط لهذا الكائن. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة يمكن أن تحتوي على عقد أخرى. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | إرجاع صحيح إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | إرجاع صحيح إذا تم تغيير تنسيق الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | إرجاع صحيح إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (حذفه) في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | يحصل على نوع هذه العقدة. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الأصل المباشر لهذه العقدة. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | يسترد الأصل[`Paragraph`](../paragraph/) من هذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range/) { get; } | إرجاع أ[`Range`](../range/) الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |

## طُرق

| اسم | وصف |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(DocumentVisitor) | يقبل الزائر. |
| [Clone](../../aspose.words/node/clone/)(bool) | إنشاء نسخة مكررة من العقدة. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | يحصل على السلف الأول للمحدد[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | الحصول على السلف الأول لنوع الكائن المحدد. |
| virtual [GetText](../../aspose.words/node/gettext/)() | الحصول على نص هذه العقدة وجميع أبنائها. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز شجرة الطلب المسبق. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز شجرة الطلب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | تصدير محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | تصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

### ملاحظات

فئة مشتقة من`Inline` يمكن أن يكون طفلا[`Paragraph`](../paragraph/).

### أمثلة

يوضح كيفية تحديد نوع المراجعة للعقدة المضمنة.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// عندما نقوم بتحرير المستند أثناء وجود خيار "تتبع التغييرات" عبر المراجعة -> تتبع،
// قيد التشغيل في Microsoft Word، والتغييرات التي نطبقها تعتبر مراجعات.
// عند تحرير مستند باستخدام Aspose.Words، يمكننا البدء في تتبع المراجعات بواسطة
// استدعاء طريقة "StartTrackRevisions" للمستند وإيقاف التتبع باستخدام طريقة "StopTrackRevisions".
// يمكننا قبول المراجعات لاستيعابها في المستند
// أو ارفضها لتغيير التغيير المقترح بشكل فعال.
Assert.AreEqual(6, doc.Revisions.Count);

// العقدة الأصلية للمراجعة هي التشغيل الذي تتعلق به المراجعة. التشغيل هو عقدة مضمنة.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// فيما يلي خمسة أنواع من المراجعات التي يمكنها وضع علامة على العقدة المضمنة.
// 1 - مراجعة "إدراج":
// تحدث هذه المراجعة عندما نقوم بإدراج نص أثناء تتبع التغييرات.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - مراجعة "التنسيق":
// تحدث هذه المراجعة عندما نقوم بتغيير تنسيق النص أثناء تتبع التغييرات.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - مراجعة "الانتقال من":
// عندما نقوم بتمييز النص في Microsoft Word، ثم نسحبه إلى مكان مختلف في المستند
// أثناء تتبع التغييرات، تظهر مراجعتان.
// مراجعة "النقل من" هي نسخة من النص في الأصل قبل نقله.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - مراجعة "الانتقال إلى":
// المراجعة "الانتقال إلى" هي النص الذي نقلناه إلى موضعه الجديد في المستند.
// تظهر مراجعات "الانتقال من" و"الانتقال إلى" في أزواج لكل مراجعة نقل نقوم بتنفيذها.
// يؤدي قبول مراجعة النقل إلى حذف مراجعة "النقل من" ونصها،
// ويحتفظ بالنص من مراجعة "الانتقال إلى".
// يؤدي رفض مراجعة النقل إلى الاحتفاظ بمراجعة "الانتقال من" وحذف مراجعة "الانتقال إلى".
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - مراجعة "الحذف":
// تحدث هذه المراجعة عندما نقوم بحذف النص أثناء تتبع التغييرات. عندما نقوم بحذف نص مثل هذا،
// سيبقى في المستند كمراجعة حتى نقبل المراجعة،
// مما سيؤدي إلى حذف النص نهائيًا، أو رفض المراجعة، مما سيبقي النص الذي حذفناه حيث كان.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### أنظر أيضا

* class [Node](../node/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


