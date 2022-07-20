---
title: Inline
second_title: Aspose.Words لمراجع .NET API
description: الفئة الأساسية للعقد ذات المستوى المضمن التي يمكن أن يكون لها تنسيق أحرف مقترن بها  ولكن لا يمكن أن يكون لها عقد فرعية خاصة بها .
type: docs
weight: 3060
url: /ar/net/aspose.words/inline/
---
## Inline class

الفئة الأساسية للعقد ذات المستوى المضمن التي يمكن أن يكون لها تنسيق أحرف مقترن بها ، ولكن لا يمكن أن يكون لها عقد فرعية خاصة بها .

```csharp
public abstract class Inline : Node
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | يحدد معرف العقدة المخصص . |
| virtual [Document](../../aspose.words/node/document) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة . |
| [Font](../../aspose.words/inline/font) { get; } | يوفر الوصول إلى تنسيق خط هذا الكائن. |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | إرجاع صحيح إذا كانت هذه العقدة يمكن أن تحتوي على عقد أخرى. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision) { get; } | إرجاع صحيح إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision) { get; } | إرجاع صحيح إذا تم تغيير تنسيق الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision) { get; } | إرجاع صحيح إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision) { get; } | عوائد **حقيقي** إذا تم نقل (حذف) هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision) { get; } | عوائد **حقيقي** إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تعقب التغيير. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| abstract [NodeType](../../aspose.words/node/nodetype) { get; } | يحصل على نوع هذه العقدة . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | الحصول على الأصل المباشر لهذه العقدة. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph) { get; } | استرداد الأصل[`Paragraph`](../paragraph) من هذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range) { get; } | إرجاع أ **نطاق** الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |

## طُرق

| اسم | وصف |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept)(DocumentVisitor) | يقبل الزائر . |
| [Clone](../../aspose.words/node/clone)(bool) | لإنشاء نسخة مكررة من العقدة . |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | يحصل على أول سلف محدد[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | الحصول على الأصل الأول لنوع الكائن المحدد. |
| virtual [GetText](../../aspose.words/node/gettext)() | يحصل على نص هذه العقدة وجميع توابعها. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [Remove](../../aspose.words/node/remove)() | يزيل نفسه من الأصل. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | يصدر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

### ملاحظات

فئة مشتقة من **في النسق** يمكن أن يكون ابنًا لـ **فقرة**.

### أمثلة

يوضح كيفية تحديد نوع المراجعة لعقدة مضمنة.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// عندما نقوم بتحرير المستند أثناء وجود خيار "تتبع التغييرات" ، الموجود في مراجعة - >; تتبع ،
// قيد التشغيل في Microsoft Word ، التغييرات التي نطبقها تعد مراجعات.
// عند تحرير مستند باستخدام Aspose.Words ، يمكننا البدء في تتبع المراجعات بواسطة
// استدعاء طريقة "StartTrackRevisions" الخاصة بالمستند وإيقاف التتبع باستخدام طريقة "StopTrackRevisions".
// يمكننا إما قبول المراجعات لاستيعابها في المستند
// أو رفضها لتغيير التغيير المقترح بشكل فعال.
Assert.AreEqual(6, doc.Revisions.Count);

// العقدة الأصلية للمراجعة هي المدى الذي تهتم به المراجعة. التشغيل هو عقدة مضمنة.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// فيما يلي خمسة أنواع من المراجعات التي يمكنها وضع علامة على عقدة مضمنة.
// 1 - مراجعة "إدراج":
// تحدث هذه المراجعة عندما نقوم بإدخال نص أثناء تتبع التغييرات.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - مراجعة "تنسيق":
// تحدث هذه المراجعة عندما نغير تنسيق النص أثناء تتبع التغييرات.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - مراجعة "الانتقال من":
// عندما نقوم بتمييز النص في Microsoft Word ، ثم اسحبه إلى مكان مختلف في المستند
// أثناء تعقب التغييرات ، تظهر مراجعتان.
// مراجعة "الانتقال من" هي نسخة من النص في الأصل قبل نقله.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - مراجعة "الانتقال إلى":
// مراجعة "الانتقال إلى" هي النص الذي نقلناه في موضعه الجديد في المستند.
تظهر المراجعات "الانتقال من" و "الانتقال إلى" في أزواج لكل مراجعة حركة نقوم بها.
// قبول مراجعة النقل يحذف مراجعة "الانتقال من" ونصها ،
// ويحافظ على النص من مراجعة "الانتقال إلى".
// رفض مراجعة الخطوة على العكس من ذلك يحافظ على "الانتقال من" المراجعة ويحذف مراجعة "الانتقال إلى".
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - مراجعة "حذف":
// تحدث هذه المراجعة عندما نحذف النص أثناء تتبع التغييرات. عندما نحذف نصًا مثل هذا ،
// سيبقى في المستند كمراجعة حتى نقبل المراجعة ،
// التي ستحذف النص نهائيًا ، أو ترفض المراجعة ، مما سيبقي النص الذي حذفناه في مكانه.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### أنظر أيضا

* class [Node](../node)
* مساحة الاسم [Aspose.Words](../../aspose.words)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
